---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317133"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notifica o formulário de que uma operação de salvamento foi concluída. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parâmetros

_pMessage_
  
> no Um ponteiro para a mensagem recentemente salva.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi bem-sucedida.
    
E_INVALIDARG 
  
> O parâmetro _PMessage_ é nulo e o formulário é no estado [HandsOffFromNormal](handsofffromnormal-state.md) ou [HandsOffAfterSave](handsoffaftersave-state.md) . 
    
E_UNEXPECTED 
  
> O formulário não está em um dos seguintes Estados:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Comentários

O método **IPersistMessage:: SaveCompleted** é chamado por um visualizador de formulários para notificar o formulário de que todas as alterações pendentes foram salvas. **SaveCompleted** deve ser chamado somente quando o formulário estiver em um dos seguintes Estados: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Há várias ações possíveis que o método **SaveCompleted** pode executar, dependendo do que o parâmetro de ponteiro de mensagem contém e o estado em que a mensagem está. No enTanto, quando uma ação for bem-sucedida, sempre salve o estado atual da mensagem de que o parâmetro _PMessage_ aponta para e migre o formulário para seu estado [normal](normal-state.md) . 
  
A tabela a seguir descreve as condições que afetam as ações que você deve executar na sua implementação do **SaveCompleted**.
  
|**Condition**|**Action**|
|:-----|:-----|
|O parâmetro _PMessage_ é nulo e o parâmetro _FSameAsLoad_ do método [IPersistMessage:: Save](ipersistmessage-save.md) é definido como true.  <br/> |Chame o método [IMAPIViewAdviseSink::](imapiviewadvisesink-onsaved.md) onsaved de todos os visualizadores registrados, marque o formulário como limpo e retorne S_OK.  <br/> |
|O parâmetro _PMessage_ é nulo e o parâmetro _FSameAsLoad_ do método **IPersistMessage:: Save** é definido como false.  <br/> |Retorne S_OK.  <br/> |
|O formulário está no estado HandsOffFromNormal.  <br/> |Liberar a mensagem atual e substituí-la pela mensagem indicada pelo parâmetro _PMessage_ . Chame o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) da mensagem de substituição e retorne S_OK.  <br/> |
|O formulário está no estado HandsOffAfterSave.  <br/> |Chame o método **IMAPIViewAdviseSink::** onsaved de todos os visualizadores registrados, marque o formulário como limpo e retorne S_OK.  <br/> |
|O formulário está no estado [norabisco](noscribble-state.md) .  <br/> |Liberar a mensagem atual e substituí-la pela mensagem indicada por _PMessage_. Chame o método **IUnknown:: AddRef** da mensagem de substituição. Chame o método **IMAPIViewAdviseSink::** onsaved de todos os visualizadores registrados, marque o formulário como limpo e retorne S_OK.  <br/> |
|O formulário está em um dos Estados HandsOff e o parâmetro _PMessage_ está definido como nulo.  <br/> |Retornar E_INVALIDARG.  <br/> |
|O formulário está em um estado diferente de um dos Estados HandsOff ou no estado noRabisco.  <br/> |Retornar E_UNEXPECTED.  <br/> |
   
Para obter mais informações sobre como salvar objetos de armazenamento, consulte a documentação dos métodos [IPersistStorage:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) ou [IPersistFile:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) . 
  
## <a name="see-also"></a>Confira também

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [Estados de formulário](form-states.md)
