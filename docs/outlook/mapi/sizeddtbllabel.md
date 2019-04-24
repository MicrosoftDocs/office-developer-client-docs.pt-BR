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
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282702"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura nomeada que inclui uma estrutura [DTBLLABEL](dtbllabel.md) para descrever um controle Label e o rótulo associado de um comprimento especificado. 
  
|||
|:-----|:-----|
|Especificado no arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Estrutura relacionada  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Parâmetros

_n_
  
> Comprimento do rótulo. Isso inclui o caractere final nulo. 
    
_u_
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedDtblLabel** permite definir um rótulo de exibição da tabela quando o número de caracteres no rótulo é conhecido. A nova estrutura é criada com os seguintes membros: 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Para usar um ponteiro para a estrutura resultante da macro **SizedDtblLabel** como um ponteiro de estrutura **DTBLLABEL** , execute a seguinte conversão: 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>Confira também

- [DTBLLABEL](dtbllabel.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

