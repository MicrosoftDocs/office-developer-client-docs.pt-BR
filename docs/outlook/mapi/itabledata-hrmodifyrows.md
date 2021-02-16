---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d0074dd006fda6d44252011d0b979169e0c3d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405356"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Insere várias linhas de tabela, possivelmente substituindo linhas existentes.
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpSRowSet_
  
> [in] Um ponteiro para uma [estrutura SRowSet](srowset.md) que contém o conjunto de linhas a ser adicionado, substituindo as linhas existentes, se necessário. Uma das estruturas de valor de propriedade apontadas pelo membro **lpProps** de cada estrutura [SRow](srow.md) no conjunto de linhas deve conter a coluna de índice, o mesmo valor especificado no _parâmetro ulPropTagIndexColumn_ na chamada para a função [CreateTable.](createtable.md) 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As linhas foram inseridas ou modificadas com êxito.
    
MAPI_E_INVALID_PARAMETER 
  
> Uma ou mais das linhas passadas não tem uma coluna de índice. Se esse erro for retornado, nenhuma linha será alterada.
    
## <a name="remarks"></a>Comentários

O **método ITableData::HrModifyRows** insere as linhas descritas pela estrutura [SRowSet](srowset.md) apontada pelo _parâmetro lpSRowSet._ Se o valor da coluna de índice de uma linha no conjunto de linhas corresponde ao valor de uma linha existente na tabela, a linha existente é substituída. Se não existir uma linha que corresponde à que está incluída na estrutura **SRowSet,** **HrModifyRows** adiciona a linha ao final da tabela. 
  
Todos os exibições da tabela são modificados para incluir as linhas apontadas por  _lpSRowSet_. No entanto, se um ponto de vista tiver uma restrição no local que exclua uma linha, talvez ele não seja visível para o usuário. 
  
As colunas nas linhas apontadas por  _lpSRowSet_ não devem estar na mesma ordem que as colunas na tabela. O chamador também pode incluir como propriedades de colunas que não estão atualmente na tabela. Para exibições existentes, **HrModifyRows** disponibiliza essas novas colunas, mas não as inclui no conjunto de colunas atual. Para exibições futuras, **HrModifyRows** inclui as novas colunas no conjunto de colunas. 
  
Depois **que HrModifyRows** tiver adicionado as linhas, as notificações serão enviadas a todos os clientes ou provedores de serviços que tenham um modo de exibição da tabela e que tenham chamado o método [IMAPITable::Advise](imapitable-advise.md) da tabela para registrar para notificações. MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows. Se mais de oito linhas são afetadas pela **chamada HrModifyRows,** MAPI envia uma única notificação TABLE_CHANGED vez. 
  
## <a name="see-also"></a>Confira também



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

