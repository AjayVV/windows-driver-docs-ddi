---
UID: NS:stiusd._STI_USD_CAPS
title: _STI_USD_CAPS
author: windows-driver-content
description: The STI_USD_CAPS structure is used as a parameter for the IStiUSD::GetCapabilities method.
old-location: image\sti_usd_caps.htm
old-project: image
ms.assetid: 24dda069-5f93-469d-8ce3-87b488019b88
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: PSTI_USD_CAPS structure pointer [Imaging Devices], *PSTI_USD_CAPS, STI_USD_CAPS, PSTI_USD_CAPS, image.sti_usd_caps, stifnc_4f136561-e3a7-467d-b8be-a60db8534126.xml, stiusd/STI_USD_CAPS, STI_USD_CAPS structure [Imaging Devices], stiusd/PSTI_USD_CAPS, _STI_USD_CAPS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: stiusd.h
req.include-header: Stiusd.h
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
-	stiusd.h
apiname: 
-	STI_USD_CAPS
product: Windows
targetos: Windows
req.typenames: *PSTI_USD_CAPS, STI_USD_CAPS
req.product: Windows 10 or later.
---

# _STI_USD_CAPS structure


## -description


The STI_USD_CAPS structure is used as a parameter for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543817">IStiUSD::GetCapabilities</a> method.


## -syntax


````
typedef struct _STI_USD_CAPS {
  DWORD dwVersion;
  DWORD dwGenericCaps;
} STI_USD_CAPS, *PSTI_USD_CAPS;
````


## -struct-fields




### -field dwVersion

STI version number. This value must be STI_VERSION, defined in <i>Sti.h</i>.


### -field dwGenericCaps

Bit flags indicating driver capabilities. The following flags are defined in <i>Stiusd.h</i>.






##### - dwGenericCaps.STI_USD_GENCAP_NATIVE_PUSHSUPPORT

The driver supports asynchronous device notifications.


##### - dwGenericCaps.STI_USD_GENCAP_OPEN_DEVICE_FOR_ME

<i>Not used.</i>

