---
UID: NE:d3dkmddi._DXGK_QUERYADAPTERINFOTYPE
title: _DXGK_QUERYADAPTERINFOTYPE
author: windows-driver-content
description: The DXGK_QUERYADAPTERINFOTYPE enumeration indicates the type of information to retrieve.
old-location: display\dxgk_queryadapterinfotype.htm
old-project: display
ms.assetid: 5cceffb1-853c-4635-b855-d0e3f107c23d
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: DXGKQAITYPE_SEGMENTMEMORYSTATE, DXGKQAITYPE_ALLOCATIONGROUP, DXGKQAITYPE_INTEGRATED_DISPLAY_DESCRIPTOR, d3dkmddi/DXGKQAITYPE_DISPLAY_DRIVERCAPS_EXTENSION, d3dkmddi/DXGKQAITYPE_QUERYSEGMENT2, display.dxgk_queryadapterinfotype, DXGKQAITYPE_QUERYSEGMENT2, d3dkmddi/DXGKQAITYPE_INTEGRATED_DISPLAY_DESCRIPTOR, DXGKQAITYPE_PHYSICALADAPTERCAPS, _DXGK_QUERYADAPTERINFOTYPE, DXGKQAITYPE_POWERCOMPONENTINFO, d3dkmddi/DXGKQAITYPE_QUERYCOLORIMETRYOVERRIDES, d3dkmddi/DXGKQAITYPE_POWERCOMPONENTINFO, DmEnums_c4637ac2-b8e0-4c30-a709-5a8ff1ee3fdc.xml, d3dkmddi/DXGKQAITYPE_UMDRIVERPRIVATE, d3dkmddi/DXGKQAITYPE_HISTORYBUFFERPRECISION, DXGKQAITYPE_UMDRIVERPRIVATE, DXGKQAITYPE_DRIVERCAPS, DXGKQAITYPE_DISPLAY_DRIVERCAPS_EXTENSION, DXGKQAITYPE_NUMPOWERCOMPONENTS, DXGKQAITYPE_QUERYSEGMENT3, DXGKQAITYPE_PAGETABLELEVELDESC, d3dkmddi/DXGKQAITYPE_PAGETABLELEVELDESC, DXGKQAITYPE_GPUMMUCAPS, DXGKQAITYPE_HISTORYBUFFERPRECISION, d3dkmddi/DXGKQAITYPE_GPUMMUCAPS, d3dkmddi/DXGK_QUERYADAPTERINFOTYPE, DXGKQAITYPE_PREFERREDGPUNODE, d3dkmddi/DXGKQAITYPE_DRIVERCAPS, d3dkmddi/DXGKQAITYPE_POWERCOMPONENTPSTATEINFO, d3dkmddi/DXGKQAITYPE_PHYSICALADAPTERCAPS, DXGKQAITYPE_QUERYSEGMENT4, DXGKQAITYPE_QUERYSEGMENT, d3dkmddi/DXGKQAITYPE_PREFERREDGPUNODE, DXGKQAITYPE_QUERYCOLORIMETRYOVERRIDES, d3dkmddi/DXGKQAITYPE_ALLOCATIONGROUP, DXGK_QUERYADAPTERINFOTYPE, DXGKQAITYPE_UEFIFRAMEBUFFERRANGES, d3dkmddi/DXGKQAITYPE_QUERYSEGMENT, d3dkmddi/DXGKQAITYPE_UEFIFRAMEBUFFERRANGES, d3dkmddi/DXGKQAITYPE_QUERYSEGMENT3, DXGKQAITYPE_POWERCOMPONENTPSTATEINFO, d3dkmddi/DXGKQAITYPE_SEGMENTMEMORYSTATE, DXGK_QUERYADAPTERINFOTYPE enumeration [Display Devices], d3dkmddi/DXGKQAITYPE_QUERYSEGMENT4, d3dkmddi/DXGKQAITYPE_NUMPOWERCOMPONENTS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows Vista.
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
-	d3dkmddi.h
apiname: 
-	DXGK_QUERYADAPTERINFOTYPE
product: Windows
targetos: Windows
req.typenames: DXGK_QUERYADAPTERINFOTYPE
---

# _DXGK_QUERYADAPTERINFOTYPE enumeration


## -description


The DXGK_QUERYADAPTERINFOTYPE enumeration indicates the type of information to retrieve.


## -syntax


