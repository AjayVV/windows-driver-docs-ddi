---
UID: NF:ndis.NdisCmDispatchIncomingDropParty
title: NdisCmDispatchIncomingDropParty function
author: windows-driver-content
description: NdisCmDispatchIncomingDropParty notifies a client that it should remove a particular party on a multipoint VC, usually because the call manager has received a request over the network to close an active multipoint connection.
old-location: netvista\ndiscmdispatchincomingdropparty.htm
old-project: netvista
ms.assetid: 9dce2b0a-1d0c-4c87-a32f-8bf72bb91cfe
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: NdisCmDispatchIncomingDropParty function [Network Drivers Starting with Windows Vista], netvista.ndiscmdispatchincomingdropparty, condis_call_manager_ref_6f7730c4-030a-45a6-b873-833bf8033ce7.xml, ndis/NdisCmDispatchIncomingDropParty, NdisCmDispatchIncomingDropParty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Desktop
req.target-min-winverclnt: Supported for NDIS 6.0 and NDIS 5.1 drivers (see       NdisCmDispatchIncomingDropParty (NDIS 5.1)) in Windows Vista. Supported for NDIS 5.1 drivers (see       NdisCmDispatchIncomingDropParty (NDIS 5.1)) in Windows XP.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: Irql_CallManager_Function
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
-	NdisCmDispatchIncomingDropParty
product: Windows
targetos: Windows
req.typenames: *PNDIS_SHARED_MEMORY_USAGE, NDIS_SHARED_MEMORY_USAGE
---

# NdisCmDispatchIncomingDropParty function


## -description


<b>NdisCmDispatchIncomingDropParty</b> notifies a client that it should remove a particular party on a
  multipoint VC, usually because the call manager has received a request over the network to close an active
  multipoint connection.


## -syntax


````
VOID NdisCmDispatchIncomingDropParty(
  _In_     NDIS_STATUS DropStatus,
  _In_     NDIS_HANDLE NdisPartyHandle,
  _In_opt_ PVOID       Buffer,
  _In_     UINT        Size
);
````


## -parameters




### -param DropStatus [in]

Indicates the reason this party is being dropped, usually NDIS_STATUS_SUCCESS if the remote party
     simply requested that its connection be closed.


### -param NdisPartyHandle [in]

Specifies the handle that identifies the party to be dropped from the multipoint VC, which must
     have other parties that are still connected.


### -param Buffer [in, optional]

Pointer to a caller-allocated resident buffer containing additional protocol-specific data
     received from the remote party, if any. Depending on the underlying medium, this pointer can be
     <b>NULL</b>.


### -param Size [in]

Specifies the size in bytes of the buffer, zero if 
     <i>Buffer</i> is <b>NULL</b>.


## -returns


None



## -remarks


In the course of normal network operations, a stand-alone call manager's 
    <mshelp:link keywords="netvista.protocolcoreceivenetbufferlists" tabindex="0"><i>
    ProtocolCoReceiveNetBufferLists</i></mshelp:link> function calls 
    <b>NdisCmDispatchIncomingDropParty</b> with the 
    <i>CloseStatus</i> set to NDIS_STATUS_SUCCESS because a remote client on a multipoint connection has
    called 
    <a href="..\ndis\nf-ndis-ndisclclosecall.md">NdisClCloseCall</a>.

However, a call manager also can call 
    <b>NdisCmDispatchIncomingDropParty</b> with a CM-determined 
    <i>CloseStatus</i> at the behest of the network itself if abnormal network conditions occur, such as the
    failure of a switch on the path between the local client and one or more client(s) on an established
    multipoint connection.

A call to 
    <b>NdisCmDispatchIncomingDropParty</b> causes NDIS to call the client's 
    <mshelp:link keywords="netvista.protocolclincomingdropparty" tabindex="0"><i>
    ProtocolClIncomingDropParty</i></mshelp:link> function.

If the 
    <i>NdisPartyHandle</i> identifies the last remaining party on the given VC, the CM calls 
    <mshelp:link keywords="netvista.ndiscmdispatchincomingclosecall" tabindex="0"><b>
    NdisCmDispatchIncomingCloseCall</b></mshelp:link>, rather than 
    <b>NdisCmDispatchIncomingDropParty</b>.

Only stand-alone call managers, which register themselves with NDIS as protocol drivers, can call 
    <b>NdisCmDispatchIncomingDropParty</b>. Connection-oriented miniport drivers that provide integrated
    call-management support call 
    <b>NdisMCmDispatchIncomingDropParty</b> instead.



## -see-also

<mshelp:link keywords="netvista.protocolcoreceivenetbufferlists" tabindex="0"><i>
   ProtocolCoReceiveNetBufferLists</i></mshelp:link>

<mshelp:link keywords="netvista.ndismcmdispatchincomingdropparty" tabindex="0"><b>
   NdisMCmDispatchIncomingDropParty</b></mshelp:link>

<mshelp:link keywords="netvista.ndiscmdispatchincomingclosecall" tabindex="0"><b>
   NdisCmDispatchIncomingCloseCall</b></mshelp:link>

<a href="..\ndis\nf-ndis-ndiscldropparty.md">NdisClDropParty</a>

<a href="..\ndis\nc-ndis-protocol_cl_incoming_drop_party.md">ProtocolClIncomingDropParty</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisCmDispatchIncomingDropParty function%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

