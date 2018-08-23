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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 989c6872e78ef78e5e0b18149a186d4f920ca603
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563461"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui uma linha da tabela.
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parâmetros

 _lpSPropValue_
  
> [in] Um ponteiro para uma estrutura de valor de propriedade que descreve a coluna de índice da linha a ser excluído. O membro **ulPropTag** da estrutura de valor de propriedade deve conter a mesma marca de propriedade, como o parâmetro _ulPropTagIndexColumn_ da chamada para a função [CreateTable](createtable.md) . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A linha foi excluída com êxito.
    
E_NOT_FOUND 
  
> A propriedade apontada pelo parâmetro _lpSPropValue_ não identifica uma linha da tabela. 
    
## <a name="remarks"></a>Comentários

O método **ITableData::HrDeleteRow** remove a linha da tabela que contém a coluna que coincida com a propriedade apontada pelo parâmetro _lpSPropValue_ . Os dados para a linha serão excluídos e a linha é removida do open todos os modos de exibição. 
  
Depois que a linha foi excluída, as notificações são enviadas para todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamou o método da tabela [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações. 
  
A exclusão de uma linha não reduz o conjunto de colunas que está disponível para modos de exibição existentes ou aberto subsequentemente modos de exibição, mesmo se a linha excluída é a última linha que tem um valor para uma coluna específica.
  
## <a name="see-also"></a>Confira também



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

