---
UID: NN:printerextension.IPrintSchemaCapabilities2
title: IPrintSchemaCapabilities2
author: windows-driver-content
description: The IPrintSchemaCapabilities2 interface represents an extension to the IPrintSchemaCapabilities object, which provides wrapper methods over a print capabilities document.
old-location: print\iprintschemacapabilities2.htm
old-project: print
ms.assetid: 1C361DC6-6517-4845-BEA6-09D2BB3B3232
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: print.iprintschemacapabilities2, IPrintSchemaCapabilities2 interface [Print Devices], IPrintSchemaCapabilities2 interface [Print Devices], described, IPrintSchemaCapabilities2, printerextension/IPrintSchemaCapabilities2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: printerextension.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: printerextension.h
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	COM
apilocation: 
-	Printerextension.h
apiname: 
-	IPrintSchemaCapabilities2
product: Windows
targetos: Windows
req.typenames: PrintSchemaSelectionType
req.product: Windows 10 or later.
---

# IPrintSchemaCapabilities2 interface


## -description


The <b>IPrintSchemaCapabilities2</b> interface represents an extension to the <a href="..\printerextension\nn-printerextension-iprintschemacapabilities.md">IPrintSchemaCapabilities</a> object, which provides wrapper methods over a print capabilities document.


## -members

The <b>IPrintSchemaCapabilities2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn465889">GetParameterDefinition</a>
</td>
<td align="left" width="63%">
The <b>GetParameterDefinition</b> method retrieves the <a href="..\printerextension\nn-printerextension-iprintschemaparameterdefinition.md">IPrintSchemaParameterDefinition</a> object, and it  represents the &lt;psf:ParameterDef&gt; element in the PrintCapabilites XML.

</td>
</tr>
</table>The <b>GetParameterDefinition</b> method retrieves the <a href="..\printerextension\nn-printerextension-iprintschemaparameterdefinition.md">IPrintSchemaParameterDefinition</a> object, and it  represents the &lt;psf:ParameterDef&gt; element in the PrintCapabilites XML.

 


## -see-also

<a href="..\printerextension\nn-printerextension-iprintschemacapabilities.md">IPrintSchemaCapabilities</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IPrintSchemaCapabilities2 interface%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

