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
  
Notifica o formulário de que uma operação de salvar foi concluída. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parâmetros

_pMessage_
  
> [in] Um ponteiro para a mensagem recém-salva.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi bem-sucedida.
    
E_INVALIDARG 
  
> O _parâmetro pMessage_ é NULL e o formulário está no estado [HandsOffFromNormal](handsofffromnormal-state.md) ou [HandsOffAfterSave.](handsoffaftersave-state.md) 
    
E_UNEXPECTED 
  
> O formulário não está em um dos seguintes estados:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Comentários

O **método IPersistMessage::SaveCompleted** é chamado por um visualizador de formulário para notificar o formulário de que todas as alterações pendentes foram salvas. **SaveCompleted** deve ser chamado somente quando o formulário estiver em um dos seguintes estados: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Há várias ações possíveis que o **método SaveCompleted** pode executar, dependendo do parâmetro do ponteiro da mensagem e do estado em que a mensagem está. No entanto, quando uma ação for bem-sucedida, salve sempre o estado atual da mensagem que o parâmetro _pMessage_ aponta e transirá o formulário para seu [estado Normal.](normal-state.md) 
  
A tabela a seguir descreve as condições que afetam as ações que você deve tomar na implementação **de SaveCompleted**.
  
|**Condition**|**Ação**|
|:-----|:-----|
|O  _parâmetro pMessage_ é NULL e  _o parâmetro fSameAsLoad_ do método [IPersistMessage::Save](ipersistmessage-save.md) é definido como TRUE.  <br/> |Chame o [método IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) de todos os visualizadores registrados, marque o formulário como limpo e retorne S_OK.  <br/> |
|O  _parâmetro pMessage_ é NULL e  _o parâmetro fSameAsLoad_ do método **IPersistMessage::Save** é definido como FALSE.  <br/> |Retorne S_OK.  <br/> |
|O formulário está no estado HandsOffFromNormal.  <br/> |Libere a mensagem atual e substitua-a pela mensagem apontada pelo _parâmetro pMessage._ Chame o método [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) da mensagem de substituição e retorne S_OK.  <br/> |
|O formulário está no estado HandsOffAfterSave.  <br/> |Chame o **método IMAPIViewAdviseSink::OnSaved** de todos os visualizadores registrados, marque o formulário como limpo e retorne S_OK.  <br/> |
|O formulário está no [estado NoScribble.](noscribble-state.md)  <br/> |Libere a mensagem atual e substitua-a pela mensagem apontada por  _pMessage_. Chame o método **IUnknown::AddRef** da mensagem de substituição. Chame o **método IMAPIViewAdviseSink::OnSaved** de todos os visualizadores registrados, marque o formulário como limpo e retorne S_OK.  <br/> |
|O formulário está em um dos estados HandsOff e o  _parâmetro pMessage_ está definido como NULL.  <br/> |Retornar E_INVALIDARG.  <br/> |
|The form is in a state other than one of the HandsOff states or the NoScribble state.  <br/> |Retornar E_UNEXPECTED.  <br/> |
   
Para obter mais informações sobre como salvar objetos de armazenamento, consulte a documentação dos métodos [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) ou [IPersistFile::SaveCompleted.](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) 
  
## <a name="see-also"></a>Confira também

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [Estados do formulário](form-states.md)
