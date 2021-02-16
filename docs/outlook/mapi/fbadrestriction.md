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
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432237"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma restrição usada para limitar um exibição de tabela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>Parâmetros

 _lpres_
  
> [in] Uma [estrutura SRestriction](srestriction.md) definindo a restrição a ser validada. 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> A restrição especificada, ou uma ou mais de suas sub-restrições, é inválida. 
    
FALSE 
  
> A restrição especificada e todas as suas sub-restrições são válidas.
    
## <a name="remarks"></a>Comentários

Depois que uma restrição é validada, ela pode ser passada em chamadas para o método [IMAPITable::Restrict](imapitable-restrict.md) para restringir a tabela a determinadas linhas, para o método [IMAPITable::FindRow](imapitable-findrow.md) para localizar uma linha de tabela e para métodos da interface [IMAPIContainer](imapicontainerimapiprop.md) para executar uma restrição em um objeto contêiner. 
  

