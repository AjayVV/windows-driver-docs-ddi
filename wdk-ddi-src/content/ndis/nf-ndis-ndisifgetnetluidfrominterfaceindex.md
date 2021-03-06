---
UID: NF:ndis.NdisIfGetNetLuidFromInterfaceIndex
title: NdisIfGetNetLuidFromInterfaceIndex function
author: windows-driver-content
description: The NdisIfGetNetLuidFromInterfaceIndex function gets the NET_LUID value that is associated with a network interface index.
old-location: netvista\ndisifgetnetluidfrominterfaceindex.htm
old-project: netvista
ms.assetid: 3cfb7f31-93ae-47a2-8da8-becfbe045f5e
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: ndis/NdisIfGetNetLuidFromInterfaceIndex, NdisIfGetNetLuidFromInterfaceIndex function [Network Drivers Starting with Windows Vista], net_if_functions_ref_eb50b72f-9bb0-4c02-88d3-dbb0fb1d82d1.xml, NdisIfGetNetLuidFromInterfaceIndex, netvista.ndisifgetnetluidfrominterfaceindex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Desktop
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: Irql_Interfaces_Function
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ndis.lib
req.dll: 
req.irql: PASSIVE_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	LibDef
apilocation: 
-	ndis.lib
-	ndis.dll
apiname: 
-	NdisIfGetNetLuidFromInterfaceIndex
product: Windows
targetos: Windows
req.typenames: *PNDIS_SHARED_MEMORY_USAGE, NDIS_SHARED_MEMORY_USAGE
---

# NdisIfGetNetLuidFromInterfaceIndex function


## -description


The 
  <b>NdisIfGetNetLuidFromInterfaceIndex</b> function gets the 
  <a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a> value that is associated with a network
  interface index.


## -syntax


````
NDIS_STATUS NdisIfGetNetLuidFromInterfaceIndex(
  _In_  NET_IFINDEX IfIndex,
  _Out_ PNET_LUID   pNetLuid
);
````


## -parameters




### -param ifIndex

TBD


### -param pNetLuid [out]

A pointer to a caller-supplied NET_LUID variable. If 
     <b>NdisIfGetNetLuidFromInterfaceIndex</b> succeeds, NDIS writes the NET_LUID value that is associated
     with the specified network interface index to this variable.


#### - IfIndex [in]

A network interface index that NDIS assigned to a 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a> value in the 
     <mshelp:link keywords="netvista.ndisifregisterinterface" tabindex="0"><b>
     NdisIfRegisterInterface</b></mshelp:link> function.


## -returns


<b>NdisIfGetNetLuidFromInterfaceIndex</b> returns one of the following status values:
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDIS_STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDIS_STATUS_INTERFACE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
<b>NdisIfGetNetLuidFromInterfaceIndex</b> failed because the specified
       network interface index is not assigned to a registered interface.

</td>
</tr>
</table> 



## -remarks


NDIS drivers can call the 
    <b>NdisIfGetNetLuidFromInterfaceIndex</b> function to get the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a> value that is associated with a network
    interface index.

For the interfaces that the NDIS proxy provider service manages, NDIS provides the interface index and
    NET_LUID in various driver initialization structures:
<ul>
<li>
Miniport drivers can obtain the interface index and NET_LUID for a miniport adapter in the 
      <mshelp:link keywords="netvista.ndis_miniport_init_parameters" tabindex="0"><b>
      NDIS_MINIPORT_INIT_PARAMETERS</b></mshelp:link> structure.

</li>
<li>
Filter drivers can obtain the interface index and NET_LUID for a filter module in the 
      <mshelp:link keywords="netvista.ndis_filter_attach_parameters" tabindex="0"><b>
      NDIS_FILTER_ATTACH_PARAMETERS</b></mshelp:link> structure.

</li>
<li>
Protocol drivers can obtain the interface index and NET_LUID of the highest and the lower interfaces
      on a driver stack in the 
      <a href="..\ndis\ns-ndis-_ndis_bind_parameters.md">NDIS_BIND_PARAMETERS</a> structure.

</li>
</ul>NDIS assigns an interface index to a network interface when the interface provider calls the 
    <a href="..\ndis\nf-ndis-ndisifregisterinterface.md">NdisIfRegisterInterface</a> function.
    An interface provider calls the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff565890">NDIS_MAKE_NET_LUID</a> macro to create the
    NET_LUID value before it registers an interface.

The interface index value can change without a computer restart. Deregistering and re-registering an
    interface that is associated with a NET_LUID value might result in different interface index values. Do
    not confuse the interface index with the NET_LUID index that persists after a computer restarts.

NDIS provides the 
    <mshelp:link keywords="netvista.ndisifgetinterfaceindexfromnetluid" tabindex="0"><b>
    NdisIfGetInterfaceIndexFromNetLuid</b></mshelp:link> function to obtain the interface index for a specified
    NET_LUID.



## -see-also

<a href="..\ndis\nf-ndis-ndisifregisterinterface.md">NdisIfRegisterInterface</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff565890">NDIS_MAKE_NET_LUID</a>

<a href="..\ndis\ns-ndis-_ndis_bind_parameters.md">NDIS_BIND_PARAMETERS</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a>

<mshelp:link keywords="netvista.ndisifgetinterfaceindexfromnetluid" tabindex="0"><b>
   NdisIfGetInterfaceIndexFromNetLuid</b></mshelp:link>

<a href="..\ndis\ns-ndis-_ndis_filter_attach_parameters.md">NDIS_FILTER_ATTACH_PARAMETERS</a>

<a href="..\ndis\ns-ndis-_ndis_miniport_init_parameters.md">NDIS_MINIPORT_INIT_PARAMETERS</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisIfGetNetLuidFromInterfaceIndex function%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

