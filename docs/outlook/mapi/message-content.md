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
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435457"
---
# <a name="message-content"></a>Conteúdo da mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há duas codificações possíveis para o conteúdo da mensagem: uma usando MIME, a outra usando Uuencode. MIME é a codificação preferencial. Além disso, o MAPI define uma propriedade por destinatário, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), que controla se as informações de TNEF devem ou não ser incluídas em uma mensagem de saída. Portanto, há um total de quatro maneiras de codificar o conteúdo da mensagem:
  
- MIME com TNEF
    
- MIME sem TNEF
    
- uuencode com TNEF
    
- uuencode sem TNEF
    
Como escolher MIME ou UUENCODE para mensagens de saída não é especificado.
  
As propriedades a seguir são excluídas do TNEF: **\*PR_SENDER_**, **PR_ATTACH_DATA_\***, **PR_BODY**. Todas as outras propriedades de mensagens de transmittable estão incluídas no fluxo TNEF.
  
As sugestões a seguir destinam-se a fornecer uma lista de parâmetros que a implementação pode decidir como oferecer suporte:
  
- Se deve ser codificada usando MIME ou UUENCODE para mensagens de saída: Boolean.
    
- Conjunto de caracteres a ser usado para mensagens de saída: cadeia de caracteres (copiado diretamente para o parâmetro charset) ou enumeração (traduzido internamente para a cadeia de caracteres charset).
    

