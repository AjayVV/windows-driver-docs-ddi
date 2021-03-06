---
UID: NN:wudfddi.IWDFNamedPropertyStore2
title: IWDFNamedPropertyStore2
author: windows-driver-content
description: Drivers obtain the IWDFNamedPropertyStore2 interface by calling IWDFPropertyStoreFactory::RetrieveDevicePropertyStore.
old-location: wdf\iwdfnamedpropertystore2.htm
old-project: wdf
ms.assetid: f6935379-bf0d-4319-bcd9-56f0e4016945
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdf.iwdfnamedpropertystore2, IWDFNamedPropertyStore2 interface, IWDFNamedPropertyStore2 interface, described, IWDFNamedPropertyStore2, wudfddi/IWDFNamedPropertyStore2, UMDFPropertyStoreObjectRef_6a5d155a-6311-4a43-9b21-2572b04da323.xml, umdf.iwdfnamedpropertystore2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wudfddi.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.9
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: wudfddi.h
req.dll: WUDFx.dll
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	COM
apilocation: 
-	WUDFx.dll
apiname: 
-	IWDFNamedPropertyStore2
product: Windows
targetos: Windows
req.typenames: *PPOWER_ACTION, POWER_ACTION
req.product: Windows 10 or later.
---

# IWDFNamedPropertyStore2 interface


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

Drivers obtain the <b>IWDFNamedPropertyStore2</b> interface by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff560228">IWDFPropertyStoreFactory::RetrieveDevicePropertyStore</a>.


## -members

The <b>IWDFNamedPropertyStore2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560176">IWDFNamedPropertyStore2::DeleteNamedValue</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ce0953d3-054f-446b-9f69-58f4580740f3">DeleteNamedValue</a> method deletes a value name from the registry.

</td>
</tr>
</table>The <a href="https://msdn.microsoft.com/ce0953d3-054f-446b-9f69-58f4580740f3">DeleteNamedValue</a> method deletes a value name from the registry.

 

