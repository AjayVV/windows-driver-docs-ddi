---
UID: NS:wwan._WWAN_IPADDRESS_ENTRY
title: _WWAN_IPADDRESS_ENTRY
author: windows-driver-content
description: The WWAN_IPADDRESS_ENTRY structure represents either the IPV4 or IPV6 address of a PDP context.
old-location: netvista\wwan_ipaddress_entry.htm
old-project: netvista
ms.assetid: 85615799-5AA0-4D83-9246-73F3C7ABFFF6
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: wwan/WWAN_IPADDRESS_ENTRY, _WWAN_IPADDRESS_ENTRY, *PWWAN_IPADDRESS_ENTRY, WWAN_IPADDRESS_ENTRY, WWAN_IPADDRESS_ENTRY structure [Network Drivers Starting with Windows Vista], PWWAN_IPADDRESS_ENTRY structure pointer [Network Drivers Starting with Windows Vista], netvista.wwan_ipaddress_entry, wwan/PWWAN_IPADDRESS_ENTRY, PWWAN_IPADDRESS_ENTRY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wwan.h
req.include-header: Wwan.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 8.1 and later versions of Windows.
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
-	wwan.h
apiname: 
-	WWAN_IPADDRESS_ENTRY
product: Windows
targetos: Windows
req.typenames: WWAN_IPADDRESS_ENTRY, *PWWAN_IPADDRESS_ENTRY
req.product: Windows 10 or later.
---

# _WWAN_IPADDRESS_ENTRY structure


## -description


The WWAN_IPADDRESS_ENTRY structure represents either the IPV4 or IPV6 address of a PDP context.


## -syntax


````
typedef struct _WWAN_IPADDRESS_ENTRY {
  ULONG IsIpv6:1;
  ULONG IsReported:1;
  union {
    WWAN_IPV4_ADDRESS Ipv4;
    WWAN_IPV6_ADDRESS Ipv6;
  };
} WWAN_IPADDRESS_ENTRY, *PWWAN_IPADDRESS_ENTRY;
````


## -struct-fields




### -field Ipv4

 


### -field Ipv6

 


### -field IsIpv6

 


### -field IsReported

 



#### - IsIpv6:1

Set if the IP address of the PDP context is an IPV6 address.


#### - IsReported:1

Reserved. Do not use.


##### - ( unnamed union ).Ipv4

The IPV4 address of the PDP context, if <b>IsIpv6</b> is not set.


##### - ( unnamed union ).Ipv6

The IPV6 address of the PDP context, if <b>IsIpv6</b> is set.


#### - ( unnamed union )

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
union
{
    WWAN_IPV4_ADDRESS    Ipv4;
    WWAN_IPV6_ADDRESS    Ipv6;
};</pre>
</td>
</tr>
</table></span></div>
