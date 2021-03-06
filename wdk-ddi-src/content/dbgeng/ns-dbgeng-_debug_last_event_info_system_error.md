---
UID: NS:dbgeng._DEBUG_LAST_EVENT_INFO_SYSTEM_ERROR
title: _DEBUG_LAST_EVENT_INFO_SYSTEM_ERROR
author: windows-driver-content
description: Describes the system error of the last event.
old-location: debugger\debug_last_event_info_system_error.htm
old-project: debugger
ms.assetid: A66C26AB-3AED-4F44-9F7F-DE5A92BB611A
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: PDEBUG_LAST_EVENT_INFO_SYSTEM_ERROR, *PDEBUG_LAST_EVENT_INFO_SYSTEM_ERROR, DEBUG_LAST_EVENT_INFO_SYSTEM_ERROR structure [Windows Debugging], debugger.debug_last_event_info_system_error, dbgeng/PDEBUG_LAST_EVENT_INFO_SYSTEM_ERROR, PDEBUG_LAST_EVENT_INFO_SYSTEM_ERROR structure pointer [Windows Debugging], _DEBUG_LAST_EVENT_INFO_SYSTEM_ERROR, DEBUG_LAST_EVENT_INFO_SYSTEM_ERROR, dbgeng/DEBUG_LAST_EVENT_INFO_SYSTEM_ERROR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dbgeng.h
req.include-header: DbgEng.h
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
-	DbgEng.h
apiname: 
-	DEBUG_LAST_EVENT_INFO_SYSTEM_ERROR
product: Windows
targetos: Windows
req.typenames: *PDEBUG_LAST_EVENT_INFO_SYSTEM_ERROR, DEBUG_LAST_EVENT_INFO_SYSTEM_ERROR
---

# _DEBUG_LAST_EVENT_INFO_SYSTEM_ERROR structure


## -description


Describes the system error of the last event.


## -syntax


````
typedef struct _DEBUG_LAST_EVENT_INFO_SYSTEM_ERROR {
  ULONG Error;
  ULONG Level;
} DEBUG_LAST_EVENT_INFO_SYSTEM_ERROR, *PDEBUG_LAST_EVENT_INFO_SYSTEM_ERROR;
````


## -struct-fields




### -field Error

The error code for the event.


### -field Level

The error level for the event.

