---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b187cccc4505256b7ab4d580c30eeb2e15ebf574
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421673"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui uma linha de tabela.
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parâmetros

 _lpSPropValue_
  
> [in] Um ponteiro para uma estrutura de valores de propriedade que descreve a coluna de índice para a linha a ser excluída. O **membro ulPropTag** da estrutura de valores de propriedade deve conter a mesma marca de propriedade que o _parâmetro ulPropTagIndexColumn_ da chamada para a função [CreateTable.](createtable.md) 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A linha foi excluída com êxito.
    
MAPI_E_NOT_FOUND 
  
> A propriedade apontada pelo parâmetro  _lpSPropValue_ não identifica uma linha na tabela. 
    
## <a name="remarks"></a>Comentários

O **método ITableData::HrDeleteRow** remove a linha da tabela que contém a coluna que corresponde à propriedade apontada pelo _parâmetro lpSPropValue._ Os dados da linha são excluídos e a linha é removida de todos os exibições abertas. 
  
Depois que a linha é excluída, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que tenham chamado o método [IMAPITable::Advise](imapitable-advise.md) da tabela para registrar para notificações. 
  
Excluir uma linha não reduz o conjunto de colunas que está disponível para exibições existentes ou exibições abertas subsequentemente, mesmo que a linha excluída seja a última linha que tenha um valor para uma coluna específica.
  
## <a name="see-also"></a>Confira também



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

