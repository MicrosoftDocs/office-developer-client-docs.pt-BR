---
title: Trabalhar com colunas com vários valores
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
# <a name="working-with-multivalued-columns"></a>Trabalhar com colunas com vários valores

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma coluna com vários valores contém os dados de uma propriedade com vários valores, que é uma propriedade que tem uma matriz de valores do tipo base em vez de um único valor. Como nenhuma das tabelas inclui propriedades com vários valores em seus conjuntos de colunas padrão, as propriedades com vários valores serão incluídas em uma tabela somente se o usuário da tabela a solicitar. 
  
Colunas com vários valores podem ser exibidas em tabelas:
  
- Em uma única linha, com todos os valores de propriedade que aparecem na instância de coluna única. É o padrão.
    
    - Ou
    
- Em uma série de linhas, com uma linha para cada valor de propriedade. Cada valor exclusivo é exibido na coluna em sua própria linha, com o mesmo número de linhas que há valores na propriedade multivalued. Cada linha tem um valor exclusivo para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), mas os mesmos valores para as outras colunas. Se uma linha contiver mais de uma coluna com vários valores, por exemplo, duas colunas com valores _M_ e _N_ respectivamente, _M\*N_ instâncias da linha aparecerão na tabela. 
    
Um usuário de tabela solicita o tipo de exibição não padrão chamando o método imApitable [::](imapitable-setcolumns.md) SetColumns com o sinalizador MVI_FLAG definido no tipo de propriedade da coluna de vários valores. O sinalizador MVI_FLAG é uma constante definida como resultado da combinação dos sinalizadores MV_FLAG e MV_INSTANCE com uma operação **ou** lógica. Além de ser usado em setColumns, MVI_FLAG também pode ser passado para imApitable [:: SortTable](imapitable-sorttable.md) no _parâmetro LpSortCriteria_ e [IMAPITable:](imapitable-restrict.md) : Restrict no membro **ulPropTag** do _lpRestriction_ **** Construtor. Quando passamos o MVI_FLAG **** , SortTable é executado de forma semelhante a SetColumns, adicionando uma linha para cada valor na coluna de vários valores e classificando os valores únicos nas instâncias. **** Uma linha é adicionada para cada valor. 
  
 No entanto, a **restrição**não expande a coluna de vários valores em linhas computadas adicionais. Uma coluna com vários valores com o conjunto MVI_FLAG instrui o provedor de serviços a usar essa coluna ao restringir a tabela. Se houver um valor de propriedade na restrição, ele deve ser uma marca de propriedade de valor único idêntica à que seria retornada por imApitable [:: QueryRows](imapitable-queryrows.md) para a coluna. 
  
Os implementadores de tabela são necessários apenas para suportar o tipo de exibição padrão e podem retornar o valor MAPI_E_TOO_COMPLEX quando um chamador solicita a outra alternativa. A capacidade de suportar ambos os tipos de exibição é mais importante para os provedores de repositório de mensagens que estão implementando tabelas de conteúdo da pasta. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

