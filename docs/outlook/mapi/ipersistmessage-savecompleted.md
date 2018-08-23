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
ms.openlocfilehash: 7813636abc1c4d6ad756c7cf670e21d4acb7f540
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592742"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notifica o formulário que uma gravação operação foi concluída. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parâmetros

_pMessage_
  
> [in] Um ponteiro para a mensagem salva recentemente.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A notificação foi bem-sucedida.
    
E_INVALIDARG 
  
> O parâmetro _pMessage_ é NULL e o formulário está no estado de [HandsOffFromNormal](handsofffromnormal-state.md) ou [HandsOffAfterSave](handsoffaftersave-state.md) . 
    
E_UNEXPECTED 
  
> O formulário não estiver em um dos seguintes estados:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Comentários

O método **IPersistMessage::SaveCompleted** é chamado por um visualizador de formulário para notificar o formulário que foram salvos todas as alterações pendentes. **SaveCompleted** deve ser chamado apenas quando o formulário está em um dos seguintes estados: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Notas para implementadores

Existem várias ações possíveis que o método **SaveCompleted** pode realizar, dependendo do que a mensagem contém o parâmetro de ponteiro e estado da qual a mensagem está em. No entanto, quando uma ação for bem-sucedido, sempre salve o estado atual da mensagem que o parâmetro _pMessage_ aponta para e transição o formulário ao seu estado [Normal](normal-state.md) . 
  
A tabela a seguir descreve as condições que afetam as ações que você deve tomar na sua implementação de **SaveCompleted**.
  
|**Condição**|**Action**|
|:-----|:-----|
|O parâmetro _pMessage_ é NULL e o parâmetro _fSameAsLoad_ do método [IPersistMessage::Save](ipersistmessage-save.md) é definido como TRUE.  <br/> |Chame o método [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) todos os visualizadores registrados, marcar o formulário como S_OK limpa e retorno.  <br/> |
|O parâmetro _pMessage_ é NULL e o parâmetro _fSameAsLoad_ do método **IPersistMessage::Save** é definido como FALSE.  <br/> |Retorne S_OK.  <br/> |
|O formulário está no estado HandsOffFromNormal.  <br/> |Liberar a mensagem atual e substituí-la com a mensagem apontada pelo parâmetro _pMessage_ . Método de [AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) da mensagem substituição de chamada e retornar S_OK.  <br/> |
|O formulário está no estado HandsOffAfterSave.  <br/> |Chame o método **IMAPIViewAdviseSink::OnSaved** todos os visualizadores registrados, marcar o formulário como S_OK limpa e retorno.  <br/> |
|O formulário está no estado [NoScribble](noscribble-state.md) .  <br/> |Liberar a mensagem atual e substituí-la com a mensagem apontada pela _pMessage_. Chame o método de **AddRef** da mensagem de substituição. Chame o método **IMAPIViewAdviseSink::OnSaved** todos os visualizadores registrados, marcar o formulário como S_OK limpa e retorno.  <br/> |
|O formulário está em um dos Estados HandsOff e o parâmetro _pMessage_ é definido como NULL.  <br/> |Retorne E_INVALIDARG.  <br/> |
|O formulário está em um estado que não seja um dos Estados HandsOff ou o estado de NoScribble.  <br/> |Retorne E_UNEXPECTED.  <br/> |
   
Para obter mais informações sobre como salvar objetos de armazenamento, consulte a documentação para os métodos [IPersistStorage::SaveCompleted](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) ou [IPersistFile::SaveCompleted](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) . 
  
## <a name="see-also"></a>Confira também

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [Estados de formulários](form-states.md)
