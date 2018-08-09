---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3de56b12fa7d34004fddbfe3633b8b8307c0ffc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770405"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**Aplica-se a**: Outlook 
  
Cria uma estrutura nomeada que inclui uma estrutura [DTBLBUTTON](dtblbutton.md) para descrever um botão e um rótulo de um comprimento especificado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>Parâmetros

 _n_
  
> Comprimento do rótulo a ser incluído na nova estrutura.
    
 _u_
  
> Nome para a nova estrutura.
    
## <a name="remarks"></a>Comentários

A nova estrutura é criada com os seguintes membros:
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>Confira também



[DTBLBUTTON](dtblbutton.md)


[Macros relacionadas a estruturas](macros-related-to-structures.md)

