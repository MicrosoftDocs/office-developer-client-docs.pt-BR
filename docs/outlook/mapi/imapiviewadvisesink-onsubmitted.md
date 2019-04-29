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
ms.openlocfilehash: ebde06d0d22320ecb5edb633cf8d04aaeec2a841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433980"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notifica o Visualizador de formulários que a mensagem atual foi enviada ao spooler MAPI.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Um objeto Form chama o método **IMAPIViewAdviseSink:: onenviar** após uma chamada para [IMAPIMessageSite:: SubmitMessage](imapimessagesite-submitmessage.md) foi retornada com êxito. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Após o cancelamento de **envio** ser chamado, você pode continuar supondo que a mensagem tenha sido atualizada. Atualize o Windows para refletir as alterações que ocorreram. 
  
Para obter mais informações sobre notificações de formulário, consulte [envio e recebimento de notificações de formulários](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Confira também



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

