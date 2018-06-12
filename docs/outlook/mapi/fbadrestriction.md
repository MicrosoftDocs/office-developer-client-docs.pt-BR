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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 43e0d8d28836b3114ab2029bc1f241197c569ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766532"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="parameters"></a>Par�metros

 _lpres_
  
> [in] Uma estrutura de [SRestriction](srestriction.md) definindo a restrição a ser validado. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> A restrição especificada, ou uma ou mais das suas subrestrictions, são inválido. 
    
FALSO 
  
> A restrição especificada e todos os seus subrestrictions são válidos.
    
## <a name="remarks"></a>Coment�rios

Depois que uma restrição é validada, ela poderá ser passada em chamadas para o método [IMAPITable:: Restrict](imapitable-restrict.md) para restringir a tabela para determinadas linhas, para o método [IMAPITable:: FindRow](imapitable-findrow.md) para localizar uma linha da tabela e para os métodos do [IMAPIContainer](imapicontainerimapiprop.md) interface para realizar uma restrição em um objeto container. 
  

