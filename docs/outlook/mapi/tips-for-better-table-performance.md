---
title: Dicas para melhorar o desempenho de tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: da49b4d8251f6b0b69d2ffbf80194943215675e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564161"
---
# <a name="tips-for-better-table-performance"></a>Dicas para melhorar o desempenho de tabela
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como muitas das operações tabela podem ser demoradas e há um meio para indicar o progresso, é útil usar as seguintes técnicas para melhorar o desempenho:
  
- **Tornar [IMAPITable: IUnknown](imapitableiunknown.md) chama na ordem correta**
    
   Clientes e provedores de serviços podem trabalhar com tabelas de várias maneiras. Abra a tabela e recuperar os dados de todas as linhas usando o conjunto de coluna padrão e ordem de classificação. Como alternativa, eles podem modificar este modo de exibição padrão da tabela alterando o conjunto de colunas, alterando a ordem de classificação ou estabelecendo uma restrição para restringir o escopo da tabela. Os usuários da tabela que pretende executar uma ou mais dessas operações antes de recuperar qualquer dado devem realizá-las na seguinte ordem:
    
    1. Defina uma coluna definidas com [IMAPITable::SetColumns](imapitable-setcolumns.md).
        
    2. Estabeleça uma restrição com [IMAPITable:: Restrict](imapitable-restrict.md).
        
    3. Defina uma ordem de classificação com [IMAPITable:: SortTable](imapitable-sorttable.md).
    
    Execução dessas tarefas nesta ordem limita o número de linhas e colunas que serão classificadas, melhorando o desempenho.
    
- **Atraso de uma operação usando o sinalizador TBL_BATCH se possível**
    
    A definição de tabela\_sinalizador de LOTE em um método permite que o implementador de tabela coletar várias chamadas antes de agir em qualquer um deles. Em vez de fazer chamadas potencialmente muitos para um servidor remoto. implementador uma tabela pode tornar um, realizando todas as operações de uma só vez. Os resultados das operações não são avaliados até que eles sejam necessários. 
    
    Por exemplo, quando um cliente chama [IMAPITable:: Restrict](imapitable-restrict.md) para especificar uma restrição com a tabela\_LOTE sinalizador definido, a restrição não precisa entram em vigor até que o cliente chama [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar os dados. Isso permite que o implementador de tabela combinar o trabalho de duas chamadas para um. Tabela de usuários que se beneficiam da tabela\_sinalizador de LOTE deve estar ciente de que o tratamento sob estas condições de erro pode ser mais complexo. 
    
    Como tratando os erros de uma operação atrasada é semelhante ao tratamento de erros quando MAPI\_DEFERRED_ERRORS sinalizador estiver definido, consulte [Adiar erros de MAPI](deferring-mapi-errors.md) para obter mais informações. 
    
- **Manter um cache de propriedades comumente usadas**
    
    Provedores de serviços de implementação de tabelas podem diminuir o tempo que leva para criar um modo de exibição armazenando em cache cópias das propriedades do objeto comumente usadas. Manter uma cópia dessas propriedades em gravações de memória precisar recuperá-las a partir do objeto cada vez que o modo de exibição deve ser recriado.
    
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

