---
UID: NF:d3dkmthk.D3DKMTQueryProtectedSessionStatus
title: D3DKMTQueryProtectedSessionStatus function
author: windows-driver-content
description: Used to query the status of the protected session.
old-location: display\d3dkmtqueryprotectedsessionstatus.htm
old-project: display
ms.assetid: 787f20a4-51b6-44e3-aefb-2dc529359545
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.d3dkmtqueryprotectedsessionstatus, D3DKMTQueryProtectedSessionStatus method [Display Devices], d3dkmthk/D3DKMTQueryProtectedSessionStatus, D3DKMTQueryProtectedSessionStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d3dkmthk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
-	d3dkmthk.h
apiname: 
-	D3DKMTQueryProtectedSessionStatus
product: Windows
targetos: Windows
req.typenames: D3DKMT_DRIVERVERSION
---

# D3DKMTQueryProtectedSessionStatus function


## -description


Used to query the status of the protected session.
			
            


## -syntax


````
NTSTATUS  D3DKMTQueryProtectedSessionStatus(
   D3DKMT_QUERYPROTECTEDSESSIONSTATUS  D3dkmt_queryprotectedsessionstatus
);
````


## -parameters





#### - D3dkmt_queryprotectedsessionstatus

Holds the information for the status of the protected session.


## -returns



Returns STATUS_SUCCESS if completed successfully.


