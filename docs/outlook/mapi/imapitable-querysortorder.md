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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328858"
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
  
> bota Ponteiro para um ponteiro para a estrutura [SSortOrderSet](ssortorderset.md) que contém a ordem de classificação atual. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A ordem de classificação atual foi retornada com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento, o que impede a inicialização da operação de recuperação da ordem de classificação. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
## <a name="remarks"></a>Comentários

O método imApitable **:: QuerySortOrder** recupera a ordem de classificação atual para uma tabela. As ordens de classificação são descritas com uma estrutura [SSortOrderSet](ssortorderset.md) . 
  
- O membro **cSorts** da estrutura **SSortOrderSet** pode ser definido como zero se: 
    
- A tabela não está classificada.
    
- Não há informações sobre como a tabela é classificada.
    
- A estrutura **SSortOrderSet** não é adequada para descrever a ordem de classificação. 
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Se for feita uma chamada para o método imApitable [:: SortTable](imapitable-sorttable.md) com uma estrutura **SSortOrderSet** que contenha zero colunas na chave de classificação, remova a ordem de classificação atual e aplique a ordem padrão, se houver uma. Em chamadas subsequentes para **QuerySortOrder**, você pode escolher se deseja retornar zero ou mais colunas para a chave de classificação. Você pode retornar mais colunas do que no modo de exibição atual.
  
Para obter mais informações sobre classificação, consulte [classificação e categorização](sorting-and-categorization.md).
  
## <a name="see-also"></a>Confira também



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

