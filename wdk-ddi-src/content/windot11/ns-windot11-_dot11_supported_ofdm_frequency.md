---
UID: NS:windot11._DOT11_SUPPORTED_OFDM_FREQUENCY
title: _DOT11_SUPPORTED_OFDM_FREQUENCY
author: windows-driver-content
description: Important  The Native 802.11 Wireless LAN interface is deprecated in Windows 10 and later.
old-location: netvista\dot11_supported_ofdm_frequency.htm
old-project: netvista
ms.assetid: 79017890-c045-4996-b5d3-fa000ffff5a0
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: DOT11_SUPPORTED_OFDM_FREQUENCY, windot11/DOT11_SUPPORTED_OFDM_FREQUENCY, PDOT11_SUPPORTED_OFDM_FREQUENCY structure pointer [Network Drivers Starting with Windows Vista], PDOT11_SUPPORTED_OFDM_FREQUENCY, Native_802.11_data_types_5a7cc235-128d-4209-a250-49ec0b2b8ad7.xml, _DOT11_SUPPORTED_OFDM_FREQUENCY, *PDOT11_SUPPORTED_OFDM_FREQUENCY, DOT11_SUPPORTED_OFDM_FREQUENCY structure [Network Drivers Starting with Windows Vista], netvista.dot11_supported_ofdm_frequency, windot11/PDOT11_SUPPORTED_OFDM_FREQUENCY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: windot11.h
req.include-header: Ndis.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 and later versions of the Windows operating   systems.
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
-	windot11.h
apiname: 
-	DOT11_SUPPORTED_OFDM_FREQUENCY
product: Windows
targetos: Windows
req.typenames: DOT11_SUPPORTED_OFDM_FREQUENCY, *PDOT11_SUPPORTED_OFDM_FREQUENCY
req.product: Windows 10 or later.
---

# _DOT11_SUPPORTED_OFDM_FREQUENCY structure


## -description


<div class="alert"><b>Important</b>  The <a href="https://msdn.microsoft.com/library/windows/hardware/ff560689">Native 802.11 Wireless LAN</a> interface is deprecated in Windows 10 and later. Please use the WLAN Device Driver Interface (WDI) instead. For more information about WDI, see <a href="https://msdn.microsoft.com/6EF92E34-7BC9-465E-B05D-2BCB29165A18">WLAN Universal Windows driver model</a>.</div><div> </div>The DOT11_SUPPORTED_OFDM_FREQUENCY structure specifies a supported channel center frequency entry in
  a 
  <mshelp:link keywords="netvista.dot11_supported_ofdm_frequency_list" tabindex="0"><b>
  DOT11_SUPPORTED_OFDM_FREQUENCY_LIST</b></mshelp:link> structure.


## -syntax


````
typedef struct _DOT11_SUPPORTED_OFDM_FREQUENCY {
  ULONG uCenterFrequency;
} DOT11_SUPPORTED_OFDM_FREQUENCY, *PDOT11_SUPPORTED_OFDM_FREQUENCY;
````


## -struct-fields




### -field uCenterFrequency

A ULONG value that represents a channel center frequency, in MHz, that the 802.11 station can
     operate with.


## -see-also

<mshelp:link keywords="netvista.dot11_supported_ofdm_frequency_list" tabindex="0"><b>
   DOT11_SUPPORTED_OFDM_FREQUENCY_LIST</b></mshelp:link>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20DOT11_SUPPORTED_OFDM_FREQUENCY structure%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

