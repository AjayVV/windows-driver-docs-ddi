---
UID: NF:wudfinterrupt.WDF_INTERRUPT_INFO_INIT
title: WDF_INTERRUPT_INFO_INIT function
author: windows-driver-content
description: The WDF_INTERRUPT_INFO_INIT function initializes a WDF_INTERRUPT_INFO structure.
old-location: wdf\wdf_interrupt_info_init_umdf.htm
old-project: wdf
ms.assetid: CFFE19FB-289C-4002-AB07-AE342D855B20
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: umdf.wdf_interrupt_info_init, WDF_INTERRUPT_INFO_INIT, wudfinterrupt/WDF_INTERRUPT_INFO_INIT, WDF_INTERRUPT_INFO_INIT function, wdf.wdf_interrupt_info_init_umdf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wudfinterrupt.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.11
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	Wudfinterrupt.h
apiname: 
-	WDF_INTERRUPT_INFO_INIT
product: Windows
targetos: Windows
req.typenames: *PWDF_INTERRUPT_PRIORITY, WDF_INTERRUPT_PRIORITY
req.product: Windows 10 or later.
---

# WDF_INTERRUPT_INFO_INIT function


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]


      The <a href="..\wudfinterrupt\nf-wudfinterrupt-wdf_interrupt_info_init.md">WDF_INTERRUPT_INFO_INIT</a> function initializes a <a href="..\wudfinterrupt\ns-wudfinterrupt-_wdf_interrupt_info.md">WDF_INTERRUPT_INFO</a> structure.


## -syntax


````
VOID WDF_INTERRUPT_INFO_INIT(
  _Out_ PWDF_INTERRUPT_INFO Info
);
````


## -parameters




### -param InterruptInfo

TBD



#### - Info [out]

A pointer to a driver-allocated <a href="..\wudfinterrupt\ns-wudfinterrupt-_wdf_interrupt_info.md">WDF_INTERRUPT_INFO</a> structure.


## -returns


None



## -remarks


The <a href="..\wudfinterrupt\nf-wudfinterrupt-wdf_interrupt_info_init.md">WDF_INTERRUPT_INFO_INIT</a> function zeros the specified <a href="..\wudfinterrupt\ns-wudfinterrupt-_wdf_interrupt_info.md">WDF_INTERRUPT_INFO</a> structure and sets the structure's <b>Size</b> member.

For more information about handling interrupts in framework-based drivers, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/handling-hardware-interrupts">Handling Interrupts</a>.



## -see-also

<a href="..\wudfinterrupt\ns-wudfinterrupt-_wdf_interrupt_info.md">WDF_INTERRUPT_INFO</a>

<a href="https://msdn.microsoft.com/744D0FFE-6D3C-4AED-8935-63EE9B0AFA0F">IWDFInterrupt::GetInfo</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WDF_INTERRUPT_INFO_INIT function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

