---
UID: NE:rilapitypes.RILCALLHANDOVERSTATEPARAMMASK
title: RILCALLHANDOVERSTATEPARAMMASK
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilcallhandoverstateparammask_2.htm
old-project: netvista
ms.assetid: a9a5c8dc-8ffa-4142-879c-3a782b45dbff
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: rilapitypes/RIL_PARAM_HANDOVER_NEW_TYPE, RIL_PARAM_HANDOVER_OLD_TYPE, RIL_PARAM_HANDOVER_NEW_TYPE, netvista.rilcallhandoverstateparammask_2, rilapitypes/RIL_PARAM_HANDOVER_OLD_TYPE, RIL_PARAM_HANDOVER_ALL, rilapitypes/RILCALLHANDOVERSTATEPARAMMASK, RIL_PARAM_HANDOVER_3GPPCAUSE, rilapitypes/RIL_PARAM_HANDOVER_ALL, RILCALLHANDOVERSTATEPARAMMASK, rilapitypes/RIL_PARAM_HANDOVER_3GPPCAUSE, RILCALLHANDOVERSTATEPARAMMASK enumeration [Network Drivers Starting with Windows Vista]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.lib: NtosKrnl.exe
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
-	RILCALLHANDOVERSTATEPARAMMASK
product: Windows
targetos: Windows
req.typenames: RILCALLHANDOVERSTATEPARAMMASK
req.product: Windows 10 or later.
---

# RILCALLHANDOVERSTATEPARAMMASK enumeration


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 


## -syntax


````
typedef enum _RILCALLHANDOVERSTATEPARAMMASK { 
  RIL_PARAM_HANDOVER_OLD_TYPE,
  RIL_PARAM_HANDOVER_NEW_TYPE,
  RIL_PARAM_HANDOVER_3GPPCAUSE,
  RIL_PARAM_HANDOVER_ALL
} RILCALLHANDOVERSTATEPARAMMASK;
````


## -enum-fields




### -field RIL_PARAM_HANDOVER_PHASE



### -field RIL_PARAM_HANDOVER_OLD_TYPE



### -field RIL_PARAM_HANDOVER_NEW_TYPE



### -field RIL_PARAM_HANDOVER_3GPPCAUSE



### -field RIL_PARAM_HANDOVER_ALL


