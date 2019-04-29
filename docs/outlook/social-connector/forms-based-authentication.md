---
title: Autenticação baseada em formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: 'O Outlook Social Connector (OSC) chama o método ISocialProvider:: GetCapabilities para determinar as funcionalidades do provedor do OSC para uma rede social.'
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435527"
---
# <a name="forms-based-authentication"></a>Autenticação baseada em formulários

O Outlook Social Connector (OSC) chama o método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) para determinar as funcionalidades do provedor do OSC para uma rede social. O OSC usa os recursos retornados para determinar como dar suporte a um usuário do Office que está fazendo logon nesta rede social. 

Se o elemento **useLogonWebAuth** no XML de **funcionalidades** retornado indicar que o provedor OSC dá suporte à autenticação baseada em formulários, o OSC poderá fazer a seguinte sequência de chamada para permitir que um usuário faça logon na rede social: 
  
1. [ISocialProvider:: Load](isocialprovider-load.md) &ndash; O OSC carrega o provedor. 
    
2. [ISocialProvider:: versão](isocialprovider-version.md) &ndash; O OSC Obtém uma cadeia de caracteres que representa o número da versão do provedor para esta rede social. 
    
3. [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; O OSC Obtém uma cadeia de caracteres que representa o nome da rede social. 
    
4. [ISocialProvider:: SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; O OSC Obtém um GUID imutável que representa a rede social. 
    
5. [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) &ndash; O OSC Obtém uma cadeia de caracteres que representa as funcionalidades do provedor e que está em conformidade com a definição de esquema para o elemento **Capabilities** . 
    
6. [ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; O OSC Obtém uma matriz de bytes que representa o ícone do site de rede social. 
    
7. [ISocialProvider:: GetSession](isocialprovider-getsession.md) &ndash; O OSC Obtém uma interface [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession:: LogonWeb](isocialsession-logonweb.md) &ndash; O OSC Inicializa o logon no site de rede social por autenticação baseada em formulários. Para essa chamada de logon inicial, o OSC passa **NULL** para o parâmetro _connectem_ . 
    
9. [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md) &ndash; O OSC Obtém a URL para exibir um formulário baseado em navegador para o usuário durante a autenticação da Web. 
    
10. [ISocialSession:: LogonWeb](isocialsession-logonweb.md) &ndash; O OSC conclui o logon no site de rede social usando a autenticação baseada em formulários. O OSC chama esse método uma segunda vez, passando a URL do formulário de logon para o provedor no parâmetro _connectem_ . 
    
11. [ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; O OSC Obtém uma interface [métodoisocialprofile](isocialprovideriunknown.md) que representa o usuário conectado. 
    
12. [ISocialSession:: GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; O OSC Obtém uma cadeia de caracteres que representa um identificador exclusivo para um site de rede social. O identificador de rede pode ser equivalente ao nome da rede. 
    
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)

