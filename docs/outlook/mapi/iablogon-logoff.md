---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416395"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicia o processo de logoff.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O processo de logoff foi iniciado com êxito.
    
## <a name="remarks"></a>Comentários

O processo de logoff geralmente é iniciado quando um cliente chama o método [IMAPISession::Logoff](imapisession-logoff.md) para encerrar uma sessão. MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process. 
  
O **método IABLogon::Logoff** faz o seguinte: 
  
- Libera todos os objetos abertos, como subobjetos ou o objeto de status.
    
- Libera o objeto de suporte do provedor.
    
Para obter mais informações sobre o processo de logoff de provedores de agendamento de endereços, consulte [Desligar um Provedor de Serviços.](shutting-down-a-service-provider.md)
  
## <a name="see-also"></a>Confira também



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

