---
UID: NF:wiamdef.WIAS_LERROR
title: WIAS_LERROR macro
author: windows-driver-content
description: The WIAS_LERROR macro is obsolete for Windows Vista and later. It is recommended that the WIAS_ERROR macro be used instead.The WIAS_LERROR macro writes a diagnostic WIA_ERROR message to the log file.
old-location: image\wias_lerror.htm
old-project: image
ms.assetid: 71949653-08c7-4f22-951d-6e1595b10700
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: WIAS_LERROR macro [Imaging Devices], wiamdef/WIAS_LERROR, WIAS_LERROR, IWiaLog_b765e146-4e57-447c-9e9d-0f3cdc784291.xml, image.wias_lerror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wiamdef.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me, Windows XP, and later. Obsolete for Windows Vista and later. Use WIAS_ERROR instead.
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
req.lib: wiamdef.h
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	wiamdef.h
apiname: 
-	WIAS_LERROR
product: Windows
targetos: Windows
req.typenames: DEVICEDIALOGDATA2, *PDEVICEDIALOGDATA2, *LPDEVICEDIALOGDATA2
req.product: Windows 10 or later.
---

# WIAS_LERROR macro


## -description


The WIAS_LERROR macro is obsolete for Windows Vista and later. It is recommended that the <a href="..\wiamdef\nf-wiamdef-wias_error.md">WIAS_ERROR</a> macro be used instead.

The WIAS_LERROR macro writes a diagnostic WIA_ERROR message to the log file.


## -syntax


````
WIAS_LERROR( WIAS_LERROR(
         IWiaLog   *pIWiaLog,
         LONG      lResId,
   const CHAR      *format_string, ...
);
````


## -parameters




### -param pILog

TBD


### -param ResID

TBD


### -param Args

TBD




#### - pIWiaLog

Pointer to an <a href="..\wia_lh\nn-wia_lh-iwialog.md">IWiaLog Interface</a>.


#### - lResId

Specifies the resource ID. This value should be set to WIALOG_NO_RESOURCE_ID.


####### - format_string, ...

Specifies a variable argument list, which starts with an ANSI format string that describes the message and any format identifiers. The ellipsis (...) specifies a variable number of arguments that need to be output. The error text should be prefixed with the full name of the method or function and generate the message in the format of "class::method, error-text".


## -remarks


The following is an example of how the macro can be used:
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>WIAS_LERROR(g_pIWiaLog, WIALOG_NO_RESOURCE_ID,
("MyClass::MyMethod, This is my text and my lValue = %d", lValue));</pre>
</td>
</tr>
</table></span></div>The WIAS_LERROR macro is not recommended for Windows Vista, because it does not record its output to the <i>Wiatrace.log </i>diagnostic log file. It is recommended that the <a href="..\wiamdef\nf-wiamdef-wias_error.md">WIAS_ERROR</a> macro be used instead. 



## -see-also

<a href="..\wiamdef\nf-wiamdef-wias_lhresult.md">WIAS_LHRESULT</a>

<a href="..\wiamdef\nf-wiamdef-wias_ltrace.md">WIAS_LTRACE</a>

<a href="..\wiamdef\nf-wiamdef-wias_lwarning.md">WIAS_LWARNING</a>

<a href="..\wiamdef\nf-wiamdef-wias_error.md">WIAS_ERROR</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [image\image]:%20WIAS_LERROR macro%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

