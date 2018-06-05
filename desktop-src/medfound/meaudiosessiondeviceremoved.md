---
Description: Raised by the audio renderer when the audio device is removed. The audio renderer is now invalid.
ms.assetid: a65a3931-e0d6-47ac-b545-9d616e914109
title: MEAudioSessionDeviceRemoved event
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# MEAudioSessionDeviceRemoved event

Raised by the audio renderer when the audio device is removed. The audio renderer is now invalid.

The Media Session forwards this event to the application.

## Event values

Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT\_EMPTY<br/>   | No event data.<br/> <br/>                                                     |
| VT\_UNKNOWN<br/> | Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.<br/> <br/> |



## Remarks

This event is sent by the audio renderer's stream sink. The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](https://msdn.microsoft.com/windows/desktop/9fd653f0-c9d1-4155-9c1e-7e6124b40cca) event from the audio session with the disconnection reason equal to **DisconnectReasonDeviceRemoval**.

The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                                           |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## See also

<dl> <dt>

[Media Foundation Events](media-foundation-events.md)
</dt> <dt>

[Streaming Audio Renderer](streaming-audio-renderer.md)
</dt> </dl>

 

 



