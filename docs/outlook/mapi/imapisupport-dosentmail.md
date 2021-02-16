---
title: IMAPISupportDosentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8289b8dd2e0ab3c760e77a37b821d2fe74e4abe9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423948"
---
# <a name="imapisupportdosentmail"></a>IMAPISupport::DoSentMail

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Processa uma mensagem enviada.
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpMessage_
  
> [in] Um ponteiro para a mensagem aberta para a qual uma mensagem deve ser gerada na pasta designada para manter os itens enviados.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::D oSentMail** é implementado para objetos de suporte do provedor de armazenamento de mensagens. Os provedores de repositório de mensagens chamam **DoSentMail** por meio de sua implementação do método [IMsgStore::FinishedMsg,](imsgstore-finishedmsg.md) que é chamado pelo spooler MAPI quando ele conclui o processamento de uma mensagem. **FinishedMsg** desbloqueia a mensagem, garante que a contagem de referência da mensagem seja 1 e chama **DoSentMail**.
  
 **O DoSentMail** executa as seguintes tarefas: 
  
- Verifica a mensagem para **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) para determinar se a mensagem deve ser excluída após o envio.
    
- Determina o local da pasta Itens Enviados.
    
- Inicia o processamento de gancho de mensagem para qualquer gancho definido na pasta Itens Enviados.
    
- Move a mensagem para a pasta Itens Enviados, pasta Itens Excluídos ou para outra pasta.
    
- Libera a mensagem.
    
## <a name="see-also"></a>Confira também



[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[Propriedade canônica PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

