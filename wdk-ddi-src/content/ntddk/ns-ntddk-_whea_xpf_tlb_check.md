---
UID: NS:ntddk._WHEA_XPF_TLB_CHECK
title: _WHEA_XPF_TLB_CHECK
author: windows-driver-content
description: The WHEA_XPF_TLB_CHECK union describes translation lookaside buffer (TLB) error information for an x86 or x64 processor.
old-location: whea\whea_xpf_tlb_check.htm
old-project: whea
ms.assetid: 3943c854-3bb9-4fc9-9af9-735c3f4ee94e
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: *PWHEA_XPF_TLB_CHECK, _WHEA_XPF_TLB_CHECK, PWHEA_XPF_TLB_CHECK, WHEA_XPF_TLB_CHECK union [WHEA Drivers and Applications], ntddk/PWHEA_XPF_TLB_CHECK, PWHEA_XPF_TLB_CHECK union pointer [WHEA Drivers and Applications], whearef_20ed4273-105d-467b-a71f-46e50078543e.xml, WHEA_XPF_TLB_CHECK, whea.whea_xpf_tlb_check, ntddk/WHEA_XPF_TLB_CHECK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddk.h
req.include-header: Ntddk.h
req.target-type: Windows
req.target-min-winverclnt: Supported in Windows Server 2008, Windows Vista SP1, and later versions of Windows.
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
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	ntddk.h
apiname: 
-	WHEA_XPF_TLB_CHECK
product: Windows
targetos: Windows
req.typenames: WHEA_XPF_TLB_CHECK, *PWHEA_XPF_TLB_CHECK
---

# _WHEA_XPF_TLB_CHECK structure


## -description


The WHEA_XPF_TLB_CHECK union describes translation lookaside buffer (TLB) error information for an x86 or x64 processor.


## -syntax


````
typedef union _WHEA_XPF_TLB_CHECK {
  struct {
    ULONGLONG TransactionTypeValid  :1;
    ULONGLONG OperationValid  :1;
    ULONGLONG LevelValid  :1;
    ULONGLONG ProcessorContextCorruptValid  :1;
    ULONGLONG UncorrectedValid  :1;
    ULONGLONG PreciseIPValid  :1;
    ULONGLONG RestartableIPValid  :1;
    ULONGLONG OverflowValid  :1;
    ULONGLONG ReservedValid  :8;
    ULONGLONG TransactionType  :2;
    ULONGLONG Operation  :4;
    ULONGLONG Level  :3;
    ULONGLONG ProcessorContextCorrupt  :1;
    ULONGLONG Uncorrected  :1;
    ULONGLONG PreciseIP  :1;
    ULONGLONG RestartableIP  :1;
    ULONGLONG Overflow  :1;
    ULONGLONG Reserved  :34;
  };
  ULONGLONG XpfTLBCheck;
} WHEA_XPF_TLB_CHECK, *PWHEA_XPF_TLB_CHECK;
````


## -struct-fields




### -field DUMMYSTRUCTNAME

 


### -field DUMMYSTRUCTNAME.TransactionTypeValid

 


### -field DUMMYSTRUCTNAME.OperationValid

 


### -field DUMMYSTRUCTNAME.LevelValid

 


### -field DUMMYSTRUCTNAME.ProcessorContextCorruptValid

 


### -field DUMMYSTRUCTNAME.UncorrectedValid

 


### -field DUMMYSTRUCTNAME.PreciseIPValid

 


### -field DUMMYSTRUCTNAME.RestartableIPValid

 


### -field DUMMYSTRUCTNAME.OverflowValid

 


### -field DUMMYSTRUCTNAME.ReservedValid

 


### -field DUMMYSTRUCTNAME.TransactionType

 


### -field DUMMYSTRUCTNAME.Operation

 


### -field DUMMYSTRUCTNAME.Level

 


### -field DUMMYSTRUCTNAME.ProcessorContextCorrupt

 


### -field DUMMYSTRUCTNAME.Uncorrected

 


### -field DUMMYSTRUCTNAME.PreciseIP

 


### -field DUMMYSTRUCTNAME.RestartableIP

 


### -field DUMMYSTRUCTNAME.Overflow

 


### -field DUMMYSTRUCTNAME.Reserved

 


### -field XpfTLBCheck

A ULONGLONG representation of the contents of the WHEA_XPF_TLB_CHECK union.


#### - TransactionTypeValid

