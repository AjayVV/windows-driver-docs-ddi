---
UID: NS:ata._IDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO
title: _IDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO
author: windows-driver-content
description: Note  This structure is for internal use only and should not be called from your code. .
old-location: storage\identify_device_data_log_page_zoned_device_info.htm
old-project: storage
ms.assetid: 2F0B6C1F-54CC-47CF-B0D0-A53FAB80AF91
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: ata/PIDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO, PIDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO, _IDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO, storage.identify_device_data_log_page_zoned_device_info, IDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO structure [Storage Devices], ata/IDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO, *PIDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO, IDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO, PIDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO structure pointer [Storage Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ata.h
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
-	Ata.h
apiname: 
-	IDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO
product: Windows
targetos: Windows
req.typenames: *PIDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO, IDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO
---

# _IDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]


<div class="alert"><b>Note</b>  This  structure is for internal use only and should not be called from your code.</div>
<div> </div>



## -syntax


````
typedef struct _IDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO {
  IDENTIFY_DEVICE_DATA_LOG_PAGE_HEADER Header;
  struct {
    ULONGLONG URSWRZ  :1;
    ULONGLONG Reserved  :62;
    ULONGLONG Valid  :1;
  } ZonedDeviceCapabilities;
  struct {
    ULONGLONG Reserved  :63;
    ULONGLONG Valid  :1;
  } ZonedDeviceSettings;
  struct {
    ULONGLONG Number  :32;
    ULONGLONG Reserved  :31;
    ULONGLONG Valid  :1;
  } OptimalNumberOfOpenSequentialWritePreferredZones;
  struct {
    ULONGLONG Number  :32;
    ULONGLONG Reserved  :31;
    ULONGLONG Valid  :1;
  } OptimalNumberOfNonSequentiallyWrittenSequentialWritePreferredZones;
  struct {
    ULONGLONG Number  :32;
    ULONGLONG Reserved  :31;
    ULONGLONG Valid  :1;
  } MaxNumberOfOpenSequentialWriteRequiredZones;
  struct {
    ULONGLONG ZacMinorVersion  :16;
    ULONGLONG Reserved0  :47;
    ULONGLONG Valid  :1;
  } Version;
  UCHAR                                Reserved[456];
} IDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO, *PIDENTIFY_DEVICE_DATA_LOG_PAGE_ZONED_DEVICE_INFO;
````


## -struct-fields




### -field ZonedDeviceCapabilities



### -field ZonedDeviceCapabilities.URSWRZ

N/A


### -field ZonedDeviceCapabilities.Reserved

N/A


### -field ZonedDeviceCapabilities.Valid

N/A


### -field ZonedDeviceSettings



### -field ZonedDeviceSettings.Reserved

N/A


### -field ZonedDeviceSettings.Valid

N/A


### -field OptimalNumberOfOpenSequentialWritePreferredZones



### -field OptimalNumberOfOpenSequentialWritePreferredZones.Number

N/A


### -field OptimalNumberOfOpenSequentialWritePreferredZones.Reserved

N/A


### -field OptimalNumberOfOpenSequentialWritePreferredZones.Valid

N/A


### -field OptimalNumberOfNonSequentiallyWrittenSequentialWritePreferredZones



### -field OptimalNumberOfNonSequentiallyWrittenSequentialWritePreferredZones.Number

N/A


### -field OptimalNumberOfNonSequentiallyWrittenSequentialWritePreferredZones.Reserved

N/A


### -field OptimalNumberOfNonSequentiallyWrittenSequentialWritePreferredZones.Valid

N/A


### -field MaxNumberOfOpenSequentialWriteRequiredZones



### -field MaxNumberOfOpenSequentialWriteRequiredZones.Number

N/A


### -field MaxNumberOfOpenSequentialWriteRequiredZones.Reserved

N/A


### -field MaxNumberOfOpenSequentialWriteRequiredZones.Valid

N/A


### -field Version



### -field Version.ZacMinorVersion

N/A


### -field Version.Reserved0

N/A


### -field Version.Valid

N/A


### -field Header

N/A


### -field Reserved

N/A

