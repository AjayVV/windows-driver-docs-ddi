---
UID: NS:ks.KSPIN_DESCRIPTOR
title: KSPIN_DESCRIPTOR
author: windows-driver-content
description: The KSPIN_DESCRIPTOR structure describes the basic KSPROPSETID_Pin properties of a pin type.
old-location: stream\kspin_descriptor.htm
old-project: stream
ms.assetid: 0e7fccd1-1ced-41e7-8e75-8f4fa496ea06
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: *PKSPIN_DESCRIPTOR, ks/KSPIN_DESCRIPTOR, PKSPIN_DESCRIPTOR structure pointer [Streaming Media Devices], stream.kspin_descriptor, KSPIN_DESCRIPTOR, ks-struct_adeadb36-6cf2-4c36-a1b4-a7852e98303f.xml, PKSPIN_DESCRIPTOR, KSPIN_DESCRIPTOR structure [Streaming Media Devices], ks/PKSPIN_DESCRIPTOR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ks.h
req.include-header: Ks.h
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
-	ks.h
apiname: 
-	KSPIN_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: *PKSPIN_DESCRIPTOR, KSPIN_DESCRIPTOR
---

# KSPIN_DESCRIPTOR structure


## -description


The KSPIN_DESCRIPTOR structure describes the basic <a href="https://msdn.microsoft.com/library/windows/hardware/ff566584">KSPROPSETID_Pin</a> properties of a pin type.


## -syntax


````
typedef struct {
  ULONG                 InterfacesCount;
  const KSPIN_INTERFACE *Interfaces;
  ULONG                 MediumsCount;
  const KSPIN_MEDIUM    *Mediums;
  ULONG                 DataRangesCount;
  const PKSDATARANGE    *DataRanges;
  KSPIN_DATAFLOW        DataFlow;
  KSPIN_COMMUNICATION   Communication;
  const GUID            *Category;
  const GUID            *Name;
  union {
    LONGLONG Reserved;
    struct {
      ULONG        ConstrainedDataRangesCount;
      PKSDATARANGE *ConstrainedDataRanges;
    };
  };
} KSPIN_DESCRIPTOR, *PKSPIN_DESCRIPTOR;
````


## -struct-fields




### -field ConstrainedDataRangesCount

Specifies the number of entries in the array pointed to by <b>ConstrainedDataRanges</b>.


### -field ConstrainedDataRanges

Points to an array of <a href="..\ks\ns-ks-ksdataformat.md">KSDATARANGE</a> structures. Indicates the set of data ranges the pin type currently supports, based on the driver's internal state.


### -field Reserved

Not used.  A member of an unnamed union used to force proper alignment on the unnamed structure.


### -field InterfacesCount

Specifies the size of the array pointed to by <b>Interfaces</b>.


### -field Interfaces

An array of <a href="..\ks\ns-ks-ksidentifier.md">KSPIN_INTERFACE</a> structures specifying the interfaces supported by this pin type.


### -field MediumsCount

Specifies the number of elements in the array pointed to by <b>Mediums</b>.


### -field Mediums

An array of <a href="..\ks\ns-ks-ksidentifier.md">KSPIN_MEDIUM</a> structures specifying the mediums supported by this pin type.


### -field DataRangesCount

Specifies the size of the array pointed to by <b>DataRanges</b>.


### -field DataRanges

An array of <a href="..\ks\ns-ks-ksdataformat.md">KSDATARANGE</a> structures specifying the data ranges supported by this pin type.


### -field DataFlow

Specifies either <b>KSPIN_DATAFLOW_IN</b> or KSPIN_DATAFLOW_OUT. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff565197">KSPROPERTY_PIN_DATAFLOW</a>.


### -field Communication

Specifies KSPIN_COMMUNICATION_NONE, KSPIN_COMMUNICATION_SINK, KSPIN_COMMUNICATION_SOURCE, KSPIN_COMMUNICATION_BOTH or KSPIN_COMMUNICATION_BRIDGE. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff565194">KSPROPERTY_PIN_COMMUNICATION</a> for the meaning of each value.


### -field Category

Specifies a pointer to a KS pin category GUID. The KS pin category GUID identifies the general category of functionality that the pin provides. Examples of KS pin category GUIDs are KSNODETYPE_SPEAKER, KSNODETYPE_HEADPHONES, and KSNODETYPE_MICROPHONE, which are all defined in <i>Ksmedia.h</i>. Also see <a href="https://msdn.microsoft.com/fd4a4afd-2c17-4002-87ae-21501b1d75c1">Pin Category Property</a>.


### -field Name

Specifies the GUID of the localized Unicode string name for the pin type, stored in the Registry.


## -remarks


Drivers typically define one KSPIN_DESCRIPTOR structure for each pin type they support.



## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff566584">KSPROPSETID_Pin</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff565194">KSPROPERTY_PIN_COMMUNICATION</a>

<a href="..\ks\ns-ks-ksidentifier.md">KSPIN_MEDIUM</a>

<a href="..\ks\ns-ks-ksdataformat.md">KSDATARANGE</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff565197">KSPROPERTY_PIN_DATAFLOW</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KSPIN_DESCRIPTOR structure%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

