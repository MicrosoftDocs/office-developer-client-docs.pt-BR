---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406322"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de subpro objecto que é usada para filtrar as linhas da tabela de anexos ou destinatários de uma mensagem.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a>Members

 **ulSubObject**
  
> Tipo de subpro objecto a ser usado como o destino da restrição. Os valores possíveis são: 
    
PR_MESSAGE_RECIPIENTS 
  
> Aplicar a restrição à tabela de destinatários de uma mensagem. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Aplicar a restrição à tabela de anexos de uma mensagem. 
    
 **lpRes**
  
> Ponteiro para uma [estrutura SRestriction.](srestriction.md) 
    
## <a name="remarks"></a>Comentários

As restrições de subpro object não são suportadas por todas as tabelas. Normalmente, apenas as tabelas de conteúdo de pastas e as pastas de resultados de pesquisa têm suporte para elas. Por exemplo, restrições de subpro object são usadas para encontrar uma mensagem que tenha um tipo específico de anexo ou destinatário. 
  
Se uma implementação não suportar restrições de subpro object, ela retornará MAPI_E_TOO_COMPLEX de seus métodos [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow.](imapitable-findrow.md) 
  
Para uma discussão geral sobre como funcionam as restrições, consulte [Sobre restrições.](about-restrictions.md) 
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)

