---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766528"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Aplica-se a**: Outlook 
  
Valida todas as cadeias de caracteres em uma matriz de cadeias de caracteres Unicode. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a>Parâmetros

 _lppszW_
  
> [in] Ponteiro para uma matriz de cadeias de caracteres de Unicode terminada em nulo. 
    
 _cStrings_
  
> [in] Contagem de cadeias de caracteres na matriz apontado pelo parâmetro _lppszW_ . 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> Um ou mais das cadeias de caracteres na matriz especificada são inválidos. 
    
FALSO 
  
> As cadeias de caracteres na matriz especificada são válidas.
    

