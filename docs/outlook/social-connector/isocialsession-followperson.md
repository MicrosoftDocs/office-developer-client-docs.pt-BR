---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Adiciona a pessoa identificada pelo parâmetro emailAddress como um amigo para o usuário de logon na rede social.
ms.openlocfilehash: 6dc289801c99f2f3bf1647e9c98c072d2f53d066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770856"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Adiciona a pessoa identificada pelo parâmetro _emailAddress_ como um amigo para o usuário de logon na rede social. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Parâmetros

_emailAddress_
  
> [in] Uma cadeia de caracteres que contém um endereço de email de uma pessoa.
    
## <a name="remarks"></a>Comentários

O parâmetro _emailAddress_ deve ser um endereço SMTP válido. Se o provedor do Outlook Social Connector (OSC) definiu o método **followPerson** como **true** nos **recursos**e o argumento de _emailAddress_ não corresponde a um usuário na rede, o provedor deve retornar o OSC_E_NOT_FOUND erro. Se o provedor definiu **followPerson** como **false** em **recursos**, o provedor deve retornar o erro OSC_E_FAIL.
  
Se o provedor implementa a interface [ISocialSession2](isocialsession2iunknown.md) e definiu **followPerson** como **true** em **recursos**, o OSC chamará [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) em vez de **ISocialSession::FollowPerson **. Se o provedor não implementa a interface **ISocialSession2** ou **ISocialSession2::FollowPersonEx** retorna o erro OSC_E_NOTIMPL, o OSC chamará **ISocialSession::FollowPerson** desde que o provedor definiu ** followPerson** como **true** em **recursos**. Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).
  
Ao decidir se para implementar **ISocalSession::FollowPerson** ou **ISocialSession2::FollowPersonEx**, você deve considerar se seu provedor precisa os outros métodos **ISocialSession2**e se você pode usar o _ djsplayName_ parâmetro em **FollowPersonEx**.
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

