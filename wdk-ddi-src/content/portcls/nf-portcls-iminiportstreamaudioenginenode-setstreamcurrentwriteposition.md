---
UID: NF:portcls.IMiniportStreamAudioEngineNode.SetStreamCurrentWritePosition
title: IMiniportStreamAudioEngineNode::SetStreamCurrentWritePosition method
author: windows-driver-content
description: Sets the current cursor position in the audio data stream that is being captured from the endpoint.
old-location: audio\iminiportstreamaudioenginenode_setstreamcurrentwriteposition.htm
old-project: audio
ms.assetid: A277FC29-AB92-4D67-9E53-F8E8B36053F9
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: SetStreamCurrentWritePosition method [Audio Devices], IMiniportStreamAudioEngineNode interface, SetStreamCurrentWritePosition method [Audio Devices], audio.iminiportstreamaudioenginenode_setstreamcurrentwriteposition, IMiniportStreamAudioEngineNode::SetStreamCurrentWritePosition, IMiniportStreamAudioEngineNode, SetStreamCurrentWritePosition, portcls/IMiniportStreamAudioEngineNode::SetStreamCurrentWritePosition, IMiniportStreamAudioEngineNode interface [Audio Devices], SetStreamCurrentWritePosition method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portcls.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: portcls.h
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	COM
apilocation: 
-	Portcls.h
apiname: 
-	IMiniportStreamAudioEngineNode.SetStreamCurrentWritePosition
product: Windows
targetos: Windows
req.typenames: PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---

# IMiniportStreamAudioEngineNode::SetStreamCurrentWritePosition method


## -description


Sets the current cursor position in the audio data stream that is being captured from the endpoint.


## -syntax


````
NTSTATUS SetStreamCurrentWritePosition(
  [in] ULONG ulCurrentWritePosition
);
````


## -parameters




### -param ulCurrentWritePosition [in]

The current cursor position in the audio data stream.


## -returns


<b>SetStreamCurrentWritePosition</b> returns S_OK, if the call was successful. Otherwise, the method returns an appropriate error code.



## -see-also

<a href="..\portcls\nn-portcls-iminiportstreamaudioenginenode.md">IMiniportStreamAudioEngineNode</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [audio\audio]:%20IMiniportStreamAudioEngineNode::SetStreamCurrentWritePosition method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

