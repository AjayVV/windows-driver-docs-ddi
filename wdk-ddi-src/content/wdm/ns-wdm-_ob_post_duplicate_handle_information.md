---
UID: NS:wdm._OB_POST_DUPLICATE_HANDLE_INFORMATION
title: _OB_POST_DUPLICATE_HANDLE_INFORMATION
author: windows-driver-content
description: The OB_POST_DUPLICATE_HANDLE_INFORMATION structure provides information to an ObjectPostCallback routine about a thread or process handle that has been duplicated.
old-location: kernel\ob_post_duplicate_handle_information.htm
old-project: kernel
ms.assetid: 780ace20-bb88-47fe-b504-dd6a5e903840
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: OB_POST_DUPLICATE_HANDLE_INFORMATION, _OB_POST_DUPLICATE_HANDLE_INFORMATION, wdm/OB_POST_DUPLICATE_HANDLE_INFORMATION, wdm/POB_POST_DUPLICATE_HANDLE_INFORMATION, POB_POST_DUPLICATE_HANDLE_INFORMATION, *POB_POST_DUPLICATE_HANDLE_INFORMATION, kernel.ob_post_duplicate_handle_information, kstruct_c_7b277d55-5e47-4b6d-a77b-9f10decc3dbd.xml, OB_POST_DUPLICATE_HANDLE_INFORMATION structure [Kernel-Mode Driver Architecture], POB_POST_DUPLICATE_HANDLE_INFORMATION structure pointer [Kernel-Mode Driver Architecture]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Server 2008 and later versions of the Windows operating system.
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
req.irql: PASSIVE_LEVEL (see Remarks section)
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	Wdm.h
apiname: 
-	OB_POST_DUPLICATE_HANDLE_INFORMATION
product: Windows
targetos: Windows
req.typenames: OB_POST_DUPLICATE_HANDLE_INFORMATION, *POB_POST_DUPLICATE_HANDLE_INFORMATION
req.product: Windows 10 or later.
---

# _OB_POST_DUPLICATE_HANDLE_INFORMATION structure


## -description


The <b>OB_POST_DUPLICATE_HANDLE_INFORMATION</b> structure provides information to an <a href="..\wdm\nc-wdm-pob_post_operation_callback.md">ObjectPostCallback</a> routine about a thread or process handle that has been duplicated.


## -syntax


````
typedef struct _OB_POST_DUPLICATE_HANDLE_INFORMATION {
  ACCESS_MASK GrantedAccess;
} OB_POST_DUPLICATE_HANDLE_INFORMATION, *POB_POST_DUPLICATE_HANDLE_INFORMATION;
````


## -struct-fields




### -field GrantedAccess

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> value that specifies the access that is granted for the handle.


## -see-also

<a href="..\wdm\nc-wdm-pob_post_operation_callback.md">ObjectPostCallback</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20OB_POST_DUPLICATE_HANDLE_INFORMATION structure%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

