---
title: Dicas para melhorar o desempenho de tabelas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412510"
---
# <a name="tips-for-better-table-performance"></a>Dicas para melhorar o desempenho de tabelas
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como muitas das operações de tabela podem ser demoradas e não há como indicar o progresso, é útil usar as seguintes técnicas para melhorar o desempenho:
  
- **Fazer [chamadas IMAPITable : IUnknown](imapitableiunknown.md) na ordem correta**
    
   Clientes e provedores de serviços podem trabalhar com tabelas de várias maneiras. Eles podem abrir a tabela e recuperar os dados de todas as linhas usando o conjunto de colunas padrão e a ordem de classificação. Como alternativa, eles podem modificar esse modo de exibição padrão da tabela alterando o conjunto de colunas, alterando a ordem de classificação ou estabelecendo uma restrição para restringir o escopo da tabela. Os usuários de tabela que pretendem executar uma ou mais dessas operações antes de recuperar dados devem es performá-los na seguinte ordem:
    
    1. Defina um conjunto de colunas [com IMAPITable::SetColumns](imapitable-setcolumns.md).
        
    2. Estabeleça uma [restrição com IMAPITable::Restrict](imapitable-restrict.md).
        
    3. Defina uma ordem de classificação com [IMAPITable::SortTable](imapitable-sorttable.md).
    
    A execução dessas tarefas nesta ordem limita o número de linhas e colunas que serão ordenadas, melhorando assim o desempenho.
    
- **Atrasar uma operação usando o sinalizador de TBL_BATCH, se possível**
    
    Definir o sinalizador BATCH TBL em um método permite que o implementador de tabela colete várias chamadas antes de \_ agir em qualquer uma delas. Em vez de fazer potencialmente muitas chamadas para um servidor remoto; um implementador de tabela pode fazer uma, executando todas as operações de uma só vez. Os resultados das operações não são avaliados até que sejam necessários. 
    
    Por exemplo, quando um cliente chama [IMAPITable::Restrict](imapitable-restrict.md) para especificar uma restrição com o sinalizador BATCH TBL definido, a restrição não precisa entrar em vigor até que o cliente chama \_ [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar os dados. Isso permite que o implementador de tabela combine o trabalho de duas chamadas em uma. Os usuários de tabela que aproveitam o sinalizador batch TBL devem estar cientes de que o tratamento de erros \_ sob essas condições pode ser mais complexo. 
    
    Como a manipulação dos erros de uma operação atrasada é semelhante a lidar com os erros quando o sinalizador mapi DEFERRED_ERRORS está definido, consulte Adiar erros mapi para obter \_ mais informações. [](deferring-mapi-errors.md) 
    
- **Manter um cache de propriedades comumente usadas**
    
    Os provedores de serviços que implementam tabelas podem diminuir o tempo necessário para criar uma exibição armazenando cópias em cache das propriedades de objeto comumente usadas. Manter uma cópia dessas propriedades na memória economiza ter que recuperá-las do objeto sempre que o ponto de vista precisar ser reconstruído.
    
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

