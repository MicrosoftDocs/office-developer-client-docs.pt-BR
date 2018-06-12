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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: eff192b0d2b5cde51a2909452b19ffe1a47b2c04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767606"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**Aplica-se a**: Outlook 
  
Carrega o formulário para uma mensagem especificada.
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a>Par�metros

 _pMessageSite_
  
> [in] Um ponteiro para o site de mensagem para o formulário a ser carregada.
    
 _pMessage_
  
> [in] Um ponteiro para a mensagem para o qual o formulário deve ser carregado.
    
 _ulMessageStatus_
  
> [in] Uma bitmask dos sinalizadores definido pelo provedor ou cliente, copiado de propriedade de **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem, que fornecem informações sobre o estado da mensagem.
    
 _ulMessageFlags_
  
> [in] Uma bitmask dos sinalizadores, copiado de propriedade de **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem, que fornecem mais informações sobre o estado da mensagem.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O formulário foi carregado com êxito.
    
## <a name="remarks"></a>Coment�rios

Visualizadores de formulário chame o método de **IPersistMessage::Load** para carregar um formulário para uma mensagem existente. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

 **Carga** é chamado somente quando um formulário estiver em um dos seguintes estados: 
  
- [Não inicializado](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Se um visualizador de formulário chama **carga** enquanto o formulário está em qualquer outro estado, o método retornará E_UNEXPECTED. 
  
Se o seu formulário tem uma referência a um site da mensagem ativa diferente daquela que é passado para o **carregamento**, libere o site original porque ele não será usado. Armazene os ponteiros para o site de mensagem e a mensagem de que os parâmetros _pMessageSite_ e _pMessage_ e chamar métodos de [AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) dos objetos para incrementar seus contagens de referência. 
  
Após **AddRef** , armazene as propriedades dos parâmetros _ulMessageStatus_ e _ulMessageFlags_ no formulário. Fazer a transição de formulário ao seu estado [Normal](normal-state.md) antes de exibi-las e notificar os visualizadores registrados chamando os métodos [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) . 
  
Se nenhum erro ocorrer, retorne S_OK. 
  
## <a name="see-also"></a>Confira também



[Propriedade canônico de PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriedade canônico de PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage: IUnknown](ipersistmessageiunknown.md)


[Estado não inicializado](uninitialized-state.md)
  
[Estado de HandsOffAfterSave](handsoffaftersave-state.md)
  
[Estado de HandsOffFromNormal](handsofffromnormal-state.md)
  
[Estados de formulário](form-states.md)


[IPersistStorage::Load](http://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream::Load](http://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile:: Load](http://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

