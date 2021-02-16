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
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436437"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida todas as cadeias de caracteres em uma matriz de cadeias de caracteres Unicode. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a>Parâmetros

 _lppszW_
  
> [in] Ponteiro para uma matriz de cadeias de caracteres Unicode terminadas por caractere nulo. 
    
 _cStrings_
  
> [in] Contagem de cadeias de caracteres na matriz apontada pelo _parâmetro lppszW._ 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> Uma ou mais cadeias de caracteres na matriz especificada são inválidas. 
    
FALSE 
  
> As cadeias de caracteres na matriz especificada são válidas.
    

