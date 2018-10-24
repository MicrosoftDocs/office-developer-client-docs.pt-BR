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
ms.openlocfilehash: 06356d60b43d7e5be61d944c07001570bdd5c678
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571105"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Insere várias linhas de tabela, substituindo possivelmente linhas existentes.
  
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
  
> [in] Um ponteiro para uma estrutura [SRowSet](srowset.md) que contém o conjunto de linhas a ser adicionado, substituindo linhas existentes, se necessário. Uma das estruturas de valor de propriedade apontadas pelo membro **lpProps** cada estrutura [SRow](srow.md) na linha definido deve conter uma coluna de índice, o mesmo valor que foi especificado no parâmetro _ulPropTagIndexColumn_ na chamada para o [ CreateTable](createtable.md) função. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As linhas com êxito foram inseridas ou modificadas.
    
MAPI_E_INVALID_PARAMETER 
  
> Um ou mais das linhas no passado não tem uma coluna de índice. Se esse erro for retornado, nenhuma linha é alterada.
    
## <a name="remarks"></a>Comentários

O método **ITableData::HrModifyRows** insere as linhas descritas pela estrutura [SRowSet](srowset.md) apontada pelo parâmetro _lpSRowSet_ . Se o valor de índice de coluna de uma linha no conjunto de linha corresponder ao valor de uma linha existente na tabela, linha existente será substituída. Se não há nenhuma linha que corresponde o um incluída na estrutura de **SRowSet** , **HrModifyRows** adiciona a linha no final da tabela. 
  
Todos os modos de exibição da tabela são modificados para incluir as linhas apontadas pela _lpSRowSet_. No entanto, se um modo de exibição tiver uma restrição vigentes que exclui uma linha, talvez não seja visível para o usuário. 
  
As colunas nas linhas apontadas pela _lpSRowSet_ não precisará ser na mesma ordem como as colunas na tabela. O chamador também pode incluir como propriedades de colunas que não estão atualmente na tabela. Para modos de exibição existentes, **HrModifyRows** disponibiliza essas novas colunas, mas não inclui-los no conjunto atual de coluna. Para futuras exibições, **HrModifyRows** inclui as novas colunas no conjunto de colunas. 
  
Depois **HrModifyRows** tiver adicionado as linhas, as notificações são enviadas para todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamou o método da tabela [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações. MAPI envia notificações de TABLE_ROW_ADDED ou TABLE_ROW_MODIFIED para cada linha, até oito linhas. Se mais de oito linhas são afetadas pela chamada **HrModifyRows** , MAPI envia uma notificação de TABLE_CHANGED única em vez disso. 
  
## <a name="see-also"></a>Confira também



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

