---
UID: NS:hbapiwmi._GetEventBuffer_OUT
title: _GetEventBuffer_OUT
author: windows-driver-content
description: The GetEventBuffer_OUT structure is used to report the output parameter data of the GetEventBuffer WMI method to the WMI client.
old-location: storage\geteventbuffer_out.htm
old-project: storage
ms.assetid: 1ba41017-8c4b-49eb-b0ec-8e58c2673314
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: GetEventBuffer_OUT structure [Storage Devices], *PGetEventBuffer_OUT, PGetEventBuffer_OUT structure pointer [Storage Devices], hbapiwmi/GetEventBuffer_OUT, storage.geteventbuffer_out, PGetEventBuffer_OUT, GetEventBuffer_OUT, _GetEventBuffer_OUT, structs-Fibre_af1916c9-60f8-4601-b9dd-d4575a100d98.xml, hbapiwmi/PGetEventBuffer_OUT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: hbapiwmi.h
req.include-header: Hbapiwmi.h
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
-	hbapiwmi.h
apiname: 
-	GetEventBuffer_OUT
product: Windows
targetos: Windows
req.typenames: GetEventBuffer_OUT, *PGetEventBuffer_OUT
---

# _GetEventBuffer_OUT structure


## -description


The GetEventBuffer_OUT structure is used to report the output parameter data of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553935">GetEventBuffer</a> WMI method to the WMI client.


## -syntax


````
typedef struct _GetEventBuffer_OUT {
  ULONG            HBAStatus;
  ULONG            EventCount;
  MSFC_EventBuffer Events[1];
} GetEventBuffer_OUT, *PGetEventBuffer_OUT;
````


## -struct-fields




### -field HBAStatus

Contains a value associated with the WMI class qualifier <a href="https://msdn.microsoft.com/library/windows/hardware/ff557233">HBA_STATUS</a> that indicates the result of an HBA query operation. 


### -field EventCount

Indicates the number of events in <b>Events</b> that were retrieved by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553935">GetEventBuffer</a> WMI method.


### -field Events

Contains an array of type <a href="..\hbapiwmi\ns-hbapiwmi-_msfc_eventbuffer.md">MSFC_EventBuffer</a> that contains the next events in the HBA's event queue.


## -remarks


The <a href="https://msdn.microsoft.com/library/windows/hardware/ff553935">GetEventBuffer</a> method retrieves the next events in the HBA's event queue. 

The WMI tool suite generates a declaration of the GetEventBuffer_OUT structure in <i>Hbapiwmi.h </i>when it compiles the <a href="https://msdn.microsoft.com/library/windows/hardware/ff562506">MSFC_HBAAdapterMethods WMI Class</a>.



## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff553935">GetEventBuffer</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20GetEventBuffer_OUT structure%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

