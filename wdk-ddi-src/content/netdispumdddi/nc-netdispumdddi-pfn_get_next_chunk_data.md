---
UID: NC:netdispumdddi.PFN_GET_NEXT_CHUNK_DATA
title: PFN_GET_NEXT_CHUNK_DATA
author: windows-driver-content
description: Provides info about the next Miracast encode chunk that was reported to the Microsoft DirectX graphics kernel subsystem when the DXGK_INTERRUPT_TYPE interrupt type is DXGK_INTERRUPT_MICACAST_CHUNK_PROCESSING_COMPLETE.The data type of this function is PFN_GET_NEXT_CHUNK_DATA.
old-location: display\getnextchunkdata.htm
old-project: display
ms.assetid: 24b1d89a-4200-41ec-aa73-15b37e4cca6d
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.getnextchunkdata, PFN_GET_NEXT_CHUNK_DATA, GetNextChunkData callback function [Display Devices], GetNextChunkData, PFN_GET_NEXT_CHUNK_DATA, PFN_GET_NEXT_CHUNK_DATA, netdispumdddi/GetNextChunkData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: netdispumdddi.h
req.include-header: Netdispumdddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
-	UserDefined
apilocation: 
-	Netdispumdddi.h
apiname: 
-	GetNextChunkData
product: Windows
targetos: Windows
req.typenames: NDK_SRQ_DISPATCH
---

# PFN_GET_NEXT_CHUNK_DATA callback


## -description


Provides info about the next Miracast encode chunk that was reported to the Microsoft DirectX graphics kernel subsystem when the <a href="..\d3dkmddi\ne-d3dkmddi-_dxgk_interrupt_type.md">DXGK_INTERRUPT_TYPE</a> interrupt type is  <b>DXGK_INTERRUPT_MICACAST_CHUNK_PROCESSING_COMPLETE</b>.The data type of this function is <b>PFN_GET_NEXT_CHUNK_DATA</b>.




## -prototype


````
PFN_GET_NEXT_CHUNK_DATA GetNextChunkData;

NTSTATUS GetNextChunkData(
  _In_     HANDLE              hMiracastDeviceHandle,
  _In_     UINT                TimeoutInMilliseconds,
  _In_     UINT                AdditionalWaitEventCount,
  _In_opt_ HANDLE              *pAdditionalWaitEvents,
  _Inout_  UINT                *pChunkDataBufferSize,
  _Out_    MIRACAST_CHUNK_DATA *pChunkDataBuffer,
  _Out_    UINT                *pOutstandingChunksToProcess
)
{ ... }
````


## -parameters




### -param hMiracastDeviceHandle [in]

A handle that represents a Miracast device. The Miracast user-mode driver previously obtained this handle as the <i>hMiracastDeviceHandle</i> parameter in a call to the <a href="..\netdispumdddi\nc-netdispumdddi-pfn_create_miracast_context.md">CreateMiracastContext</a> function.


### -param TimeoutInMilliseconds [in]

The timeout interval value, in milliseconds, supplied by the Miracast user-mode driver.

If this value is <b>INFINITE</b>, the operating system blocks calls to <b>GetNextChunkData</b> until a chunk becomes available.

If this value is zero and a chunk is not ready, the operating system will not block a call to <b>GetNextChunkData</b>.


### -param AdditionalWaitEventCount [in]

The number of additional events that are supplied in the <i>pAdditionalWaitEvents</i> parameter.

 A maximum of 4 wait events can be supplied.


### -param *pAdditionalWaitEvents



### -param *pChunkDataBufferSize



### -param *pChunkDataBuffer



### -param *pOutstandingChunksToProcess






#### - pChunkDataBuffer [out]

A pointer to a buffer of type  <a href="..\netdispumdddi\ns-netdispumdddi-miracast_chunk_data.md">MIRACAST_CHUNK_DATA</a> that the operating system provides to store information about the next encode chunk. This parameter is provided only if the call to <b>GetNextChunkData</b> is successful.


#### - pAdditionalWaitEvents [in, optional]

An optional pointer to an array of events that  <b>GetNextChunkData</b> will wait on while waiting for a new encode chunk.


#### - pChunkDataBufferSize [in, out]

A pointer to a variable that contains the size, in bytes, of the <i>pChunkDataBuffer</i> buffer.

When <b>GetNextChunkData</b> is called, this parameter contains the size of <i>pChunkDataBuffer</i>.

When  <b>GetNextChunkData</b> returns a success code, this parameter contains the size of actual encode chunk data returned in <i>pChunkDataBuffer</i>.


#### - pOutstandingChunksToProcess [out]

A pointer to a variable that contains the number of outstanding encode chunks that are available for the driver at the time this call returned.  This parameter is provided only if the call to <b>GetNextChunkData</b> is successful.

Note that as chunks are completed by the GPU asynchronously, this parameter only gives an indication of the number of outstanding chunks.


## -returns


If info on an encode chunk was returned successfully, the <b>STATUS_SUCCESS</b> status code is returned, and the value of *<i>pChunkDataBufferSize</i> is non-zero.

These additional status codes can be returned:



## -remarks


This function is optional. The user-mode display driver should only call it if the display miniport driver responds to  interrupts from the GPU when the GPU completes the encoding of a chunk by passing data in the <a href="..\netdispumdddi\ns-netdispumdddi-miracast_chunk_data.md">MIRACAST_CHUNK_DATA</a>.<b>PrivateDriverData</b> member at that interrupt time.

The user-mode display driver can use the sizes of the <a href="..\netdispumdddi\ns-netdispumdddi-miracast_chunk_data.md">MIRACAST_CHUNK_DATA</a> structure and the <b>MIRACAST_CHUNK_DATA</b>.<b>PrivateDriverData</b> member to compute the size of a chunk and hence how to move from chunk to chunk in the returned buffer.

In a call to this function, as many available packets as can fit will be placed sequentially in the supplied buffer. This code snippet shows how to calculate the size of each packet:
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ChunkSize == FIELD_OFFSET
    (D3DKMT_MIRACAST_CHUNK_DATA, PrivateDriverData) \
    + Chunk-&gt;ChunkData.PrivateDriverDataSize;</pre>
</td>
</tr>
</table></span></div>


## -see-also

<a href="..\d3dkmddi\ne-d3dkmddi-_dxgk_interrupt_type.md">DXGK_INTERRUPT_TYPE</a>

<a href="..\netdispumdddi\ns-netdispumdddi-miracast_chunk_data.md">MIRACAST_CHUNK_DATA</a>

<a href="..\netdispumdddi\nc-netdispumdddi-pfn_create_miracast_context.md">CreateMiracastContext</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFN_GET_NEXT_CHUNK_DATA callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

