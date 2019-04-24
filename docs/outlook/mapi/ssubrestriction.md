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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336411"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de subobjeto que é usada para filtrar as linhas da tabela de associação ou de destinatário de uma mensagem.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a>Members

 **ulSubObject**
  
> Tipo de subobjeto a ser usado como o destino para a restrição. Os valores possíveis são os seguintes: 
    
PR_MESSAGE_RECIPIENTS 
  
> Aplicar a restrição à tabela de destinatários de uma mensagem. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Aplicar a restrição à tabela de anexos de uma mensagem. 
    
 **lpRes**
  
> Ponteiro para uma estrutura [SRestriction](srestriction.md) . 
    
## <a name="remarks"></a>Comentários

As restrições de subobjeto não são suportadas por todas as tabelas. Normalmente, apenas as pastas de conteúdo da pasta e de resultados de pesquisa dão suporte a elas. Por exemplo, as restrições de subobjeto são usadas para localizar uma mensagem que tem um tipo específico de anexo ou destinatário. 
  
Se uma implementação não oferecer suporte a restrições de subobjeto, ela retornará MAPI_E_TOO_COMPLEX de seus métodos imApitable: [: Restrict](imapitable-restrict.md) ou IMAPITable [:: FindRow](imapitable-findrow.md) . 
  
Para uma discussão geral de como as restrições funcionam, consulte [about Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)

