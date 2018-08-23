---
title: Chamar QueryRows para tabelas pequenas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 34975677bedccf3f9111985d371e21d482b45584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589333"
---
# <a name="calling-queryrows-for-small-tables"></a>Chamar QueryRows para tabelas pequenas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao recuperar linhas de uma pequena tabela, chame [IMAPITable:: QueryRows](imapitable-queryrows.md) em vez de primeira criando uma restrição. Criar uma restrição afeta o desempenho, pois o provedor deve primeiro criar uma tabela, encontre as linhas correspondentes na tabela original e copie as linhas para a nova tabela. Se o número total de linhas da tabela for menor do que 100, é provavelmente mais efetiva ler todas as linhas e então chamar [IMAPITable:: FindRow](imapitable-findrow.md) para localizar a linha apropriada. Essa é uma estratégia de particularmente boa se essa informação é necessária somente ocasionalmente. 
  
O tempo adequado para usar uma restrição é quando as informações restritas ou filtradas serão usadas por um período maior de tempo ou usadas frequentemente. Por exemplo, se você sempre precisa de um modo de exibição com mensagens não lidas, uma restrição é a chamada adequada para usar.
  

