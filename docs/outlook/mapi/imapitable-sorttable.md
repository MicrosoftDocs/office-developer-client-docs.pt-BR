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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: efeff92f1a21d076c1ee58b82ad3ab25797df014
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592301"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O método **IMAPITable:: SortTable** ordena as linhas da tabela, dependendo da classificação de critérios. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

_lpSortCriteria_
  
> [in] Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que contém os critérios de classificação a ser aplicado. Passar uma estrutura **SSortOrderSet** que contém as colunas de zero indica que a tabela não precisa ser classificados em alguma ordem específica. 
    
_ulFlags_
  
> [in] Bitmask dos sinalizadores que controla o tempo da operação **IMAPITable:: SortTable** . Sinalizadores a seguir podem ser definidos: 
    
TBL_ASYNC 
  
> Inicia a operação assíncrona e retorna antes que a operação seja concluída.
    
TBL_BATCH 
  
> Submete-se a conclusão da classificação até que os dados na tabela são necessários.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A operação de classificação foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede que a operação de classificação seja iniciado. Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.
    
MAPI_E_NO_SUPPORT 
  
> A tabela não oferece suporte para o tipo de classificação solicitada.
    
MAPI_E_TOO_COMPLEX 
  
> A tabela não é possível executar a operação porque os critérios de classificação determinado apontados pelo parâmetro _lpSortCriteria_ é muito complexa. **SortTable** pode retornar MAPI_E_TOO_COMPLEX sob as condições a seguintes. 
    
   - Uma operação de classificação é solicitada para uma coluna de propriedade que a implementação não é possível classificar.
    
   - A implementação não dá suporte a ordem de classificação solicitada no membro **ulOrder** da estrutura **SSortOrderSet** . 
    
   - O número de colunas a serem classificados, conforme especificado no membro **cSorts** em **SSortOrderSet**, é maior do que a implementação pode manipular.
    
   - Uma operação de classificação é solicitada, conforme indicado por uma marca de propriedade em **SSortOrderSet**, com base em uma propriedade que não seja o conjunto disponível ou ativo e a implementação não oferece suporte a propriedades não esteja no conjunto disponível de classificação.
    
   - Uma propriedade é especificada várias vezes em um conjunto de ordem de classificação, conforme indicado pelo várias instâncias da marca de propriedade do mesmo e a implementação não puder executar uma operação de classificação tais.
    
   - Uma operação de classificação com base em colunas de vários valores de propriedade é solicitada usando MVI_FLAG e a implementação não oferece suporte a classificação nas propriedades de valores múltiplos. 
    
   - Uma marca de propriedade para uma propriedade **SSortOrderSet** Especifica uma propriedade ou tipo não suporta a implementação. 
    
   - Uma operação de classificação que não seja aquele que prossegue no índice da propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) encaminhar é especificada apenas para uma tabela de anexos que ofereça suporte a esse tipo de classificação.
    
## <a name="remarks"></a>Comentários

O método **IMAPITable:: SortTable** ordena as linhas em um modo de exibição de tabela. Enquanto algumas tabelas suportam a classificação de padrão e categorizados em várias colunas de chave de classificação, outras tabelas mais estão limitadas em seu suporte. Provedores de catálogo de endereços normalmente não suportam a classificação de tabela. Provedores de armazenamento de mensagem normalmente suportam a classificação na medida em que elas mantenham a ordem de classificação das pastas que resulte quando uma tabela completa (uma tabela sem restrições) é classificada. 
  
Algumas tabelas permitem classificação ser executado em qualquer coluna da tabela. Outras tabelas, não; colunas não são incluídas no modo de exibição de tabela não são afetadas por uma chamada **SortTable** . Algumas tabelas exigem que as chaves de classificação ser criados apenas com colunas no conjunto atual de coluna da tabela. 
  
Uma tabela pode retornar MAPI_E_NO_SUPPORT ou MAPI_E_TOO_COMPLEX de **SortTable** quando ele não é possível concluir uma operação de classificação. Além disso, provedores de armazenamento não há uma garantia honram especificada para tabelas de hierarquias de definir a ordem de classificação. 
  
Quando houver zero colunas na estrutura [SSortOrderSet](ssortorderset.md) apontada pelo parâmetro _lpSortCriteria_ , a tabela retorna o conjunto atual de coluna. A ordem de classificação atual pode ser recuperada chamando o método da tabela [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
Todos os indicadores para uma tabela são invalidados e devem ser excluídos quando é feita uma chamada para **SortTable** e indicador BOOKMARK_CURRENT que indica a posição atual do cursor, deve ser definida para o início da tabela. 
  
Se você estiver classificando em uma coluna que contém uma propriedade de valores múltiplos sem o MVI_FLAG sinalizador definido, os valores da coluna são tratados como uma tupla completamente ordenada. Uma comparação de duas colunas de valores múltiplos compara os elementos de coluna em ordem, relatórios a relação entre as colunas na inequação primeira e retorna a igualdade somente se as colunas que estão sendo comparadas contêm os mesmos valores na mesma ordem. Se uma coluna tiver valores menos que o outro, a relação relatada é de um valor nulo para o outro valor.
  
## <a name="notes-to-callers"></a>Notas para chamadores

**SortTable** opera de maneira síncrona, a menos que você defina um dos sinalizadores. Se você definir o sinalizador TBL_BATCH, **SortTable** adia a operação de classificação, a menos que você solicitar os dados. Se o sinalizador TBL_ASYNC estiver definido, **SortTable** opera de forma assíncrona, retornando potencialmente antes da conclusão da operação. 
  
Chame o método [IMAPITable::Abort](imapitable-abort.md) para interromper uma operação assíncrona em andamento, se a classificação deve ser feita imediatamente. Se **SortTable** não pode continuar porque um ou mais operações assíncronas na tabela estejam em andamento, ele retornará MAPI_E_BUSY. 
  
Para obter melhor desempenho, chame **SetColumns** para personalizar o conjunto de colunas da tabela e **Restrict** para limitar o número de linhas da tabela antes de chamar **SortTable** para executar a classificação. 
  
Sempre que **SortTable** falhar, a ordem de classificação que estava em vigor antes da falha ainda está em vigor. 
  
## <a name="see-also"></a>Confira também

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

