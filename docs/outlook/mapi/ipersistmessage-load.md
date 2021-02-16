---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317126"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Carrega o formulário para uma mensagem especificada.
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a>Parâmetros

 _pMessageSite_
  
> [in] Um ponteiro para o site de mensagens para o formulário a ser carregado.
    
 _pMessage_
  
> [in] Um ponteiro para a mensagem para a qual o formulário deve ser carregado.
    
 _ulMessageStatus_
  
> [in] Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor, copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)da mensagem, que fornecem informações sobre o estado da mensagem.
    
 _ulMessageFlags_
  
> [in] Uma bitmask de sinalizadores, copiada da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem, que fornecem mais informações sobre o estado da mensagem.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O formulário foi carregado com êxito.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam **o método IPersistMessage::Load** para carregar um formulário para uma mensagem existente. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

 **Load** é chamado somente quando um formulário está em um dos seguintes estados: 
  
- [Não reinicializado](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Se um visualizador de formulário **chamar Load** enquanto o formulário estiver em qualquer outro estado, o método retornará E_UNEXPECTED. 
  
Se o seu formulário tiver uma referência a um site de mensagem ativo diferente do que é passado para o **Load**, libere o site original porque ele não será mais usado. Armazene os ponteiros para o site de mensagens e a mensagem dos parâmetros  _pMessageSite_ e  _pMessage_ e chame os métodos [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) dos dois objetos para incrementar suas contagens de referência. 
  
Após **a conclusão de AddRef,** armazene as propriedades dos parâmetros  _ulMessageStatus_ e  _ulMessageFlags_ no formulário. Transifique o formulário para seu estado [Normal](normal-state.md) antes de exibi-lo e notifique os visualizadores registrados chamando seus métodos [IMAPIViewAdviseSink::OnNewMessage.](imapiviewadvisesink-onnewmessage.md) 
  
Se não ocorrerem erros, retorne S_OK. 
  
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estado Não Reinicializado](uninitialized-state.md)
  
[Estado HandsOffAfterSave](handsoffaftersave-state.md)
  
[Estado HandsOffFromNormal](handsofffromnormal-state.md)
  
[Estados do formulário](form-states.md)


[IPersistStorage::Load](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream::Load](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile::Load](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

