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
ms.openlocfilehash: 78f6083cf17bb21152df1a7ea09825f3be7f0e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572939"
---
# <a name="working-with-multivalued-columns"></a>Trabalhar com colunas com vários valores

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma coluna de valores múltiplos contém os dados de uma propriedade de vários valores, que é uma propriedade que tem uma matriz de valores do tipo base, em vez de um único valor. Porque nenhuma das tabelas inclui vários valores de propriedades em seus conjuntos de coluna padrão, vários valores de propriedades são incluídas em uma tabela somente se solicitado pelo usuário da tabela. 
  
Colunas de valores múltiplos podem ser exibidas nas tabelas:
  
- Em uma única linha, com todos os valores de propriedade que aparecem na instância única coluna. Este é o padrão.
    
    - Ou -
    
- Em uma série de linhas, com uma linha para cada um dos valores de propriedade. Cada valor exclusivo aparece na coluna na sua própria linha com daí sendo conforme o número de linhas daí é valores na propriedade multivalorado. Cada linha tem um valor exclusivo para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), mas os mesmos valores para as outras colunas. Se uma linha contiver mais de uma coluna com vários valores, por exemplo, duas colunas com _M_ e _N_ valores respectivamente, em seguida, _M\*N_ instâncias da linha aparecem na tabela. 
    
Um usuário de tabela solicita o tipo de fora do padrão de exibição chamando o método [IMAPITable::SetColumns](imapitable-setcolumns.md) com o sinalizador MVI_FLAG definido no tipo de propriedade da coluna de valores múltiplos. O sinalizador MVI_FLAG é uma constante definida como resultado de combinar os sinalizadores MV_FLAG e MV_INSTANCE com uma operação **OR** lógica. Além do que está sendo usado em **SetColumns**, MVI_FLAG pode também ser passado para [IMAPITable:: SortTable](imapitable-sorttable.md) no parâmetro _lpSortCriteria_ and [IMAPITable:: Restrict](imapitable-restrict.md) no membro **ulPropTag** a _lpRestriction_ Use o parâmetro. Quando passado a MVI_FLAG, **SortTable** da mesma forma realiza a **SetColumns**, adicionando uma linha para cada valor na coluna multivalorada e classificação nos valores único nas instâncias. Uma linha é adicionada para cada valor. 
  
 **Restrict**, no entanto, não expandir a coluna de valores múltiplos em linhas computadas adicionais. Uma coluna de valores múltiplos com o conjunto de MVI_FLAG instrui o provedor de serviços para usar essa coluna na restringindo a tabela. Se houver um valor de propriedade na restrição, ele deve ser uma marca de propriedade de valor único idêntica ao que seria retornada pela [IMAPITable:: QueryRows](imapitable-queryrows.md) da coluna. 
  
Implementadores de tabela apenas requeridos para suportar o tipo de padrão de exibição e podem retornar o valor MAPI_E_TOO_COMPLEX quando um chamador solicita a outra alternativa. A capacidade de suportar os dois tipos de exibição é mais importante para a implementação de tabelas de conteúdo de pasta de provedores de armazenamento de mensagem. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

