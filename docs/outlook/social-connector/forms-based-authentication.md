---
title: Autenticação baseada em formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: O Outlook Social Connector (OSC) chama o método ISocialProvider::GetCapabilities para determinar os recursos do provedor OSC para uma rede social.
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435527"
---
# <a name="forms-based-authentication"></a>Autenticação baseada em formulários

O Outlook Social Connector (OSC) chama o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar os recursos do provedor OSC para uma rede social. O OSC usa os recursos retornados para determinar como dar suporte a um usuário do Office que está fazendo logon nessa rede social. 

Se o elemento **useLogonWebAuth** no **XML** de recursos retornados indicar que o provedor OSC oferece suporte à autenticação baseada em formulários, o OSC poderá fazer a seguinte sequência de chamada para permitir que um usuário faça logon nessa rede social: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; O OSC carrega o provedor. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; O OSC obtém uma cadeia de caracteres que representa o número de versão do provedor para essa rede social. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; O OSC obtém uma cadeia de caracteres que representa o nome da rede social. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; O OSC obtém um GUID imutável que representa a rede social. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; O OSC obtém uma cadeia de caracteres que representa os recursos do provedor e que está em conformidade com a definição de esquema para o **elemento capabilities.** 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; O OSC obtém uma matriz de byte que representa o ícone do site da rede social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; O OSC obtém uma interface [ISocialSession.](isocialsessioniunknown.md) 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; O OSC inicializa o logon no site da rede social por meio de autenticação baseada em formulários. Para essa chamada de logon inicial, o OSC passa **nulo** para o _parâmetro connectIn._ 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; O OSC obtém a URL para exibir um formulário baseado em navegador para o usuário durante a autenticação da Web. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; O OSC conclui o logon no site da rede social usando autenticação baseada em formulários. O OSC chama esse método uma segunda vez, passando a URL do formulário de logon para o provedor no _parâmetro connectIn._ 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; O OSC obtém uma interface [ISocialProfile](isocialprovideriunknown.md) que representa o usuário conectado. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; O OSC obtém uma cadeia de caracteres que representa um identificador exclusivo para um site de rede social. O identificador de rede pode ser equivalente ao nome da rede. 
    
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)

