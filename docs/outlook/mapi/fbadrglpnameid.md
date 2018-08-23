---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96dddc438df67b76f854827eab4dc3e210523243
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588143"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma matriz de estruturas que descrevem propriedades nomeadas e verifica sua alocação. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>Parâmetros

 _lppNameId_
  
> [in] Ponteiro para uma matriz de estruturas [MAPINAMEID](mapinameid.md) descrevendo as propriedades nomeadas. 
    
 _cNames_
  
> [in] Contagem de estruturas de propriedade nomeada na matriz apontado pelo parâmetro _lppNameId_ . 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> Um ou mais das estruturas de nome de propriedade especificado são inválido. 
    
FALSO 
  
> As estruturas de nome de propriedade especificado são válidas.
    
## <a name="remarks"></a>Comentários

A função **FBadRglpNameID** pode ser usada ao configurar para uma chamada para [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). 
  

