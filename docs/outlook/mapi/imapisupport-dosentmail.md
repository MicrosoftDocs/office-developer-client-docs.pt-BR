---
title: IMAPISupportDoSentMail
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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2bded946a1fc7d7ab181d3953defa24e247c003c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767248"
---
# <a name="imapisupportdosentmail"></a>IMAPISupport::DoSentMail

  
  
**Aplica-se a**: Outlook 
  
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
  
> [in] Um ponteiro para a mensagem de aberta para o qual uma mensagem deve ser gerada na pasta designada para armazenar itens enviados.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::DoSentMail** é implementado para objetos de suporte do provedor de repositório de mensagem. Provedores de armazenamento de mensagem chamarem **DoSentMail** da sua implementação do método [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) , que é chamado pelo spooler MAPI quando ele tiver terminado de processamento de uma mensagem. **FinishedMsg** desbloqueia a mensagem, garante que a contagem de referência da mensagem é 1 e chama **DoSentMail**.
  
 **DoSentMail** executa as seguintes tarefas: 
  
- Verifica a mensagem para a propriedade **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) determinar se a mensagem deve ser excluída após o envio.
    
- Determina o local da pasta Itens enviados.
    
- Inicia o processamento para qualquer ganchos definidas na pasta Itens enviados do gancho de mensagem.
    
- Move a mensagem para a pasta Itens enviados, itens excluídos ou para outra pasta.
    
- Libera a mensagem.
    
## <a name="see-also"></a>Confira também



[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[Propriedade canônica PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