````
typedef enum _DXGK_QUERYADAPTERINFOTYPE { 
  DXGKQAITYPE_UMDRIVERPRIVATE                   = 0,
  DXGKQAITYPE_DRIVERCAPS                        = 1,
  DXGKQAITYPE_QUERYSEGMENT                      = 2,
#if (DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WIN7)
  DXGKQAITYPE_ALLOCATIONGROUP                   = 3,
  DXGKQAITYPE_QUERYSEGMENT2                     = 4,
#endif 
#if (DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WIN8)
  DXGKQAITYPE_QUERYSEGMENT3                     = 5,
  DXGKQAITYPE_NUMPOWERCOMPONENTS                = 6,
  DXGKQAITYPE_POWERCOMPONENTINFO                = 7,
  DXGKQAITYPE_PREFERREDGPUNODE                  = 8,
#endif 
#if (DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WDDM1_3)
  DXGKQAITYPE_POWERCOMPONENTPSTATEINFO          = 9,
  DXGKQAITYPE_HISTORYBUFFERPRECISION            = 10,
#endif 
#if (DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WDDM2_0)
  DXGKQAITYPE_QUERYSEGMENT4                     = 11,
  DXGKQAITYPE_SEGMENTMEMORYSTATE                = 12,
  DXGKQAITYPE_GPUMMUCAPS                        = 13,
  DXGKQAITYPE_PAGETABLELEVELDESC                = 14,
  DXGKQAITYPE_PHYSICALADAPTERCAPS               = 15,
  DXGKQAITYPE_DISPLAY_DRIVERCAPS_EXTENSION      = 16,
#endif 
#if (DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WDDM2_2)
  DXGKQAITYPE_INTEGRATED_DISPLAY_DESCRIPTOR     = 17,
  DXGKQAITYPE_UEFIFRAMEBUFFERRANGES             = 18,
  DXGKQAITYPE_QUERYCOLORIMETRYOVERRIDES         = 19
} DXGK_QUERYADAPTERINFOTYPE;
````


## -enum-fields




### -field DXGKQAITYPE_UMDRIVERPRIVATE

Indicates private data for the user-mode display driver.


### -field DXGKQAITYPE_DRIVERCAPS

Indicates the driver capabilities in a <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_drivercaps.md">DXGK_DRIVERCAPS</a> structure.


### -field DXGKQAITYPE_QUERYSEGMENT


      Indicates memory-segment information in a <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_querysegmentout.md">DXGK_QUERYSEGMENTOUT</a> structure.
     


### -field DXGKQAITYPE_RESERVED



### -field DXGKQAITYPE_QUERYSEGMENT2

Reserved for system use. Do not use in your driver.
     Note that this constant occurs starting with Windows 7.


### -field DXGKQAITYPE_QUERYSEGMENT3

Indicates memory-segment information in a <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_querysegmentout3.md">DXGK_QUERYSEGMENTOUT3</a> structure.

Supported starting with Windows 8.


### -field DXGKQAITYPE_NUMPOWERCOMPONENTS

Indicates the number of power components used by the display miniport driver.  For more information, see Remarks.

Supported starting with Windows 8.


### -field DXGKQAITYPE_POWERCOMPONENTINFO

Indicates information about power components used by the display miniport driver. For more information, see Remarks.

Supported starting with Windows 8.


### -field DXGKQAITYPE_PREFERREDGPUNODE

Reserved for system use. Do not use in your driver.

Supported starting with Windows 8.


### -field DXGKQAITYPE_POWERCOMPONENTPSTATEINFO

Reserved for system use. Do not use in your driver.

Supported starting with Windows 8.1.


### -field DXGKQAITYPE_HISTORYBUFFERPRECISION

Indicates info about the precision of history buffer data used by the display miniport driver. For more information, see Remarks.

Supported starting with Windows 8.1.


### -field DXGKQAITYPE_QUERYSEGMENT4

Indicates memory-segment information in a <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_querysegmentout4.md">DXGK_QUERYSEGMENTOUT4</a> structure.

Supported starting with Windows 10.


### -field DXGKQAITYPE_SEGMENTMEMORYSTATE

Indicates bad memory ranges in a <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_memoryrange.md">DXGK_MEMORYRANGE</a> structure. 

Supported starting with Windows 10.


### -field DXGKQAITYPE_GPUMMUCAPS

Indicates physical adapter GPU capabilities.

Supported starting with Windows 10.


### -field DXGKQAITYPE_PAGETABLELEVELDESC

Reserved for system use. Do not use in your driver.


### -field DXGKQAITYPE_PHYSICALADAPTERCAPS

Reserved for system use. Do not use in your driver.


### -field DXGKQAITYPE_DISPLAY_DRIVERCAPS_EXTENSION

Reserved for system use. Do not use in your driver.


### -field DXGKQAITYPE_INTEGRATED_DISPLAY_DESCRIPTOR

Indicates a request for an integrated panel descriptor where the input buffer to the query will be a DXGK_QUERYINTEGRATEDDISPLAYIN structure and the output buffer is a DXGK_QUERYINTEGRATEDDISPLAYOUT structure.

