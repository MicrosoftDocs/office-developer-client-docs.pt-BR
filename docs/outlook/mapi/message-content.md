---
title: Conteúdo da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5e8debcd5a60357f05dfb7b6bde1faf972e50a26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768125"
---
# <a name="message-content"></a>Conteúdo da mensagem

  
  
**Aplica-se a**: Outlook 
  
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
    

