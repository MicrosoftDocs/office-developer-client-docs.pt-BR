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
  
Define as propriedades específicas e a ordem das propriedades que aparecerão como colunas na tabela.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpPropTagArray_
  
> [in] Ponteiro para uma matriz de marcas de propriedade que identificam as propriedades a serem incluídas como colunas na tabela. A parte do tipo de propriedade de cada  marca pode ser definida como um tipo válido ou PR_NULL para reservar espaço para adições subsequentes. O  _parâmetro lpPropTagArray_ não pode ser definido como NULL; cada tabela deve ter pelo menos uma coluna. 
    
 _ulFlags_
  
> [in] Bitmask de sinalizadores que controla o retorno de uma chamada assíncrona para **SetColumns**, por exemplo, quando **SetColumns** é usado na notificação. Os sinalizadores a seguir podem ser definidos: 
    
TBL_ASYNC 
  
> Solicita que a operação de configuração de coluna seja executada de forma assíncrona, fazendo com que **SetColumns** retorne potencialmente antes que a operação seja concluída completamente. 
    
TBL_BATCH 
  
> Permite que a tabela adie a operação de configuração de coluna até que os dados realmente são necessários.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de configuração de coluna foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede o início da operação de configuração de coluna. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
## <a name="remarks"></a>Comentários

O conjunto de colunas de uma tabela é o grupo de propriedades que com as colunas das linhas na tabela. Há um conjunto de colunas padrão para cada tipo de tabela. O conjunto de colunas padrão é criado com as propriedades que o implementador de tabela inclui automaticamente. Os usuários de tabela podem alterar esse conjunto padrão chamando o **método IMAPITable::SetColumns.** Eles podem solicitar que outras colunas sejam adicionadas ao conjunto padrão se o implementador de tabelas suportar que as colunas sejam removidas ou se a ordem das colunas for alterada. **SetColumns** especifica as colunas que são retornadas com cada linha e a ordem dessas colunas dentro da linha. 
  
O sucesso da **operação SetColumns** é aparente apenas após uma chamada subsequente ter sido feita para recuperar os dados da tabela. Em seguida, é relatado qualquer erro. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Alguns provedores permitem uma **chamada SetColumns** para ordenar apenas colunas de tabela que fazem parte das colunas disponíveis para um modo de exibição de tabela. Outros provedores permitem uma **chamada SetColumns** para ordenar todas as colunas da tabela, incluindo aquelas que contêm propriedades que não estão no conjunto de colunas original. 
  
Quando TBL_BATCH é definido para operações assíncronas, os provedores devem retornar um tipo de propriedade de PT_ERROR e um valor de propriedade null para colunas sem suporte.
  
Você não precisa responder ao sinalizador de TBL_ASYNC solicitando que a operação seja assíncrona. Se você não tiver suporte para definição de conjunto de colunas assíncrona, execute a operação de forma síncrona. Se você puder dar suporte TBL_ASYNC sinalizador e outra operação assíncrona ainda estiver em andamento, retorne MAPI_E_BUSY. Caso contrário, retorne S_OK independentemente de você dar suporte ou não a todas as propriedades incluídas na matriz de marca de propriedades. Erros resultantes de propriedades sem suporte devem ser retornados dos métodos **IMAPITable** que recuperam dados, como **QueryRows**. 
  
Não gere notificações para linhas de tabela ocultas da exibição por chamadas para **Restringir.** 
  
Ao enviar notificações de tabela, a  ordem das propriedades no membro da linha da estrutura TABLE_NOTIFICATION e a ordem especificada pela chamada **SetColumns** mais recente devem ser as mesmas do momento em que [a](table_notification.md) solicitação de notificação foi enviada. 
  
Outro sinalizador, TBL_BATCH, permite que os chamadores especifiquem que o implementador da tabela pode adiar a avaliação dos resultados da operação até um momento posterior. Sempre que possível, os chamadores devem definir esse sinalizador porque a operação em lote melhora o desempenho.
  
Geralmente, é conveniente para os chamadores reservar algumas colunas no conjunto de linhas recuperado para que os valores sejam adicionados mais tarde. Os chamadores fazem isso colocando **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) nas posições desejadas na matriz de marca de propriedade passada para **SetColumns**; a tabela passará de volta **PR_NULL** essas posições em todas as linhas recuperadas com **QueryRows**.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Ao criar a matriz de marcas de propriedade para o parâmetro  _lpPropTagArray,_ peça as marcas na ordem em que você deseja que as colunas apareçam no modo de exibição de tabela. 
  
Você pode especificar propriedades de vários valores a serem incluídas no conjunto de colunas aplicando o sinalizador de instância de múltiplos valores ou MVI_FLAG constante, à marca de propriedade. De definir esse sinalizador passando a marca de propriedade para a versão de valor único da propriedade como um parâmetro para a macro MVI_PROP da seguinte forma:
  
```
MVI_PROP(ulPropTag)

```

A MVI_PROP macro definirá MVI_FLAG para a propriedade, transformando a marca em uma marca de vários valores. Se você tentar chamar a MVI_PROP em uma propriedade de valor único, MAPI ignorará a chamada e deixará a marca de propriedade inalterada. 
  
Você pode incluir marcas de propriedade definidas **como PR_NULL** na matriz de marcas de propriedade para reservar espaço no conjunto de colunas. Reservar espaço permite que você adicione a um conjunto de colunas sem precisar alocar uma nova matriz de marca de propriedade. 
  
Quando sua chamada para **SetColumns** causa uma alteração na ordem das colunas de uma tabela e uma ou mais dessas colunas representam uma propriedade de múltiplos valores, é possível que o número de linhas na tabela aumente. Se isso ocorrer, todos os indicadores da tabela serão descartados. Para obter mais informações sobre como colunas de valores múltiplos afetam as tabelas, consulte [Trabalhando com colunas de múltiplos valores.](working-with-multivalued-columns.md)
  
Definir colunas é, por padrão, uma operação síncrona. No entanto, você pode permitir que a tabela adie a operação até que tal tempo como os dados são necessários definindo o TBL_BATCH sinalizador. Definir esse sinalizador pode melhorar o desempenho. Outro sinalizador, TBL_ASYNC, torna a operação assíncrona, permitindo que **SetColumns** retorne antes de a operação ser concluída. Para determinar quando a conclusão ocorre, chame [IMAPITable::GetStatus](imapitable-getstatus.md).
  
Se uma chamada para **SetColumns** retornar MAPI_E_BUSY, indicando que outra operação está impedindo a operação de iniciar, você pode chamar [IMAPITable::Abort](imapitable-abort.md) para interromper a operação em andamento. 
  
Você também pode chamar [HrAddColumnsEx para](hraddcolumnsex.md) alterar um conjunto de colunas. A diferença entre **HrAddColumnsEx** e **IMAPITable::SetColumns** é que **HrAddColumnsEx** é menos flexível; só pode adicionar colunas. As colunas adicionais são colocadas no início do conjunto de colunas; todas as colunas existentes aparecem após essas colunas. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI usa o **método IMAPITable::SetColumns** para definir as colunas desejadas para a tabela.  <br/> |
   
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

