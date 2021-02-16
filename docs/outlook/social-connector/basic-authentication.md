---
title: Autenticação básica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: O Outlook Social Connector (OSC) chama o método ISocialProvider::GetCapabilities para determinar os recursos do provedor OSC para uma rede social.
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439923"
---
# <a name="basic-authentication"></a>Autenticação básica

O Outlook Social Connector (OSC) chama o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar os recursos do provedor OSC para uma rede social. O OSC usa os recursos retornados para determinar como dar suporte a um usuário do Office que está fazendo logon nessa rede social. Se o elemento **useLogonWebAuth** no **XML** de recursos retornados indicar que o provedor OSC dá suporte à autenticação básica, o OSC poderá fazer a seguinte sequência de chamada para permitir que um usuário faça logon nessa rede social: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) — O OSC carrega o provedor. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) — O OSC obtém uma cadeia de caracteres que representa o número de versão do provedor OSC. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — O OSC obtém uma cadeia de caracteres que representa o nome da rede social. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) — O OSC obtém um GUID imutável que representa a rede social. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) — O OSC obtém uma cadeia de caracteres que representa os recursos do provedor e que está em conformidade com a definição de esquema para o elemento **capabilities.** 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — O OSC obtém uma matriz de byte que representa o ícone do site da rede social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) — O OSC obtém uma interface [ISocialSession.](isocialsessioniunknown.md) 
    
8. [ISocialSession::Logon](isocialsession-logon.md) — o OSC faz logon do usuário no site da rede social usando o nome de usuário e a senha especificados. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — O OSC obtém uma interface [ISocialProfile](isocialprovideriunknown.md) que representa o usuário conectado. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — O OSC obtém uma cadeia de caracteres que representa um identificador exclusivo para um site de rede social. O identificador de rede pode ser equivalente ao nome da rede. 
    
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)

