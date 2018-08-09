---
title: Dicas para trabalhar com tabelas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 451bab57d4e2e8669a25d119f9ce28a8f78e628f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770591"
---
# <a name="tips-for-working-with-tables"></a>Dicas para trabalhar com tabelas

  
  
**Aplica-se a**: Outlook 
  
Trabalhando com um MAPI tabela é um pouco semelhante a trabalhar com uma tabela de banco de dados relacional. Um usuário pode limitar o número de linhas e colunas no modo de exibição e especifique sua ordem. Linhas podem ser recuperados de um por vez ou em grupos. Um cursor que controla a posição atual pode ser movido para um local específico na tabela. 
  
Para trabalhar com tabelas, os clientes usam a interface de somente leitura, [IMAPITable: IUnknown](imapitableiunknown.md), enquanto os provedores de serviço, dependendo se eles possuem os dados que a tabela for baseada em, podem usar qualquer um dos **IMAPITable** ou [ITableData: IUnknown](itabledataiunknown.md). As operações definidas nessas interfaces podem ser categorizadas como operações que todos os usuários das tabelas tenham ou podem chamar e operações que não são usadas como amplamente porque eles são mais avançados. Algumas das operações avançadas são mais complexas de implementar; outras pessoas não mais complexas, mas são de interesse para uma pequena minoria dos componentes MAPI. 
  
Operações mais comuns são:
  
- Operações de coluna, que afetam o única colunas. Eles incluem especificando as propriedades a serem incluídos no conjunto de colunas e a ordem em que eles devem ser incluídos.
    
- Operações de linha, que afetam o única linhas. Eles incluem as operações de manutenção e recuperação de dados: adição, exclusão e modificação de uma única linha ou linhas.
    
- Operações globais, que afetam a tabela inteira. Isso inclui a notificação de evento, pesquisa e classificação.
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

