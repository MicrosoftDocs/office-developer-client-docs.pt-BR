---
title: Correlação de TNEF em gateways e transporte X.400
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e08f16ff60a282f1be3adf93d858471e38d19957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406371"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a>Correlação de TNEF em gateways e transporte X.400

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gateways e transporte que se conectam a sistemas baseados em X.400 usam o valor do atributo IM_THIS_IPM X.400 e o atributo **TNEF attMessageID** para implementar a correlação TNEF. 
  
O valor do IM_THIS_IPM atributo da mensagem de saída é copiado para **attMessageID** no fluxo TNEF. O IM_THIS_IPM atributo X.400 normalmente é uma cadeia de caracteres, enquanto o atributo **TNEF attMessageID** é uma cadeia de caracteres de dígitos hexadecimais que representam um valor binário. Portanto, cada caractere no atributo IM_THIS_IPM X.400, incluindo o caractere nulo de encerramento, deve ser convertido em uma cadeia hexadecimal de 2 caracteres representando o valor ASCII desse caractere. Por exemplo, se o IM_THIS_IPM atributo X.400 for a seguinte cadeia de caracteres: 
  
3030322D3030312D305337533A3A3A3936303631312D31353373030
  
em seguida, o **valor de attMessageID** seria a seguinte sequência de dígitos hexadecimais: 
  
33 30 33 30 33 32 32 44
  
33 30 33 30 33 31 32 44
  
33 30 35 33 33 37 35 33
  
33 41 33 41 33 39 33 36
  
33 30 33 36 33 31 33 31
  
32 44 33 31 33 35 33 33
  
33 37 33 30 33 30 00
  
Essa técnica é usada pelo Conector X.400 do Microsoft Exchange Server. Essa técnica deve ser usada por gateways e transporte X.400 que se conectam ao Microsoft Exchange Server para maximizar a interoperabilidade.
  
Para maior compatibilidade com o futuro, bem como com o software microsoft atual, o atributo IM_THIS_IPM X.400 também deve ser copiado para a propriedade **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) . No entanto, **como PR_TNEF_CORRELATION_KEY** é uma propriedade binária, nenhuma conversão em uma cadeia de caracteres hexadecimal é necessária. 
  

