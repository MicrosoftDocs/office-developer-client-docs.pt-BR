---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ce4d57ab4837f40ffbc898fde68e44cc802676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766996"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**Aplica-se a**: Outlook 
  
Indica se o formulário pode lidar com a classe de mensagem da próxima mensagem para exibir.
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a>Parâmetros

 _lpszMessageClass_
  
> [in] Um ponteiro para a classe de mensagem da próxima mensagem.
    
 _ulMessageStatus_
  
> [in] Uma bitmask dos sinalizadores definido pelo provedor ou cliente, copiado da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem próxima a exibir, que fornece informações de status sobre a tabela de conteúdo que a mensagem é incluída in.
    
 _ulMessageFlags_
  
> [in] Um ponteiro para uma bitmask dos sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem próxima a exibir que indica o estado atual da mensagem.
    
 _ppPersistMessage_
  
> [out] Um ponteiro para um ponteiro para a implementação de [IPersistMessage](ipersistmessageiunknown.md) para o objeto de formulário usado para o novo formulário, se um novo formulário é necessário. Um ponteiro como NULL pode ser retornado se o objeto atual do formulário pode ser usado para exibir e salvar a próxima mensagem. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A notificação foi bem-sucedida e o formulário pode manipular a próxima mensagem.
    
S_FALSE 
  
> O formulário não processa a classe de mensagem da próxima mensagem.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIFormAdviseSink::OnActivateNext** para ajudar a determinar se ele pode exibir a próxima mensagem em uma pasta de formulário. A próxima mensagem poderia ser uma mensagem de qualquer classe, mas geralmente é da mesma classe ou uma classe relacionada. Isso faz com que o processo de leitura várias mensagens da mesma classe mais eficiente, permitindo que aplicativos de cliente reutilizar os objetos de formulário sempre que possível. 
  
A maioria dos objetos do formulário usará a classe de mensagem apontada pelo parâmetro _lpszMessageClass_ para determinar se podem lidar com a próxima mensagem. Geralmente, um formulário pode manipular mensagens que pertencem às classes do qual a classe do formulário padrão é uma subclasse, além das mensagens que pertencem à classe padrão. No entanto, um formulário pode usar outros fatores para determinar sem pergunta se uma mensagem pode ser lida, como o status enviado ou não enviado da próxima mensagem. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Retorne S_OK e NULL no parâmetro _ppPersistMessage_ se o formulário pode manipular a classe da mensagem. Se o formulário pode criar um novo formulário que pode manipular a mensagem que o formulário é capaz de manipular, siga estas etapas: 
  
1. Chame o alocador de classe do formulário para criar uma instância de um novo objeto de formulário.
    
2. Armazene essa instância no conteúdo do parâmetro _ppPersistMessage_ ponteiro. 
    
3. Retorne S_OK.
    
A tela de formulário será carregado a mensagem usando o método [IPersistMessage::Load](ipersistmessage-load.md) que pertence ao objeto apontado pela _ppPersistMessage_.
  
Se nem o formulário nem em um formulário que você pode criar pode manipular a próxima mensagem, retorne S_FALSE. No entanto, em geral, formulários não devem retornar que esse valor porque isso causar redução de desempenho no Visualizador do formulário.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI usa o método **IMAPIFormAdviseSink::OnActivateNext** para implementar o método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) .  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

