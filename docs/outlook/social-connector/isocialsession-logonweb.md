---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Logs para o site de rede social usando a autenticação baseada em formulários.
ms.openlocfilehash: 4af0301d5b619ce7f9ff54b97f54b4b00408a564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770864"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Logs para o site de rede social usando a autenticação baseada em formulários.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parâmetros

_connectIn_
  
> [in] Uma string que é **Nulo**, uma URL para um formulário de logon na web, ou uma cadeia de caracteres que contém as credenciais de logon, dependendo do contexto no processo de logon, quando esse método é chamado.
    
_connectOut_
  
> [out] Uma cadeia de caracteres que contém as credenciais de logon.
    
## <a name="remarks"></a>Comentários

Outlook Social Connector (OSC) chama o método **LogonWeb** somente se o provedor indica que ele oferece suporte a autenticação baseada em formulários. O provedor indica que ele requer autenticação baseada em formulários, definindo **useLogonWebAuth** como **true** no XML de **recursos**. Se o provedor define **useLogonWebAuth** como **false**, o OSC usará a autenticação básica e chama o método [ISocialSession::Logon](isocialsession-logon.md) . 
  
Fazer logon em um site de rede social usando a autenticação baseada em formulários envolve chamando os métodos **LogonWeb** e [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) em uma ordem específica: 
  
1. O OSC chama **LogonWeb** na primeira vez, passando **Nulo** para o parâmetro _connectIn_ . 
    
2. O provedor gera o erro OSC_E_AUTH_ERROR para o OSC.
    
3. Em seguida, o OSC chama **GetLogonUrl**.
    
4. O provedor retorna a URL adequada para uma página de logon no método **GetLogonUrl** . 
    
5. O OSC usa a URL retornada pela **GetLogonUrl** para exibir a página de logon baseada em formulários. 
    
6. O OSC chama **LogonWeb** uma segunda vez, passando a URL para o formulário de logon no parâmetro _connectIn_ . 
    
7. Se a autenticação tiver êxito, o provedor retorna as credenciais de logon no parâmetro _connectOut_ para o OSC. Se a autenticação falhar, o provedor gera o erro OSC_E_AUTH_ERROR para o OSC. 
    
Se o provedor do OSC suporta logon usando as credenciais armazenadas em cache, ele especifica **useLogonCached** como **true** em **recursos** XML. O provedor deve colocar qualquer credenciais de logon na cadeia de caracteres _connectOut_ que deseja que o provedor do OSC para armazenar nas conexões. O OSC não interpretar a cadeia de caracteres _connectOut_ . Depois que o OSC verifica que **useLogonCached** for **true**, o OSC criptografa a cadeia de caracteres para segurança antes de armazená-lo no registro do Windows. O OSC passa essa cadeia de caracteres para o parâmetro _connectIn_ em fazer logon rede social chamando [ISocialSession2::LogonCached](isocialsession2-logoncached.md)as tentativas posteriores. 
  
Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Autenticação baseada em formulários](forms-based-authentication.md)

