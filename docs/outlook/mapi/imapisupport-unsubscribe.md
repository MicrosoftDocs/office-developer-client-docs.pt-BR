---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9ee071bb303c7518a23c5e57909f8618b7aebdde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767302"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**Aplica-se a**: Outlook 
  
Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method. 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Par�metros

 _ulConnection_
  
> [in] O n�mero de conex�o diferente de zero que representa o registro de notifica��o que tenha estabelecido por meio de **IMAPISupport::Subscribe**.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro de notifica��o foi cancelado.
    
E_NOT_FOUND 
  
> O n�mero de conex�o passado no par�metro  _ulConnection_ n�o existe. 
    
## <a name="remarks"></a>Coment�rios

O m�todo **IMAPISupport::Unsubscribe** � implementado para todos os objetos de suporte de provedor de servi�o. Provedores de servi�os de chamarem **Unsubscribe** para cancelar um registro de notifica��o configurado anteriormente pelo **Subscribe**. **Unsubscribe** cancela o registro, liberando o ponteiro de coletor de eventos advise passado na chamada **Subscribe**. 
  
Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call. However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns. 
  
## <a name="see-also"></a>Ver tamb�m



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

