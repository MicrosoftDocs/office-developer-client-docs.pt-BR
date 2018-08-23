---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6ed73cd683f1668900a76f7b8c48494952e9fc14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573345"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui a mensagem atual.
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parâmetros

 _pViewContext_
  
> [in] Um ponteiro para um objeto de contexto do modo de exibição.
    
 _prcPosRect_
  
> [in] Um ponteiro para uma estrutura de [Retangular](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) que contém o tamanho da janela e a posição atual do formulário. A próxima forma exibida também usa esse retângulo de janela. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_NO_SUPPORT 
  
> A operação não é suportada por este site de mensagem.
    
## <a name="remarks"></a>Comentários

Um objeto form chama o método **IMAPIMessageSite::DeleteMessage** para excluir a mensagem que o formulário está exibindo no momento. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Após o retorno de **DeleteMessage**, os objetos de formulário devem verificar se há uma nova mensagem e, em seguida, descartar sozinhos, se não houver nenhum. Para determinar se a mensagem **que deletemessage** realizadas foi excluída ou movida para uma pasta de **Itens excluídos** , um objeto form pode chamar o método [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) para determinar se o sinalizador DELETE_IS_MOVE foi retornado. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Se a implementação do Visualizador de um formulário do método **DeleteMessage** move para a próxima mensagem após ela exclui uma mensagem, a implementação deve chamar o método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) e passar o sinalizador VCDIR_DELETE antes de executar a exclusão real. Se a implementação do Visualizador de um formulário de **DeleteMessage** move a mensagem excluída (por exemplo, para uma pasta de **Itens excluídos** ), a implementação deve salvar alterações na mensagem se a mensagem foi modificada. 
  
Uma implementação típica de **DeleteMessage** executa as seguintes tarefas: 
  
1. Se a mensagem está se movendo a implementação, ele chama o método [IPersistMessage::Save](ipersistmessage-save.md) , passando **null** no parâmetro _pMessage_ e **true** no parâmetro _fSameAsLoad_ . 
    
2. Ele chama o método **IMAPIViewContext::ActivateNext** , passando o sinalizador VCDIR_DELETE no parâmetro _ulDir_ . 
    
3. Se a chamada **ActivateNext** falha, será retornado. Se **ActivateNext** retornar S_FALSE, ele chama o método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) . 
    
4. Exclui ou move a mensagem.
    
Para obter a estrutura de **Retangular** usada pela janela de um formulário, chame a função do Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) . 
  
Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::DeleteMessage  <br/> |Não foi implementado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

