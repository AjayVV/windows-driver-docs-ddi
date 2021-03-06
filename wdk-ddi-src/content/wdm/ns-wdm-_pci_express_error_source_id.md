---
UID: NS:wdm._PCI_EXPRESS_ERROR_SOURCE_ID
title: _PCI_EXPRESS_ERROR_SOURCE_ID
author: windows-driver-content
description: The PCI_EXPRESS_ERROR_SOURCE_ID structure describes the identifiers of the first correctable error and the first uncorrectable error that are reported in the PCI Express (PCIe) root error status register.
old-location: pci\pci_express_error_source_id.htm
old-project: PCI
ms.assetid: 53efddbc-0e65-487c-b406-c7d093ca5667
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: pci_struct_f111f61b-46a0-450d-bbce-172f125a6903.xml, PCI_EXPRESS_ERROR_SOURCE_ID, PPCI_EXPRESS_ERROR_SOURCE_ID union pointer [Buses], *PPCI_EXPRESS_ERROR_SOURCE_ID, PCI_EXPRESS_ERROR_SOURCE_ID union [Buses], PPCI_EXPRESS_ERROR_SOURCE_ID, wdm/PCI_EXPRESS_ERROR_SOURCE_ID, PCI.pci_express_error_source_id, _PCI_EXPRESS_ERROR_SOURCE_ID, wdm/PPCI_EXPRESS_ERROR_SOURCE_ID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wdm.h
req.include-header: Ntddk.h, Wdm.h
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
req.irql: PASSIVE_LEVEL (see Remarks section)
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	wdm.h
apiname: 
-	PCI_EXPRESS_ERROR_SOURCE_ID
product: Windows
targetos: Windows
req.typenames: *PPCI_EXPRESS_ERROR_SOURCE_ID, PCI_EXPRESS_ERROR_SOURCE_ID
req.product: Windows 10 or later.
---

# _PCI_EXPRESS_ERROR_SOURCE_ID structure


## -description


The PCI_EXPRESS_ERROR_SOURCE_ID structure describes the identifiers of the first correctable error and the first uncorrectable error that are reported in the PCI Express (PCIe) root error status register.


## -syntax


````
typedef union _PCI_EXPRESS_ERROR_SOURCE_ID {
  struct {
    USHORT CorrectableSourceIdFun  :3;
    USHORT CorrectableSourceIdDev  :5;
    USHORT CorrectableSourceIdBus  :8;
    USHORT UncorrectableSourceIdFun  :3;
    USHORT UncorrectableSourceIdDev  :5;
    USHORT UncorrectableSourceIdBus  :8;
  };
  ULONG  AsULONG;
} PCI_EXPRESS_ERROR_SOURCE_ID, *PPCI_EXPRESS_ERROR_SOURCE_ID;
````


## -struct-fields




### -field DUMMYSTRUCTNAME

 


### -field DUMMYSTRUCTNAME.CorrectableSourceIdFun

 


### -field DUMMYSTRUCTNAME.CorrectableSourceIdDev

 


### -field DUMMYSTRUCTNAME.CorrectableSourceIdBus

 


### -field DUMMYSTRUCTNAME.UncorrectableSourceIdFun

 


### -field DUMMYSTRUCTNAME.UncorrectableSourceIdDev

 


### -field DUMMYSTRUCTNAME.UncorrectableSourceIdBus

 


### -field AsULONG

A ULONG representation of the contents of the PCI_EXPRESS_ERROR_SOURCE_ID structure.


#### - UncorrectableSourceIdFun

The function number of the requester that reported the first uncorrectable error.


#### - UncorrectableSourceIdBus

The bus number of the requester that reported the first uncorrectable error.


#### - UncorrectableSourceIdDev

The device number of the requester that reported the first uncorrectable error.


#### - CorrectableSourceIdBus

The bus number of the requester that reported the first correctable error.


#### - CorrectableSourceIdDev

The device number of the requester that reported the first correctable error.


#### - CorrectableSourceIdFun

The function number of the requester that reported the first correctable error.


## -remarks


The PCI_EXPRESS_ERROR_SOURCE_ID structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_ERROR_SOURCE_ID structure is contained in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537472">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a> structure.



## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff537472">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [PCI\buses]:%20PCI_EXPRESS_ERROR_SOURCE_ID union%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

