---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425271"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica se o provedor de transporte recebeu uma ou mais mensagens de entrada.
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>Parâmetros

 _lpulIncoming_
  
> [out] Um valor que indica a existência de mensagens de entrada. Um valor que não seja zero indica que há mensagens de entrada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama periodicamente o método **IXPLogon::P oll** se o provedor de transporte indicar que ele deve ser sondado para novas mensagens, o que o provedor faz passando o sinalizador LOGON_SP_POLL para a chamada para o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) no início de uma sessão. Se o provedor de transporte indicar em resposta à chamada de **Sondagem** que há uma ou mais mensagens de entrada disponíveis para processamento, o spooler MAPI chamará o método [IXPLogon::StartMessage](ixplogon-startmessage.md) para permitir que o provedor processe a primeira mensagem de entrada. O provedor de transporte indica mensagens de entrada definindo o valor no parâmetro  _lpulIncoming_ para um valor que não seja zero. 
  
## <a name="see-also"></a>Confira também



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

