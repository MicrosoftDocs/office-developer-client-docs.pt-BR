---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4ea77023bdc9442325f4af46d23c107e7172ceaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770412"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**Aplica-se a**: Outlook 
  
Cria uma estrutura nomeada que inclui uma estrutura [DTBLEDIT](dtbledit.md) para descrever um controle de edição e o número máximo de caracteres que podem ser inseridos no controle. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Parâmetros

_n_
  
> Número máximo de caracteres que podem ser inseridos no controle de edição.
    
_u_
  
> Nome para a nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedDtblEdit** permite definir um controle de edição quando o número de caracteres enabled é conhecido. A nova estrutura é criada com os seguintes membros: 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Para usar um ponteiro para a estrutura resultante de macro **SizedDtblEdit** como um ponteiro de estrutura **DTBLEDIT** , execute a seguinte projeção: 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>Confira também

- [DTBLEDIT](dtbledit.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

