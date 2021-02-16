---
title: Transport Neutral Encapsulation Format (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Última modificação: 12 de março de 2013'
ms.openlocfilehash: d902039fa1081e30947ddd8f70ead9ae7acec06a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428687"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Transport Neutral Encapsulation Format (TNEF)

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O TNEF é um formato para converter um conjunto de propriedades MAPI — uma mensagem MAPI — em um fluxo serial de dados. As funções TNEF são usadas principalmente por provedores de transporte que precisam codificar propriedades de mensagens MAPI para transmissão por meio de um sistema de mensagens que não suporta essas propriedades diretamente. Por exemplo, um transporte baseado em SMTP usa TNEF para codificar propriedades como **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), que não têm representações diretas na estrutura de uma mensagem SMTP.
  
A implementação do TNEF define vários atributos específicos do TNEF, cada um deles corresponde a uma propriedade MAPI específica. Esses atributos são usados para codificar suas respectivas propriedades MAPI no fluxo TNEF. Além disso, um atributo especial é definido que pode ser usado para encapsular qualquer propriedade MAPI que não tenha um atributo específico correspondente a ela. O motivo pelo qual esses atributos são definidos — em vez de simplesmente usar um método de codificação uniforme para todas as propriedades MAPI — é habilitar a compatibilidade com MAPI com software que está usando TNEF.
  
O restante desta seção descreve a estrutura e a sintaxe de um fluxo TNEF, o mapeamento entre propriedades MAPI e atributos TNEF e considerações importantes para determinados atributos TNEF.
  

