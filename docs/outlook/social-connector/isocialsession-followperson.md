---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Adiciona a pessoa identificada pelo parâmetro emailAddress como um amigo do usuário conectado na rede social.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423255"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Adiciona a pessoa identificada pelo  _parâmetro emailAddress_ como um amigo do usuário conectado na rede social. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Parâmetros

_emailAddress_
  
> [in] Uma cadeia de caracteres que contém um endereço de email de uma pessoa.
    
## <a name="remarks"></a>Comentários

O  _parâmetro emailAddress_ deve ser um endereço SMTP válido. Se o provedor do Outlook Social Connector (OSC) tiver definido o método **followPerson** como true em recursos e o argumento para _emailAddress_ não corresponder a um usuário na rede, o provedor deverá retornar o erro OSC_E_NOT_FOUND.  Se o provedor definiu **followPerson como** **falso** **nos** recursos, o provedor deve retornar o OSC_E_FAIL erro.
  
Se o provedor implementa a interface [ISocialSession2](isocialsession2iunknown.md) e definiu **followPerson** como **true** **em** recursos , o OSC chamará [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) em vez de **ISocialSession::FollowPerson**. Se o provedor não implementar OSC_E_NOTIMPL interface **ISocialSession2** ou **ISocialSession2::FollowPersonEx** retornar o erro OSC_E_NOTIMPL, o OSC chamará **ISocialSession::FollowPerson,** desde que o provedor tenha definido **followPerson** como **verdadeiro** em **recursos.** Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).
  
Ao decidir se **implementará ISocalSession::FollowPerson** ou **ISocialSession2::FollowPersonEx**, você deve considerar se seu provedor precisa dos outros métodos em **ISocialSession2** e se você pode usar o parâmetro  _djsplayName_ em **FollowPersonEx**.
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

