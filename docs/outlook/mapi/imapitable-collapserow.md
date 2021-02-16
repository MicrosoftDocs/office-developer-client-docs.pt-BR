---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416171"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a>Parâmetros

 _cbInstanceKey_
  
> [in] A contagem de bytes na propriedade PR_INSTANCE_KEY apontado pelo parâmetro _pbInstanceKey._ 
    
 _pbInstanceKey_
  
> [in] Um ponteiro para a **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica a linha de título para a categoria. 
    
 _ulFlags_
  
> Reservado; deve ser zero.
    
 _lpulRowCount_
  
> [out] Um ponteiro para o número total de linhas que estão sendo removidas do ponto de vista da tabela.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de re collapse foi bem-sucedida.
    
MAPI_E_NOT_FOUND 
  
> A linha identificada pelo  _parâmetro pbInstanceKey_ não existe. 
    
MAPI_E_INVALID_ENTRYID 
  
> A linha identificada pelo  _parâmetro pbInstanceKey_ não existe. Esse erro é uma alternativa à MAPI_E_NOT_FOUND; os provedores de serviços podem retornar qualquer um deles. 
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::CollapseRow** collapses a table category and removes it from the table view. As linhas são recolhidos começando na linha identificada pela propriedade **PR_INSTANCE_KEY** apontada pelo parâmetro _pbInstanceKey._ O número de linhas removidas do ponto de vista é retornado no conteúdo do parâmetro _lpulRowCount._ 
  
As notificações nunca são geradas para linhas de tabela removidas de uma exibição como resultado de uma operação de remoção. 
  
Quando uma linha definida por um indicador é recolhido para fora da exibição, o indicador é movido para apontar para a próxima linha visível. 
  
Para obter mais informações sobre tabelas categorizadas, consulte [Classificação e Categorização.](sorting-and-categorization.md)
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI usa o **método IMAPITable::CollapseRow** para recaír uma categoria de tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

