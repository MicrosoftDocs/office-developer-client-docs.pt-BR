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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3426854e727ebce7a2ac2243491994ce0e066ac6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591377"
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
  
> [out] Um valor que indica a existência de mensagens de entrada. Um valor diferente de zero indica que não existem mensagens de entrada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

O MAPI spooler periodicamente chama o método **IXPLogon::Poll** se o provedor de transporte indica que ele deve ser sondado para novas mensagens, o qual o provedor passando o LOGON_SP_POLL sinalizar para a chamada para o [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) método no início de uma sessão. Se o provedor de transporte indica em resposta à chamada **votação** que há um ou mais mensagens de entrada disponíveis para ele ao processo, o MAPI spooler chama o método [IXPLogon::StartMessage](ixplogon-startmessage.md) para permitir que o provedor de processo na primeira entrada Mensagem. O provedor de transporte indica mensagens de entrada, definindo o valor no parâmetro _lpulIncoming_ para um valor diferente de zero. 
  
## <a name="see-also"></a>Confira também



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

