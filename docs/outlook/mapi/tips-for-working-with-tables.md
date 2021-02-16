---
title: Dicas para trabalhar com tabelas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439734"
---
# <a name="tips-for-working-with-tables"></a>Dicas para trabalhar com tabelas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Trabalhar com uma tabela MAPI é um pouco parecido com trabalhar com uma tabela de banco de dados relacional. Um usuário pode limitar o número de linhas e colunas no modo de exibição e especificar sua ordem. As linhas podem ser recuperadas uma de cada vez ou em grupos. Um cursor que mantém o controle da posição atual pode ser movido para um local específico na tabela. 
  
Para trabalhar com tabelas, os clientes usam a interface somente leitura, [IMAPITable : IUnknown](imapitableiunknown.md), enquanto provedores de serviços, dependendo se eles são os próprios dados nos quais a tabela se baseia, podem usar **IMAPITable** ou [ITableData : IUnknown](itabledataiunknown.md). As operações definidas nessas interfaces podem ser categorizadas como operações que todos os usuários de tabelas fazem ou podem invocar e operações que não são tão amplamente usadas porque são mais avançadas. Algumas das operações avançadas são mais complexas de implementar; outros não são mais complexos, mas são de interesse para uma pequena minoritária dos componentes MAPI. 
  
As operações mais comuns são:
  
- Operações de coluna, que afetam colunas individuais. Isso inclui especificar as propriedades a serem incluídas no conjunto de colunas e a ordem em que elas devem ser incluídas.
    
- Operações de linha, que afetam linhas simples. Isso inclui a recuperação de dados e as operações de manutenção: adição, exclusão e modificação de uma única linha ou linha.
    
- Operações globais, que afetam a tabela inteira. Isso inclui notificação de evento, pesquisa e classificação.
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

