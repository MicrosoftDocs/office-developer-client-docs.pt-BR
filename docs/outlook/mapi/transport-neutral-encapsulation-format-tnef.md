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
ms.openlocfilehash: 34b64df25cb2f7f591f7c799dec957a0072840dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770624"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Transport Neutral Encapsulation Format (TNEF)

 
  
**Aplica-se a**: Outlook 
  
TNEF é um formato para converter um conjunto de propriedades MAPI — uma mensagem MAPI — em um fluxo de dados serial. As funções TNEF são usadas principalmente pelos provedores de transporte que precisa codificar propriedades de mensagem MAPI para transmissão através de um sistema de mensagens que não oferece suporte a essas propriedades diretamente. Por exemplo, um transporte baseados em SMTP usa o TNEF para codificar propriedades como **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), que não possuem representações diretas na estrutura de uma mensagem de SMTP.
  
A implementação de TNEF define vários atributos específicos TNEF, cada uma delas corresponde a uma determinada propriedade MAPI. Esses atributos são usados para codificar suas respectivas propriedades MAPI no fluxo TNEF. Além disso, um atributo especial é definido que pode ser usado para encapsular qualquer propriedade MAPI que não tem um atributo específico correspondente a ela. O motivo pelo qual esses atributos forem definidos — em vez de simplesmente usar um método para todas as propriedades MAPI de codificação de uniforme — é permitir a compatibilidade com versões anteriores com o software não compatível com MAPI que está usando o TNEF.
  
O restante desta seção descreve a estrutura e a sintaxe de um stream TNEF, o mapeamento entre propriedades MAPI e atributos TNEF e considerações importantes sobre determinados atributos TNEF.
  

