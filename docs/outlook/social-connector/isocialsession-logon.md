---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: Faz logon no site da rede social usando o nome de usuário e a senha especificados.
ms.openlocfilehash: 7915097e456d6fafa713901f8074e6531bfaa001
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361037"
---
# <a name="isocialsessionlogon"></a>ISocialSession::Logon

Faz logon no site da rede social usando o nome de usuário e a senha especificados.
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a>Parâmetros

_username_
  
> [in] Uma cadeia de caracteres que contém o nome de usuário para logon.
    
_password_
  
> [in] Uma cadeia de caracteres que contém a senha para logon.
    
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

