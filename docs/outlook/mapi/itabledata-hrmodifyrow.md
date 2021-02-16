---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408996"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Insere uma nova linha de tabela, possivelmente substituindo uma linha existente.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parâmetros

 _lpSRow_
  
> [in] Um ponteiro para uma [estrutura SRow](srow.md) que descreve a linha a ser adicionada ou para substituir uma linha existente. Uma das estruturas de valor de propriedade apontadas pelo membro **lpProps** da estrutura **SRow** deve conter a coluna de índice, o mesmo valor especificado no parâmetro _ulPropTagIndexColumn_ na chamada para a função [CreateTable.](createtable.md) 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A linha foi inserida ou modificada com êxito.
    
MAPI_E_INVALID_PARAMETER 
  
> A linha passada não tem uma coluna de índice.
    
## <a name="remarks"></a>Comentários

O **método ITableData::HrModifyRow** insere a linha descrita pela estrutura **SRow** apontada pelo _parâmetro lpSRow._ Se uma linha com o mesmo valor de sua coluna de índice que a linha  _que lpSRow_ aponta já existir na tabela, a linha existente será substituída. Se não existir uma linha que corresponde à que está incluída na estrutura **SRow,** **HrModifyRow** adiciona a linha ao final da tabela. 
  
Todos os exibições da tabela são modificados para incluir a linha apontada por  _lpSRow_. No entanto, se um ponto de vista tiver uma restrição no local que exclua a linha, talvez ele não seja visível para o usuário. 
  
As colunas na linha apontada por  _lpSRow_ não devem estar na mesma ordem que as colunas na tabela. O chamador também pode incluir como propriedades de colunas que não estão atualmente na tabela. Para exibições existentes, **HrModifyRow** disponibiliza essas novas colunas, mas não as inclui no conjunto de colunas atual. Para exibições futuras, **HrModifyRow** inclui as novas colunas no conjunto de colunas. 
  
Depois **que HrModifyRow** adiciona a linha, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamam o método [IMAPITable::Advise](imapitable-advise.md) da tabela para registrar para notificações. 
  
## <a name="see-also"></a>Confira também



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

