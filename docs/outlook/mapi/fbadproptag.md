---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d1503aaa5bddd23a90035219901e1dc232dbd026
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766531"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**Aplica-se a**: Outlook 
  
Valida uma marca de propriedade especificado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parâmetros

 _ulPropTag_
  
> [in] A marca de propriedade a ser validado.
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> A marca de propriedade especificado não é uma marca de propriedade MAPI válida. 
    
FALSO 
  
> A marca de propriedade especificado é uma marca de propriedade MAPI válida.
    
## <a name="remarks"></a>Comentários

A função **FBadPropTag** valida a marca de propriedade especificado com base nas definições de MAPI. Ele faz sures que o tipo de propriedade é um dos tipos definidos pelo MAPI e que o identificador de propriedade é definido para ser desse tipo. 
  
## <a name="see-also"></a>Confira também



[FBadProp](fbadprop.md)

