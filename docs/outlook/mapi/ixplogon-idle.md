---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 12aa8b79e38320d9767a6c333cb0197ea5669862
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578007"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica que o sistema está ocioso, permitindo que o provedor de transporte executar operações de baixa prioridade.
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

O MAPI spooler periodicamente chama o método de **IXPLogon::Idle** , se solicitado, durante os horários quando o sistema está ocioso passando o sinalizador XP_LOGON_SP na chamada para o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) que aberto a sessão atual. Às vezes quando o sistema está ocioso, o provedor de transporte pode executar operações em segundo plano que não forem adequados durante outras chamadas ou que precisam ocorrer regularmente. 
  
## <a name="see-also"></a>Confira também



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

