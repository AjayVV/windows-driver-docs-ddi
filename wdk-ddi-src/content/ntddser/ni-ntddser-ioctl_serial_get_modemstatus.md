---
UID: NI:ntddser.IOCTL_SERIAL_GET_MODEMSTATUS
title: IOCTL_SERIAL_GET_MODEMSTATUS
author: windows-driver-content
description: The IOCTL_SERIAL_GET_MODEMSTATUS request updates the modem status, and returns the value of the modem status register before the update.
old-location: serports\ioctl_serial_get_modemstatus.htm
old-project: serports
ms.assetid: d3926476-758d-4bc0-a1e8-114dc47dc846
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: serports.ioctl_serial_get_modemstatus, IOCTL_SERIAL_GET_MODEMSTATUS control code [Serial Ports], IOCTL_SERIAL_GET_MODEMSTATUS, ntddser/IOCTL_SERIAL_GET_MODEMSTATUS, serref_6948e4a9-43c8-4ebe-9a0c-c47a2d3f1a7a.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntddser.h
req.include-header: Ntddser.h
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
-	Ntddser.h
apiname: 
-	IOCTL_SERIAL_GET_MODEMSTATUS
product: Windows
targetos: Windows
req.typenames: SD_REQUEST_FUNCTION
---

# IOCTL_SERIAL_GET_MODEMSTATUS IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


The <b>IOCTL_SERIAL_GET_MODEMSTATUS</b> request updates the modem status, and returns the value of the modem status register before the update.

For more information, see the definitions of the modem status register bits (SERIAL_MSR_DCTS through SERIAL_MSR_DCD) in the Serial.h header file in the <a href="http://go.microsoft.com/fwlink/p/?LinkId=617962">Serial driver sample</a> on GitHub.


## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

The <b>AssociatedIrp.SystemBuffer</b> member points to a client-allocated ULONG buffer that the serial controller driver uses to output the value of the modem status register.


### -output-buffer-length

The <b>Parameters.DeviceIoControl.OutputBufferLength</b> member is set to the size, in bytes, of a ULONG.


### -in-out-buffer


<text></text>



### -inout-buffer-length


<text></text>



### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of a ULONG. Otherwise, the <b>Information</b> member is set to zero.

The <b>Status</b> member is set to one of the <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/serports/serial-device-control-requests2">Generic Status Values for Serial Device Control Requests</a>.


## -see-also

<a href="..\ntddser\ni-ntddser-ioctl_serial_set_modem_control.md">IOCTL_SERIAL_SET_MODEM_CONTROL</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [serports\serports]:%20IOCTL_SERIAL_GET_MODEMSTATUS control code%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

