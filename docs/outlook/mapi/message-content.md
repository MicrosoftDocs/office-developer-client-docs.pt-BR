---
title: Conteúdo da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 85bd3f7db53f195295405fb0b02c25f084786a67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586078"
---
# <a name="message-content"></a>Conteúdo da mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há duas codificações possíveis para o conteúdo da mensagem: um usando MIME, o outro usando uuencode. MIME é a codificação preferencial. Além disso, o MAPI define uma propriedade por destinatário, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), que determina se ou não informações TNEF devem ser incluídas em uma mensagem de saída. Portanto, há um total de quatro maneiras de codificação de conteúdo da mensagem:
  
- MIME com TNEF
    
- MIME sem TNEF
    
- UUENCODE com TNEF
    
- UUENCODE sem TNEF
    
Como escolher MIME ou uuencode para mensagens de saída não for especificado.
  
As seguintes propriedades são excluídas dos TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**. Todas as outras propriedades de mensagem transmittable estão incluídas no fluxo TNEF.
  
As sugestões a seguir servem para fornecer uma lista de parâmetros que a implementação pode decidir como oferecer suporte a:
  
- Se deseja codificar usando MIME ou uuencode para mensagens de saída: booleano.
    
- Conjunto a ser usado para mensagens de saída de caracteres: cadeia de caracteres (copiado diretamente para o parâmetro charset) ou enumeração (traduzido internamente como cadeia de caracteres do conjunto de caracteres).
    

