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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1be4fd95d29859c542fe553bdc3728ea23444694
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767726"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**Aplica-se a**: Outlook 
  
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
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

O método **ITableData::HrNotify** envia uma notificação de TABLE_ROW_MODIFIED para a linha que corresponde a linha descrita pelas propriedades apontadas pelo parâmetro _lpSPropValue_ . **HrNotify** envia a notificação independentemente se ocorreram alterações na linha. Todos os clientes e provedores de serviços que têm modos de exibição da tabela e tem chamado [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações nos seus modos de exibição recebem essa notificação. 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

