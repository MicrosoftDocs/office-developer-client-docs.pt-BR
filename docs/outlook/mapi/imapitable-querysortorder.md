---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407547"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera a ordem de classificação atual para uma tabela.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Parâmetros

 _lppSortCriteria_
  
> [out] Ponteiro para um ponteiro para a [estrutura SSortOrderSet](ssortorderset.md) que mantém a ordem de classificação atual. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A ordem de classificação atual foi retornada com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede o início da operação de recuperação de ordem de classificação. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::QuerySortOrder** recupera a ordem de classificação atual de uma tabela. As ordens de classificação são descritas com [uma estrutura SSortOrderSet.](ssortorderset.md) 
  
- O **membro cSorts** da **estrutura SSortOrderSet** pode ser definido como zero se: 
    
- A tabela está sem classificação.
    
- Não há informações sobre como a tabela é ordenada.
    
- A **estrutura SSortOrderSet** não é apropriada para descrever a ordem de classificação. 
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Se uma chamada for feita para seu método [IMAPITable::SortTable](imapitable-sorttable.md) com uma estrutura **SSortOrderSet** contendo zero colunas na chave de classificação, remova a ordem de classificação atual e aplique a ordem padrão, se houver uma. Em chamadas subsequentes **para QuerySortOrder**, você pode optar por retornar zero ou mais colunas para a chave de classificação. Você pode retornar mais colunas do que as que estão no ponto de vista atual.
  
Para obter mais informações sobre classificação, consulte [Classificação e Categorização.](sorting-and-categorization.md)
  
## <a name="see-also"></a>Confira também



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

