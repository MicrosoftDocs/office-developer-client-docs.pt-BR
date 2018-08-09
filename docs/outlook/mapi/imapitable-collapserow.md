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
ms.openlocfilehash: 1fd711683ff476ef5d381bca2f9db6bc25b07c68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767325"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**Aplica-se a**: Outlook 
  
Recolhe uma categoria de tabela expandida, removendo qualquer títulos de nível inferior e linhas da folha que pertencem à categoria da visualização de tabela.
  
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
  
> [in] A contagem de bytes na propriedade PR_INSTANCE_KEY apontado pelo parâmetro _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> [in] Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica a linha de título para a categoria. 
    
 _ulFlags_
  
> Reservado; deve ser zero.
    
 _lpulRowCount_
  
> [out] Um ponteiro para o número total de linhas que estão sendo removidos do modo de exibição de tabela.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A operação de recolher teve êxito.
    
E_NOT_FOUND 
  
> A linha identificada pelo parâmetro _pbInstanceKey_ não existe. 
    
MAPI_E_INVALID_ENTRYID 
  
> A linha identificada pelo parâmetro _pbInstanceKey_ não existe. Esse erro é uma alternativa ao E_NOT_FOUND; provedores de serviços podem retornar qualquer deles. 
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::CollapseRow** recolhe uma categoria de tabela e a remove do modo de exibição de tabela. As linhas são contraídas começando na linha identificada pela propriedade **PR_INSTANCE_KEY** apontada pelo parâmetro _pbInstanceKey_ . O número de linhas que foram removidos do modo de exibição é retornado no conteúdo do parâmetro _lpulRowCount_ . 
  
Notificações nunca são geradas para as linhas de tabela que são removidas de um modo de exibição como resultado de uma operação de recolher. 
  
Quando uma linha que é definida por um indicador é recolhida fora do modo de exibição, o indicador é movido para apontar para a próxima linha visível. 
  
Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |MFCMAPI usa o método **IMAPITable::CollapseRow** para recolher uma categoria de tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

