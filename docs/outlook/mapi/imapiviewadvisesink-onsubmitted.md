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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2aa1aca2816b8f0e148d35d1fcec761f621a2239
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579442"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notifica o Visualizador de formulário que a mensagem atual tiver sido enviada para o spooler MAPI.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Um objeto form chama o método **IMAPIViewAdviseSink::OnSubmitted** após uma chamada para [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) ter retornado com êxito. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Após a chamada **OnSubmitted** , você pode continuar na pressuposição de que a mensagem foi atualizada. Atualize suas janelas para refletir quaisquer alterações que tenham ocorrido. 
  
Para obter mais informações sobre as notificações do formulário, consulte [de envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Confira também



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

