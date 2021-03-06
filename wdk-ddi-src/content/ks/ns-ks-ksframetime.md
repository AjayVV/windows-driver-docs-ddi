---
UID: NS:ks.KSFRAMETIME
title: KSFRAMETIME
author: windows-driver-content
description: The KSFRAMETIME structure is supported by rendering pins, and is used to return the duration of the next &#0034;frame&#0034; of data, and flags associated with that frame.
old-location: stream\ksframetime.htm
old-project: stream
ms.assetid: 0e3beb72-2b00-41be-a7b4-341bcf065e92
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: *PKSFRAMETIME, ks/PKSFRAMETIME, PKSFRAMETIME structure pointer [Streaming Media Devices], stream.ksframetime, KSFRAMETIME structure [Streaming Media Devices], PKSFRAMETIME, KSFRAMETIME, ks-struct_3abc9b81-d7e7-455c-a577-2efa7c986cc5.xml, ks/KSFRAMETIME
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ks.h
req.include-header: Ks.h
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
-	ks.h
apiname: 
-	KSFRAMETIME
product: Windows
targetos: Windows
req.typenames: *PKSFRAMETIME, KSFRAMETIME
---

# KSFRAMETIME structure


## -description


The KSFRAMETIME structure is supported by rendering pins, and is used to return the duration of the next "frame" of data, and flags associated with that frame.


## -syntax


````
typedef struct {
  LONGLONG Duration;
  ULONG    FrameFlags;
  ULONG    Reserved;
} KSFRAMETIME, *PKSFRAMETIME;
````


## -struct-fields




### -field Duration

Specifies the duration in presentation time units.


### -field FrameFlags

Specifies the flags specific to the next frame, or to all frames. Flags are described on the reference page for <a href="..\ks\ns-ks-ksallocator_framing.md">KSALLOCATOR_FRAMING</a>.


### -field Reserved

Set to zero.


## -remarks


Note that this is an optional property, which need only be implemented if the pin instance understands the specifics of the media type it is transporting.


