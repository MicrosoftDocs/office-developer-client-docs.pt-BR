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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411243"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Conclui a lista de destinatários de uma mensagem, expandindo listas de distribuição específicas.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpMessage_
  
> [in] Um ponteiro para a mensagem que tem a lista de destinatários a ser processada.
    
 _lpulFlags_
  
> [out] Um ponteiro para uma máscara de bits de sinalizadores que controla o tipo de processamento que ocorre. Os sinalizadores a seguir podem ser definidos:
    
NEEDS_PREPROCESSING 
  
> A mensagem precisa ser pré-processada antes de ser enviada.
    
NEEDS_SPOOLER 
  
> O spooler MAPI (em vez do provedor de transporte ao qual o chamador está fortemente próximo) deve enviar a mensagem.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A lista de destinatários da mensagem foi processada com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::ExpandRecips** é implementado para objetos de suporte do provedor de armazenamento de mensagens. Os provedores de armazenamento de mensagens **chamam ExpandRecips** para solicitar que o MAPI execute as seguintes tarefas: 
  
- Expanda determinadas listas de distribuição pessoais para seus destinatários de componentes.
    
- Substitua todos os nomes de exibição que foram alterados com os nomes originais.
    
- Marque qualquer entrada duplicada.
    
- Resolver todos os endereços one-off. 
    
- Verifique se a mensagem precisa de pré-processamento e, se precisar, defina o sinalizador apontado por  _lpulFlags_ como NEEDS_PREPROCESSING. 
    
 **ExpandRecips** expande todas as listas de distribuição que tenham o tipo de endereço de mensagens de MAPIPDL. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Sempre chame **ExpandRecips** como parte do processamento de mensagens. Faça uma chamada para **ExpandRecips** uma das primeiras chamadas na implementação do método [IMessage::SubmitMessage.](imessage-submitmessage.md) 
  
## <a name="see-also"></a>Confira também



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

