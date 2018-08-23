---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 179d76b56c1ba9b40768c691d0b1555377f7adb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595045"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma ou mais linhas de uma tabela, começando à meia posição atual do cursor.
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>Parâmetros

 _lRowCount_
  
> [in] Número máximo de linhas a ser retornado.
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores que controlam como as linhas são retornadas. O seguinte sinalizador pode ser definido:
    
TBL_NOADVANCE 
  
> Impede que o cursor avançando como resultado de recuperação de linha. Se o sinalizador TBL_NOADVANCE estiver definido, os pontos de cursor à primeira linha é retornada. Se o sinalizador TBL_NOADVANCE não estiver definido, o cursor aponta para a linha após a última linha retornada.
    
 _lppRows_
  
> [out] Ponteiro para um ponteiro para uma estrutura [SRowSet](srowset.md) reter as linhas de tabela. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> As linhas foram retornadas com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede que a operação de recuperação de linha seja iniciado. Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.
    
MAPI_E_INVALID_PARAMETER 
  
> O parâmetro _IRowCount_ é definido como zero. 
    
## <a name="remarks"></a>Comentários

O método **IMAPITable:: QueryRows** obtém uma ou mais linhas de dados de uma tabela. O valor do parâmetro _IRowCount_ afeta o ponto de partida para a recuperação. Se _IRowCount_ for positivo, as linhas são lidas em uma direção sequencial, começando na posição atual. Se _IRowCount_ for negativo, **QueryRows** redefine o ponto de partida movendo para trás o número de linhas indicado. Depois que o cursor é redefinido, linhas são lidas em ordem sequencial. 
  
O membro de **pássaros** na estrutura [SRowSet](srowset.md) apontado pelo parâmetro _lppRows_ indica o número de linhas retornadas. Se zero linhas são retornadas: 
  
- O cursor já foi posicionado no início da tabela e o valor de _IRowCount_ for negativo. - Ou - 
    
- O cursor já foi posicionado no final da tabela e o valor de _IRowCount_ for positivo. 
    
O número de colunas e seus ordenação é o mesmo para cada linha. Se não existir uma propriedade para uma linha ou não há um erro ao ler uma propriedade, a estrutura de **SPropValue** para a propriedade na linha contém os seguintes valores: 
  
- PT_ERROR para o tipo de propriedade no membro **ulPropTag** . 
    
- E_NOT_FOUND para o membro de **valor** . 
    
Memória usada para as estruturas de [SPropValue](spropvalue.md) no conjunto de linha apontado pelo parâmetro _lppRows_ deve ser alocada separadamente e liberada para cada linha. Use [MAPIFreeBuffer](mapifreebuffer.md) para liberar as estruturas de valor de propriedade e liberar a linha definido. Quando uma chamada para **QueryRows** retornará zero, no entanto, indicando o início ou fim da tabela, apenas a estrutura de **SRowSet** em si precisa ser liberada. Para obter mais informações sobre como alocar e liberar memória em uma estrutura **SRowSet** , consulte [Gerenciando memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
As linhas que são retornadas e a ordem na qual eles são retornados dependem ou não chamadas bem-sucedidas tem sofridas [IMAPITable:: Restrict](imapitable-restrict.md) e [IMAPITable:: SortTable](imapitable-sorttable.md). **Restrict** filtra linhas da exibição, causando **QueryRows** retornar somente as linhas que coincidem com os critérios especificados na restrição. **SortTable** estabelece um padrão ou categorizados a ordem de classificação, que afetam a sequência de linhas retornadas por **QueryRows**. As linhas retornadas são na ordem especificada na estrutura [SSortOrderSet](ssortorderset.md) passada para **SortTable**.
  
As colunas são retornadas para cada linha e a ordem na qual eles são retornados dependem se ou não uma chamada bem sucedida foi feita para [IMAPITable::SetColumns](imapitable-setcolumns.md). **SetColumns** estabelece um conjunto de colunas, especificando as propriedades a serem incluídos nas colunas na tabela e a ordem em que eles devem ser incluídos. Se foi feita uma chamada **SetColumns** , as colunas específicas de cada linha e a ordem das colunas correspondem a coluna definir especificada na chamada. Se nenhuma chamada **SetColumns** tiverem sido feita, a tabela retorna seu conjunto de coluna padrão. 
  
Se nenhuma dessas chamadas foi feita, **QueryRows** retorna todas as linhas na tabela. Cada linha contém a coluna padrão definida na ordem padrão. 
  
Quando o conjunto de colunas estabelecido em uma chamada para [IMAPITable::SetColumns](imapitable-setcolumns.md) inclui colunas definidas como PR_NULL, a matriz de [SPropValue](spropvalue.md) dentro do conjunto de linhas retornada nos _lppRows_ irá conter slots vazios. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Você pode permitir que um chamador solicitar uma coluna sem suporte a serem incluídos no conjunto de colunas. Quando isso ocorre, coloque PT_ERROR na parte de tipo de propriedade da marca de propriedade e E_NOT_FOUND no valor da propriedade para a coluna sem suporte. 
  
Trate a contagem de linhas como uma solicitação ao invés um requisito. Você pode retornar em qualquer lugar do zero linhas, se não houver nenhuma linha na direção da consulta, para o número solicitado. 
  
Retorne somente as linhas que o usuário verá quando linhas são solicitadas a partir de um modo de exibição de tabela categorizados, permitindo que o chamador para tornar as suposições válidas sobre o escopo dos dados e evitar trabalho extra. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Geralmente você acabará com quantas linhas você especificou no parâmetro _lRowCount_ . No entanto, quando os limites de memória ou implementação são um problema ou a operação atinge o início ou fim da tabela prematuramente, **QueryRows** vai retornar menos linhas do que o solicitado. 
  
Se **QueryRows** retornar MAPI_E_BUSY, chame o método [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) e repetir a chamada para **QueryRows** quando a operação assíncrona seja concluída. 
  
Ao chamar **QueryRows**, lembre-se de que o tempo de notificações assíncronas poderão causar o conjunto de linhas que você obtenha volta de **QueryRows** não para representar com precisão os dados subjacentes. Por exemplo, uma chamada para **QueryRows** seguinte de tabela de conteúdo de uma pasta da linha excluída a ser retornado na linha fará com que a exclusão de uma mensagem, mas antes do recebimento da notificação correspondente é definido. Aguarde sempre uma notificação chegar antes de atualizar o modo de exibição do usuário dos dados. 
  
Para obter mais informações sobre como recuperar linhas de tabelas, consulte [Recuperando dados de linhas da tabela](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa o método **IMAPITable:: QueryRows** para recuperar linhas da tabela para carregar no modo de exibição.  <br/> |
   
## <a name="see-also"></a>Confira também



[ADRENTRY](adrentry.md)
  
[FreeProws](freeprows.md)
  
[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

