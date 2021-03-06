---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420805"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura nomeada que inclui uma [estrutura DTBLCHECKBOX](dtblcheckbox.md) para descrever um controle de caixa de seleção e um rótulo de um comprimento especificado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>Parâmetros

_n_
  
> Comprimento do rótulo a ser incluído na nova estrutura.
    
_u_
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedDtblCheckBox** permite definir uma caixa de seleção quando o número de caracteres de rótulo é conhecido. A nova estrutura é criada com os seguintes membros: 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

Para usar um ponteiro para a estrutura resultante da macro **SizedDtblCheckBox** como um ponteiro de **estrutura DTBLCHECKBOX,** execute a seguinte projeção: 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>Confira também

- [DTBLCHECKBOX](dtblcheckbox.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

