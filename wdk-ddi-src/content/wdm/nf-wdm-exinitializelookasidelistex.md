---
UID: NF:wdm.ExInitializeLookasideListEx
title: ExInitializeLookasideListEx function
author: windows-driver-content
description: The ExInitializeLookasideListEx routine initializes a lookaside list.
old-location: kernel\exinitializelookasidelistex.htm
old-project: kernel
ms.assetid: 2f6072d2-808b-452f-a789-0c6f63195440
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: kernel.exinitializelookasidelistex, ExInitializeLookasideListEx routine [Kernel-Mode Driver Architecture], k102_1ceb4bd5-41cb-4f77-b435-a8bf922afbc2.xml, wdm/ExInitializeLookasideListEx, ExInitializeLookasideListEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows Vista.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: <= DISPATCH_LEVEL (see Remarks section)
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	DllExport
apilocation: 
-	NtosKrnl.exe
apiname: 
-	ExInitializeLookasideListEx
product: Windows
targetos: Windows
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# ExInitializeLookasideListEx function


## -description


The <b>ExInitializeLookasideListEx</b> routine initializes a lookaside list.


## -syntax


````
NTSTATUS ExInitializeLookasideListEx(
  _Out_    PLOOKASIDE_LIST_EX    Lookaside,
  _In_opt_ PALLOCATE_FUNCTION_EX Allocate,
  _In_opt_ PFREE_FUNCTION_EX     Free,
  _In_     POOL_TYPE             PoolType,
  _In_     ULONG                 Flags,
  _In_     SIZE_T                Size,
  _In_     ULONG                 Tag,
  _In_     USHORT                Depth
);
````


## -parameters




### -param Lookaside [out]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff554329">LOOKASIDE_LIST_EX</a> structure to initialize. On return, this structure describes an empty lookaside list. The caller must use nonpaged system space for this structure, regardless of whether the entries in the lookaside list are allocated from paged or nonpaged memory. On 64-bit platforms, this structure must be 16-byte aligned.


### -param Allocate [in, optional]

A pointer to a caller-supplied <a href="https://msdn.microsoft.com/library/windows/hardware/ff554322">LookasideListAllocateEx</a> routine that allocates a new lookaside-list entry. The <a href="..\wdm\nf-wdm-exallocatefromlookasidelistex.md">ExAllocateFromLookasideListEx</a> routine calls this <i>LookasideListAllocateEx</i> routine if the lookaside list is empty (contains no entries). This parameter is optional and can be specified as <b>NULL</b> if a custom allocation routine is not required. If this parameter is <b>NULL</b>, calls to <b>ExAllocateFromPagedLookasideList</b> automatically allocate the paged or nonpaged storage (as determined by the <i>PoolType</i> parameter) for the new entries.


### -param Free [in, optional]

A pointer to a caller-supplied <a href="https://msdn.microsoft.com/library/windows/hardware/ff554324">LookasideListFreeEx</a> routine that frees a previously allocated lookaside-list entry. The <a href="..\wdm\nf-wdm-exfreetopagedlookasidelist.md">ExFreeToPagedLookasideList</a> routine calls this <i>LookasideListFreeEx</i> routine if the lookaside list is full (that is, the list already contains the maximum number of entries, as determined by the operating system). This parameter is optional and can be specified as <b>NULL</b> if a custom deallocation routine is not required. If this parameter is <b>NULL</b>, calls to <b>ExFreeToPagedLookasideList</b> automatically free the storage for the specified entries.


### -param PoolType [in]

Specifies the pool type of the entries in the lookaside list. Set this parameter to a valid <a href="..\wdm\ne-wdm-_pool_type.md">POOL_TYPE</a> enumeration value.


### -param Flags [in]

Specifies an optional flag value to modify the default behavior of the <i>LookasideListAllocateEx</i> routine. Set this parameter to zero or to one of the following EX_LOOKASIDE_LIST_EX_FLAGS_<i>XXX</i> flag bits.
<table>
<tr>
<th>Flag bit</th>
<th>Meaning</th>
</tr>
<tr>
<td>
EX_LOOKASIDE_LIST_EX_FLAGS_RAISE_ON_FAIL

