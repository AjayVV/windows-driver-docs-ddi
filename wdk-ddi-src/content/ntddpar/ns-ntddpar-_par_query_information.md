---
UID: NS:ntddpar._PAR_QUERY_INFORMATION
title: _PAR_QUERY_INFORMATION
author: windows-driver-content
description: The PAR_QUERY_INFORMATION structure specifies the operating status of a parallel port.
old-location: parports\par_query_information.htm
old-project: parports
ms.assetid: 3115b0c2-0190-4c5c-8b31-dbafddc9c44d
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: PPAR_QUERY_INFORMATION, cisspd_d7d19b6f-e1a0-4ad7-b0ee-b8e291e63956.xml, *PPAR_QUERY_INFORMATION, PPAR_QUERY_INFORMATION structure pointer [Parallel Ports], PAR_QUERY_INFORMATION, parports.par_query_information, ntddpar/PPAR_QUERY_INFORMATION, _PAR_QUERY_INFORMATION, PAR_QUERY_INFORMATION structure [Parallel Ports], ntddpar/PAR_QUERY_INFORMATION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddpar.h
req.include-header: Ntddpar.h
req.target-type: Windows
req.target-min-winverclnt: 
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
-	ntddpar.h
apiname: 
-	PAR_QUERY_INFORMATION
product: Windows
targetos: Windows
req.typenames: PAR_QUERY_INFORMATION, *PPAR_QUERY_INFORMATION
---

# _PAR_QUERY_INFORMATION structure


## -description


The PAR_QUERY_INFORMATION structure specifies the operating status of a parallel port.


## -syntax


````
typedef struct _PAR_QUERY_INFORMATION {
  UCHAR Status;
} PAR_QUERY_INFORMATION, *PPAR_QUERY_INFORMATION;
````


## -struct-fields




### -field Status

Specifies the operating status of a parallel port. The value of <b>Status</b> is a bitwise OR of one or more of the following flags:




##### - Status.PARALLEL_AUTOFEED



##### - Status.PARALLEL_BUSY



##### - Status.PARALLEL_INIT



##### - Status.PARALLEL_PAPER_EMPTY



##### - Status.PARALLEL_NOT_CONNECTED



##### - Status.PARALLEL_SELECTED



##### - Status.PARALLEL_POWER_OFF



##### - Status.PARALLEL_OFF_LINE



## -remarks


This structure is used with an <a href="..\ntddpar\ni-ntddpar-ioctl_par_query_information.md">IOCTL_PAR_QUERY_INFORMATION</a> request.



## -see-also

<a href="..\ntddpar\ni-ntddpar-ioctl_par_query_information.md">IOCTL_PAR_QUERY_INFORMATION</a>

<a href="..\ntddpar\ns-ntddpar-_par_set_information.md">PAR_SET_INFORMATION</a>

<a href="..\ntddpar\ni-ntddpar-ioctl_par_set_information.md">IOCTL_PAR_SET_INFORMATION</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [parports\parports]:%20PAR_QUERY_INFORMATION structure%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

