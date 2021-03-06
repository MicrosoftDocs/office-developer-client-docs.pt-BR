---
title: Classificar tabelas após definir colunas e restrições
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409878"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Classificar tabelas após definir colunas e restrições

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando você precisar limitar o modo de exibição de uma tabela ordenada, sempre faça as seguintes chamadas **IMAPITable** na seguinte ordem: 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) para definir o conjunto de colunas. 
    
2. [IMAPITable::Restrict](imapitable-restrict.md) para impor a restrição. 
    
3. [IMAPITable::SortTable](imapitable-sorttable.md) para executar a classificação. 
    
Se a tabela classificada for categorizada, faça uma chamada para [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), se necessário, após a **chamada sorttable.** Essa ordem de chamadas é importante porque a maioria dos provedores de serviços classificar uma tabela como a última tarefa para obter o melhor desempenho. Se, por exemplo, um provedor de armazenamento de mensagens tiver que categorizar uma tabela de conteúdo de pasta antes que uma restrição possa ser imposta, essa categorização será removida durante o processamento da restrição. Uma segunda categorização será necessária. 
  

