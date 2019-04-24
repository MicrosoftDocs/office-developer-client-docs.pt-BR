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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348668"
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
  
> no Serve deve ser zero.
    
 _lpSRowSet_
  
> no Um ponteiro para uma estrutura [SRowSet](srowset.md) que contém o conjunto de linhas a serem adicionadas, substituindo linhas existentes, se necessário. Uma das estruturas de valor de propriedade apontadas pelo membro **lpProps** de cada estrutura [SRow](srow.md) no conjunto de linhas deve conter a coluna de índice, o mesmo valor que foi especificado no parâmetro _ulPropTagIndexColumn_ na chamada para o [ ](createtable.md)Função CreateTable. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As linhas foram inseridas ou modificadas com êxito.
    
MAPI_E_INVALID_PARAMETER 
  
> Uma ou mais das linhas passadas não têm uma coluna de índice. Se esse erro for retornado, nenhuma linha será alterada.
    
## <a name="remarks"></a>Comentários

O método **ITableData:: HrModifyRows** insere as linhas descritas pela estrutura [SRowSet](srowset.md) apontada pelo parâmetro _lpSRowSet_ . Se o valor da coluna de índice de uma linha no conjunto de linhas corresponder ao valor de uma linha existente na tabela, a linha existente será substituída. Se não existir nenhuma linha que coincida com a incluída na estrutura **SRowSet** , **HrModifyRows** adicionará a linha ao final da tabela. 
  
Todos os modos de exibição da tabela são modificados para incluir as linhas apontadas pelo _lpSRowSet_. No enTanto, se um modo de exibição tiver uma restrição no lugar que exclua uma linha, ele pode não estar visível para o usuário. 
  
As colunas nas linhas apontadas por _lpSRowSet_ não precisam estar na mesma ordem das colunas da tabela. O chamador também pode incluir as propriedades de colunas que não estão na tabela no momento. Para modos de exibição existentes, o **HrModifyRows** torna essas novas colunas disponíveis, mas não as inclui no conjunto de colunas atual. Para modos de exibição futuros, o **HrModifyRows** inclui as novas colunas no conjunto de colunas. 
  
Após o **HrModifyRows** ter adicionado as linhas, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamaram o método IMAPITable [:: Advise](imapitable-advise.md) da tabela para se registrarem para notificações. MAPI envia notificações TABLE_ROW_ADDED ou TABLE_ROW_MODIFIED para cada linha, até oito linhas. Se mais de oito linhas forem afetadas pela chamada **HrModifyRows** , o MAPI enviará uma única notificação TABLE_CHANGED em vez disso. 
  
## <a name="see-also"></a>Confira também



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

