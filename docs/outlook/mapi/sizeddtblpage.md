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
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407442"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura nomeada que inclui uma estrutura [DTBLPAGE](dtblpage.md) para descrever um controle de página com guias, um rótulo de um tamanho especificado e uma entrada de arquivo de ajuda de um comprimento especificado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Estrutura relacionada:  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Parâmetros

_n_
  
> Comprimento do rótulo da guia de página.
    
_N1_
  
> Comprimento da entrada que aparece no arquivo MAPISVC. inf que identifica o arquivo de ajuda que será usado com o controle de página com guias.
    
_u_
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedDtblPage** permite que você defina um controle de página com guias quando o número de caracteres no rótulo associado e entrada de arquivo de ajuda for conhecido. A nova estrutura é criada com os seguintes membros: 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Para usar um ponteiro para a estrutura resultante da macro **SizedDtblPage** como um ponteiro de estrutura **DTBLPAGE** , execute a seguinte conversão: 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>Confira também

- [DTBLPAGE](dtblpage.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