Although this function addresses a target, only DxgKrnl adapter locks are taken over this call, not child device locks.  In practice, since this call will be made before the child device is exposed, there should be no concurrent DDI calls which address the same target.
<div class="alert"><b>Note</b>  Unlike most QueryAdapterInfo calls, the output buffer size is variable although it is still known in advance from the DescriptorLength field of the DXGK_INTEGRATED_DISPLAY_CHILD structure for the target id.  The size of the output buffer is:
DescriptorLength + FIELD_OFFSET( DXGK_QUERYINTEGRATEDDISPLAYOUT, Descriptor )
</div><div> </div>

### -field DXGKQAITYPE_UEFIFRAMEBUFFERRANGES

Indicates request for the UEFI frame buffer ranges.


### -field DXGKQAITYPE_QUERYCOLORIMETRYOVERRIDES

Indicates a request for colorimetry overrides for an external display where the input buffer to the query will be a DXGK_QUERYCOLORIMETRYOVERRIDESIN structure, containing only the target id being addressed and the output buffer is a DXGK_COLORIMETRY structure into which the driver writes overrides for the monitor attached to the target.

Although this function addresses a target, only DxgKrnl adapter locks are taken over this call, not child device locks.  Since this call will be made before the child device is exposed, there should be no concurrent DDI calls which address the same target.

The output buffer is zeroed when passed to the driver.  If the driver has no overrides for the monitor, it should return STATUS_SUCCESS and leave the output buffer zeroed.  If the driver has overrides, it fill in all fields of the DXGK_COLORIMETRY to describe the monitor capabilities as the OS will not accept partial overrides.


### -field DXGKQAITYPE_DISPLAYID_DESCRIPTOR




#### - DXGKQAITYPE_ALLOCATIONGROUP


      Reserved for system use. Do not use in your driver. Note that this constant occurs starting with Windows 7.


## -remarks


The display miniport driver must fill the buffer pointed to by the <b>pOutputData</b> member of the <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_queryadapterinfo.md">DXGKARG_QUERYADAPTERINFO</a> structure as follows:
<table>
<tr>
<th>Value of <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_queryadapterinfo.md">DXGKARG_QUERYADAPTERINFO</a>.<b>Type</b></th>
<th>Contents of output buffer pointed to by <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_queryadapterinfo.md">DXGKARG_QUERYADAPTERINFO</a>.<b>pOutputData</b></th>
</tr>
<tr>
<td><b>DXGKQAITYPE_UMDRIVERPRIVATE</b></td>
<td>Proprietary buffer</td>
</tr>
<tr>
<td><b>DXGKQAITYPE_DRIVERCAPS</b></td>
<td>Populated <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_drivercaps.md">DXGK_DRIVERCAPS</a> structure</td>
</tr>
<tr>
<td><b>DXGKQAITYPE_QUERYSEGMENT</b></td>
<td>Populated <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_querysegmentout.md">DXGK_QUERYSEGMENTOUT</a> structure</td>
</tr>
<tr>
<td><b>DXGKQAITYPE_QUERYSEGMENT3</b></td>
<td>Populated <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_querysegmentout3.md">DXGK_QUERYSEGMENTOUT3</a> structure</td>
</tr>
<tr>
<td><b>DXGKQAITYPE_NUMPOWERCOMPONENTS</b></td>
<td>A UINT value that specifies the number of power components used by the display miniport driver</td>
</tr>
<tr>
<td><b>DXGKQAITYPE_POWERCOMPONENTINFO</b></td>
<td>Populated <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_power_runtime_component.md">DXGK_POWER_RUNTIME_COMPONENT</a> structure that provides information about the <i>n</i>th power component, where <i>n</i> is the component index specified by  <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_queryadapterinfo.md">DXGKARG_QUERYADAPTERINFO</a>.<b>pInputData</b>  in a call to the <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_queryadapterinfo.md">DxgkDdiQueryAdapterInfo</a> function</td>
</tr>
<tr>
<td><b>DXGKQAITYPE_HISTORYBUFFERPRECISION</b></td>
<td>Populated <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_historybufferprecision.md">DXGKARG_HISTORYBUFFERPRECISION</a> structure</td>
</tr>
</table> 



## -see-also

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_power_runtime_component.md">DXGK_POWER_RUNTIME_COMPONENT</a>

<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_queryadapterinfo.md">DxgkDdiQueryAdapterInfo</a>

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_historybufferprecision.md">DXGKARG_HISTORYBUFFERPRECISION</a>

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_querysegmentout.md">DXGK_QUERYSEGMENTOUT</a>

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_querysegmentout3.md">DXGK_QUERYSEGMENTOUT3</a>

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_queryadapterinfo.md">DXGKARG_QUERYADAPTERINFO</a>

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_drivercaps.md">DXGK_DRIVERCAPS</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXGK_QUERYADAPTERINFOTYPE enumeration%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

