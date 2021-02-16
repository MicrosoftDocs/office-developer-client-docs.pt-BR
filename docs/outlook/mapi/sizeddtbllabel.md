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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408611"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura nomeada que inclui uma estrutura [DTBLLABEL](dtbllabel.md) para descrever um controle label e o rótulo associado de um comprimento especificado. 
  
|||
|:-----|:-----|
|Especificado no arquivo de header:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Parâmetros

_n_
  
> Comprimento do rótulo. Isso inclui o caractere NULL final. 
    
_u_
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedDtblLabel** permite definir um rótulo de tabela de exibição quando o número de caracteres no rótulo for conhecido. A nova estrutura é criada com os seguintes membros: 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Para usar um ponteiro para a estrutura resultante da macro **SizedDtblLabel** como um ponteiro de estrutura **DTBLLABEL,** execute a seguinte projeção: 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>Confira também

- [DTBLLABEL](dtbllabel.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

