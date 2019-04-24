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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278855"
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
  
> no Um ponteiro para uma estrutura de valor de propriedade que descreve a coluna de índice da linha a ser excluída. O membro **ulPropTag** da estrutura de valor da propriedade deve conter a mesma marca de propriedade que o parâmetro _ulPropTagIndexColumn_ da chamada para a função [CreateTable](createtable.md) . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A linha foi excluída com êxito.
    
MAPI_E_NOT_FOUND 
  
> A propriedade indicada pelo parâmetro _lpSPropValue_ não identifica uma linha na tabela. 
    
## <a name="remarks"></a>Comentários

O método **ITableData:: HrDeleteRow** remove a linha da tabela que contém a coluna que corresponde à propriedade indicada pelo parâmetro _lpSPropValue_ . Os dados para a linha são excluídos e a linha é removida de todos os modos de exibição abertos. 
  
Depois que a linha é excluída, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamaram o método imApitable [:: Advise](imapitable-advise.md) da tabela para se registrarem para notificações. 
  
A exclusão de uma linha não reduz o conjunto de colunas que está disponível para modos de exibição existentes ou abertos subsequentemente, mesmo que a linha excluída seja a última linha que tenha um valor para uma coluna específica.
  
## <a name="see-also"></a>Confira também



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

