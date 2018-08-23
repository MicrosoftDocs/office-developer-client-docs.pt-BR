---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3d729e2a12ee19ee3aa4ded71263697eb739f154
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566303"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma restrição usada para limitar a um modo de exibição de tabela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>Parâmetros

 _lpres_
  
> [in] Uma estrutura de [SRestriction](srestriction.md) definindo a restrição a ser validado. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> A restrição especificada, ou uma ou mais das suas subrestrictions, são inválido. 
    
FALSO 
  
> A restrição especificada e todos os seus subrestrictions são válidos.
    
## <a name="remarks"></a>Comentários

Depois que uma restrição é validada, ela poderá ser passada em chamadas para o método [IMAPITable:: Restrict](imapitable-restrict.md) para restringir a tabela para determinadas linhas, para o método [IMAPITable:: FindRow](imapitable-findrow.md) para localizar uma linha da tabela e para os métodos do [IMAPIContainer](imapicontainerimapiprop.md) interface para realizar uma restrição em um objeto container. 
  

