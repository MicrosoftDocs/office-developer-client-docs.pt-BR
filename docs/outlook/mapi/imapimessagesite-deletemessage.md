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
  
> no Um ponteiro para um objeto de contexto de exibição.
    
 _prcPosRect_
  
> no Um ponteiro para uma estrutura de [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contém o tamanho e a posição da janela do formulário atual. O próximo formulário também usa este retângulo de janela. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NO_SUPPORT 
  
> A operação não é suportada por este site de mensagem.
    
## <a name="remarks"></a>Comentários

Um objeto Form chama o método **IMAPIMessageSite::D eletemessage** para excluir a mensagem que o formulário está exibindo no momento. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Após o retorno de **DeleteMessage**, os objetos Form devem verificar uma nova mensagem e, em seguida, se não houver nenhum. Para determinar se a mensagem **DeleteMessage** atuou em foi excluída ou movida para uma pasta **itens excluídos** , um objeto Form pode chamar o método [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) para determinar se o sinalizador DELETE_IS_MOVE foi retornado. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se a implementação de um visualizador de formulários do método **DeleteMessage** for movida para a próxima mensagem depois de excluir uma mensagem, a implementação deverá chamar o método [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) e passar o sinalizador VCDIR_DELETE antes de executar a exclusão real. Se a implementação de um visualizador de formulários do **DeleteMessage** mover a mensagem excluída (por exemplo, para uma pasta **itens excluídos** ), a implementação deverá salvar as alterações na mensagem se a mensagem tiver sido modificada. 
  
Uma implementação típica do **DeleteMessage** realiza as seguintes tarefas: 
  
1. Se a implementação estiver movendo a mensagem, ela chamará o método [IPersistMessage:: Save](ipersistmessage-save.md) , passando **NULL** no parâmetro _PMessage_ e **true** no parâmetro _fSameAsLoad_ . 
    
2. Ele chama o método **IMAPIViewContext:: ActivateNext** , passando o sinalizador VCDIR_DELETE no parâmetro _ulDir_ . 
    
3. Se a chamada **ActivateNext** falhar, ela retornará. Se **ActivateNext** retornar S_FALSE, ele chamará o método [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) . 
    
4. Ele exclui ou move a mensagem.
    
Para obter a estrutura do **Rect** usada pela janela de um formulário, chame a função [GetWindowRect](https://msdn.microsoft.com/library/ms633519) do Windows. 
  
Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer::D eleteMessage  <br/> |Não implementado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

