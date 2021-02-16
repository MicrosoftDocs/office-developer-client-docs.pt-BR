---
title: Trabalhando com colunas de múltiplos valores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420182"
---
# <a name="working-with-multivalued-columns"></a>Trabalhando com colunas de múltiplos valores

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma coluna de múltiplos valores contém os dados de uma propriedade de múltiplos valores, que é uma propriedade que tem uma matriz de valores do tipo base em vez de um único valor. Como nenhuma das tabelas inclui propriedades de múltiplos valores em seus conjuntos de colunas padrão, as propriedades de valores múltiplos são incluídas em uma tabela somente se o usuário da tabela solicitar. 
  
Colunas de múltiplos valores podem ser exibidas em tabelas:
  
- Em uma única linha, com todos os valores de propriedade aparecendo na instância de coluna única. É o padrão.
    
    - Ou -
    
- Em uma série de linhas, com uma linha para cada um dos valores de propriedade. Cada valor exclusivo aparece na coluna em sua própria linha, com tantas linhas quanto valores na propriedade de múltiplos valores. Cada linha tem um valor exclusivo para a **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), mas os mesmos valores para as outras colunas. Se uma linha contiver mais de uma coluna com vários valores, por exemplo, duas colunas com valores  _M_ e  _N_ respectivamente, as instâncias  _M \* N_ da linha aparecerão na tabela. 
    
Um usuário de tabela solicita o tipo não padrão de exibição chamando o método [IMAPITable::SetColumns](imapitable-setcolumns.md) com o sinalizador MVI_FLAG definido no tipo de propriedade da coluna de vários valores. O MVI_FLAG sinalizador é uma constante definida como resultado da combinação dos sinalizadores MV_FLAG e MV_INSTANCE com uma operação **OR** lógica. Além de ser usado em **SetColumns**, MVI_FLAG também pode ser passado para [IMAPITable::SortTable](imapitable-sorttable.md) no parâmetro _lpSortCriteria_ e [IMAPITable::Restrict](imapitable-restrict.md) no **membro ulPropTag** do parâmetro _lpRestriction._ Quando passada a MVI_FLAG, **SortTable** tem um desempenho semelhante a **SetColumns**, adicionando uma linha para cada valor na coluna de vários valores e classificação nos valores individuais nas instâncias. Uma linha é adicionada para cada valor. 
  
 **Restringir**, no entanto, não expande a coluna de múltiplos valores em linhas computadas adicionais. Uma coluna de vários valores com o conjunto MVI_FLAG instrui o provedor de serviços a usar essa coluna para restringir a tabela. Se houver um valor de propriedade na restrição, deverá ser uma marca de propriedade de valor único idêntica à que seria retornada por [IMAPITable::QueryRows](imapitable-queryrows.md) para a coluna. 
  
Implementadores de tabela só são necessários para dar suporte ao tipo padrão de exibição e podem retornar o valor MAPI_E_TOO_COMPLEX quando um chamador solicita a outra alternativa. A capacidade de dar suporte a ambos os tipos de exibição é mais importante para provedores de armazenamento de mensagens que implementam tabelas de conteúdo de pastas. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

