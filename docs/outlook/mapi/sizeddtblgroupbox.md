---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a3d8a76905aa9abb0e5bf001688608e03446704a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770420"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**Aplica-se a**: Outlook 
  
Cria uma estrutura nomeada que inclui uma estrutura [DTBLGROUPBOX](dtblgroupbox.md) para descrever um controle de caixa de grupo e um rótulo de um comprimento especificado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>Parâmetros

_n_
  
> Comprimento do rótulo da caixa de grupo. 
    
_u_
  
> Nome para a nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedDtblGroupBox** permite definir um controle de caixa de grupo quando o comprimento do rótulo é conhecido. A nova estrutura é criada com os seguintes membros: 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

Para usar um ponteiro para a estrutura resultante de macro **SizedDtblGroupBox** como um ponteiro de estrutura **DTBLGROUPBOX** , execute a seguinte projeção: 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>Confira também

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

