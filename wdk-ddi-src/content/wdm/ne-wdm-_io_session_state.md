---
UID: NE:wdm._IO_SESSION_STATE
title: _IO_SESSION_STATE
author: windows-driver-content
description: The IO_SESSION_STATE enumeration contains constants that indicate the current state of a user session.
old-location: kernel\io_session_state.htm
old-project: kernel
ms.assetid: 3e181b22-ae82-4287-8175-bc6043332d5a
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: wdm/IoSessionStateDisconnectedLoggedOn, IoSessionStateTerminated, wdm/IO_SESSION_STATE, IoSessionStateLoggedOff, IoSessionStateDisconnectedLoggedOn, wdm/IoSessionStateLoggedOff, IoSessionStateLoggedOn, IoSessionStateMax, wdm/IoSessionStateDisconnected, IoSessionStateConnected, IoSessionStateInitialized, PIO_SESSION_STATE enumeration pointer [Kernel-Mode Driver Architecture], IO_SESSION_STATE enumeration [Kernel-Mode Driver Architecture], wdm/IoSessionStateLoggedOn, PIO_SESSION_STATE, IoSessionStateCreated, wdm/IoSessionStateConnected, *PIO_SESSION_STATE, wdm/IoSessionStateCreated, _IO_SESSION_STATE, kernel.io_session_state, sysenum_1a899498-22e4-4567-a88e-0773b3590b95.xml, wdm/PIO_SESSION_STATE, wdm/IoSessionStateTerminated, IoSessionStateDisconnected, wdm/IoSessionStateMax, IO_SESSION_STATE, wdm/IoSessionStateInitialized
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Fltkernel.h
req.target-type: Windows
req.target-min-winverclnt: Supported in Windows 7 and later versions of the Windows operating system.
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
req.irql: PASSIVE_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	wdm.h
apiname: 
-	IO_SESSION_STATE
product: Windows
targetos: Windows
req.typenames: IO_SESSION_STATE, *PIO_SESSION_STATE
req.product: Windows 10 or later.
---

# _IO_SESSION_STATE enumeration


## -description


The <b>IO_SESSION_STATE</b> enumeration contains constants that indicate the current state of a user session.


## -syntax


````
typedef enum _IO_SESSION_STATE { 
  IoSessionStateCreated               = 1,
  IoSessionStateInitialized           = 2,
  IoSessionStateConnected             = 3,
  IoSessionStateDisconnected          = 4,
  IoSessionStateDisconnectedLoggedOn  = 5,
  IoSessionStateLoggedOn              = 6,
  IoSessionStateLoggedOff             = 7,
  IoSessionStateTerminated            = 8,
  IoSessionStateMax                   = 9
} IO_SESSION_STATE, *PIO_SESSION_STATE;
````


## -enum-fields




### -field IoSessionStateCreated

The session has been created.


### -field IoSessionStateInitialized

The session has been initialized but has not yet been created.


### -field IoSessionStateConnected

The session is connected but the user has not yet logged on.


### -field IoSessionStateDisconnected

The session has been disconnected.


### -field IoSessionStateDisconnectedLoggedOn

The session was disconnected while the user was logged on.


### -field IoSessionStateLoggedOn

The user is logged on to the session.


### -field IoSessionStateLoggedOff

The user has logged off of the session. 


### -field IoSessionStateTerminated

The session has been terminated.


### -field IoSessionStateMax

Specifies the maximum value in this enumeration type. 


## -remarks


When a driver calls the <a href="..\wdm\nf-wdm-iogetcontainerinformation.md">IoGetContainerInformation</a> routine to obtain information about a user session (<i>InformationClass</i> = <b>IoSessionStateInformation</b>), the I/O manager writes an <a href="..\wdm\ns-wdm-_io_session_state_information.md">IO_SESSION_STATE_INFORMATION</a> structure to the buffer pointed to by the routine's <i>Buffer</i> parameter. The I/O manager sets the <b>SessionState</b> member of this structure to an <b>IO_SESSION_STATE</b> enumeration constant (other than <b>IoSessionStateMax</b>).

The following table shows the session state transitions. For each state transition, the table shows the following:
<ul>
<li>
The <i>from</i> state (a column label in a gray box)

</li>
<li>
The <i>to</i> state (a row label in a gray box)

</li>
<li>
The event that causes the transition (a table entry in a white box)

</li>
</ul>A blank white box indicates that no transition can occur directly from the associated <i>from</i> state to the corresponding <i>to</i> state.
<img alt="Table listing session state transitions " src="images/sessionstate.png"/>In the preceding table, the <i>from</i> and <i>to</i> states are represented by <b>IO_SESSION_STATE</b> enumeration constants, and the events are represented by <a href="..\wdm\ne-wdm-_io_session_event.md">IO_SESSION_EVENT</a> enumeration constants. For example, if the session state is <b>IoSessionStateConnected</b> (abbreviated as "Connected" in the table), an <b>IoSessionEventLogon</b> event (abbreviated as "Logon") causes a transition to the <b>IoSessionStateLoggedOn</b> state (abbreviated as "LoggedOn"). The starting state for a new session is <b>IoSessionStateInitialized</b> (abbreviated as "Initialized"). 



## -see-also

<a href="..\wdm\ne-wdm-_io_session_event.md">IO_SESSION_EVENT</a>

<a href="..\wdm\nf-wdm-iogetcontainerinformation.md">IoGetContainerInformation</a>

<a href="..\wdm\ns-wdm-_io_session_state_information.md">IO_SESSION_STATE_INFORMATION</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20IO_SESSION_STATE enumeration%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

