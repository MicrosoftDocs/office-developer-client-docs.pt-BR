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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a1388545597cf0000f270bf693c93f9349fb6426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767731"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**Aplica-se a**: Outlook 
  
Insere uma nova linha de tabela, possivelmente, substituindo uma linha existente.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parâmetros

 _lpSRow_
  
> [in] Um ponteiro para uma estrutura de [SRow](srow.md) que descreve a linha a ser adicionado ou substituir uma linha existente. Uma das estruturas de valor de propriedade apontadas pelo membro **lpProps** da estrutura **SRow** deve conter uma coluna de índice, o mesmo valor que foi especificado no parâmetro _ulPropTagIndexColumn_ na chamada para o [CreateTable ](createtable.md)função. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A linha foi inserida ou modificada com êxito.
    
MAPI_E_INVALID_PARAMETER 
  
> A linha no passado não tem uma coluna de índice.
    
## <a name="remarks"></a>Comentários

O método **ITableData::HrModifyRow** insere a linha descrita pela estrutura **SRow** apontada pelo parâmetro _lpSRow_ . Se uma linha que tem o mesmo valor para a coluna de seu índice como a linha que aponta de _lpSRow_ para já existe na tabela, linha existente será substituída. Se não há nenhuma linha que corresponde o um incluída na estrutura de **SRow** , **HrModifyRow** adiciona a linha no final da tabela. 
  
Todos os modos de exibição da tabela são modificados para incluir a linha apontada pela _lpSRow_. No entanto, se um modo de exibição tiver uma restrição vigentes que exclui a linha, talvez não seja visível para o usuário. 
  
As colunas na linha apontado pela _lpSRow_ não precisará ser na mesma ordem como as colunas na tabela. O chamador também pode incluir como propriedades de colunas que não estão atualmente na tabela. Para modos de exibição existentes, **HrModifyRow** disponibiliza essas novas colunas, mas não inclui-los no conjunto atual de coluna. Para futuras exibições, **HrModifyRow** inclui as novas colunas no conjunto de colunas. 
  
Após **HrModifyRow** adiciona a linha, as notificações são enviadas para todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamou o método da tabela [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações. 
  
## <a name="see-also"></a>Confira também



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

