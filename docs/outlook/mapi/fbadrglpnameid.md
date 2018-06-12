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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 3f04c5be240f63d35ea8dba0f7abbf1085f2a41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766526"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="parameters"></a>Par�metros

 _lppNameId_
  
> [in] Ponteiro para uma matriz de estruturas [MAPINAMEID](mapinameid.md) descrevendo as propriedades nomeadas. 
    
 _cNames_
  
> [in] Contagem de estruturas de propriedade nomeada na matriz apontado pelo parâmetro _lppNameId_ . 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> Um ou mais das estruturas de nome de propriedade especificado são inválido. 
    
FALSO 
  
> As estruturas de nome de propriedade especificado são válidas.
    
## <a name="remarks"></a>Coment�rios

A função **FBadRglpNameID** pode ser usada ao configurar para uma chamada para [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). 
  

