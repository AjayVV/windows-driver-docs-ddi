---
UID: NS:dot11wdi._WDI_FRAME_METADATA
title: _WDI_FRAME_METADATA
author: windows-driver-content
description: The WDI_FRAME_METADATA structure defines the frame metadata.
old-location: netvista\wdi_frame_metadata.htm
old-project: netvista
ms.assetid: 34733e8f-cbe0-4fcd-abcf-6791e298282f
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: PWDI_FRAME_METADATA structure pointer [Network Drivers Starting with Windows Vista], *PWDI_FRAME_METADATA, dot11wdi/PWDI_FRAME_METADATA, netvista.wdi_frame_metadata, netvista.wifi_frame_metadata, WDI_FRAME_METADATA, PWDI_FRAME_METADATA, _WDI_FRAME_METADATA, WDI_FRAME_METADATA structure [Network Drivers Starting with Windows Vista], dot11wdi/WDI_FRAME_METADATA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dot11wdi.h
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
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	dot11wdi.h
apiname: 
-	WDI_FRAME_METADATA
product: Windows
targetos: Windows
req.typenames: WDI_FRAME_METADATA, *PWDI_FRAME_METADATA
---

# _WDI_FRAME_METADATA structure


## -description


The 
  WDI_FRAME_METADATA structure defines the frame metadata.


## -syntax


````
typedef struct _WDI_FRAME_METADATA {
  LIST_ENTRY       Linkage;
  PNET_BUFFER_LIST pNBL;
  WDI_FRAME_ID     FrameID;
  UINT16           wPad;
#ifdef _WIN64
  UINT32           dPad;
#endif 
  union {
    WDI_TX_METADATA txMetaData;
    WDI_RX_METADATA rxMetaData;
  } u;
} WDI_FRAME_METADATA, *PWDI_FRAME_METADATA;
````


## -struct-fields




### -field u



### -field u.txMetaData

TX metadata.


### -field u.rxMetaData

RX metadata.


### -field Linkage

Reserved for use by the Microsoft component.


### -field pNBL

Set by the LE on RX path and the UE on TX path when the metadata is associated with an NBL.


### -field FrameID

Filled in by the Microsoft component.


### -field wPad

Padding.


### -field dPad

Padding.


## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff554296">LIST_ENTRY</a>

<a href="..\dot11wdi\ns-dot11wdi-_wdi_tx_metadata.md">WDI_TX_METADATA</a>

<a href="..\dot11wdi\ns-dot11wdi-_wdi_rx_metadata.md">WDI_RX_METADATA</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/mt297642">WDI_FRAME_ID</a>

<a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20WDI_FRAME_METADATA structure%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

