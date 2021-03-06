---
UID: NS:hidclass._HID_XFER_PACKET
title: _HID_XFER_PACKET
author: windows-driver-content
description: The HID_XFER_PACKET structure contains information about a HID report that the HID class driver uses with I/O requests to get or set a report.
old-location: hid\hid_xfer_packet.htm
old-project: hid
ms.assetid: b256e6fd-d44f-482a-836d-a812634b4b3a
ms.author: windowsdriverdev
ms.date: 12/21/2017
ms.keywords: hidclass/PHID_XFER_PACKET, hid.hid_xfer_packet, HID_XFER_PACKET structure [Human Input Devices], *PHID_XFER_PACKET, _HID_XFER_PACKET, hidclass/HID_XFER_PACKET, hidstrct_55f22385-a5ed-46b5-9f97-9d47ee731145.xml, HID_XFER_PACKET, PHID_XFER_PACKET structure pointer [Human Input Devices], PHID_XFER_PACKET
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: hidclass.h
req.include-header: Hidport.h
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
-	hidclass.h
apiname: 
-	HID_XFER_PACKET
product: Windows
targetos: Windows
req.typenames: *PHID_XFER_PACKET, HID_XFER_PACKET
---

# _HID_XFER_PACKET structure


## -description


The HID_XFER_PACKET structure contains information about a HID report that the HID class driver uses with I/O requests to get or set a report.


## -syntax


````
typedef struct _HID_XFER_PACKET {
  PUCHAR reportBuffer;
  ULONG  reportBufferLen;
  UCHAR  reportId;
} HID_XFER_PACKET, *PHID_XFER_PACKET;
````


## -struct-fields




### -field reportBuffer

Pointer to a report buffer.


### -field reportBufferLen

Specifies the length of the report at <b>reportBuffer</b>.


### -field reportId

Specifies the report ID of the report contained at <b>reportBuffer</b>. This parameter is optional, and, if not specified, should be set to zero.


## -remarks


The HID class driver uses this structure to specify information about a HID report when it uses an I/O request to get or set a report.



## -see-also

<a href="..\hidclass\ni-hidclass-ioctl_hid_set_feature.md">IOCTL_HID_SET_FEATURE</a>

<a href="..\hidclass\ni-hidclass-ioctl_hid_get_feature.md">IOCTL_HID_GET_FEATURE</a>

<a href="..\hidclass\ni-hidclass-ioctl_hid_get_input_report.md">IOCTL_HID_GET_INPUT_REPORT</a>

<a href="..\hidclass\ni-hidclass-ioctl_hid_set_output_report.md">IOCTL_HID_SET_OUTPUT_REPORT</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [hid\hid]:%20HID_XFER_PACKET structure%20 RELEASE:%20(12/21/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

