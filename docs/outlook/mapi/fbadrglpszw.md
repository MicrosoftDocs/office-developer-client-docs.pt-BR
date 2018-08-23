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
ms.openlocfilehash: 3b3b6b5ca0b06fc55a60e035ffd9118391cab8f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565911"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
    

