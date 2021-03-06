---
UID: NS:winddiui._ATTRIBUTE_INFO_2
title: _ATTRIBUTE_INFO_2
author: windows-driver-content
description: The ATTRIBUTE_INFO_2 structure is used as a parameter for a printer interface DLL's DrvQueryJobAttributes function. All member values are function-supplied.
old-location: print\attribute_info_2.htm
old-project: print
ms.assetid: c5bb9943-ee5b-4128-9e5f-438971119e3a
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: ATTRIBUTE_INFO_2 structure [Print Devices], _ATTRIBUTE_INFO_2, winddiui/ATTRIBUTE_INFO_2, PATTRIBUTE_INFO_2 structure pointer [Print Devices], print.attribute_info_2, PATTRIBUTE_INFO_2, ATTRIBUTE_INFO_2, winddiui/PATTRIBUTE_INFO_2, print_interface-graphics_681158ae-a9ad-40f6-a3de-c82cda7156e0.xml, *PATTRIBUTE_INFO_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winddiui.h
req.include-header: Winddiui.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	winddiui.h
apiname: 
-	ATTRIBUTE_INFO_2
product: Windows
targetos: Windows
req.typenames: *PATTRIBUTE_INFO_2, ATTRIBUTE_INFO_2
req.product: Windows 10 or later.
---

# _ATTRIBUTE_INFO_2 structure


## -description


The ATTRIBUTE_INFO_2 structure is used as a parameter for a printer interface DLL's <a href="..\winddiui\nf-winddiui-drvqueryjobattributes.md">DrvQueryJobAttributes</a> function. All member values are function-supplied.


## -syntax


````
typedef struct _ATTRIBUTE_INFO_2 {
  DWORD dwJobNumberOfPagesPerSide;
  DWORD dwDrvNumberOfPagesPerSide;
  DWORD dwNupBorderFlags;
  DWORD dwJobPageOrderFlags;
  DWORD dwDrvPageOrderFlags;
  DWORD dwJobNumberOfCopies;
  DWORD dwDrvNumberOfCopies;
  DWORD dwColorOptimization;
} ATTRIBUTE_INFO_2, *PATTRIBUTE_INFO_2;
````


## -struct-fields




### -field dwJobNumberOfPagesPerSide

Number of document pages to be placed on one side of a physical page, as requested by the user. Allowable values are 1, 2, 4, 6, 9, or 16.


### -field dwDrvNumberOfPagesPerSide

Number of document pages that the printer and driver can place on one side of a physical page. This value must be 1 or the value specified for <b>dwJobNumberOfPagesPerSide</b>.


### -field dwNupBorderFlags

One of the following bit flag values:
<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
BORDER_PRINT

</td>
<td>
The print processor should draw a border around the page.

</td>
</tr>
<tr>
<td>
NO_BORDER_PRINT

</td>
<td>
The print processor should not draw a border around the page.

</td>
</tr>
</table> 


### -field dwJobPageOrderFlags

One of the following bit flag values:
<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
BOOKLET_PRINT

</td>
<td>
Pages should be printed in booklet form, with two document pages printed on one side of a physical page. In landscape mode, the two document pages are printed side-by-side on the paper. In portrait mode, the two document pages are printed top-and-bottom.

</td>
</tr>
<tr>
<td>
NORMAL_PRINT

</td>
<td>
Pages should be printed in normal order: page 1, page 2, and so on.

</td>
</tr>
<tr>
<td>
REVERSE_PRINT

</td>
<td>
Pages should be printed in reverse order: last page, next-to-last page, and so on.

</td>
</tr>
</table> 


### -field dwDrvPageOrderFlags

Bit flags indicating which page ordering options are supported by the printer and driver. Uses the same flags as <b>dwJobPageOrderFlags</b>.


### -field dwJobNumberOfCopies

Number of copies of the print job, as requested by the user.


### -field dwDrvNumberOfCopies

Maximum number of copies the printer and driver can handle at once, taking into account such job attributes as collating and stapling.


### -field dwColorOptimization

One of the following bit flag values:
<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
COLOR_OPTIMIZATION

</td>
<td>
The print processor should use monochrome color optimization.

</td>
</tr>
<tr>
<td>
NO_COLOR_OPTIMIZATION

</td>
<td>
The print processor should not use monochrome color optimization.

</td>
</tr>
</table> 


## -remarks


The EMF print processor uses the flag specified for <b>dwColorOptimization</b> to determine whether to request GDI to perform monochrome color optimization. If monochrome color optimization is enabled, the print job can be switched between monochrome and color rendering as appropriate.

If you are creating a Unidrv rendering plug-in to generate color watermarks, note that when the <b>dwColorOptimization</b> member is set to COLOR_OPTIMIZATION, color watermarks are printed in black and white when they are printed on black-and-white documents. To ensure that color watermarks print correctly with color and black-and-white documents, disable color optimization. Color optimization also can be controlled by the Unidrv *<b>ChangeColorModeOnDoc?</b> color attribute (see <a href="https://msdn.microsoft.com/c8de0186-9cf5-43e5-81e7-33351a34c13c">Color Attributes</a>), and by the <a href="..\winppi\nf-winppi-gdiendpageemf.md">GdiEndPageEMF</a> function. 

For more information about other structure members, see <a href="..\winddiui\ns-winddiui-_attribute_info_1.md">ATTRIBUTE_INFO_1</a>.



## -see-also

<a href="..\winppi\nf-winppi-gdiendpageemf.md">GdiEndPageEMF</a>

<a href="..\winddiui\nf-winddiui-drvqueryjobattributes.md">DrvQueryJobAttributes</a>

<a href="..\winddiui\ns-winddiui-_attribute_info_1.md">ATTRIBUTE_INFO_1</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20ATTRIBUTE_INFO_2 structure%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

