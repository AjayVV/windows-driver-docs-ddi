---
UID: NS:gnssdriver.GNSS_PLATFORM_CAPABILITY
title: GNSS_PLATFORM_CAPABILITY
author: windows-driver-content
description: This structure is used to communicate the platform/HLOS capabilities to the underlying GNSS driver.
old-location: sensors\gnss_platform_capability.htm
old-project: sensors
ms.assetid: A97DE517-26ED-452F-9066-94F73BC47BDE
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: GNSS_PLATFORM_CAPABILITY structure [Sensor Devices], PGNSS_PLATFORM_CAPABILITY, sensors.gnss_platform_capability, gnssdriver/GNSS_PLATFORM_CAPABILITY, GNSS_PLATFORM_CAPABILITY, *PGNSS_PLATFORM_CAPABILITY, gnssdriver/PGNSS_PLATFORM_CAPABILITY, PGNSS_PLATFORM_CAPABILITY structure pointer [Sensor Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: gnssdriver.h
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
-	gnssdriver.h
apiname: 
-	GNSS_PLATFORM_CAPABILITY
product: Windows
targetos: Windows
req.typenames: *PGNSS_PLATFORM_CAPABILITY, GNSS_PLATFORM_CAPABILITY
---

# GNSS_PLATFORM_CAPABILITY structure


## -description


This structure is used to communicate the platform/HLOS capabilities to the underlying GNSS driver.


## -syntax


````
typedef struct {
  ULONG Size;
  ULONG Version;
  BOOL  SupportAgnssInjection;
  ULONG AgnssFormatSupported;
  BOOL  Reserved;
  BYTE  Unused[512];
} GNSS_PLATFORM_CAPABILITY, *PGNSS_PLATFORM_CAPABILITY;
````


## -struct-fields




### -field Size

Structure size.


### -field Version

Version number.


### -field SupportAgnssInjection

Indicates that the platform supports AGNSS injection via the location platform.


### -field AgnssFormatSupported

Specifies a bitmask containing the different AGNSS formats (GNSS_AGNSSFORMAT_*) that the GNSS driver or device supports.


### -field Unused

 



#### - Reserved

Reserved for future use.


#### - Unused[512]

Padding buffer.


## -remarks


 This is a list of individual capability support of the GNSS adapter. The platform capability is represented in the same way as the device capabilities are represented.


