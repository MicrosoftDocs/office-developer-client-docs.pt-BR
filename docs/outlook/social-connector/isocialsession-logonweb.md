---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Faz o login no site da rede social usando a autenticação baseada em formulários.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430333"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Faz o login no site da rede social usando a autenticação baseada em formulários.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parâmetros

_connectIn_
  
> [in] Uma cadeia de caracteres nula **,** uma URL para um formulário de logon na Web ou uma cadeia de caracteres que contém credenciais de logon, dependendo do contexto no processo de logon quando esse método é chamado.
    
_connectOut_
  
> [out] Uma cadeia de caracteres que contém credenciais de logon.
    
## <a name="remarks"></a>Comentários

O Outlook Social Connector (OSC) chama o **método LogonWeb** somente se o provedor indicar que ele oferece suporte à autenticação baseada em formulários. O provedor indica que requer autenticação baseada em formulários definindo **useLogonWebAuth** como **verdadeiro** no XML para **recursos.** Se o provedor definir **useLogonWebAuth** como **false**, o OSC usa autenticação básica e chama o método [ISocialSession::Logon](isocialsession-logon.md). 
  
Fazer logon em um site de rede social usando autenticação baseada em formulários envolve chamar os métodos **LogonWeb** e [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) em uma ordem específica: 
  
1. O OSC chama **LogonWeb** pela primeira vez, passando **nulo** para _o parâmetro connectIn._ 
    
2. O provedor gera o OSC_E_AUTH_ERROR erro para o OSC.
    
3. Em seguida, o OSC **chama GetLogonUrl**.
    
4. O provedor retorna a URL apropriada para uma página de logon no **método GetLogonUrl.** 
    
5. O OSC usa a URL retornada **por GetLogonUrl** para exibir a página de logon baseada em formulários. 
    
6. Em seguida, o OSC **chama LogonWeb** uma segunda vez, passando a URL para o formulário de logon no _parâmetro connectIn._ 
    
7. Se a autenticação for bem-sucedida, o provedor retornará credenciais de logon no  _parâmetro connectOut_ para o OSC. Se a autenticação falhar, o provedor a OSC_E_AUTH_ERROR para o OSC. 
    
Se o provedor OSC suportar o logon usando credenciais armazenadas em cache, ele **especificará useLogonCached** como **true** no XML **de recursos.** O provedor deve colocar quaisquer credenciais de logon na cadeia de caracteres  _connectOut_ que o provedor deseja que o OSC armazene entre conexões. O OSC não interpreta a _cadeia de caracteres connectOut._ Depois que o OSC verifica se **o uso deLogonCached** é **verdadeiro,** o OSC criptografa a cadeia de caracteres para segurança antes de armazenar no Registro do Windows. O OSC passa essa cadeia de caracteres para o parâmetro  _connectIn_ em tentativas subsequentes de fazer logon na rede social chamando [ISocialSession2::LogonCached](isocialsession2-logoncached.md). 
  
Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Autenticação baseada em formulários](forms-based-authentication.md)

