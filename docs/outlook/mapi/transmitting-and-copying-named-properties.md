---
title: Transmitir e copiar propriedades nomeadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6534e7344a62717e406c112249d26407b0852d93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437774"
---
# <a name="transmitting-and-copying-named-properties"></a>Transmitir e copiar propriedades nomeadas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Sempre que uma propriedade nomeada é enviada, movida ou copiada, o nome permanece constante, mas o identificador deve ser alterado para aderir ao mapeamento do objeto de destino. A única exceção a essa regra é quando a origem e o destino têm a mesma assinatura de mapeamento, tornando o remapeamento desnecessário.
  
É responsabilidade do provedor de transporte remapear os nomes das propriedades nomeadas transmitidas para os identificadores apropriados que funcionam no destino. O provedor de transporte de envio não pode saber qual é o mapeamento correto no destino; Ele deve transmitir os nomes e confiar no provedor de transporte de recebimento para mapeá-los para os identificadores que funcionam. A implementação de MAPI do TNEF manipula o remapeamento de propriedades nomeadas para provedores de transporte. Os provedores de transporte podem manipular o remapeamento manualmente ou usar a implementação TNEF. 
  
Um remapeamento semelhante de propriedades nomeadas deve ocorrer quando essas propriedades são copiadas entre repositórios de mensagens. No enTanto, como os provedores de repositórios de mensagens podem recuperar o nome para o mapeamento de identificadores do destino, eles podem remapear as propriedades imediatamente e não precisam depender do repositório de mensagens de destino. 
  
## <a name="see-also"></a>Confira também



[MAPI denominada propriedades](mapi-named-properties.md)

