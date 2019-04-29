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
ms.openlocfilehash: 897330feb216dbc3ab143378977c77141cf488f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416346"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define as propriedades específicas e a ordem das propriedades a serem exibidas como colunas na tabela.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpPropTagArray_
  
> no Ponteiro para uma matriz de marcas de propriedade que identificam as propriedades a serem incluídas como colunas na tabela. A parte de tipo de propriedade de cada marca pode ser definida como um tipo válido ou **PR_NULL** para reservar espaço para adições subsequentes. O parâmetro _lpPropTagArray_ não pode ser definido como nulo; cada tabela deve ter pelo menos uma coluna. 
    
 _ulFlags_
  
> no Bitmask de sinalizadores que controlam o retorno de uma chamada assíncrona para setColumns, por exemplo, quando setColumns é usado na notificação. **** **** Os seguintes sinalizadores podem ser definidos: 
    
TBL_ASYNC 
  
> Solicita que a operação de configuração de coluna seja executada **** de forma assíncrona fazendo com que SetColumns possa retornar antes de a operação ter sido totalmente concluída. 
    
TBL_BATCH 
  
> Permite que a tabela adie a operação de configuração da coluna até que os dados sejam realmente necessários.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de configuração de coluna foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento, o que impede a inicialização da operação de configuração da coluna. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
## <a name="remarks"></a>Comentários

O conjunto de colunas de uma tabela é o grupo de propriedades que compõem as colunas das linhas da tabela. Há uma coluna padrão definida para cada tipo de tabela. O conjunto de colunas padrão é composto pelas propriedades que o implementador de tabelas inclui automaticamente. Os usuários de tabela podem alterar esse conjunto padrão chamando o método imApitable **::** SetColumns. Eles podem solicitar que outras colunas sejam adicionadas ao conjunto padrão se o implementador de tabelas oferecer suporte a essas colunas ou se a ordem das colunas for alterada. **** SetColumns especifica as colunas que são retornadas com cada linha e a ordem dessas colunas dentro da linha. 
  
O sucesso da operação **** SetColumns é aparente somente depois que uma chamada subsequente foi feita para recuperar os dados da tabela. Em seguida, os erros são relatados. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Alguns provedores permitem uma **** chamada SetColumns para ordenar somente colunas da tabela que fazem parte das colunas disponíveis para um modo de exibição de tabela. Outros provedores permitem uma **** chamada SetColumns para ordenar todas as colunas da tabela, incluindo as que contêm propriedades que não estão no conjunto de colunas original. 
  
Quando TBL_BATCH é definido para operações assíncronas, os provedores devem retornar um tipo de propriedade de PT_ERROR e um valor de propriedade de NULL para colunas que não são suportadas.
  
Você não precisa responder ao sinalizador TBL_ASYNC solicitando que a operação seja assíncrona. Se você não oferecer suporte à definição de conjunto de colunas assíncrono, execute a operação de forma síncrona. Se você puder suportar o sinalizador TBL_ASYNC e outra operação assíncrona ainda estiver em andamento, retorne MAPI_E_BUSY. Caso contrário, retorna S_OK independentemente de você ter ou não suporte a todas as propriedades incluídas na matriz de marca de propriedade. Os erros resultantes de propriedades sem suporte devem ser retornados **** de métodos imapitados que recuperam dados, como **QueryRows**. 
  
Não gere notificações para linhas de tabela ocultas da exibição por chamadas para **restringir**. 
  
Ao enviar notificações de tabela, a ordem das propriedades no membro de **linha** da estrutura [TABLE_NOTIFICATION](table_notification.md) e a ordem especificada pela chamada SetColumns **** mais recente deve ser a mesma da hora em que a solicitação de notificação foi enviada. 
  
Outro sinalizador, TBL_BATCH, permite que os chamadores especifiquem que o implementador de tabelas pode adiar a avaliação dos resultados da operação até um momento posterior. Sempre que possível, os chamadores devem definir esse sinalizador porque a operação em lote melhora o desempenho.
  
É sempre conveniente que os chamadores reservem algumas colunas no conjunto de linhas recuperadas para que os valores sejam adicionados posteriormente. Os chamadores fazem isso colocando **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) nas posições desejadas na matriz de marca de propriedade **** passadas para SetColumns; a tabela passará de volta **PR_NULL** nessas posições em todas as linhas recuperadas com o **QueryRows**.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Ao criar a matriz de marca de propriedade para o parâmetro _lpPropTagArray_ , ordene as marcas na ordem em que você deseja que as colunas apareçam no modo de exibição de tabela. 
  
Você pode especificar as propriedades de vários valores a serem incluídas no conjunto de colunas aplicando o sinalizador de instância de vários valores, ou a constante MVI_FLAG, à marca da propriedade. Defina esse sinalizador passando a marca de propriedade para a versão de valor único da propriedade como um parâmetro para a macro MVI_PROP da seguinte maneira:
  
```
MVI_PROP(ulPropTag)

```

A macro MVI_PROP definirá MVI_FLAG para a propriedade, transformando a marca em uma marca de vários valores. Se você tentar chamar o MVI_PROP em uma propriedade de valor único, o MAPI ignorará a chamada e deixará a marca da propriedade inalterada. 
  
Você pode incluir as marcas de propriedade definidas como **PR_NULL** na matriz de marca de propriedade para reservar espaço no conjunto de colunas. Reservar espaço permite que você adicione a um conjunto de colunas sem precisar alocar uma nova matriz de marca de propriedade. 
  
Quando sua chamada para **** SetColumns causa uma alteração na ordem das colunas de uma tabela e uma ou mais dessas colunas representam uma propriedade com vários valores, é possível que o número de linhas na tabela aumentem. Se isso ocorrer, todos os indicadores para a tabela serão descartados. Para obter mais informações sobre como as colunas com vários valores afetam as tabelas, confira [trabalhar com colunas com vários valores](working-with-multivalued-columns.md).
  
A configuração das colunas é, por padrão, uma operação síncrona. No enTanto, você pode permitir que a tabela adie a operação até o momento em que os dados são necessários, definindo o sinalizador TBL_BATCH. A definição desse sinalizador pode melhorar o desempenho. Outro sinalizador, TBL_ASYNC, torna a operação assíncrona, **** permitindo que SetColumns seja retornado antes que a operação seja concluída. Para determinar quando a conclusão ocorre, chame imApitable [:: GetStatus](imapitable-getstatus.md).
  
Se uma chamada a **** SetColumns retornar MAPI_E_BUSY, indicando que outra operação está impedindo a inicialização da operação, você poderá chamar IMAPITable [:: Abort](imapitable-abort.md) para interromper a operação em andamento. 
  
Você também pode chamar [HrAddColumnsEx](hraddcolumnsex.md) para alterar um conjunto de colunas. A diferença entre **HrAddColumnsEx** e **IMAPITable::** SetColumns é que o **HrAddColumnsEx** é menos flexível; Só é possível adicionar colunas. As colunas adicionais são colocadas no início do conjunto de colunas; todas as colunas existentes aparecem seguindo estas colunas. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI usa o método imApitable **::** SetColumns para definir as colunas desejadas para a tabela.  <br/> |
   
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


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

