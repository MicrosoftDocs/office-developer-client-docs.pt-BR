---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 20831901567f177ada70a6cea94db0537786db94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571434"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Envia uma notificação para uma linha da tabela.
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _cValues_
  
> [in] A contagem dos valores de propriedade na estrutura [SPropValue](spropvalue.md) apontado pelo parâmetro _lpSPropValue_ . 
    
 _lpSPropValue_
  
> [in] Um ponteiro para uma estrutura **SPropValue** que descreve os valores das colunas na linha destino. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

O método **ITableData::HrNotify** envia uma notificação de TABLE_ROW_MODIFIED para a linha que corresponde a linha descrita pelas propriedades apontadas pelo parâmetro _lpSPropValue_ . **HrNotify** envia a notificação independentemente se ocorreram alterações na linha. Todos os clientes e provedores de serviços que têm modos de exibição da tabela e tem chamado [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações nos seus modos de exibição recebem essa notificação. 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

