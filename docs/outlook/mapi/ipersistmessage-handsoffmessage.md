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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 84f0ca88403980ff9ea1c91821a8a3d7edae74fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309713"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Faz com que o formulário libere a mensagem atual.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Parâmetros

Nenhuma
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A mensagem foi liberada com êxito.
    
## <a name="remarks"></a>Comentários

Transição de formulários para dois Estados do HandsOff:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Quando um formulário está em um desses Estados, ele está no processo de ser armazenado permanentemente. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando um visualizador de formulários chama o método **IPersistMessage:: HandsOffMessage** enquanto o formulário está no estado [normal](normal-state.md) ou norabisco, chame recursivamente **HandsOffMessage** em cada mensagem inserida na mensagem atual e na [](noscribble-state.md) [ IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) método em cada objeto OLE incorporado na mensagem atual. Em seguida, libere a mensagem atual e todas as mensagens inseridas e objetos OLE. Se o formulário estava no estado normal, transição para o estado HandsOffFromNormal. Se o formulário estava no estado noRabisco, transição para o estado HandsOffAfterSave. Após uma transição bem-sucedida, chame o método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do Message e retorne S_OK. 
  
Quando um visualizador de formulários chama **HandsOffMessage** enquanto o formulário está em um dos Estados HandsOff, retorne E_UNEXPECTED. 
  
Para obter mais informações sobre os diferentes Estados de um formulário, confira [Estados de formulário](form-states.md). Para obter mais informações sobre como trabalhar com o estado HandsOff de objetos de armazenamento, consulte o método [IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) . 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estados de formulário](form-states.md)