</td>
<td>
If the allocation fails, raise an exception.

</td>
</tr>
<tr>
<td>
EX_LOOKASIDE_LIST_EX_FLAGS_FAIL_NO_RAISE

</td>
<td>
If the allocation fails, return <b>NULL</b> instead of raising an exception. This flag is intended for use with an allocation routine, such as <a href="..\wdm\nf-wdm-exallocatepoolwithquotatag.md">ExAllocatePoolWithQuotaTag</a>, that charges quotas for pool usage. 

</td>
</tr>
</table> 

These two flag bits are mutually exclusive.

If <i>Allocate</i> is <b>NULL</b>, set <i>Flags</i> to either zero or EX_LOOKASIDE_LIST_EX_FLAGS_RAISE_ON_FAIL, but not to EX_LOOKASIDE_LIST_EX_FLAGS_FAIL_NO_RAISE. Otherwise, the behavior of the default allocation routine is undefined.

If <i>Flags</i> = EX_LOOKASIDE_LIST_EX_FLAGS_RAISE_ON_FAIL, the <i>PoolType</i> parameter value is bitwise ORed with the POOL_RAISE_IF_ALLOCATION_FAILURE flag bit to form the <i>PoolType</i> parameter value that is passed to the <i>LookasideListAllocateEx</i> routine. The <i>LookasideListAllocateEx</i> routine can pass this <i>PoolType</i> value, without modification, to the <b>ExAllocatePoolWithTag</b> routine. For more information about the POOL_RAISE_IF_ALLOCATION_FAILURE flag, see <a href="..\wdm\nf-wdm-exallocatepoolwithtag.md">ExAllocatePoolWithTag</a>.

If <i>Flags</i> = EX_LOOKASIDE_LIST_EX_FLAGS_FAIL_NO_RAISE, the <i>PoolType</i> parameter value is bitwise ORed with the POOL_QUOTA_FAIL_INSTEAD_OF_RAISE flag bit to form the <i>PoolType</i> parameter value that is passed to the <i>LookasideListAllocateEx</i> routine. The <i>LookasideListAllocateEx</i> routine can pass this <i>PoolType</i> value, without modification, to the <b>ExAllocatePoolWithQuotaTag</b> routine. For more information about the POOL_QUOTA_FAIL_INSTEAD_OF_RAISE flag, see <a href="..\wdm\nf-wdm-exallocatepoolwithquotatag.md">ExAllocatePoolWithQuotaTag</a>. 


### -param Size [in]

Specifies the size, in bytes, of each entry in the lookaside list.


### -param Tag [in]

Specifies the four-byte pool tag to use to mark the allocated storage for lookaside-list entries. For more information about pool tags, see the description of the <i>Tag</i> parameter in <b>ExAllocatePoolWithTag</b>. 


### -param Depth [in]

Reserved. Always set this parameter to zero.


## -returns


<b>ExInitializeLookasideListEx</b> returns STATUS_SUCCESS if the call is successful. Possible return values include the following error code:
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER_4</b></dt>
</dl>
</td>
<td width="60%">
The <i>PoolType</i> parameter value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER_5</b></dt>
</dl>
</td>
<td width="60%">
The <i>Flags</i> parameter value is not valid.

</td>
</tr>
</table> 



## -remarks


A driver must call this routine to initialize a lookaside list before the driver can begin to use the list. A lookaside list is a pool of fixed-size buffers that the driver can manage locally to reduce the number of calls to system allocation routines and, thereby, to improve performance. The buffers are stored as entries in the lookaside list. All entries in the list are of the same, uniform size, which is specified by the <i>Size</i> parameter.

