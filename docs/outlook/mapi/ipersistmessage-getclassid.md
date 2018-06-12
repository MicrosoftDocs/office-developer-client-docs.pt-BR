---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e0937eed2e8ca61bc18ee45ff20337267808ea70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767601"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**Aplica-se a**: Outlook 
  
Retorna um identificador que representa o servidor de formulário que pode gerenciar o formulário. 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>Par�metros

 _lpClassID_
  
> [além, out] Um ponteiro para o identificador de classe (CLSID) do formulário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O identificador de classe foi retornado com êxito.
    
## <a name="remarks"></a>Coment�rios

O método **IPersistMessge::GetClassID** define o conteúdo do parâmetro _lpClassID_ como identificador de classe do servidor formulário e retorna S_OK. Quando um visualizador de formulário chama **GetClassID** e ela retorna com êxito, o formulário é colocado no estado [não inicializado](uninitialized-state.md) . 
  
Para obter mais informações sobre como os identificadores de classe são usados com os objetos de armazenamento estruturado, consulte a documentação para o método [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) . 
  
## <a name="see-also"></a>Confira também



[IPersistMessage: IUnknown](ipersistmessageiunknown.md)

