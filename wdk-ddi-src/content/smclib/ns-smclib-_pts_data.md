---
UID: NS:smclib._PTS_DATA
title: _PTS_DATA
author: windows-driver-content
description: The PTS_DATA structure is used for protocol type selection (PTS).
old-location: smartcrd\pts_data.htm
old-project: smartcrd
ms.assetid: aa542c6f-24f9-4ef4-a425-93905cca976a
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: PPTS_DATA, PTS_DATA structure [Smart Card Reader Devices], PPTS_DATA structure pointer [Smart Card Reader Devices], scstruct_8540d432-b29a-4227-a305-da7aba23a26d.xml, smartcrd.pts_data, *PPTS_DATA, smclib/PTS_DATA, PTS_DATA, _PTS_DATA, smclib/PPTS_DATA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: smclib.h
req.include-header: Smclib.h
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
-	smclib.h
apiname: 
-	PTS_DATA
product: Windows
targetos: Windows
req.typenames: PTS_DATA, *PPTS_DATA
req.product: Windows 10 or later.
---

# _PTS_DATA structure


## -description


The PTS_DATA structure is used for protocol type selection (PTS).


## -syntax


````
typedef struct _PTS_DATA {
  UCHAR Type;
  UCHAR Fl;
  UCHAR Dl;
  ULONG CLKFrequency;
  ULONG DataRate;
  UCHAR StopBits;
} PTS_DATA, *PPTS_DATA;
````


## -struct-fields




### -field Type

Controls how the remaining members of this structure are calculated. This member can have one of the following values:




### -field Fl

The Fl value to use as part of PTS1 for the PTS request.


### -field Dl

The Dl value to use as part of PTS1 for the PTS request.


### -field CLKFrequency

Contains the clock frequency. Some smart card readers must be programmed by using the new clock frequency to use after the PTS request.


### -field DataRate

Contains the new data rate. Some smart card readers (for example, serial readers) must be set to the new data rate to use after a PTS request.


### -field StopBits

Contains the number of stop bits to use with the inserted card.


##### - Type.PTS_TYPE_USER

Calculates user-defined parameters for PTS.

The smart card driver library populates the remaining members of this structure when the reader driver calls its <a href="https://msdn.microsoft.com/library/windows/hardware/ff548972">SmartcardUpdateCardCapabilities (WDM)</a> routine. However, in some cases, the reader driver might be responsible for setting these parameters. For example, if a PTS request that specifies optimal parameters fails, the reader driver can set the parameters in a callback function that specifies the protocol. To specify the protocol, the callback function should set the type to PTS_TYPE_DEFAULT and call <b>SmartcardUpdateCardCapabilities</b> again. 


##### - Type.PTS_TYPE_OPTIMAL

Calculates the best possible parameters for PTS.


##### - Type.PTS_TYPE_DEFAULT

Calculates standard parameters for PTS.


## -remarks


The smart card reader driver library assigns values to the members of this structure before it calls the callback function that sets the protocol. The driver library considers the characteristics of the inserted smart card, the supported clock frequencies, and supported data rates of the reader when it assigns the values. 


