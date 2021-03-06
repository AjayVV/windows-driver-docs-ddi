---
UID: NF:ntintsafe.RtlByteToChar
title: RtlByteToChar function
author: windows-driver-content
description: Converts a value of type BYTE to a value of type CHAR.
old-location: kernel\rtlbytetochar.htm
old-project: kernel
ms.assetid: A571B2C7-F97E-4717-AA22-D25DE47469E8
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: RtlByteToChar, kernel.rtlbytetochar, RtlByteToChar function [Kernel-Mode Driver Architecture], ntintsafe/RtlByteToChar
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntintsafe.h
req.include-header: 
req.target-type: Desktop
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
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	Ntintsafe.h
apiname: 
-	RtlByteToChar
product: Windows
targetos: Windows
req.typenames: PUBLIC_OBJECT_TYPE_INFORMATION, *PPUBLIC_OBJECT_TYPE_INFORMATION
---

# RtlByteToChar function


## -description


Converts a value of type <b>BYTE</b> to a value of type <b>CHAR</b>.


## -syntax


````
NTSTATUS RtlByteToChar(
  _In_  BYTE bOperand,
  _Out_ CHAR *pch
);
````


## -parameters




### -param bOperand [in]

The value to be converted.


### -param pch [out]

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns STATUS_INTEGER_OVERFLOW and this parameter is not valid.


## -remarks


This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.


