---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Faz logon no site de rede social usando a autenticação baseada em formulários.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430333"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Faz logon no site de rede social usando a autenticação baseada em formulários.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parâmetros

_conectar-se_
  
> no Uma cadeia de caracteres que é **NULL**, uma URL para um formulário de logon na Web ou uma cadeia de caracteres que contém credenciais de logon, dependendo do contexto no processo de logon quando esse método é chamado.
    
_conexão_
  
> bota Uma cadeia de caracteres que contém credenciais de logon.
    
## <a name="remarks"></a>Comentários

O Outlook Social Connector (OSC) chama o método **LogonWeb** somente se o provedor indicar que oferece suporte à autenticação baseada em formulários. O provedor indica que ela requer autenticação baseada em formulários Configurando **useLogonWebAuth** como **true** no XML para **recursos**. Se o provedor definir **useLogonWebAuth** como **false**, o OSC usa autenticação básica e chama o método [ISocialSession::Logon](isocialsession-logon.md). 
  
Fazer logon em um site de rede social usando a autenticação baseada em formulários envolve chamar os métodos **LogonWeb** e [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md) em uma ordem específica: 
  
1. O OSC chama **LogonWeb** pela primeira vez, passando **NULL** para o __ parâmetro connectem. 
    
2. O provedor gera o erro OSC_E_AUTH_ERROR para o OSC.
    
3. O OSC chama **GetLogonUrl**.
    
4. O provedor retorna a URL apropriada para uma página de logon no método **GetLogonUrl** . 
    
5. O OSC usa a URL retornada por **GetLogonUrl** para exibir a página de logon baseada em formulários. 
    
6. Em seguida, o OSC chama **LogonWeb** uma segunda vez, passando a URL para o formulário de logon no parâmetro _connectem_ . 
    
7. Se a autenticação for bem-sucedida, o provedor retornará as credenciais de __ logon no parâmetro connectout para o OSC. Se a autenticação falhar, o provedor gerará o erro OSC_E_AUTH_ERROR para o OSC. 
    
Se o provedor do OSC suportar logon usando credenciais armazenadas em cache, ele especifica **useLogonCached** como **true** no XML **Capabilities** . O provedor deve colocar as credenciais de logon na cadeia de caracteres de _conexão_ que o provedor deseja que o OSC armazene entre as conexões. O OSC não interpreta a cadeia de caracteres de _conexão_ . Depois que o OSC verifica se **useLogonCached** é **true**, o OSC criptografa a cadeia de caracteres para segurança antes de armazená-la no registro do Windows. O OSC passa essa cadeia de caracteres __ para o parâmetro connectem em tentativas subsequentes de fazer logon na rede social chamando [ISocialSession2:: LogonCached](isocialsession2-logoncached.md). 
  
Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Autenticação baseada em formulários](forms-based-authentication.md)

