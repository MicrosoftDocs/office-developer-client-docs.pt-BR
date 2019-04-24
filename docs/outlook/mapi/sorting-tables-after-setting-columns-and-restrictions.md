---
title: Classificar tabelas após a definição de colunas e restrições
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344482"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Classificar tabelas após a definição de colunas e restrições

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando você precisa limitar o modo de exibição de uma tabela classificada, sempre faça **** as seguintes chamadas imapitadas na seguinte ordem: 
  
1. [IMAPITable::](imapitable-setcolumns.md) SetColumns para definir o conjunto de colunas. 
    
2. [IMAPITable:: strict](imapitable-restrict.md) para impor a restrição. 
    
3. [IMAPITable:: SortTable](imapitable-sorttable.md) para executar a classificação. 
    
Se a tabela classificada for categorizada, faça uma chamada para imApitable [::](imapitable-setcollapsestate.md)setcollapsestate, se necessário **** , após a chamada SortTable. Essa ordenação de chamadas é importante porque a maioria dos provedores de serviços classifica uma tabela como a última tarefa para obter o melhor desempenho. Se, por exemplo, um provedor de repositório de mensagens deve categorizar uma tabela de conteúdo da pasta antes que uma restrição possa ser imposta, essa categorização será removida durante o processamento da restrição. Uma segunda categorização será necessária. 
  

