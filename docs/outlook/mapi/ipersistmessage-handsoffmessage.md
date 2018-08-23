---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2cd4c86dc45bca85632a3fadc9023c9ad25cfa37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583026"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Faz com que o formulário liberar a sua mensagem atual.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum
  
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A mensagem foi liberada com êxito.
    
## <a name="remarks"></a>Comentários

Transição de formulários em dois estados HandsOff:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Quando um formulário estiver em um desses estados, ele está sendo armazenados permanentemente. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Quando um visualizador de formulário chama o método **IPersistMessage::HandsOffMessage** enquanto o formulário está no estado [Normal](normal-state.md) ou [NoScribble](noscribble-state.md) , chame recursivamente **HandsOffMessage** em cada mensagem incorporada na mensagem atual e o [ IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) método em cada objeto OLE incorporado na mensagem atual. Em seguida, libere a mensagem atual e incorporadas todas as mensagens e objetos OLE. Se seu formulário estava no estado Normal, fazer a transição para o estado de HandsOffFromNormal. Se seu formulário estava no estado NoScribble, fazer a transição para o estado de HandsOffAfterSave. Após uma transição bem-sucedida, chame o método de [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) da mensagem e retornar S_OK. 
  
Quando um visualizador de formulário chama **HandsOffMessage** enquanto o formulário estiver em qualquer um dos Estados HandsOff, retorne E_UNEXPECTED. 
  
Para obter mais informações sobre os diferentes estados de um formulário, consulte [Estados de formulário](form-states.md). Para obter mais informações sobre como trabalhar com o estado de HandsOff de objetos de armazenamento, consulte o método [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) . 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estados de formulários](form-states.md)

