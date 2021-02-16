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
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434827"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma matriz de estruturas que descrevem propriedades nomeadas e verifica sua alocação. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>Parâmetros

 _lppNameId_
  
> [in] Ponteiro para uma matriz de [estruturas MAPINAMEID](mapinameid.md) que descrevem as propriedades nomeadas. 
    
 _cNames_
  
> [in] Contagem de estruturas de propriedades nomeadas na matriz apontada pelo _parâmetro lppNameId._ 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> Uma ou mais das estruturas de nome de propriedade especificadas são inválidas. 
    
FALSE 
  
> Todas as estruturas de nome de propriedade especificadas são válidas.
    
## <a name="remarks"></a>Comentários

A **função FBadRglpNameID** pode ser usada ao configurar uma chamada para [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). 
  

