---
UID: NE:pepfx._PEP_PERF_STATE_TYPE
title: _PEP_PERF_STATE_TYPE
author: windows-driver-content
description: The PEP_PERF_STATE_TYPE enumeration indicates the type of performance information that is specified for a performance state (P-state) of a component.
old-location: kernel\pep_perf_state_type.htm
old-project: kernel
ms.assetid: 8DF40988-995E-4C37-8864-0C405DE885C9
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: PepPerfStateTypeMax, *PPEP_PERF_STATE_TYPE, pepfx/PepPerfStateTypeDiscrete, _PEP_PERF_STATE_TYPE, pepfx/PepPerfStateTypeRange, PepPerfStateTypeRange, PEP_PERF_STATE_TYPE, pepfx/PepPerfStateTypeMax, pepfx/PEP_PERF_STATE_TYPE, PEP_PERF_STATE_TYPE enumeration [Kernel-Mode Driver Architecture], PepPerfStateTypeDiscrete, kernel.pep_perf_state_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: pepfx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 10.
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
req.irql: See Remarks.
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	pepfx.h
apiname: 
-	PEP_PERF_STATE_TYPE
product: Windows
targetos: Windows
req.typenames: PEP_PERF_STATE_TYPE, *PPEP_PERF_STATE_TYPE
---

# _PEP_PERF_STATE_TYPE enumeration


## -description


The <b>PEP_PERF_STATE_TYPE</b> enumeration indicates the type of performance information that is specified for a performance state (P-state) of a component.


## -syntax


````
typedef enum _PEP_PERF_STATE_TYPE { 
  PepPerfStateTypeDiscrete  = 0,
  PepPerfStateTypeRange,
  PepPerfStateTypeMax
} PEP_PERF_STATE_TYPE;
````


## -enum-fields




### -field PepPerfStateTypeDiscrete

The performance information is specified as a set of discrete values.


### -field PepPerfStateTypeRange

The performance information is specified as a range of values.


### -field PepPerfStateTypeMax

Reserved for use by operating system.


## -remarks


The <b>Type</b> member of the <a href="..\pepfx\ns-pepfx-_pep_component_perf_set.md">PEP_COMPONENT_PERF_SET</a> structure is a <b>PEP_PERF_STATE_TYPE</b> enumeration value.



## -see-also

<a href="..\pepfx\ns-pepfx-_pep_component_perf_set.md">PEP_COMPONENT_PERF_SET</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20PEP_PERF_STATE_TYPE enumeration%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

