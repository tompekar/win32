---
Description: Specifies how the Voice Capture DSP performs microphone array processing.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE Property
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE Property

Specifies how the Voice Capture DSP performs microphone array processing.

## Constant for IPropertyBag

Available only by using [**IPropertyStore**](https://msdn.microsoft.com/windows/desktop/e995aaa1-d4c9-475f-b1fa-b9123cd5b653).

## Data Type

VT\_I4

## Default Value

MICARRAY\_SINGLE\_BEAM

## Applies To

-   [Voice Capture DSP](voicecapturedmo.md)

## Remarks

The value of this property is a member of the [MIC\_ARRAY\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) enumeration. The default value is MICARRAY\_SINGLE\_BEAM. Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.

The DSP uses this property only when microphone array processing is enabled.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                          |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## See also

<dl> <dt>

[Media Foundation Properties](media-foundation-properties.md)
</dt> <dt>

[Voice Capture DSP](voicecapturedmo.md)
</dt> </dl>

 

 



