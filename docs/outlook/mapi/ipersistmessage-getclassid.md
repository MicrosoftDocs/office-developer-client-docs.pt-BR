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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309622"
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
  
> [in, out] Um ponteiro para o identificador de classe (CLSID) do formulário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O identificador de classe foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IPersistMessge::GetClassID** define o conteúdo do parâmetro  _lpClassID_ para o identificador de classe do servidor de formulário e retorna S_OK. Quando um visualizador de formulário chama **GetClassID** e retorna com êxito, o formulário é colocado no estado [Não reinicializado.](uninitialized-state.md) 
  
Para obter mais informações sobre como os identificadores de classe são usados com objetos de armazenamento estruturados, consulte a documentação do método [IPersist::GetClassID.](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

