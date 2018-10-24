---
title: Correlação de TNEF em transportes e gateways SMTP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8192646007e8935a750a70e46b8210eebbc353f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578532"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Correlação de TNEF em transportes e gateways SMTP

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gateways e transportes que se conectam à internet com base em sistemas, aqueles que usam SMTP, use o valor das propriedades de cabeçalho SMTP MessageID e **PR_TNEF_CORRELATION_KEY** implementar correlação TNEF. 
  
O valor do cabeçalho da mensagem de saída MessageID deve ser copiado para a propriedade **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) e codificado no atributo [attMAPIProps](attmapiprops.md) do stream TNEF. Observe que **PR_TNEF_CORRELATION_KEY** é uma propriedade binária, enquanto o MessageID é uma cadeia de caracteres; o terminador null deve ser incluído na cópia e na comparação. 
  
Essa técnica é usada pelo software da Microsoft que se conecta com base em MAPI de sistemas de mensagens da Internet, como o Microsoft Exchange Server. Essa técnica deve ser usada por qualquer gateways de SMTP e transportes que se conectam aos sistemas que oferecem suporte a clientes MAPI para maximizar a interoperabilidade.
  

