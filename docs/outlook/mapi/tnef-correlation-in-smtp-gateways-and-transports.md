---
title: Correlação de TNEF em gateways e transporte SMTP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413665"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Correlação de TNEF em gateways e transporte SMTP

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gateways e transporte que se conectam a sistemas baseados na Internet, aqueles que usam SMTP, usam o valor do header SMTP MessageID e a propriedade **PR_TNEF_CORRELATION_KEY** para implementar a correlação TNEF. 
  
O valor do header MessageID da mensagem de saída deve ser copiado para a propriedade **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) e codificado no atributo [attMAPIProps](attmapiprops.md) do fluxo TNEF. Observe que **PR_TNEF_CORRELATION_KEY** é uma propriedade binária, enquanto MessageID é uma cadeia de caracteres; o terminador nulo deve ser incluído na cópia e na comparação. 
  
Essa técnica é usada por todos os softwares da Microsoft que conectam sistemas de mensagens baseados em MAPI à Internet, como o Microsoft Exchange Server. Essa técnica deve ser usada por gateways SMTP e transporte que se conectam a sistemas que suportam clientes MAPI para maximizar a interoperabilidade.
  

