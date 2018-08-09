---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2e41701d3a739864b1eafc8001833b7df5c8908b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767237"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**Aplica-se a**: Outlook 
  
Conclui a lista de destinatários da mensagem, expandindo listas de distribuição particular.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpMessage_
  
> [in] Um ponteiro para a mensagem que tem a lista de destinatários a serem processados.
    
 _lpulFlags_
  
> [out] Um ponteiro para uma bitmask dos sinalizadores que controla o tipo de processamento ocorre. Sinalizadores a seguir podem ser definidos:
    
NEEDS_PREPROCESSING 
  
> A mensagem precisa ser processado antes de serem enviada.
    
NEEDS_SPOOLER 
  
> O MAPI spooler (ao invés do provedor de transporte para o qual o chamador está intimamente ligado) deve enviar a mensagem.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Lista de destinatários da mensagem foi processada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::ExpandRecips** é implementado para objetos de suporte do provedor de repositório de mensagem. Provedores de armazenamento de mensagem chamarem **ExpandRecips** para solicitar que o MAPI para executar as seguintes tarefas: 
  
- Expanda certas listas de distribuição pessoal aos destinatários componente.
    
- Substitua todos os nomes para exibição que foram alterados os nomes originais.
    
- Marca quaisquer entradas duplicadas.
    
- Resolva todos os endereços únicos. 
    
- Verifique se a mensagem precisa pré-processamento e, se contiver, defina o sinalizador apontado pela _lpulFlags_ para NEEDS_PREPROCESSING. 
    
 **ExpandRecips** expande quaisquer listas de distribuição que tenham o tipo de endereço de mensagens de MAPIPDL. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Sempre chame **ExpandRecips** como parte do seu processamento de mensagens. Fazer uma chamada para **ExpandRecips** uma das chamadas primeira na sua implementação do método [IMessage::SubmitMessage](imessage-submitmessage.md) . 
  
## <a name="see-also"></a>Confira também



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

