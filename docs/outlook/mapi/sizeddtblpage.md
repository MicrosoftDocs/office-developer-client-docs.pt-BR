---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a1530443600df7cb73ff27d5cfbeab46f81bc53c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770415"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**Aplica-se a**: Outlook 
  
Cria uma estrutura nomeada que inclui uma estrutura [DTBLPAGE](dtblpage.md) para descrever a um controle de páginas com guias, um rótulo de um comprimento especificado e uma entrada de arquivo de ajuda de um comprimento especificado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Parâmetros

_n_
  
> Comprimento do rótulo para a guia página.
    
_N1_
  
> Comprimento da entrada que aparecem no arquivo Mapisvc que identifica o arquivo de Ajuda que será usado com o controle de página com guias.
    
_u_
  
> Nome para a nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedDtblPage** permite definir um controle de páginas com guias quando o número de caracteres no rótulo associado e entrada de arquivo de Ajuda é conhecido. A nova estrutura é criada com os seguintes membros: 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Para usar um ponteiro para a estrutura resultante de macro **SizedDtblPage** como um ponteiro de estrutura **DTBLPAGE** , execute a seguinte projeção: 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>Confira também

- [DTBLPAGE](dtblpage.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

