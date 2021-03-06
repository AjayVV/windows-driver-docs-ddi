---
UID: NC:video.PVIDEO_HW_START_IO
title: PVIDEO_HW_START_IO
author: windows-driver-content
description: HwVidStartIO processes the specified VRP.
old-location: display\hwvidstartio.htm
old-project: display
ms.assetid: 82951291-cf3e-486b-ad0e-f347fefe0370
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.hwvidstartio, HwVidStartIO callback function [Display Devices], HwVidStartIO, PVIDEO_HW_START_IO, PVIDEO_HW_START_IO, video/HwVidStartIO, VideoMiniport_Functions_5dd4317e-f80d-4f93-86b5-b7c83aca2546.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: video.h
req.include-header: Video.h
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
req.lib: 
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	UserDefined
apilocation: 
-	video.h
apiname: 
-	HwVidStartIO
product: Windows
targetos: Windows
req.typenames: VHF_CONFIG, *PVHF_CONFIG
req.product: Windows 10 or later.
---

# PVIDEO_HW_START_IO callback


## -description


<i>HwVidStartIO</i> processes the specified <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VRP</a>.


## -prototype


````
PVIDEO_HW_START_IO HwVidStartIO;

BOOLEAN HwVidStartIO(
   PVOID                 HwDeviceExtension,
   PVIDEO_REQUEST_PACKET RequestPacket
)
{ ... }
````


## -parameters




### -param HwDeviceExtension

Pointer to the miniport driver's per-adapter storage area. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff543119">Device Extensions</a>.


### -param RequestPacket

Pointer to a <a href="..\video\ns-video-_video_request_packet.md">VIDEO_REQUEST_PACKET</a> structure, which contains all the parameters originally passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564838">EngDeviceIoControl</a>.


## -returns


<i>HwVidStartIO</i> must return <b>TRUE</b>, indicating that it has completed the request.



## -remarks


Every video miniport driver must have a <i>HwVidStartIO</i> function.

The video port driver calls <i>HwVidStartIO</i> in response to each GDI <a href="https://msdn.microsoft.com/library/windows/hardware/ff564838">EngDeviceIoControl</a> request, which originates in the corresponding display driver. When <i>HwVidStartIO</i> is called, the miniport driver owns the input video request packet until it completes the requested operation. <i>HwVidStartIO</i> must do the following:
<ol>
<li>
Look at the <b>IoControlCode</b> member of the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VRP</a> to determine the operation being requested by the display driver.

</li>
<li>
Check that the VRP <b>InputBufferLength</b> and/or <b>OutputBufferLength</b> indicates a buffer that is large enough to satisfy the request. The miniport driver should return an error if either buffer is too small.

</li>
<li>
Satisfy the request.

</li>
<li>
Set the <b>Status</b> and <b>Information</b> members in the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VRP</a> and return <b>TRUE</b>.

</li>
</ol>The system video port driver serializes all requests. A miniport driver need not perform any serialization of its own unless it has a <a href="..\video\nc-video-pvideo_hw_interrupt.md">HwVidInterrupt</a> function.

However, every miniport driver's <i>HwVidStartIO</i> function must complete each requested operation or set an appropriate error in the VRP's <b>StatusBlock</b> before it returns control.

<i>HwVidStartIO</i> should be made pageable.



## -see-also

<a href="..\video\nf-video-videoportsynchronizeexecution.md">VideoPortSynchronizeExecution</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff570515">Video Miniport Driver I/O Control Codes</a>

<a href="..\video\ns-video-_video_request_packet.md">VIDEO_REQUEST_PACKET</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PVIDEO_HW_START_IO callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