A single bit that indicates that the <b>TransactionType</b> member contains valid data.


#### - Operation

The type of translation lookaside buffer (TLB) access operation that caused the error. Possible values are:



This member contains valid data only if the <b>OperationValid</b> bit is set.


##### - Operation.XPF_TLB_CHECK_OPERATION_PREFETCH

An instruction prefetch operation.


#### - TransactionType

The type of transaction that was in progress when the error occurred. Possible values are:



This member contains valid data only if the <b>TransactionTypeValid</b> bit is set.


#### - Overflow

A single bit that indicates that an error overflow occurred.

This member contains valid data only if the <b>OverflowValid</b> bit is set.


##### - Operation.XPF_TLB_CHECK_OPERATION_INSTRUCTIONFETCH

An instruction fetch operation.


#### - UncorrectedValid

A single bit that indicates that the <b>Uncorrected</b> member contains valid data.


#### - LevelValid

A single bit that indicates that the <b>Level</b> member contains valid data.


#### - ProcessorContextCorrupt

A single bit that indicates that the processor context might have been corrupted.

This member contains valid data only if the <b>ProcessorContextCorruptValid</b> bit is set.


##### - Operation.XPF_TLB_CHECK_OPERATION_DATAREAD

A data read operation.


#### - Level

The level of the TLB where the error occurred.

This member contains valid data only if the <b>LevelValid</b> bit is set.


#### - RestartableIPValid

A single bit that indicates that the <b>RestartableIP</b> member contains valid data.


#### - OperationValid

A single bit that indicates that the <b>Operation</b> member contains valid data.


#### - Uncorrected

A single bit that indicates that the error has not been corrected.

This member contains valid data only if the <b>UncorrectedValid</b> bit is set.


#### - ProcessorContextCorruptValid

A single bit that indicates that the <b>ProcessorContextCorrupt</b> member contains valid data.


#### - RestartableIP

A single bit that indicates that program execution can be restarted reliably at the instruction pointer that is specified in the <b>InstructionPointer</b> member of the <a href="..\ntddk\ns-ntddk-_whea_xpf_procinfo.md">WHEA_XPF_PROCINFO</a> union that contains this WHEA_XPF_TLB_CHECK structure.

This member contains valid data only if the <b>RestartableIPValid</b> bit is set.


##### - Operation.XPF_TLB_CHECK_OPERATION_DATAWRITE

A data write operation.


#### - PreciseIPValid

A single bit that indicates that the <b>PreciseIP</b> member contains valid data.


##### - TransactionType.XPF_TLB_CHECK_TRANSACTIONTYPE_INSTRUCTION

A processor instruction transaction.


##### - Operation.XPF_TLB_CHECK_OPERATION_GENERIC

The type of operation cannot be determined.


#### - Reserved

Reserved for system use.


##### - TransactionType.XPF_TLB_CHECK_TRANSACTIONTYPE_DATAACCESS

A data access transaction.


##### - TransactionType.XPF_TLB_CHECK_TRANSACTIONTYPE_GENERIC

A generic transaction.


#### - ReservedValid

Reserved for system use.


#### - PreciseIP

A single bit that indicates that the instruction pointer that is specified in the <b>InstructionPointer</b> member of the <a href="..\ntddk\ns-ntddk-_whea_xpf_procinfo.md">WHEA_XPF_PROCINFO</a> structure that contains this WHEA_XPF_TLB_CHECK union is directly associated with the error.

This member contains valid data only if the <b>PreciseIPValid</b> bit is set.


##### - Operation.XPF_TLB_CHECK_OPERATION_GENREAD

A generic read operation.


#### - OverflowValid

A single bit that indicates that the <b>Overflow</b> member contains valid data.


##### - Operation.XPF_TLB_CHECK_OPERATION_GENWRITE

A generic write operation.


## -remarks


If the <b>CheckInfoId</b> member of a <a href="..\ntddk\ns-ntddk-_whea_xpf_procinfo.md">WHEA_XPF_PROCINFO</a> structure contains WHEA_TLBCHECK_GUID, the <b>CheckInfo</b> member of the WHEA_XPF_PROCINFO structure contains a WHEA_XPF_TLB_CHECK union.



## -see-also

<a href="..\ntddk\ns-ntddk-_whea_xpf_procinfo.md">WHEA_XPF_PROCINFO</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [whea\whea]:%20WHEA_XPF_TLB_CHECK union%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

