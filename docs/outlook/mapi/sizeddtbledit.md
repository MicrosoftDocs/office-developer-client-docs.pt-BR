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
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437641"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedDtblEdit** permite definir um controle de edição quando o número de caracteres habilitados for conhecido. A nova estrutura é criada com os seguintes membros: 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Para usar um ponteiro para a estrutura resultante da macro **SizedDtblEdit** como um ponteiro de estrutura **DTBLEDIT,** execute a seguinte projeção: 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>Confira também

- [DTBLEDIT](dtbledit.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

