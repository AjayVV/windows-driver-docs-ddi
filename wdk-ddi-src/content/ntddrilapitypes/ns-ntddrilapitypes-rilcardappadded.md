---
UID: NS:ntddrilapitypes.RILCARDAPPADDED
title: RILCARDAPPADDED
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilcardappadded.htm
old-project: netvista
ms.assetid: f0488502-8c0c-4e2d-81d0-98b206c74d78
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: RILCARDAPPADDED, netvista.rilcardappadded, RILCARDAPPADDED structure [Network Drivers Starting with Windows Vista], ntddrilapitypes/RILCARDAPPADDED, *LPRILCARDAPPADDED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
-	RILCARDAPPADDED
product: Windows
targetos: Windows
req.typenames: *LPRILCARDAPPADDED, RILCARDAPPADDED
---

# RILCARDAPPADDED structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef struct _RILCARDAPPADDED {
  DWORD           cbSize;
  DWORD           dwParams;
  DWORD           dwSlotIndex;
  RILUICCAPPINFO  rilUiccAppInfo;
} RILCARDAPPADDED, RILCARDAPPADDED;
````


## -struct-fields




### -field cbSize



### -field dwParams



### -field dwSlotIndex



### -field rilUiccAppInfo


