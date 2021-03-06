---
UID: NF:dbgeng.IDebugSymbols3.GetSourcePathElement
title: IDebugSymbols3::GetSourcePathElement method
author: windows-driver-content
description: The GetSourcePathElement method returns an element from the source path.
old-location: debugger\getsourcepathelement.htm
old-project: debugger
ms.assetid: 69507aed-ff32-46f2-8efb-68c1a7288bfb
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: GetSourcePathElement method [Windows Debugging], IDebugSymbols3 interface, IDebugSymbols::GetSourcePathElement, GetSourcePathElement, debugger.getsourcepathelement, dbgeng/IDebugSymbols::GetSourcePathElement, GetSourcePathElement method [Windows Debugging], IDebugSymbols interface, IDebugSymbols3 interface [Windows Debugging], GetSourcePathElement method, IDebugSymbols_517435f9-812c-43c2-bf82-5924de7955a2.xml, IDebugSymbols2 interface [Windows Debugging], GetSourcePathElement method, IDebugSymbols2::GetSourcePathElement, GetSourcePathElement method [Windows Debugging], dbgeng/IDebugSymbols2::GetSourcePathElement, IDebugSymbols3::GetSourcePathElement, IDebugSymbols3, IDebugSymbols interface [Windows Debugging], GetSourcePathElement method, GetSourcePathElement method [Windows Debugging], IDebugSymbols2 interface, dbgeng/IDebugSymbols3::GetSourcePathElement
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
-	IDebugSymbols.GetSourcePathElement
-	IDebugSymbols2.GetSourcePathElement
-	IDebugSymbols3.GetSourcePathElement
product: Windows
targetos: Windows
req.typenames: *PDOT4_ACTIVITY, DOT4_ACTIVITY
---

# IDebugSymbols3::GetSourcePathElement method


## -description


The <b>GetSourcePathElement</b>  method returns an element from the source path.


## -syntax


````
HRESULT GetSourcePathElement(
  [in]            ULONG  Index,
  [out, optional] PSTR   Buffer,
  [in]            ULONG  BufferSize,
  [out, optional] PULONG ElementSize
);
````


## -parameters




### -param Index [in]

Specifies the index of the element in the source path that will be returned.  The source path is a string that contains elements separated by semicolons (;).  The index of the first element is zero.


### -param Buffer [out, optional]

Receives the source path element.  Each source path element can be a directory or a source server.  If <i>Buffer</i> is <b>NULL</b>, this information is not returned.


### -param BufferSize [in]

Specifies the size, in characters, of the <i>Buffer</i> buffer.


### -param ElementSize [out, optional]

Receives the size, in characters, of the source path element.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The source path contains fewer than <i>Index</i> elements.

</td>
</tr>
</table> 



## -remarks


The source path is used by the engine when searching for source files.

For more information about manipulating the source path, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff560141">Using Source Files</a>.  For an overview of the source path and its syntax, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff556906">Source Path</a>.



## -see-also

<a href="..\dbgeng\nn-dbgeng-idebugsymbols2.md">IDebugSymbols2</a>

<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff538102">AppendSourcePath</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff548358">GetSourcePath</a>

<a href="..\dbgeng\nn-dbgeng-idebugsymbols.md">IDebugSymbols</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugSymbols::GetSourcePathElement method%20 RELEASE:%20(1/19/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

