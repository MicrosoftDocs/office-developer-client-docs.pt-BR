---
title: Chamando QueryRows para tabelas pequenas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404173"
---
# <a name="calling-queryrows-for-small-tables"></a>Chamando QueryRows para tabelas pequenas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao recuperar linhas de uma tabela pequena, chame [IMAPITable::QueryRows](imapitable-queryrows.md) em vez de primeiro criar uma restrição. A criação de uma restrição afeta o desempenho porque o provedor deve primeiro criar uma tabela, encontrar as linhas correspondentes na tabela original e, em seguida, copiar as linhas para a nova tabela. Se o número total de linhas na tabela for menor que 100, provavelmente será mais eficaz ler todas as linhas e, em seguida, chamar [IMAPITable::FindRow](imapitable-findrow.md) para encontrar a linha apropriada. Essa é uma estratégia particularmente boa se essas informações só são necessárias ocasionalmente. 
  
O momento adequado para usar uma restrição é quando as informações restritas ou filtradas serão usadas por um período mais longo ou usadas com frequência. Por exemplo, se você sempre precisar de uma exibição com mensagens não lidas, uma restrição será a chamada adequada a ser usada.
  

