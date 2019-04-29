---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Adiciona a pessoa identificada pelo parâmetro emailAddress como um amigo para o usuário conectado na rede social.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423255"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Adiciona a pessoa identificada pelo parâmetro _EmailAddress_ como um amigo para o usuário conectado na rede social. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Parâmetros

_emailAddress_
  
> no Uma cadeia de caracteres que contém um endereço de email de uma pessoa.
    
## <a name="remarks"></a>Comentários

O parâmetro _EmailAddress_ deve ser um endereço SMTP válido. Se o provedor do Outlook Social Connector (OSC) tiver definido o método **followPerson** como **true** nos **recursos**e o argumento para _EmailAddress_ não corresponder a um usuário na rede, o provedor deverá retornar o OSC_E_NOT_FOUND erros. Se o provedor tiver definido **followPerson** como **falso** em **recursos**, o provedor deverá retornar o erro OSC_E_FAIL.
  
Se o provedor implementar a interface [ISocialSession2](isocialsession2iunknown.md) e tiver definido **followPerson** como **true** nos **recursos**, o OSC chamará [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) em vez de **ISocialSession:: followPerson **. Se o provedor não implementar a interface **ISocialSession2** ou **ISocialSession2:: FollowPersonEx** retorna o erro OSC_E_NOTIMPL, o OSC chamará **ISocialSession:: FollowPerson** , desde que o provedor tenha definido ** followPerson** como **verdadeiro** em **recursos**. Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).
  
Ao decidir se deve implementar **ISocalSession:: FollowPerson** ou **ISocialSession2:: FollowPersonEx**, você deve considerar se o provedor precisa de outros métodos no **ISocialSession2**e se você pode usar o _ parâmetro djsplayName_ em **FollowPersonEx**.
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

