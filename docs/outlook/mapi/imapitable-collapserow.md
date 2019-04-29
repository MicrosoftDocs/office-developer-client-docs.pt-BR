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
  
Recolhe uma categoria de tabela expandida, removendo quaisquer títulos de nível inferior e linhas de folha pertencentes à categoria do modo de exibição de tabela.
  
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
  
> no A contagem de bytes na propriedade PR_INSTANCE_KEY indicada pelo parâmetro _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> no Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica a linha de título para a categoria. 
    
 _ulFlags_
  
> Serve deve ser zero.
    
 _lpulRowCount_
  
> bota Um ponteiro para o número total de linhas que estão sendo removidas do modo de exibição de tabela.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de recolhimento foi bem-sucedida.
    
MAPI_E_NOT_FOUND 
  
> A linha identificada pelo parâmetro _pbInstanceKey_ não existe. 
    
MAPI_E_INVALID_ENTRYID 
  
> A linha identificada pelo parâmetro _pbInstanceKey_ não existe. Este erro é uma alternativa ao MAPI_E_NOT_FOUND; os provedores de serviços podem retornar um. 
    
## <a name="remarks"></a>Comentários

O método imApitable **:: CollapseRow** recolhe uma categoria de tabela e a remove da exibição de tabela. As linhas são recolhidas começando pela linha identificada pela propriedade **PR_INSTANCE_KEY** indicada pelo parâmetro _pbInstanceKey_ . O número de linhas que são removidas do modo de exibição é retornado no conteúdo do parâmetro _lpulRowCount_ . 
  
As notificações nunca são geradas para linhas de tabela que são removidas de um modo de exibição como resultado de uma operação de recolhimento. 
  
Quando uma linha definida por um indicador é recolhida da exibição, o indicador é movido para apontar para a próxima linha visível. 
  
Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI usa o método imApitable **:: CollapseRow** para recolher uma categoria de tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

