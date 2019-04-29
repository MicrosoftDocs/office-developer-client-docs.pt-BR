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
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411761"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica se o formulário pode manipular a classe de mensagem da próxima mensagem a ser exibida.
  
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
  
> no Um ponteiro para a classe de mensagem da próxima mensagem.
    
 _ulMessageStatus_
  
> no Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor, copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da próxima mensagem a ser exibida, que fornece informações de status sobre a tabela de conteúdo que a mensagem está incluída no.
    
 _ulMessageFlags_
  
> no Um ponteiro para uma bitmask de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da próxima mensagem a ser exibida, indicando o estado atual da mensagem.
    
 _ppPersistMessage_
  
> bota Um ponteiro para um ponteiro para a implementação do [IPersistMessage](ipersistmessageiunknown.md) do objeto Form usado para o novo formulário, se um novo formulário for necessário. Um ponteiro para nulo pode ser retornado se o objeto Form atual puder ser usado para exibir e salvar a próxima mensagem. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi bem-sucedida e o formulário pode lidar com a próxima mensagem.
    
S_FALSE 
  
> O formulário não manipula a classe de mensagem da mensagem seguinte.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormAdviseSink:: OnActivateNext** para ajudar o formulário a determinar se pode exibir a próxima mensagem em uma pasta. A próxima mensagem pode ser uma mensagem de qualquer classe, mas geralmente é da mesma classe ou de uma classe relacionada. Isso torna mais eficiente o processo de leitura de várias mensagens da mesma classe, permitindo que os aplicativos cliente reutilizem objetos de formulário sempre que possível. 
  
A maioria dos objetos de formulário usará a classe de mensagem apontada pelo parâmetro _lpszMessageClass_ para determinar se eles podem manipular a próxima mensagem. Geralmente, um formulário pode lidar com mensagens que pertencem a classes das quais a classe padrão do formulário é uma subclasse, além de mensagens que pertencem à classe padrão. No enTanto, um formulário pode usar outros fatores para determinar sem dúvida se uma mensagem pode ser tratada, como o status enviado ou não enviado da mensagem seguinte. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Retornar S_OK e NULL no parâmetro _ppPersistMessage_ se o formulário puder manipular a classe de mensagem. Se o formulário puder criar um novo formulário que possa lidar com a mensagem de que o formulário não pode lidar, siga estas etapas: 
  
1. Chame o alocador de classe do formulário para criar uma instância de um novo objeto Form.
    
2. Armazene essa instância no conteúdo do parâmetro de ponteiro _ppPersistMessage_ . 
    
3. Retorne S_OK.
    
O Visualizador de formulários carregará a mensagem usando o método [IPersistMessage:: Load](ipersistmessage-load.md) que pertence ao objeto apontado por _ppPersistMessage_.
  
Se nem o formulário nem um formulário que você pode criar podem manipular a próxima mensagem, retorne S_FALSE. No enTanto, em geral, os formulários não devem retornar esse valor porque causa uma redução no desempenho no Visualizador de formulários.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |CMyMAPIFormViewer:: ActivateNext  <br/> |MFCMAPI usa o método **IMAPIFormAdviseSink:: OnActivateNext** para implementar o método [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) .  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

