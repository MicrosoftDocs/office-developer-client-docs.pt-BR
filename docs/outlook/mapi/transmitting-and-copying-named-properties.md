---
title: Transmitir e copiar propriedades nomeadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a5d2244270463fcc2fe0a9786112590e741a8a66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770617"
---
# <a name="transmitting-and-copying-named-properties"></a>Transmitir e copiar propriedades nomeadas

  
  
**Aplica-se a**: Outlook 
  
Sempre que uma propriedade nomeada é enviada, movido ou copiadas, o nome permanece constante, mas o identificador deve alterar para cumpram o mapeamento de objeto de destino. A única exceção a essa regra é quando a origem e destino têm a mesma assinatura de mapeamento, tornando o novo mapeamento desnecessária.
  
É responsabilidade do provedor de transporte para remapear os nomes das propriedades nomeadas transmitidos aos identificadores apropriados que funcionam no destino. O provedor de transporte de envio não é possível saber qual é o mapeamento correto no destino; ela deve transmita os nomes e contam com o provedor de transporte de recebimento para mapeá-los aos identificadores que funcionam. A implementação de MAPI do TNEF lida com o novo mapeamento de propriedades nomeadas para provedores de transporte. Provedores de transporte podem lidar com o novo mapeamento manualmente ou usar a implementação de TNEF. 
  
Um novo semelhante mapeamento de propriedades nomeadas deve ocorrer quando essas propriedades são copiadas entre as lojas de mensagem. No entanto, porque os provedores de armazenamento de mensagem podem recuperar o nome para o mapeamento de identificador do destino, podem remapear as propriedades imediatamente e não precisará contam com o armazenamento de mensagens de destino. 
  
## <a name="see-also"></a>Confira também



[MAPI denominada propriedades](mapi-named-properties.md)

