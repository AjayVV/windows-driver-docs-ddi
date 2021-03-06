---
UID: NE:fwpsk.FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6_
title: FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6_
author: windows-driver-content
description: The FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6enumeration type specifies the data field identifiers for the FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 and FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD run-time filtering layers.
old-location: netvista\fwps_fields_ale_resource_assignment_v6.htm
old-project: netvista
ms.assetid: d8e0bfd0-933e-4936-845a-e45020634f26
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_ADDRESS_TYPE, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_APP_ID, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_MAX, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_TUNNEL_TYPE, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_FLAGS, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_TUNNEL_TYPE, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_MAX, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_USER_ID, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_PORT, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_LOCAL_INTERFACE_PROFILE_ID, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_FLAGS, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_LOCAL_INTERFACE_PROFILE_ID, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_APP_ID, FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_ADDRESS_TYPE, wfp_ref_5_const_3_data_fields_3b5b5eec-48af-4e0a-8f71-2856253467ea.xml, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_INTERFACE, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_PROTOCOL, netvista.fwps_fields_ale_resource_assignment_v6, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_PROTOCOL, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_INTERFACE, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_USER_ID, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_ADDRESS, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PACKAGE_ID, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_SIO_FIREWALL_SOCKET_PROPERTY, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PROMISCUOUS_MODE, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_SIO_FIREWALL_SOCKET_PROPERTY, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PACKAGE_ID, fwpsk/FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_PORT, FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_INTERFACE_TYPE, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PROMISCUOUS_MODE, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_ADDRESS, fwpsk/FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_INTERFACE_TYPE, FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6_, FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6 enumeration [Network Drivers Starting with Windows Vista]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: fwpsk.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Unless otherwise noted, supported starting with Windows Vista.
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
req.irql: <= DISPATCH_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	fwpsk.h
apiname: 
-	FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6
product: Windows
targetos: Windows
req.typenames: FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6
---

# FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6_ enumeration


## -description


The FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6enumeration type specifies the data field identifiers for
  the FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 and FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD 
  <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa366492">run-time filtering layers</a>.


## -syntax


````
typedef enum FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6_ { 
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_APP_ID,
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_USER_ID,
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_ADDRESS,
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_ADDRESS_TYPE,
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_PORT,
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_PROTOCOL,
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PROMISCUOUS_MODE,
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_INTERFACE,
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_FLAGS,
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_INTERFACE_TYPE,
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_TUNNEL_TYPE,
#if (NTDDI_VERSION >= NTDDI_WIN7)
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_LOCAL_INTERFACE_PROFILE_ID,
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_SIO_FIREWALL_SOCKET_PROPERTY,
#if (NTDDI_VERSION >= NTDDI_WIN8)
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PACKAGE_ID,
#endif 
#endif 
  FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_MAX
} FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6;
````


## -enum-fields




### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_APP_ID

The full path of the application.


### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_USER_ID

The identifier of the local user.


### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_ADDRESS

The local IP address.


### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_ADDRESS_TYPE

The local IP address type. The possible values are defined by the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff568757">NL_ADDRESS_TYPE</a> enumeration.


### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_PORT

The local transport protocol port number.


### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_PROTOCOL

The IP protocol number, as specified in RFC 1700.


### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PROMISCUOUS_MODE



### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_INTERFACE

The locally unique identifier (<a href="..\igpupvdev\ns-igpupvdev-_luid.md">LUID</a>) for the network interface associated with the
     local IP address.


### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_FLAGS

A bitwise OR of a combination of filtering condition flags. For information about the possible
     flags, see 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff549942">Filtering Condition Flags</a>.


### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_INTERFACE_TYPE

The type of the network interface, as defined by the Internet Assigned Numbers Authority (IANA).
     For more information, see 
     <a href="http://go.microsoft.com/fwlink/p/?linkid=60066">IANAifType-MIB Definitions</a>.


### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_TUNNEL_TYPE

The encapsulation method used by a tunnel if the 
     <b>IfType</b> member of the IP_ADAPTER_ADDRESSES structure is IF_TYPE_TUNNEL. The tunnel type is defined
     by IANA. For more information, see 
     <a href="http://go.microsoft.com/fwlink/p/?linkid=60066">IANAifType-MIB Definitions</a> and the
     Windows SDK.


### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_LOCAL_INTERFACE_PROFILE_ID

The profile identifier (network category) of the network interface associated with the local IP
     address. The possible network category values are: public (1), private (2), or domain (3).
     
<div class="alert"><b>Note</b>  Supported starting with Windows 7.</div><div> </div>

### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_SIO_FIREWALL_SOCKET_PROPERTY

The IP_PROTECTION_LEVEL property associated with the socket.
     
<div class="alert"><b>Note</b>  Supported starting with Windows 7.</div><div> </div>

### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PACKAGE_ID

The package identifier is a security identifier (SID) that identifies the associated AppContainer process. For more information about the SID structure, see the description for the SID structure in the Microsoft Windows SDK documentation.
<div class="alert"><b>Note</b>  Supported starting with Windows 8.</div><div> </div>

### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_SECURITY_ATTRIBUTE_FQBN_VALUE



### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_COMPARTMENT_ID



### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_BITMAP_IP_LOCAL_ADDRESS



### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_BITMAP_IP_LOCAL_PORT



### -field FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.


###### - FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PROMISCUOUS_MODE.For a description of these raw socket modes, see WSAIoctl in the Windows SDK documentation.



##### - FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PROMISCUOUS_MODE.SIO_RCVALL_IGMPMCAST



##### - FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PROMISCUOUS_MODE.SIO_RCVALL



##### - FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PROMISCUOUS_MODE.SIO_RCVALL_MCAST



###### - FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_ALE_PROMISCUOUS_MODE.The raw socket mode that is allowed or denied. The possible values are:



## -remarks


For the case of an implicit bind, the local address and port information might not be available. In
    this situation, the FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_ADDRESS,
    FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_ADDRESS_TYPE, and/or
    <b>FWPS_FIELD_ALE_RESOURCE_ASSIGNMENT_V6_IP_LOCAL_PORT</b> data fields might be of type FWP_EMPTY.



## -see-also

<a href="..\igpupvdev\ns-igpupvdev-_luid.md">LUID</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff568757">NL_ADDRESS_TYPE</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FWPS_FIELDS_ALE_RESOURCE_ASSIGNMENT_V6 enumeration%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

