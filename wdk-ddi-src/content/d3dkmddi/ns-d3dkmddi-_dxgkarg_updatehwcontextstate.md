---
UID: NS:d3dkmddi._DXGKARG_UPDATEHWCONTEXTSTATE
title: _DXGKARG_UPDATEHWCONTEXTSTATE
author: windows-driver-content
description: Used to update the context state.
old-location: display\dxgkarg_updatehwcontextstate.htm
old-project: display
ms.assetid: 39BF7EBF-DD13-41F0-9F54-78E5D82CAB4F
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: d3dkmddi/DXGKARG_UPDATEHWCONTEXTSTATE, DXGKARG_UPDATEHWCONTEXTSTATE, DXGKARG_UPDATEHWCONTEXTSTATE structure [Display Devices], display.dxgkarg_updatehwcontextstate, _DXGKARG_UPDATEHWCONTEXTSTATE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dkmddi.h
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
req.irql: PASSIVE_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	d3dkmddi.h
apiname: 
-	DXGKARG_UPDATEHWCONTEXTSTATE
product: Windows
targetos: Windows
req.typenames: DXGKARG_UPDATEHWCONTEXTSTATE
---

# _DXGKARG_UPDATEHWCONTEXTSTATE structure


## -description


Used to update the context state.


## -syntax


````
typedef struct _DXGKARG_UPDATEHWCONTEXTSTATE {
  HANDLE                          hHwContext;
  UINT64                          ContextSwitchFence;
  UINT                            Priority;
  DXGK_UPDATEHWCONTEXTSTATE_FLAGS Flags;
} DXGKARG_UPDATEHWCONTEXTSTATE;
````


## -struct-fields




### -field hHwContext

The hardware context whose priority or execution state is being changed.


### -field ContextSwitchFence

Context switch fence value associated with this state change request.


### -field Priority

Execution priority of this context relative to other running contexts on this node.


### -field Flags

Context execution state flags.


