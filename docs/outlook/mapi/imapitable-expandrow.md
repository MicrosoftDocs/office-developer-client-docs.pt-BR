---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329034"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Expande uma categoria de tabela recolhida, adicionando as linhas de título de folha ou de nível inferior pertencentes à categoria para o modo de exibição de tabela.
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a>Parâmetros

 _cbInstanceKey_
  
> no A contagem de bytes na propriedade PR_INSTANCE_KEY indicada pelo parâmetro _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> no Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica a linha de título para a categoria. 
    
 _ulRowCount_
  
> no O número máximo de linhas a serem retornadas no parâmetro _lppRows_ . 
    
 _ulFlags_
  
> Serve deve ser zero.
    
 _lppRows_
  
> bota Um ponteiro para uma estrutura [SRowSet](srowset.md) recebendo as primeiras (até _ulRowCount_) linhas que foram inseridas no modo de exibição de tabela como resultado da expansão. Essas linhas são inseridas após a linha de título identificada pelo parâmetro _pbInstanceKey_ . O parâmetro _lppRows_ pode ser NULL se o parâmetro _ulRowCount_ for zero. 
    
 _lpulMoreRows_
  
> bota Um ponteiro para o número total de linhas que foram adicionadas ao modo de exibição de tabela.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A categoria foi expandida com êxito.
    
MAPI_E_NOT_FOUND 
  
> A linha identificada pelo parâmetro _pbInstanceKey_ não existe. 
    
## <a name="remarks"></a>Comentários

O método imApitable **:: ExpandRow** expande uma categoria de tabela recolhida, adicionando a folha ou linhas de título de nível inferior que pertencem à categoria para o modo de exibição de tabela. Um limite para o número de linhas a serem retornadas no parâmetro _lppRows_ pode ser especificado no parâmetro _ulRowCount_ . Quando _ulRowCount_ é definido como um valor maior que zero e uma ou mais linhas são retornadas no conjunto de linhas apontado por _lppRows_, a posição do indicador BOOKMARK_CURRENT é movida para a linha imediatamente após a última linha no conjunto de linhas.
  
Quando _ulRowCount_ é definido como zero, solicitar que as linhas de título de nível inferior ou folha zero sejam adicionadas à categoria ou linhas zero são retornadas porque não há linhas de título de folha ou de nível inferior na categoria, a posição de BOOKMARK_CURRENT é definida como a linha após a linha identificada por _pbInstanceKey_. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Não gerar notificações em linhas que são adicionadas a um modo de exibição de tabela devido à expansão de categoria.
  
## <a name="notes-to-callers"></a>Notas para chamadores

O número de linhas no conjunto de linhas apontado pelo parâmetro _lppRows_ pode não ser igual ao número de linhas que foram realmente adicionadas à tabela, a todo o conjunto de linhas de título de folha ou de nível inferior para a categoria. Podem ocorrer erros, como memória insuficiente ou o número de linhas na categoria excedendo o número especificado no parâmetro _ulRowCount_ . Em ambos os casos, BOOKMARK_CURRENT será posicionado na última linha retornada. Para recuperar imediatamente o restante das linhas da categoria, chame imApitable [:: QueryRows](imapitable-queryrows.md).
  
Não espera receber uma notificação de tabela quando uma categoria altera seu estado. Você pode manter um cache local de linhas que podem ser atualizadas com todas as chamadas **ExpandRow** ou **CollapseRow** . 
  
Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI usa o método imApitable **:: ExpandRow** para expandir uma categoria de tabela recolhida.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

