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
ms.openlocfilehash: de92a1328eb9a089a7914978ab20ab0bf5c430ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581955"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de subsites do objeto que é usada para filtrar as linhas de anexo de uma mensagem ou tabela de destinatários.
  
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
  
> Tipo de objeto sub-recurso para servir como o destino para a restrição. Os valores possíveis são: 
    
PR_MESSAGE_RECIPIENTS 
  
> Aplica a restrição a tabela de destinatário da mensagem. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Aplica a restrição a tabela de anexos da mensagem. 
    
 **lpRes**
  
> Ponteiro para uma estrutura [SRestriction](srestriction.md) . 
    
## <a name="remarks"></a>Comentários

Restrições do objeto sub-recurso não são compatíveis com todas as tabelas. Normalmente, tabelas de conteúdo da pasta somente e pastas de resultados de pesquisa dão suporte a eles. Por exemplo, restrições de objeto sub-recurso são usadas para localizar uma mensagem que tenha um tipo de anexo ou um destinatário específico. 
  
Se uma implementação não oferece suporte a restrições do objeto subsites, ele retornará MAPI_E_TOO_COMPLEX de seus métodos [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md) . 
  
Para obter uma discussão geral de como funcionam os restrições, consulte [Sobre restrições](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)

