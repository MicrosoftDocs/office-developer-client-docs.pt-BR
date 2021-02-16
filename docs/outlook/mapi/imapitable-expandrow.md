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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415163"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Expande uma categoria de tabela recolhido, adicionando as linhas de título de nível folha ou inferior pertencentes à categoria ao exibição de tabela.
  
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
  
> [in] A contagem de bytes na propriedade PR_INSTANCE_KEY apontado pelo parâmetro _pbInstanceKey._ 
    
 _pbInstanceKey_
  
> [in] Um ponteiro para a **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica a linha de título para a categoria. 
    
 _ulRowCount_
  
> [in] O número máximo de linhas a ser retornada no parâmetro _lppRows._ 
    
 _ulFlags_
  
> Reservado; deve ser zero.
    
 _lppRows_
  
> [out] Um ponteiro para uma [estrutura SRowSet](srowset.md) recebendo as primeiras linhas (até  _ulRowCount_) que foram inseridas no exibição de tabela como resultado da expansão. Essas linhas são inseridas após a linha de título identificada pelo _parâmetro pbInstanceKey._ O  _parâmetro lppRows_ pode ser NULL se  _o parâmetro ulRowCount_ for zero. 
    
 _lpulMoreRows_
  
> [out] Um ponteiro para o número total de linhas que foram adicionadas ao exibição de tabela.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A categoria foi expandida com êxito.
    
MAPI_E_NOT_FOUND 
  
> A linha identificada pelo  _parâmetro pbInstanceKey_ não existe. 
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::ExpandRow expande** uma categoria de tabela recolhido, adicionando as linhas de título de nível folha ou inferior que pertencem à categoria ao modo de exibição de tabela. Um limite para o número de linhas a serem retornadas no parâmetro _lppRows_ pode ser especificado no _parâmetro ulRowCount._ Quando  _ulRowCount_ é definido para um valor maior do que zero e uma ou mais linhas são retornadas no conjunto de linhas apontado por  _lppRows_, a posição do indicador BOOKMARK_CURRENT é movida para a linha imediatamente após a última linha no conjunto de linhas.
  
Quando  _ulRowCount_ é definido como zero, solicitando que linhas de título de nível zero ou de nível inferior sejam adicionadas à categoria ou zero linhas são retornadas porque não há linhas de título de nível inferior ou folha na categoria, a posição de BOOKMARK_CURRENT é definida como a linha após a linha identificada por  _pbInstanceKey_. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Não gere notificações em linhas adicionadas a um exibição de tabela devido à expansão da categoria.
  
## <a name="notes-to-callers"></a>Notas para chamadores

O número de linhas no conjunto de linhas apontado pelo parâmetro  _lppRows_ pode não ser igual ao número de linhas que foram realmente adicionadas à tabela, todo o conjunto de linhas de título de nível folha ou inferior para a categoria. Podem ocorrer erros, como memória insuficiente ou o número de linhas na categoria excedendo o número especificado no _parâmetro ulRowCount._ Em ambos os casos, BOOKMARK_CURRENT será posicionado na última linha retornada. Para recuperar imediatamente o restante das linhas na categoria, chame [IMAPITable::QueryRows](imapitable-queryrows.md).
  
Não espere receber uma notificação de tabela quando uma categoria mudar seu estado. Você pode manter um cache local de linhas que pode ser atualizado a cada **chamada ExpandRow** ou **CollapseRow.** 
  
Para obter mais informações sobre tabelas categorizadas, consulte [Classificação e Categorização.](sorting-and-categorization.md)
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI usa o **método IMAPITable::ExpandRow** para expandir uma categoria de tabela recolhido.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

