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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432363"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O **método IMAPITable::SortTable** ordena as linhas da tabela, dependendo dos critérios de classificação. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

_lpSortCriteria_
  
> [in] Ponteiro para uma [estrutura SSortOrderSet](ssortorderset.md) que contém os critérios de classificação a aplicar. Passar uma **estrutura SSortOrderSet** que contém zero colunas indica que a tabela não precisa ser ordenada em nenhuma ordem específica. 
    
_ulFlags_
  
> [in] Máscara de bits de sinalizadores que controla o tempo da **operação IMAPITable::SortTable.** Os sinalizadores a seguir podem ser definidos: 
    
TBL_ASYNC 
  
> Inicia a operação de forma assíncrona e retorna antes que a operação seja concluída.
    
TBL_BATCH 
  
> Adia a conclusão da classificação até que os dados na tabela são necessários.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de classificação foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede o início da operação de classificação. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
MAPI_E_NO_SUPPORT 
  
> A tabela não dá suporte ao tipo de classificação solicitado.
    
MAPI_E_TOO_COMPLEX 
  
> A tabela não pode executar a operação porque os critérios de classificação específicos apontados pelo parâmetro  _lpSortCriteria_ são muito complexos. **SortTable** pode retornar MAPI_E_TOO_COMPLEX sob as seguintes condições. 
    
   - Uma operação de classificação é solicitada para uma coluna de propriedade que a implementação não pode classificar.
    
   - A implementação não dá suporte à ordem de classificação solicitada no **membro ulOrder** da **estrutura SSortOrderSet.** 
    
   - O número de colunas a serem ordenadas, conforme especificado no membro **cSorts** em **SSortOrderSet**, é maior do que a implementação pode manipular.
    
   - Uma operação de classificação é solicitada, conforme indicado por uma marca de propriedade em **SSortOrderSet**, com base em uma propriedade que não está no conjunto disponível ou ativo e a implementação não suporta a classificação em propriedades que não estão no conjunto disponível.
    
   - Uma propriedade é especificada várias vezes em um conjunto de ordem de classificação, conforme indicado por várias instâncias da mesma marca de propriedade, e a implementação não pode executar essa operação de classificação.
    
   - Uma operação de classificação com base em colunas de propriedade de múltiplos valores é solicitada usando MVI_FLAG e a implementação não dá suporte à classificação em propriedades de vários valores. 
    
   - A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support. 
    
   - Uma operação de classificação diferente de uma que prossiga pela tabela a partir da propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para frente é especificada apenas para uma tabela de anexos que oferece suporte a esse tipo de classificação.
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::SortTable** ordena as linhas em um modo de exibição de tabela. Enquanto algumas tabelas suportam classificação padrão e categorizada em várias colunas de chave de classificação, outras tabelas são mais limitadas em seu suporte. Os provedores de agendamento de endereço normalmente não suportam a classificação de tabelas. Os provedores de armazenamento de mensagens geralmente suportam a classificação na medida em que mantêm a ordem de classificação de pastas que resulta quando uma tabela completa (uma tabela sem restrições) é ordenada. 
  
Algumas tabelas permitem que a classificação seja feita em qualquer coluna de tabela. Outras tabelas não; colunas não incluídas no exibição de tabela não são afetadas por uma **chamada SortTable.** Algumas tabelas exigem que as chaves de classificação sejam criadas somente com colunas no conjunto de colunas atual da tabela. 
  
Uma tabela pode retornar uma MAPI_E_NO_SUPPORT ou MAPI_E_TOO_COMPLEX da **Tabela** de Classificação quando não puder concluir uma operação de classificação. Além disso, os provedores de armazenamento não têm garantia de atender ao conjunto de ordem de classificação especificado para tabelas de hierarquia. 
  
Quando há zero colunas na estrutura [SSortOrderSet](ssortorderset.md) apontada pelo parâmetro  _lpSortCriteria,_ a tabela retorna o conjunto de colunas atual. A ordem de classificação atual pode ser recuperada chamando o método [IMAPITable::QuerySortOrder da](imapitable-querysortorder.md) tabela. 
  
Todos os indicadores de uma tabela são invalidados e devem ser excluídos quando uma chamada para **SortTable** é feita, e o indicador BOOKMARK_CURRENT que indica a posição atual do cursor deve ser definido como o início da tabela. 
  
Se você estiver classificação em uma coluna que contém uma propriedade de valores múltiplos sem o MVI_FLAG de sinalização definido, os valores da coluna serão tratados como uma tupla completamente ordenada. Uma comparação de duas colunas de múltiplos valores compara os elementos de coluna na ordem, relatando a relação das colunas na primeira situação e retorna a igualdade somente se as colunas que estão sendo comparadas contêm os mesmos valores na mesma ordem. Se uma coluna tiver menos valores do que a outra, a relação relatada será aquela de um valor nulo para o outro valor.
  
## <a name="notes-to-callers"></a>Notas para chamadores

**SortTable** funciona de forma síncrona, a menos que você de definir um dos sinalizadores. Se você definir o sinalizador TBL_BATCH, **SortTable** adia a operação de classificação, a menos que você solicite os dados. Se o TBL_ASYNC sinalizador estiver definido, **SortTable** opera de forma assíncrona, potencialmente retornando antes da conclusão da operação. 
  
Chame o [método IMAPITable::Abort](imapitable-abort.md) para interromper uma operação assíncrona em andamento se sua classificação tiver que ser feita imediatamente. Se **SortTable não** puder continuar porque uma ou mais operações assíncronas na tabela estão em andamento, ela retornará MAPI_E_BUSY. 
  
Para melhorar o desempenho, chame **SetColumns** para personalizar o conjunto de colunas da tabela e **Restringir** para limitar o número de linhas na tabela antes de chamar **SortTable** para executar a classificação. 
  
Sempre **que SortTable** falhar, a ordem de classificação que estava em vigor antes da falha ainda está em vigor. 
  
## <a name="see-also"></a>Confira também

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

