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
  
Faz com que o formulário libere sua mensagem atual.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A mensagem foi liberada com êxito.
    
## <a name="remarks"></a>Comentários

Os formulários são transições para dois estados handsoff:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Quando um formulário está em qualquer um desses estados, ele está em processo de ser armazenado permanentemente. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando um visualizador de formulário chama o método **IPersistMessage::HandsOffMessage** enquanto o formulário está no estado [Normal](normal-state.md) ou [NoScribble,](noscribble-state.md) chame recursivamente **HandsOffMessage** em cada mensagem incorporada na mensagem atual e no método [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) em cada objeto OLE incorporado na mensagem atual. Em seguida, libere a mensagem atual e todas as mensagens e objetos OLE incorporados. Se o formulário estiver no estado Normal, transição para o estado HandsOffFromNormal. Se o formulário estava no estado NoScribble, transição para o estado HandsOffAfterSave. Após uma transição bem-sucedida, chame o [método IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) da mensagem e retorne S_OK. 
  
Quando um visualizador de formulário chamar **HandsOffMessage** enquanto o formulário estiver em um dos estados HandsOff, retorne E_UNEXPECTED. 
  
For more information about the different states of a form, see [Form States](form-states.md). Para obter mais informações sobre como trabalhar com o estado HandsOff de objetos de armazenamento, consulte o método [IPersistStorage::HandsOffStorage.](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estados do formulário](form-states.md)

