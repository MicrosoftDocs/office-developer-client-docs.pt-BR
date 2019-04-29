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
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436045"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica que o sistema está ocioso, permitindo que o provedor de transporte realize operações de baixa prioridade.
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama periodicamente o método **IXPLogon:: Idle** , se solicitado, durante os horários em que o sistema está ocioso passando o sinalizador XP_LOGON_SP na chamada para o método [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) que abriu a sessão atual. Às vezes em que o sistema está ocioso, o provedor de transporte pode executar operações de plano de fundo que não são apropriadas durante outras chamadas ou que precisam ocorrer regularmente. 
  
## <a name="see-also"></a>Confira também



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

