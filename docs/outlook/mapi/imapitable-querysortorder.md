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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b5eb671be022a6c3aa22e66f68386691fe23b275
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767334"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**Aplica-se a**: Outlook 
  
Recupera a ordem de classificação atual para uma tabela.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Parâmetros

 _lppSortCriteria_
  
> [out] Ponteiro para um ponteiro para a estrutura de [SSortOrderSet](ssortorderset.md) mantendo a ordem de classificação atual. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A ordem de classificação atual foi retornada com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede que a operação de recuperação de ordem de classificação seja iniciado. Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::QuerySortOrder** recupera a ordem de classificação atual para uma tabela. Ordens de classificação são descritas com uma estrutura [SSortOrderSet](ssortorderset.md) . 
  
- O membro **cSorts** da estrutura **SSortOrderSet** pode ser definido como zero se: 
    
- A tabela está sem classificação.
    
- Não há nenhuma informação sobre como a tabela é classificada.
    
- A estrutura de **SSortOrderSet** não é apropriada para descrever a ordem de classificação. 
    
## <a name="notes-to-implementers"></a>Notas para implementadores

Se uma chamada for feita para o seu método [IMAPITable:: SortTable](imapitable-sorttable.md) com uma estrutura **SSortOrderSet** contendo zero colunas na chave de classificação, remova a ordem de classificação atual e aplicar a ordem padrão, se houver uma. Em chamadas subsequentes para **QuerySortOrder**, você pode escolher se deseja retornar zero ou mais colunas para a chave de classificação. Você pode retornar mais colunas que estão no modo de exibição presente.
  
Para obter mais informações sobre a classificação, consulte [classificação e categorização](sorting-and-categorization.md).
  
## <a name="see-also"></a>Confira também



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

