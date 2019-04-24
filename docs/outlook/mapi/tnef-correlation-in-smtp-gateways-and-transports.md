---
title: Correlação de TNEF em gateways e transportes SMTP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339687"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Correlação de TNEF em gateways e transportes SMTP

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gateways e transportes que se conectam a sistemas baseados na Internet, aqueles que usam SMTP, usam o valor do cabeçalho SMTP MessageID e a propriedade **PR_TNEF_CORRELATION_KEY** para implementar a correlação de TNEF. 
  
O valor do cabeçalho MessageID da mensagem de saída deve ser copiado para a propriedade **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) e codificado no atributo [attMAPIProps](attmapiprops.md) do fluxo TNEF. Observe que **PR_TNEF_CORRELATION_KEY** é uma propriedade binária, enquanto MessageId é uma cadeia de caracteres; o terminador NULL deve ser incluído na cópia e na comparação. 
  
Essa técnica é usada por todos os softwares da Microsoft que conectam sistemas de mensagens baseados em MAPI à Internet, como o Microsoft Exchange Server. Essa técnica deve ser usada por quaisquer gateways SMTP e transportes que se conectam a sistemas que dão suporte a clientes MAPI para maximizar a interoperabilidade.
  

