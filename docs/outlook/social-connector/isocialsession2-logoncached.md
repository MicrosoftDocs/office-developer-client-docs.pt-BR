---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Logs para o site de rede social usando credenciais armazenadas em cache.
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770871"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Logs para o site de rede social usando credenciais armazenadas em cache.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parâmetros

_connectIn_
  
> [in] Uma cadeia de caracteres que pode ser vazia ou contém as credenciais de logon, dependendo do contexto no qual o OSC está chamando **LogonCached**.
    
_userName_
  
> [in] Uma cadeia de caracteres que contém o nome de usuário.
    
_senha_
  
> [in] Uma cadeia de caracteres que contém a senha do usuário.
    
_connectOut_
  
> [out] Uma cadeia de caracteres opaca que contém as credenciais.
    
## <a name="remarks"></a>Comentários

Este método é chamado para autenticação somente se **useLogonCached** estiver definida como **true** nas **capacidades** XML retornado pelo [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).
  
Outlook Social Connector (OSC) chamará o **LogonCached**e passará uma sequência vazia para _connectIn_ e não vazias cadeias de caracteres de _nome de usuário_ e _senha_ . O provedor usa o _nome de usuário_ e _senha_ para fazer logon na rede social e retorna um parâmetro opaco _connectOut_ para o OSC se a autenticação tiver êxito. Se a autenticação falhar, o provedor retorna o erro OSC_E_LOGON_FAILURE para o OSC. 
  
O parâmetro _connectOut_ é uma sequência de caracteres opaca para o OSC e é passado para o parâmetro _connectIn_ as tentativas posteriores pelo OSC para fazer logon na rede social. O provedor deve colocar qualquer credenciais na cadeia de caracteres _connectOut_ que deseja que o provedor do OSC para armazenar nas conexões. O OSC não interpreta a cadeia de caracteres em _connectOut_e criptografa a cadeia de caracteres para fins de segurança antes de armazená-lo no registro do Windows.
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

