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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341031"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma matriz de estruturas que descrevem as propriedades nomeadas e verifica sua alocação. 
  
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
  
> no Ponteiro para uma matriz de estruturas [MAPINAMEID](mapinameid.md) descrevendo as propriedades nomeadas. 
    
 _cNames_
  
> no Contagem de estruturas de propriedade nomeadas na matriz apontada pelo parâmetro _lppNameId_ . 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> Uma ou mais das estruturas de nome de propriedade especificadas são inválidas. 
    
FALSE 
  
> As estruturas de nome de propriedade especificadas são válidas.
    
## <a name="remarks"></a>Comentários

A função **FBadRglpNameID** pode ser usada ao configurar uma chamada para [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md). 
  

