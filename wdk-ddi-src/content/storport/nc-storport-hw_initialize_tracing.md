---
UID: NC:storport.HW_INITIALIZE_TRACING
title: HW_INITIALIZE_TRACING
author: windows-driver-content
description: The HwStorInitializeTracing callback routine allows the Storport virtual miniport driver to set up tracing and any related resources.
old-location: storage\hwstorinitializetracing.htm
old-project: storage
ms.assetid: e0d4ea58-415b-4ea4-9001-8a23ab44a1bf
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: storage.hwstorinitializetracing, HwStorInitializeTracing routine [Storage Devices], HwStorInitializeTracing, HW_INITIALIZE_TRACING, HW_INITIALIZE_TRACING, storport/HwStorInitializeTracing, storvmini_0c53c6e6-7c5c-4400-b923-c03a7756614f.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: storport.h
req.include-header: Storport.h
req.target-type: Universal
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
-	UserDefined
apilocation: 
-	Storport.h
apiname: 
-	HwStorInitializeTracing
product: Windows
targetos: Windows
req.typenames: *PSTORAGE_DEVICE_UNIQUE_IDENTIFIER, STORAGE_DEVICE_UNIQUE_IDENTIFIER
req.product: Windows 10 or later.
---

# HW_INITIALIZE_TRACING callback


## -description


The <b>HwStorInitializeTracing</b> callback routine allows the Storport virtual miniport driver to set up tracing and any related resources.


## -prototype


````
HW_INITIALIZE_TRACING HwStorInitializeTracing;

VOID HwStorInitializeTracing(
   IN PVOID Arg1,
   IN PVOID Arg2
)
{ ... }
````


## -parameters




### -param Arg1

The first parameter that is passed to <a href="..\storport\nf-storport-storportinitialize.md">StorPortInitialize</a>.


### -param Arg2

The second parameter that is passed to <a href="..\storport\nf-storport-storportinitialize.md">StorPortInitialize</a>.


## -returns


None



## -remarks


The name <b>HwStorInitializeTracing</b> is placeholder text for the actual routine name. The actual prototype of this routine is defined in Storport.h as follows:
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef
VOID
HW_INITIALIZE_TRACING (
  _In_ PVOID  Arg1,
  _In_ PVOID  Arg2
  );</pre>
</td>
</tr>
</table></span></div>The port driver calls the Storport virtual miniport's <b>HwStorInitializeTracing</b> at PASSIVE_LEVEL.


