---
title: Autenticação básica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Outlook Social Connector (OSC) chama o método ISocialProvider::GetCapabilities para determinar os recursos do provedor de OSC para uma rede social.
ms.openlocfilehash: 8287133445a4e8fa928f6b7724ab41ca9b58baf9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770847"
---
# <a name="basic-authentication"></a>Autenticação básica

Outlook Social Connector (OSC) chama o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar os recursos do provedor de OSC para uma rede social. O OSC usa os recursos retornados para determinar como oferecer suporte a um usuário do Office que está fazendo logon com essa rede social. Se o elemento de **useLogonWebAuth** em **recursos** retornado XML indica que o provedor do OSC suporta a autenticação básica, o OSC pode fazer a seguinte sequência de chamada para permitir que um usuário fazer logon na rede social: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) — o OSC carrega o provedor. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) — o OSC obtém uma string que representa o número da versão do provedor do OSC. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — o OSC obtém uma string que representa o nome de rede social. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) — o OSC obtém uma GUID imutável que representa a rede social. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) — o OSC obtém uma string que representa os recursos do provedor e que está em conformidade com a definição de esquema para o elemento de **recursos** . 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — o OSC obtém uma matriz de bytes que representa o ícone para o site de rede social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) — o OSC obtém uma interface [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession::Logon](isocialsession-logon.md) — o OSC logs do usuário no site de rede social usando o nome de usuário especificado e a senha. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — o OSC obtém uma interface [ISocialProfile](isocialprovideriunknown.md) que representa o usuário conectado. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — o OSC obtém uma string que representa um identificador exclusivo para um site de rede social. O identificador de rede pode ser equivalente ao nome de rede. 
    
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [Sequências de chamadas comuns do OSC](osc-typical-calling-sequences.md)

