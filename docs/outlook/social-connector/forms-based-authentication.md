---
title: Autenticação baseada em formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: Outlook Social Connector (OSC) chama o método ISocialProvider::GetCapabilities para determinar os recursos do provedor de OSC para uma rede social.
ms.openlocfilehash: bf6534b72af7db92e02bed74f2028a086b26cbcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770835"
---
# <a name="forms-based-authentication"></a>Autenticação baseada em formulários

Outlook Social Connector (OSC) chama o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar os recursos do provedor de OSC para uma rede social. O OSC usa os recursos retornados para determinar como oferecer suporte a um usuário do Office que está fazendo logon com essa rede social. 

Se o elemento de **useLogonWebAuth** em **recursos** retornado XML indica que o provedor do OSC suporta a autenticação baseada em formulários, o OSC pode fazer a seguinte sequência de chamada para permitir que um usuário fazer logon na rede social: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; O OSC carrega o provedor. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; O OSC obtém uma string que representa o número da versão do provedor para esta rede social. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; O OSC obtém uma string que representa o nome de rede social. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; O OSC obtém uma GUID imutável que representa a rede social. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; O OSC obtém uma string que representa os recursos do provedor e que está em conformidade com a definição de esquema para o elemento de **recursos** . 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; O OSC obtém uma matriz de bytes que representa o ícone para o site de rede social. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; O OSC obtém uma interface [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; O OSC inicializa fazer logon no site de rede social pela autenticação baseada em formulários. Essa chamada logon inicial, o OSC passa **Nulo** para o parâmetro _connectIn_ . 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; O OSC obtém a URL para exibir um formulário baseado em navegador para o usuário durante a autenticação da web. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; O OSC conclui o logon para o site de rede social usando a autenticação baseada em formulários. O OSC chama esse método uma segunda vez, passando a URL do formulário de logon para o provedor no parâmetro _connectIn_ . 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; O OSC obtém uma interface [ISocialProfile](isocialprovideriunknown.md) que representa o usuário conectado. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; O OSC obtém uma string que representa um identificador exclusivo para um site de rede social. O identificador de rede pode ser equivalente ao nome de rede. 
    
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [Sequências de chamadas comuns do OSC](osc-typical-calling-sequences.md)

