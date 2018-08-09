---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c2e275e373677e50510a0aa87f5060070a870a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770429"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Aplica-se a**: Outlook 
  
Cria uma estrutura nomeada que inclui uma estrutura [DTBLLABEL](dtbllabel.md) para descrever um controle label e o rótulo associado de um comprimento especificado. 
  
|||
|:-----|:-----|
|Especificados no arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Parâmetros

_n_
  
> Comprimento do rótulo. Isso inclui o caractere final de nulo. 
    
_u_
  
> Nome para a nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedDtblLabel** permite definir uma etiqueta de exibição tabela quando o número de caracteres no rótulo é conhecido. A nova estrutura é criada com os seguintes membros: 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Para usar um ponteiro para a estrutura resultante de macro **SizedDtblLabel** como um ponteiro de estrutura **DTBLLABEL** , execute a seguinte projeção: 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>Confira também

- [DTBLLABEL](dtbllabel.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

