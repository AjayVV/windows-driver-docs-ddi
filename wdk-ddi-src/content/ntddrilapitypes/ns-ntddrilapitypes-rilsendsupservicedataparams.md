---
UID: NS:ntddrilapitypes.RILSENDSUPSERVICEDATAPARAMS
title: RILSENDSUPSERVICEDATAPARAMS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilsendsupservicedataparams.htm
old-project: netvista
ms.assetid: a48c9543-602f-4f3c-876e-9acc76ca1a6b
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: RILSENDSUPSERVICEDATAPARAMS structure [Network Drivers Starting with Windows Vista], *LPRILSENDSUPSERVICEDATAPARAMS, RILSENDSUPSERVICEDATAPARAMS, ntddrilapitypes/RILSENDSUPSERVICEDATAPARAMS, netvista.rilsendsupservicedataparams
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
-	RILSENDSUPSERVICEDATAPARAMS
product: Windows
targetos: Windows
req.typenames: RILSENDSUPSERVICEDATAPARAMS, *LPRILSENDSUPSERVICEDATAPARAMS
---

# RILSENDSUPSERVICEDATAPARAMS structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef struct _RILSENDSUPSERVICEDATAPARAMS {
  DWORD     dwExecutor;
  DWORD     dwDataSize;
  WCHAR [1] wszData;
} RILSENDSUPSERVICEDATAPARAMS, RILSENDSUPSERVICEDATAPARAMS;
````


## -struct-fields




### -field dwExecutor



### -field dwDataSize



### -field wszData


