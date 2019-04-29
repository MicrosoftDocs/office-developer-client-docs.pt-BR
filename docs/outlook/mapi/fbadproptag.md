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
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433644"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma marca de propriedade especificada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parâmetros

 _ulPropTag_
  
> no A marca de propriedade a ser validada.
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> A marca de propriedade especificada não é uma marca de propriedade MAPI válida. 
    
FALSE 
  
> A marca de propriedade especificada é uma marca de propriedade MAPI válida.
    
## <a name="remarks"></a>Comentários

A função **FBadPropTag** valida a marca de propriedade especificada com base nas definições de MAPI. Ele garante que o tipo de propriedade é um dos tipos definidos por MAPI e que o identificador de propriedade é definido para ser daquele tipo. 
  
## <a name="see-also"></a>Confira também



[FBadProp](fbadprop.md)

