---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 40a72bed0b3e763ea482b228174b85d9f42185c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767351"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**Aplica-se a**: Outlook 
  
Notifica o Visualizador de formulário que a mensagem atual tiver sido enviada para o spooler MAPI.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Parâmetros

None
  
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A notificação foi bem-sucedida.
    
## <a name="remarks"></a>Coment�rios

Um objeto form chama o método **IMAPIViewAdviseSink::OnSubmitted** após uma chamada para [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) ter retornado com êxito. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Após a chamada **OnSubmitted** , você pode continuar na pressuposição de que a mensagem foi atualizada. Atualize suas janelas para refletir quaisquer alterações que tenham ocorrido. 
  
Para obter mais informações sobre as notificações do formulário, consulte [de envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Confira também



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)

