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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390454"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um identificador que representa o servidor de formulário que pode gerenciar o formulário. 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>Parâmetros

 _lpClassID_
  
> [além, out] Um ponteiro para o identificador de classe (CLSID) do formulário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O identificador de classe foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IPersistMessge::GetClassID** define o conteúdo do parâmetro _lpClassID_ como identificador de classe do servidor formulário e retorna S_OK. Quando um visualizador de formulário chama **GetClassID** e ela retorna com êxito, o formulário é colocado no estado [não inicializado](uninitialized-state.md) . 
  
Para obter mais informações sobre como os identificadores de classe são usados com os objetos de armazenamento estruturado, consulte a documentação para o método [IPersist::GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) . 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

