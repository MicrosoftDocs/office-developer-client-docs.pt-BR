---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f16ba9164d55fdb7bd688d4068f99dc4407e5413
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328851"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O método imApitable **:: SortTable** ordena as linhas da tabela, dependendo dos critérios de classificação. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

_lpSortCriteria_
  
> no Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que contém o critério de classificação a ser aplicado. Passar uma estrutura **SSortOrderSet** que contém zero colunas indica que a tabela não precisa ser classificada em uma ordem específica. 
    
_ulFlags_
  
> no Bitmask de sinalizadores que controlam o intervalo da operação imApitable **:: SortTable** . Os seguintes sinalizadores podem ser definidos: 
    
TBL_ASYNC 
  
> Inicia a operação de forma assíncrona e retorna antes de a operação ser concluída.
    
TBL_BATCH 
  
> Adia a conclusão da classificação até que os dados da tabela sejam necessários.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de classificação foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento, o que impede a inicialização da operação de classificação. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
MAPI_E_NO_SUPPORT 
  
> A tabela não dá suporte ao tipo de classificação solicitada.
    
MAPI_E_TOO_COMPLEX 
  
> A tabela não pode executar a operação porque o critério de classificação específico apontado pelo parâmetro _lpSortCriteria_ é muito complexo. **SortTable** pode retornar MAPI_E_TOO_COMPLEX sob as condições a seguir. 
    
   - Uma operação de classificação é solicitada para uma coluna de propriedade que a implementação não pode classificar.
    
   - A implementação não é compatível com a ordem de classificação solicitada no membro **ulOrder** da estrutura **SSortOrderSet** . 
    
   - O número de colunas a serem classificadas, conforme especificado no membro **cSorts** no **SSortOrderSet**, é maior do que a implementação pode lidar.
    
   - Uma operação de classificação é solicitada, conforme indicado por uma marca de propriedade no **SSortOrderSet**, com base em uma propriedade que não está no conjunto disponível ou ativo e a implementação não dá suporte à classificação de propriedades que não estão no conjunto disponível.
    
   - Uma propriedade é especificada várias vezes em um conjunto de ordem de classificação, conforme indicado por várias instâncias da mesma marca de propriedade e a implementação não pode executar tal operação de classificação.
    
   - Uma operação de classificação baseada em colunas de propriedade com valores múltiplos é solicitada usando MVI_FLAG e a implementação não dá suporte à classificação em Propriedades de vários valores. 
    
   - Uma marca de propriedade para uma propriedade no **SSortOrderSet** especifica uma propriedade ou tipo que a implementação não suporta. 
    
   - Uma operação de classificação diferente de uma que prossegue através da tabela da propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) forward é especificada somente para uma tabela de anexo que ofereça suporte a esse tipo de classificação.
    
## <a name="remarks"></a>Comentários

O método imApitable **:: SortTable** ordena as linhas em um modo de exibição de tabela. Enquanto algumas tabelas oferecem suporte à classificação padrão e categorizadas em várias colunas de chave de classificação, outras tabelas são mais limitadas no suporte. Os provedores de catálogo de endereços normalmente não oferecem suporte à classificação de tabelas. Os provedores de repositórios de mensagens geralmente dão suporte à ordenação de que eles mantêm a ordem de classificação das pastas que resultam quando uma tabela completa (uma tabela sem restrições) é classificada. 
  
Algumas tabelas permitem que a classificação seja feita em qualquer coluna de tabela. Outras tabelas não; as colunas não incluídas no modo de exibição de tabela não são afetadas por uma chamada **SortTable** . Algumas tabelas exigem que as chaves de classificação sejam criadas apenas com colunas no conjunto de colunas atual da tabela. 
  
Uma tabela pode retornar MAPI_E_NO_SUPPORT ou MAPI_E_TOO_COMPLEX de **SortTable** quando não puder concluir uma operação de classificação. Além disso, os provedores de repositório não são garantidos para honrar o conjunto de ordem de classificação especificado para tabelas de hierarquia. 
  
Quando há zero colunas na estrutura [SSortOrderSet](ssortorderset.md) apontadas pelo parâmetro _lpSortCriteria_ , a tabela retorna o conjunto de colunas atual. A ordem de classificação atual pode ser recuperada chamando o método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) da tabela. 
  
Todos os indicadores de uma tabela são invalidados e devem ser excluídos quando uma chamada para **SortTable** é feita, e o indicador BOOKMARK_CURRENT que indica a posição atual do cursor, deve ser definido para o início da tabela. 
  
Se você estiver classificando em uma coluna que contenha uma propriedade de vários valores sem o sinalizador MVI_FLAG definido, os valores da coluna serão tratados como uma tupla completamente ordenada. Uma comparação de duas colunas com vários valores compara os elementos de coluna em ordem, relatando a relação entre as colunas na primeira inequação e retorna igualdade somente se as colunas que estão sendo comparadas contiverem os mesmos valores na mesma ordem. Se uma coluna tiver menos valores do que o outro, a relação relatada será a de um valor nulo para o outro valor.
  
## <a name="notes-to-callers"></a>Notas para chamadores

**SortTable** funciona de forma síncrona, a menos que você defina um dos sinalizadores. Se você definir o sinalizador TBL_BATCH, **SortTable** adia a operação de classificação, a menos que você solicite os dados. Se o sinalizador TBL_ASYNC for definido, **SortTable** funciona de forma assíncrona, potencialmente retornando antes da conclusão da operação. 
  
Chame o método imApitable [:: Abort](imapitable-abort.md) para interromper uma operação assíncrona em andamento se a classificação deve ser feita imediatamente. Se **SortTable** não puder continuar porque uma ou mais operações assíncronas na tabela estão em andamento, ela retornará MAPI_E_BUSY. 
  
Para melhor desempenho, chame **** SetColumns para personalizar o conjunto de colunas da tabela e **restrinja** para limitar o número de linhas na tabela antes de chamar **SortTable** para executar a classificação. 
  
Sempre **** que SortTable falhar, a ordem de classificação que estava em vigor antes da falha ainda estará em vigor. 
  
## <a name="see-also"></a>Confira também

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

