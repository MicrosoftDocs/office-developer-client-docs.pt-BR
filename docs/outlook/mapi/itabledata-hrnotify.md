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
ms.openlocfilehash: aa2170bf4bedfb441ad4808f774f6f71d5caf85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413266"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Envia uma notificação para uma linha de tabela.
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser zero.
    
 _cValues_
  
> no A contagem de valores de propriedade na estrutura [SPropValue](spropvalue.md) apontada pelo parâmetro _lpSPropValue_ . 
    
 _lpSPropValue_
  
> no Um ponteiro para uma estrutura **SPropValue** que descreve os valores das colunas na linha de destino. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

O método **ITableData:: HrNotify** envia uma notificação TABLE_ROW_MODIFIED para a linha que corresponde à linha descrita pelas propriedades apontadas pelo parâmetro _lpSPropValue_ . O **HrNotify** envia a notificação independentemente de ocorrerem alterações na linha. Todos os clientes e provedores de serviço que possuem modos de exibição da tabela e chamaram imApitable [:: Advise](imapitable-advise.md) para registrar notificações em seus modos de exibição recebem esta notificação. 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

