---
UID: NS:rilapitypes.RILSETSLOTPOWERPARAMS
title: RILSETSLOTPOWERPARAMS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilsetslotpowerparams_2.htm
old-project: netvista
ms.assetid: 1f62344f-9e54-4a17-9c0c-ef46614508f2
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: RILSETSLOTPOWERPARAMS structure [Network Drivers Starting with Windows Vista], *LPRILSETSLOTPOWERPARAMS, netvista.rilsetslotpowerparams_2, RILSETSLOTPOWERPARAMS, rilapitypes/RILSETSLOTPOWERPARAMS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: rilapitypes.h
req.include-header: 
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
-	rilapitypes.h
apiname: 
-	RILSETSLOTPOWERPARAMS
product: Windows
targetos: Windows
req.typenames: RILSETSLOTPOWERPARAMS, *LPRILSETSLOTPOWERPARAMS
req.product: Windows 10 or later.
---

# RILSETSLOTPOWERPARAMS structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 


## -syntax


````
typedef struct _RILSETSLOTPOWERPARAMS {
  DWORD  dwSlotIndex;
  BOOL   fPowerOn;
} RILSETSLOTPOWERPARAMS, RILSETSLOTPOWERPARAMS;
````


## -struct-fields




### -field dwSlotIndex



### -field fPowerOn


