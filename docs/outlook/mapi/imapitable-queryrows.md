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
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416290"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma ou mais linhas de uma tabela, começando na posição atual do cursor.
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>Parâmetros

 _lRowCount_
  
> no Número máximo de linhas a serem retornadas.
    
 _ulFlags_
  
> no Bitmask de sinalizadores que controlam como as linhas são retornadas. O seguinte sinalizador pode ser definido:
    
TBL_NOADVANCE 
  
> Impede que o cursor avança como resultado da recuperação de linha. Se o sinalizador TBL_NOADVANCE estiver definido, o cursor apontará para a primeira linha retornada. Se o sinalizador TBL_NOADVANCE não estiver definido, o cursor apontará para a linha após a última linha retornada.
    
 _lppRows_
  
> bota Ponteiro para um ponteiro para uma estrutura [SRowSet](srowset.md) que contém as linhas da tabela. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As linhas foram retornadas com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento, o que impede a inicialização da operação de recuperação de linha. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
MAPI_E_INVALID_PARAMETER 
  
> O parâmetro _IRowCount_ é definido como zero. 
    
## <a name="remarks"></a>Comentários

O método imApitable **:: QueryRows** Obtém uma ou mais linhas de dados de uma tabela. O valor do parâmetro _IRowCount_ afeta o ponto de partida da recuperação. Se _IRowCount_ for positivo, as linhas são lidas em uma direção de encaminhamento, começando na posição atual. Se _IRowCount_ for negativo, **QueryRows** redefine o ponto de partida movendo para trás o número indicado de linhas. Após o cursor ser redefinido, as linhas são lidas na ordem de encaminhamento. 
  
O membro de **galinha** na estrutura [SRowSet](srowset.md) apontada pelo parâmetro _lppRows_ indica o número de linhas retornadas. Se forem retornadas zero linhas: 
  
- O cursor já estava posicionado no início da tabela e o valor de _IRowCount_ é negativo. Ou 
    
- O cursor já estava posicionado no final da tabela e o valor de _IRowCount_ é positivo. 
    
O número de colunas e sua ordenação são os mesmos para cada linha. Se uma propriedade não existir para uma linha ou se houver um erro de leitura de uma propriedade, a estrutura **SPropValue** da propriedade na linha conterá os seguintes valores: 
  
- PT_ERROR para o tipo de propriedade no membro **ulPropTag** . 
    
- MAPI_E_NOT_FOUND para o membro **Value** . 
    
A memória usada para as estruturas [SPropValue](spropvalue.md) no conjunto de linhas apontado pelo parâmetro _lppRows_ deve ser alocada separadamente e liberada para cada linha. Use [MAPIFreeBuffer](mapifreebuffer.md) para liberar as estruturas de valor da propriedade e liberar o conjunto de linhas. No entanto, quando uma chamada a **QueryRows** retorna zero, indicando o início ou o fim da tabela, somente a estrutura do **SRowSet** precisa ser liberada. Para obter mais informações sobre como alocar e liberar memória em uma estrutura do **SRowSet** , consulte [Managing Memory for das ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
As linhas que são retornadas e a ordem em que são retornadas dependem de se as chamadas bem-sucedidas foram feitas ou não a imApitable [:: Restrict](imapitable-restrict.md) e IMAPITable [:: SortTable](imapitable-sorttable.md). **Restringir** as linhas de filtro do modo de exibição, fazendo com que o **QueryRows** retorne apenas as linhas que correspondam aos critérios especificados na restrição. **SortTable** estabelece uma ordem de classificação padrão ou categorizada, afetando a sequência de linhas retornadas por **QueryRows**. As linhas retornadas estão na ordem especificada na estrutura [SSortOrderSet](ssortorderset.md) passada para **SortTable**.
  
As colunas retornadas para cada linha e a ordem em que são retornadas dependem de uma chamada bem-sucedida ter sido feita ou não para [IMAPITable::](imapitable-setcolumns.md)SetColumns. **** SetColumns estabelece um conjunto de colunas, especificando as propriedades a serem incluídas em colunas na tabela e a ordem em que elas devem ser incluídas. Se uma **** chamada SetColumns tiver sido feita, as colunas específicas em cada linha e a ordem dessas colunas corresponderão ao conjunto de colunas especificado na chamada. Se nenhuma **** chamada SetColumns tiver sido feita, a tabela retornará seu conjunto de colunas padrão. 
  
Se nenhuma dessas chamadas tiver sido feita, **QueryRows** retornará todas as linhas da tabela. Cada linha contém o conjunto de colunas padrão na ordem padrão. 
  
Quando o conjunto de colunas estabelecido em uma chamada para imApitable [::](imapitable-setcolumns.md) SetColumns inclui colunas definidas como PR_NULL, a matriz [SPropValue](spropvalue.md) dentro do conjunto de linhas retornado em _lppRows_ conterá Slots vazios. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode permitir que um chamador solicite a inclusão de uma coluna sem suporte no conjunto de colunas. Quando isso ocorre, coloque PT_ERROR na parte de tipo de propriedade da marca de propriedade e MAPI_E_NOT_FOUND no valor da propriedade para a coluna sem suporte. 
  
Tratar a contagem de linhas como uma solicitação, e não um requisito. Você pode retornar em qualquer lugar de zero linhas, se não houver linhas na direção da consulta, para o número solicitado. 
  
Retornar somente as linhas que o usuário verá quando as linhas são solicitadas de um modo de exibição de tabela Categorizado, permitindo que o chamador faça suposições válidas sobre o escopo dos dados e evite o trabalho extra. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Normalmente, você terminará com quantas linhas forem especificadas no parâmetro _lRowCount_ . No enTanto, quando os limites de memória ou implementação são um problema ou quando a operação atinge o início ou o fim da tabela prematuramente, o **QueryRows** retornará menos linhas do que o solicitado. 
  
Se **QueryRows** retornar MAPI_E_BUSY, chame o método IMAPITable [:: WaitForCompletion](imapitable-waitforcompletion.md) e repita a chamada para **QueryRows** quando a operação assíncrona estiver concluída. 
  
Ao chamar **QueryRows**, lembre-se de que o tempo das notificações assíncronas pode fazer com que o conjunto de linhas obtido de volta do **QueryRows** não represente precisamente os dados subjacentes. Por exemplo, uma chamada para **QueryRows** para a tabela de conteúdo de uma pasta após a exclusão de uma mensagem, mas antes do recebimento da notificação correspondente fará com que a linha excluída seja retornada no conjunto de linhas. Sempre espere uma notificação chegar antes de atualizar o modo de exibição do usuário dos dados. 
  
Para obter mais informações sobre como recuperar linhas de tabelas, consulte [recuperaNdo dados de linhas de tabela](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa o método imApitable **:: QueryRows** para recuperar linhas na tabela para carregar no modo de exibição.  <br/> |
   
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


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

