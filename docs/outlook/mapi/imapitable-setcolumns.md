---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9eeab1e1186aeb5a9b458facd59bd4cc155e8014
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767339"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**Aplica-se a**: Outlook 
  
Define as propriedades específicas e a ordem das propriedades aparecer como colunas na tabela.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _lpPropTagArray_
  
> [in] Ponteiro para uma matriz de marcas de propriedade identificando propriedades a serem incluídos como colunas na tabela. A parte de tipo de propriedade de cada marca pode ser definida para um tipo válido ou **PR_NULL** para reservar espaço para adições subsequentes. O parâmetro _lpPropTagArray_ não pode ser definido como NULL; cada tabela deve ter pelo menos uma coluna. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores que controla o retorno de uma chamada assíncrona para **SetColumns**, por exemplo, quando **SetColumns** é usado na notificação. Sinalizadores a seguir podem ser definidos: 
    
TBL_ASYNC 
  
> Solicitações que a operação de configuração de coluna ser executada assincronamente causando **SetColumns** retornar potencialmente antes que a operação foi totalmente concluída. 
    
TBL_BATCH 
  
> Permite que a tabela para adiar a operação de configuração de coluna até que os dados são realmente necessários.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A operação de configuração de coluna foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede que a coluna a definição de início da operação. Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.
    
## <a name="remarks"></a>Comentários

O conjunto de colunas de uma tabela é o grupo de propriedades que compõem as colunas para as linhas da tabela. Não há uma coluna padrão definido para cada tipo de tabela. O conjunto de colunas padrão é formado pelas propriedades que o implementador tabela inclui automaticamente. Os usuários da tabela podem alterar esse padrão definido chamando o método **IMAPITable::SetColumns** . Eles podem solicitar que outras colunas seja adicionado ao padrão definido se o implementador tabela oferece suporte a eles que colunas seja removido ou que a ordem das colunas seja alterado. **SetColumns** Especifica as colunas que são retornadas com cada linha e a ordem dessas colunas dentro da linha. 
  
O êxito da operação **SetColumns** seja aparente somente depois que uma chamada subsequente foi feita para recuperar os dados da tabela. Em seguida, é que quaisquer erros informados. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Alguns provedores de permitir que uma chamada **SetColumns** somente as colunas de tabela que fazem parte das colunas disponíveis para um modo de exibição de tabela de pedidos. Outros provedores de permitir que uma chamada **SetColumns** solicitar todas as colunas de tabela, inclusive aquelas que contém as propriedades não no conjunto de coluna original. 
  
Quando TBL_BATCH é definida para operações assíncronas, provedores devem retornar um tipo de propriedade de PT_ERROR e um valor de propriedade de valor nulo para as colunas que não são suportados.
  
Você não precisará responder ao sinalizador TBL_ASYNC solicitando que a operação ser assíncrona. Se você não têm suporte para a definição do conjunto de coluna assíncrona, execute a operação de maneira síncrona. Se você pode suportar o sinalizador TBL_ASYNC e outro assíncrono operação ainda está em andamento, MAPI_E_BUSY retorno. Caso contrário, Retorna S_OK independentemente de estarem ou não suportam todas as propriedades incluídas na matriz de marca de propriedade. Erros resultantes das propriedades sem suporte devem ser retornados da **IMAPITable** métodos que recuperar dados, como **QueryRows**. 
  
Não gere notificações de linhas da tabela que estão ocultas do modo por chamadas para **Restrict**. 
  
Quando envio de notificações de tabela, a ordem das propriedades no membro da **linha** da estrutura [TABLE_NOTIFICATION](table_notification.md) e a ordem especificada pela chamada mais recente do **SetColumns** deve ser iguais desde o momento em que a solicitação de notificação foi enviada. 
  
Sinalizador de outro, TBL_BATCH, permite que os chamadores especificar que o implementador tabela pode adiar avaliando os resultados da operação até um momento posterior. Sempre que possível, os chamadores devem definir este sinalizador como operação em lote melhora o desempenho.
  
Costuma ser conveniente para os chamadores reservar algumas colunas do conjunto de linha recuperados para valores sejam adicionados posteriormente. Os chamadores fazer isso, colocando **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) nas posições desejadas na propriedade tag matriz passadas **SetColumns**; a tabela será então secreta volta **PR_NULL** nesses cargos em todas as linhas recuperadas com **QueryRows**.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Ao construir a matriz de marca de propriedade para o parâmetro _lpPropTagArray_ , ordem as marcas na ordem em que você deseja que as colunas apareçam na exibição da tabela. 
  
Você pode especificar vários valores de propriedades a serem incluídos na coluna definir aplicando o sinalizador multivalorado instância ou a constante MVI_FLAG, como a marca de propriedade. Defina esse sinalizador, passando a marca de propriedade para a versão de valor único da propriedade como um parâmetro para a macro MVI_PROP da seguinte maneira:
  
```
MVI_PROP(ulPropTag)

```

A macro MVI_PROP definirão MVI_FLAG para a propriedade, transformando a marca em uma marca de valores múltiplos. Se você tentar chamar MVI_PROP em uma propriedade de valor único erroneamente, MAPI irá ignorar a chamada e deixe a marca de propriedade inalterada. 
  
Você pode incluir marcas de propriedade definidas como **PR_NULL** na matriz de marca de propriedade para reservar espaço no conjunto de colunas. Reservar espaço permite que você adicione a uma coluna definida sem precisar alocar uma nova matriz de marca de propriedade. 
  
Quando a chamada para **SetColumns** faz com que uma alteração à ordem de colunas de uma tabela e um ou mais dessas colunas representam uma propriedade de vários valores, é possível para o número de linhas da tabela para aumentar. Caso isso aconteça, todos os indicadores da tabela são descartados. Para obter mais informações sobre como colunas de valores múltiplos afetam as tabelas, consulte [Trabalhando com vários valores de colunas](working-with-multivalued-columns.md).
  
Definir colunas é por padrão uma operação síncrona. No entanto, você pode permitir que a tabela adiar a operação até que os dados forem necessários, definindo o sinalizador TBL_BATCH. Defina esse sinalizador pode melhorar o desempenho. Sinalizador de outro, TBL_ASYNC, faz com que a operação assíncrona, permitindo que **SetColumns** retornar antes que a operação seja concluída. Para determinar quando ocorre de conclusão, chame [IMAPITable::GetStatus](imapitable-getstatus.md).
  
Se uma chamada para **SetColumns** retornará MAPI_E_BUSY, indicando que a outra operação está impedindo a operação seja iniciado, é possível chamar [IMAPITable::Abort](imapitable-abort.md) para interromper a operação em andamento. 
  
Você também pode chamar [HrAddColumnsEx](hraddcolumnsex.md) para alterar um conjunto de colunas. A diferença entre **HrAddColumnsEx** e **IMAPITable::SetColumns** é que **HrAddColumnsEx** menos flexíveis; ele só poderá adicionar colunas. As colunas adicionais são colocadas no início do conjunto de colunas; todas as colunas existentes aparecem seguindo essas colunas. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoSetColumns  <br/> |MFCMAPI usa o método **IMAPITable::SetColumns** para definir as colunas desejadas para a tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

