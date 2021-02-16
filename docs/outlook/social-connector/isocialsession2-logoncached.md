---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Faz o login no site da rede social usando credenciais armazenadas em cache.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436619"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Faz o login no site da rede social usando credenciais armazenadas em cache.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parâmetros

_connectIn_
  
> [in] Uma cadeia de caracteres que pode estar vazia ou contém as credenciais de logon, dependendo do contexto no qual o OSC está chamando **LogonCached**.
    
_userName_
  
> [in] Uma cadeia de caracteres que contém o nome de usuário.
    
_password_
  
> [in] Uma cadeia de caracteres que contém a senha do usuário.
    
_connectOut_
  
> [out] Uma cadeia de caracteres opaca que contém credenciais.
    
## <a name="remarks"></a>Comentários

Esse método é chamado para autenticação somente se **useLogonCached** for definido como **true** nos recursos **XML** retornados por [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).
  
O Outlook Social Connector (OSC) chama **LogonCached** e passa uma cadeia de caracteres vazia para cadeias de caracteres _userName_ e _password_ não vazias e _connectIn._ O provedor usa  _userName_ e senha para fazer logon na rede social e retorna um parâmetro _connectOut_ opaco ao OSC se a autenticação for bem-sucedida. Se a autenticação falhar, o provedor retornará o OSC_E_LOGON_FAILURE para o OSC. 
  
O  _parâmetro connectOut_ é uma cadeia de caracteres opaca para o OSC e é passado para o parâmetro  _connectIn_ em tentativas subsequentes pelo OSC de fazer logon na rede social. O provedor deve colocar quaisquer credenciais na cadeia de caracteres  _connectOut_ que o provedor deseja que o OSC armazene entre conexões. O OSC não interpreta a cadeia de caracteres em  _connectOut_ e criptografa a cadeia de caracteres para fins de segurança antes de armazenar no Registro do Windows.
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

