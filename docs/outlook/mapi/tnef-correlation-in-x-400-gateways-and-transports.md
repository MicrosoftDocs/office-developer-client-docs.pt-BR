---
title: Correlação de TNEF em transportes e gateways X.400
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ea5ca41ef21c72377ade72370e0aee1b313c92d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770602"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a>Correlação de TNEF em transportes e gateways X.400

  
  
**Aplica-se a**: Outlook 
  
Gateways e transportes que se conectam ao sistemas baseados em x. 400, use o valor do atributo IM_THIS_IPM 400 e o atributo TNEF **attMessageID** para implementar correlação TNEF. 
  
O valor do atributo IM_THIS_IPM da mensagem de saída é copiado para **attMessageID** no stream TNEF. O atributo IM_THIS_IPM 400 geralmente é uma cadeia de caracteres, enquanto o atributo TNEF **attMessageID** é uma cadeia de caracteres de dígitos hexadecimais representando um valor binário. Portanto, cada caractere no atributo IM_THIS_IPM 400, incluindo o caractere de terminação null, deve ser convertido em uma sequência de 2 caracteres hexadecimal que representa o valor ASCII do caractere. Por exemplo, se o atributo de x. 400 do IM_THIS_IPM é a cadeia de caracteres a seguir: 
  
3030322D3030312D305337533A3A3936303631312D313533373030
  
em seguida, o valor da **attMessageID** seria a seguinte sequência de dígitos hexadecimais: 
  
33 30 33 30 33 32 32 44
  
33 30 33 30 33 31 32 44
  
33 30 35 33 33 37 35 33
  
33 41 33 41 33 39 33 36
  
33 30 33 36 33 31 33 31
  
32 44 33 31 33 35 33 33
  
33 37 33 30 33 30 00
  
Essa técnica é usada pelo Microsoft Exchange Server x. 400 Connector. Essa técnica deve ser usada por qualquer gateways x. 400 e transportes que se conectar ao Microsoft Exchange Server para maximizar a interoperabilidade.
  
Para melhor compatibilidade com o software Microsoft futuro bem como presente, o atributo IM_THIS_IPM 400 também deve ser copiado para a propriedade **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). No entanto, como **PR_TNEF_CORRELATION_KEY** é uma propriedade binária, nenhuma tradução em uma cadeia de caracteres hexadecimal é necessária. 
  

