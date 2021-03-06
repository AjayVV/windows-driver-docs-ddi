---
UID: NE:ntddrilapitypes.RILSUPSERVICEDATASTATUS
title: RILSUPSERVICEDATASTATUS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilsupservicedatastatus.htm
old-project: netvista
ms.assetid: 60cecce7-9085-4cbd-b637-e24af51d1c22
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: ntddrilapitypes/RIL_SUPSVCDATASTATUS_ERROR, netvista.rilsupservicedatastatus, RIL_SUPSVCDATASTATUS_FURTHERINFOREQUIRED, RIL_SUPSVCDATASTATUS_MAX, ntddrilapitypes/RIL_SUPSVCDATASTATUS_TIMEOUT, RILSUPSERVICEDATASTATUS, RIL_SUPSVCDATASTATUS_ERROR, ntddrilapitypes/RILSUPSERVICEDATASTATUS, RIL_SUPSVCDATASTATUS_TIMEOUT, ntddrilapitypes/RIL_SUPSVCDATASTATUS_MAX, ntddrilapitypes/RIL_SUPSVCDATASTATUS_FURTHERINFOREQUIRED, RILSUPSERVICEDATASTATUS enumeration [Network Drivers Starting with Windows Vista]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntddrilapitypes.h
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
-	ntddrilapitypes.h
apiname: 
-	RILSUPSERVICEDATASTATUS
product: Windows
targetos: Windows
req.typenames: RILSUPSERVICEDATASTATUS
---

# RILSUPSERVICEDATASTATUS enumeration


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef enum _RILSUPSERVICEDATASTATUS { 
  RIL_SUPSVCDATASTATUS_FURTHERINFOREQUIRED,
  RIL_SUPSVCDATASTATUS_TIMEOUT,
  RIL_SUPSVCDATASTATUS_ERROR,
  RIL_SUPSVCDATASTATUS_MAX
} RILSUPSERVICEDATASTATUS;
````


## -enum-fields




### -field RIL_SUPSVCDATASTATUS_NOINFOREQUIRED



### -field RIL_SUPSVCDATASTATUS_FURTHERINFOREQUIRED



### -field RIL_SUPSVCDATASTATUS_TIMEOUT



### -field RIL_SUPSVCDATASTATUS_ERROR



### -field RIL_SUPSVCDATASTATUS_MAX


