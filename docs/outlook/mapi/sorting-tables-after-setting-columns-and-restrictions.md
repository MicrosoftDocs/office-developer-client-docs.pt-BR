---
title: Classificar tabelas depois de configurar colunas e restrições
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9e75143cb59e782993b9a7f9937432f0b4894d5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770480"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Classificar tabelas depois de configurar colunas e restrições

  
  
**Aplica-se a**: Outlook 
  
Quando você precisa limitar o modo de exibição de uma tabela classificado, sempre verifique as seguintes chamadas **IMAPITable** na seguinte ordem: 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) para definir o conjunto de coluna. 
    
2. [IMAPITable:: Restrict](imapitable-restrict.md) para impor a restrição. 
    
3. [IMAPITable:: SortTable](imapitable-sorttable.md) para executar a classificação. 
    
Se a tabela classificada é categorizada, fazer uma chamada para [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), se necessário, após a chamada **SortTable** . Essa classificação de chamadas é importante, porque a maioria dos provedores de serviço classificar uma tabela como a última tarefa para obter o melhor desempenho. Se, por exemplo, um provedor de armazenamento de mensagem deve categorizar a uma tabela de conteúdo de pasta antes de uma restrição pode ser imposta, essa classificação será removida durante o processamento da restrição. Uma segunda categorização será necessária. 
  