After <b>ExInitializeLookasideListEx</b> returns, the lookaside list is initialized but contains no entries. When a client calls the <a href="..\wdm\nf-wdm-exallocatefromlookasidelistex.md">ExAllocateFromLookasideListEx</a> routine to request an entry, this routine determines that the lookaside list is empty and calls the driver-supplied <a href="https://msdn.microsoft.com/library/windows/hardware/ff554322">LookasideListAllocateEx</a> routine to dynamically allocate storage for a new entry. Additional entries might be allocated in response to similar requests from clients. Later, when clients call the <a href="..\wdm\nf-wdm-exfreetolookasidelistex.md">ExFreeToLookasideListEx</a> to release these entries, this routine inserts the entries into the lookaside list. If the number of entries in the list reaches a limit that is determined by the operating system, <b>ExFreeToLookasideListEx</b> ceases to add further entries to the list and instead passes these entries to the driver-supplied <a href="https://msdn.microsoft.com/library/windows/hardware/ff554324">LookasideListFreeEx</a> routine to be freed.

If the driver does not supply <i>LookasideListAllocateEx</i> and <i>LookasideListFreeEx</i> routines, the <b>ExAllocateFromLookasideListEx</b> and <b>ExFreeToLookasideListEx</b> routines use default allocation and deallocation routines instead.

There is no benefit to providing <i>LookasideListAllocateEx</i> and <i>LookasideListFreeEx</i> routines that do nothing but call <a href="..\wdm\nf-wdm-exallocatepoolwithtag.md">ExAllocatePoolWithTag</a> and <a href="..\wdm\nf-wdm-exfreepool.md">ExFreePool</a>. The same effect can be achieved with better performance by simply setting the <i>Allocate</i> and <i>Free</i> parameters to <b>NULL</b>.

Before a driver unloads, it must explicitly free any lookaside lists it created. Failure to do so is a serious programming error. Call the <a href="..\wdm\nf-wdm-exdeletelookasidelistex.md">ExDeleteLookasideListEx</a> routine to free a lookaside list. This routine frees the storage for any remaining entries in the specified lookaside list and then removes the list from the system-wide set of active lookaside lists.

The operating system keeps track of all lookaside lists that are currently in use. As both the amount of available nonpaged memory and the demand for lookaside list entries vary over time, the operating system dynamically adjusts its limits for the maximum number of entries in each nonpaged lookaside list.

In Windows 2000 and later versions of Windows, a lookaside list that contains paged or nonpaged entries can be described by a <a href="https://msdn.microsoft.com/library/windows/hardware/ff558775">PAGED_LOOKASIDE_LIST</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff556431">NPAGED_LOOKASIDE_LIST</a> structure, respectively.

For more information about lookaside lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff565416">Using Lookaside Lists</a>.

Callers of <b>ExInitializeLookasideListEx</b> can be running at IRQL &lt;= DISPATCH_LEVEL, but are typically running at IRQL = PASSIVE_LEVEL.



## -see-also

<a href="..\wdm\nf-wdm-exdeletelookasidelistex.md">ExDeleteLookasideListEx</a>

<a href="..\wdm\ne-wdm-_pool_type.md">POOL_TYPE</a>

<a href="..\wdm\nf-wdm-exfreetolookasidelistex.md">ExFreeToLookasideListEx</a>

<a href="..\wdm\nf-wdm-exallocatefromlookasidelistex.md">ExAllocateFromLookasideListEx</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff554329">LOOKASIDE_LIST_EX</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff558775">PAGED_LOOKASIDE_LIST</a>

<a href="..\wdm\nf-wdm-exallocatepoolwithtag.md">ExAllocatePoolWithTag</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff556431">NPAGED_LOOKASIDE_LIST</a>

<a href="..\wdm\nf-wdm-interlockedincrement.md">InterlockedIncrement</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff554324">LookasideListFreeEx</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff554322">LookasideListAllocateEx</a>

<a href="..\wdm\nf-wdm-interlockeddecrement.md">InterlockedDecrement</a>

<a href="..\wdm\nf-wdm-exfreepool.md">ExFreePool</a>

<a href="..\wdm\nf-wdm-exallocatepoolwithquotatag.md">ExAllocatePoolWithQuotaTag</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20ExInitializeLookasideListEx routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

