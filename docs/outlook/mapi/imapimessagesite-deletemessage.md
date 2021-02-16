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
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321410"
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
  
> [in] Um ponteiro para um objeto de contexto de exibição.
    
 _prcPosRect_
  
> [in] Um ponteiro para uma [estrutura RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contém o tamanho e a posição da janela do formulário atual. O próximo formulário exibido também usa esse retângulo de janela. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_NO_SUPPORT 
  
> A operação não é suportada por este site de mensagens.
    
## <a name="remarks"></a>Comentários

Um objeto de formulário chama o **método IMAPIMessageSite::D eleteMessage** para excluir a mensagem que o formulário está exibindo no momento. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Após o retorno de **DeleteMessage**, os objetos de formulário devem verificar se há uma nova mensagem e, em seguida, descartar a si mesmos se não existe. Para determinar se **a** mensagem em que **DeleteMessage** atuou foi excluída ou movida para uma pasta Itens Excluídos, um objeto de formulário pode chamar o método [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) para determinar se o sinalizador DELETE_IS_MOVE foi retornado. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se a implementação do método **DeleteMessage** de um visualizador de formulário for para a próxima mensagem depois de excluir uma mensagem, a implementação deverá chamar o método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) e passar o sinalizador VCDIR_DELETE antes de executar a exclusão real. Se a implementação de **DeleteMessage** de um visualizador de formulário mover **a** mensagem excluída (por exemplo, para uma pasta Itens Excluídos), a implementação deverá salvar as alterações na mensagem se a mensagem tiver sido modificada. 
  
Uma implementação típica **de DeleteMessage** executa as seguintes tarefas: 
  
1. Se a implementação estiver movendo a mensagem, ela chamará o método [IPersistMessage::Save,](ipersistmessage-save.md) passando **nulo** no parâmetro _pMessage_ e **true** no parâmetro _fSameAsLoad._ 
    
2. Ele chama o **método IMAPIViewContext::ActivateNext,** passando o VCDIR_DELETE de texto no _parâmetro ulDir._ 
    
3. Se a **chamada ActivateNext** falhar, ela retornará. Se **ActivateNext** retornar S_FALSE, ele chamará o [método IPersistMessage::HandsOffMessage.](ipersistmessage-handsoffmessage.md) 
    
4. Ele exclui ou move a mensagem.
    
Para obter a **estrutura RECT** usada pela janela de um formulário, chame a função [Windows GetWindowRect.](https://msdn.microsoft.com/library/ms633519) 
  
Para uma lista de interfaces relacionadas a servidores de formulário, consulte [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::D eleteMessage  <br/> |Não implementado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

