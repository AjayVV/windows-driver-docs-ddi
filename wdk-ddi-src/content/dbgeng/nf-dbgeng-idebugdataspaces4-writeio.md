---
UID: NF:dbgeng.IDebugDataSpaces4.WriteIo
title: IDebugDataSpaces4::WriteIo method
author: windows-driver-content
description: The WriteIo method writes to the system and bus I/O memory.
old-location: debugger\writeio.htm
old-project: debugger
ms.assetid: 3bc84b15-7c13-4ad9-b9a1-6abd5a7389eb
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: WriteIo method [Windows Debugging], IDebugDataSpaces3 interface, IDebugDataSpaces4, IDebugDataSpaces_d36b33ec-db19-4df1-8813-b77f22705279.xml, dbgeng/IDebugDataSpaces4::WriteIo, debugger.writeio, WriteIo method [Windows Debugging], IDebugDataSpaces3::WriteIo, IDebugDataSpaces::WriteIo, IDebugDataSpaces4::WriteIo, WriteIo method [Windows Debugging], IDebugDataSpaces2 interface, IDebugDataSpaces3 interface [Windows Debugging], WriteIo method, dbgeng/IDebugDataSpaces2::WriteIo, dbgeng/IDebugDataSpaces3::WriteIo, IDebugDataSpaces interface [Windows Debugging], WriteIo method, WriteIo method [Windows Debugging], IDebugDataSpaces4 interface, IDebugDataSpaces2::WriteIo, WriteIo method [Windows Debugging], IDebugDataSpaces interface, dbgeng/IDebugDataSpaces::WriteIo, IDebugDataSpaces2 interface [Windows Debugging], WriteIo method, IDebugDataSpaces4 interface [Windows Debugging], WriteIo method, WriteIo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Desktop
req.target-min-winverclnt: 
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
req.lib: dbgeng.h
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	COM
apilocation: 
-	dbgeng.h
apiname: 
-	IDebugDataSpaces.WriteIo
-	IDebugDataSpaces2.WriteIo
-	IDebugDataSpaces3.WriteIo
-	IDebugDataSpaces4.WriteIo
product: Windows
targetos: Windows
req.typenames: *PDOT4_ACTIVITY, DOT4_ACTIVITY
---

# IDebugDataSpaces4::WriteIo method


## -description


The <b>WriteIo</b> method writes to the system and bus I/O memory.


## -syntax


````
HRESULT WriteIo(
  [in]            ULONG   InterfaceType,
  [in]            ULONG   BusNumber,
  [in]            ULONG   AddressSpace,
  [in]            ULONG64 Offset,
  [in]            PVOID   Buffer,
  [in]            ULONG   BufferSize,
  [out, optional] PULONG  BytesWritten
);
````


## -parameters




### -param InterfaceType [in]

Specifies the interface type of the I/O bus.  This parameter may take values in the INTERFACE_TYPE enumeration defined in wdm.h.


### -param BusNumber [in]

Specifies the system-assigned number of the bus.  This is usually zero, unless the system has more than one bus of the same interface type.


### -param AddressSpace [in]

Set to one.


### -param Offset [in]

Specifies the location of the requested data.


### -param Buffer [in]

Specifies the data to write to the I/O bus.


### -param BufferSize [in]

Specifies the size in bytes of the buffer <i>Buffer</i>.  This is the maximum number of bytes that will be written.


### -param BytesWritten [out, optional]

Receives the number of bytes written to I/O bus.  If <i>BytesWritten</i> is <b>NULL</b>, this information is not returned.


## -returns


This method can also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table> 



## -remarks


This method is only available in kernel-mode debugging.


