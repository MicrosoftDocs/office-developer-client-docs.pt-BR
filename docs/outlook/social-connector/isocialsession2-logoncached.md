---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Faz logon no site de rede social usando credenciais armazenadas em cache.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336502"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Faz logon no site de rede social usando credenciais armazenadas em cache.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parâmetros

_conectar-se_
  
> no Uma cadeia de caracteres que pode ser vazia ou contém as credenciais de logon, dependendo do contexto no qual o OSC está chamando **LogonCached**.
    
_userName_
  
> no Uma cadeia de caracteres que contém o nome de usuário.
    
_la_
  
> no Uma cadeia de caracteres que contém a senha do usuário.
    
_conexão_
  
> bota Uma cadeia de caracteres opaca que contém credenciais.
    
## <a name="remarks"></a>Comentários

Este método é chamado para autenticação somente se **useLogonCached** estiver definido como **true** no XML de **recursos** retornado por [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md).
  
O Outlook Social Connector (OSC) chama **LogonCached**e passa uma cadeia de caracteres vazia para cadeias de nome de _usuário_ e _senha_ de _conexão_ e não vazia. O provedor usa o _nome de usuário_ e _senha_ para fazer logon na rede social e retorna um parâmetro de _conexão_ opaco para o OSC se a autenticação for bem-sucedida. Se a autenticação falhar, o provedor retornará o erro OSC_E_LOGON_FAILURE para o OSC. 
  
O __ parâmetro connectout é uma cadeia de caracteres opaca para o OSC e é passado para o parâmetro _connectem_ em tentativas subsequentes pelo OSC para fazer logon na rede social. O provedor deve colocar qualquer credencial na cadeia de caracteres de _conexão_ que o provedor deseja que o OSC armazene entre as conexões. O OSC não interpreta a cadeia de caracteres __ em connectout e criptografa a cadeia de caracteres para fins de segurança antes de armazená-la no registro do Windows.
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

