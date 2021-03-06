---
UID: NF:ndis.NdisClCloseAddressFamily
title: NdisClCloseAddressFamily function
author: windows-driver-content
description: NdisClCloseAddressFamily releases the association between a client protocol and a call manager's or MCM driver's registered AF for a particular NIC to which the client is bound.
old-location: netvista\ndisclcloseaddressfamily.htm
old-project: netvista
ms.assetid: ae6b9133-bb98-4858-bef5-1cbe0ae0dd4f
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: NdisClCloseAddressFamily function [Network Drivers Starting with Windows Vista], netvista.ndisclcloseaddressfamily, condis_client_ref_6aa6db12-2ebe-444a-a239-46542dd1be4a.xml, NdisClCloseAddressFamily, ndis/NdisClCloseAddressFamily
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Desktop
req.target-min-winverclnt: Supported for NDIS 6.0 and NDIS 5.1 drivers (see    NdisClCloseAddressFamily (NDIS   5.1)) in Windows Vista. Supported for NDIS 5.1 drivers (see    NdisClCloseAddressFamily (NDIS   5.1)) in Windows XP.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: Irql_Protocol_Driver_Function
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ndis.lib
req.dll: 
req.irql: <= DISPATCH_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	LibDef
apilocation: 
-	ndis.lib
-	ndis.dll
apiname: 
-	NdisClCloseAddressFamily
product: Windows
targetos: Windows
req.typenames: *PNDIS_SHARED_MEMORY_USAGE, NDIS_SHARED_MEMORY_USAGE
---

# NdisClCloseAddressFamily function


## -description


<b>NdisClCloseAddressFamily</b> releases
  the association between a client protocol and a call manager's or MCM driver's registered AF for a
  particular NIC to which the client is bound.


## -syntax


````
NDIS_STATUS NdisClCloseAddressFamily(
  _In_ NDIS_HANDLE NdisAfHandle
);
````


## -parameters




### -param NdisAfHandle [in]

Specifies the NDIS-supplied handle returned by 
     <mshelp:link keywords="netvista.ndisclopenaddressfamilyex" tabindex="0"><b>
     NdisClOpenAddressFamilyEx</b></mshelp:link>.


## -returns


When 
      <b>
      NdisClCloseAddressFamily</b> returns anything other than NDIS_STATUS_PENDING, the client should make
      an internal call to its 
      <mshelp:link keywords="netvista.protocolclcloseafcomplete" tabindex="0"><i>
      ProtocolClCloseAfComplete</i></mshelp:link> function. Otherwise, NDIS calls the client's 
      <i>
      ProtocolClCloseAfComplete</i> function when this operation is completed.

If 
      <b>
      NdisClCloseAddressFamily</b> returns NDIS_STATUS_PENDING, a client that is waiting for its 
      <mshelp:link keywords="netvista.protocolclcloseafcomplete" tabindex="0"><i>
      ProtocolClCloseAfComplete</i></mshelp:link> function to be called should not block the current thread since this
      could cause a deadlock. This is particularly important when a client calls 
      <b>NdisClCloseAddressFamily</b> in the
      context of handling an 
      <mshelp:link keywords="netvista.ndiscmnotifycloseaddressfamily" tabindex="0"><b>
      NdisCmNotifyCloseAddressFamily</b></mshelp:link> request. In this case, the call manager may not close the address
      family until after the client has returned from handling the 
      <b>NdisCmNotifyCloseAddressFamily</b> request. If the client blocks the
      current thread, the client will never complete the handling of the 
      <b>NdisCmNotifyCloseAddressFamily</b> request, thus causing a deadlock.



## -remarks


A client commonly calls 
    <b>NdisClCloseAddressFamily</b> from its
    
    <mshelp:link keywords="netvista.protocolunbindadapterex" tabindex="0"><i>
    ProtocolUnbindAdapterEx</i></mshelp:link> function, after it closes all the client's open VCs on the binding with
    calls to 
    <a href="..\ndis\nf-ndis-ndisclclosecall.md">NdisClCloseCall</a> and/or 
    <a href="..\ndis\nf-ndis-ndisclderegistersap.md">NdisClDeregisterSap</a>. A client can
    also call 
    <b>NdisClCloseAddressFamily</b> in the
    context of processing an 
    <mshelp:link keywords="netvista.ndiscmnotifycloseaddressfamily" tabindex="0"><b>
    NdisCmNotifyCloseAddressFamily</b></mshelp:link> request.

NDIS calls a client's 
    <mshelp:link keywords="netvista.protocolunbindadapterex" tabindex="0"><i>
    ProtocolUnbindAdapterEx</i></mshelp:link> function whenever an underlying NIC to which that client is bound is being
    removed from the machine or is being reconfigured. A PnP reconfiguration of the underlying miniport
    driver causes the call manager or MCM driver to reregister the address family it supports over that NIC.
    This, in turn, causes a subsequent call to the client's 
    <mshelp:link keywords="netvista.protocolcoafregisternotify" tabindex="0"><i>
    ProtocolCoAfRegisterNotify</i></mshelp:link> function. In either scenario, the client's 
    <i>
    ProtocolUnbindAdapterEx</i> function must call 
    <b>NdisClCloseAddressFamily</b> with any
    outstanding 
    <i>NdisAfHandle</i> it is currently using that depends on the underlying miniport
    driver.

As a general guideline, a client should release all the resources it allocated for connection-oriented
    communications through the miniport driver before its 
    <mshelp:link keywords="netvista.protocolunbindadapterex" tabindex="0"><i>
    ProtocolUnbindAdapterEx</i></mshelp:link> function calls 
    <a href="..\ndis\nf-ndis-ndiscloseadapterex.md">NdisCloseAdapterEx</a>.

The 
    <i>NdisAfHandle</i> passed to 
    <b>NdisClCloseAddressFamily</b> becomes
    invalid for the client as soon as this call occurs.

Before a call to 
    <b>NdisClCloseAddressFamily</b>, the
    client may use the 
    <i>NdisAfHandle</i> while the AF is open or while a 
    <mshelp:link keywords="netvista.protocolclnotifycloseaf" tabindex="0"><i>
    ProtocolClNotifyCloseAf</i></mshelp:link> operation is pending. If the 
    <i>
    ProtocolClNotifyCloseAf</i> function returns NDIS_STATUS_PENDING, use the handle in the 
    <mshelp:link keywords="netvista.ndisclnotifycloseaddressfamilycomplete" tabindex="0"><b>
    NdisClNotifyCloseAddressFamilyComplete</b></mshelp:link> call after the close operation completes.



## -see-also

<a href="..\ndis\nc-ndis-protocol_cm_close_af.md">ProtocolCmCloseAf</a>

<a href="..\ndis\nf-ndis-ndisclclosecall.md">NdisClCloseCall</a>

<a href="..\ndis\nc-ndis-protocol_unbind_adapter_ex.md">ProtocolUnbindAdapterEx</a>

<a href="..\ndis\nc-ndis-protocol_cl_close_af_complete.md">ProtocolClCloseAfComplete</a>

<a href="..\ndis\nf-ndis-ndisclopenaddressfamilyex.md">NdisClOpenAddressFamilyEx</a>

<a href="..\ndis\nc-ndis-protocol_co_af_register_notify.md">ProtocolCoAfRegisterNotify</a>

<a href="..\ndis\nf-ndis-ndisclderegistersap.md">NdisClDeregisterSap</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisClCloseAddressFamily function%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

