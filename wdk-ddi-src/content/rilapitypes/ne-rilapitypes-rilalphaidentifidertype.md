---
UID: NE:rilapitypes.RILALPHAIDENTIFIDERTYPE
title: RILALPHAIDENTIFIDERTYPE
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilalphaidentifidertype_2.htm
old-project: netvista
ms.assetid: 25e65540-b221-453a-95ff-ec2b96857475
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: netvista.rilalphaidentifidertype_2, rilapitypes/RIL_ALPHAIDENTIFIERTYPE_PRESENT, RILALPHAIDENTIFIDERTYPE enumeration [Network Drivers Starting with Windows Vista], RILALPHAIDENTIFIDERTYPE, RIL_ALPHAIDENTIFIERTYPE_MAX, RIL_ALPHAIDENTIFIERTYPE_PRESENT, rilapitypes/RIL_ALPHAIDENTIFIERTYPE_MAX, RIL_ALPHAIDENTIFIERTYPE_NOTPRESENT, rilapitypes/RILALPHAIDENTIFIDERTYPE, rilapitypes/RIL_ALPHAIDENTIFIERTYPE_NOTPRESENT
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
-	RILALPHAIDENTIFIDERTYPE
product: Windows
targetos: Windows
req.typenames: RILALPHAIDENTIFIDERTYPE
req.product: Windows 10 or later.
---

# RILALPHAIDENTIFIDERTYPE enumeration


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 


## -syntax


````
typedef enum _RILALPHAIDENTIFIDERTYPE { 
  RIL_ALPHAIDENTIFIERTYPE_PRESENT,
  RIL_ALPHAIDENTIFIERTYPE_NOTPRESENT,
  RIL_ALPHAIDENTIFIERTYPE_MAX
} RILALPHAIDENTIFIDERTYPE;
````


## -enum-fields




### -field RIL_ALPHAIDENTIFIERTYPE_UNKNOWN



### -field RIL_ALPHAIDENTIFIERTYPE_PRESENT



### -field RIL_ALPHAIDENTIFIERTYPE_NOTPRESENT



### -field RIL_ALPHAIDENTIFIERTYPE_MAX


