---
title: Autenticação básica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: 'O Outlook Social Connector (OSC) chama o método ISocialProvider:: GetCapabilities para determinar as funcionalidades do provedor do OSC para uma rede social.'
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281214"
---
# <a name="basic-authentication"></a><span data-ttu-id="6135a-103">Autenticação básica</span><span class="sxs-lookup"><span data-stu-id="6135a-103">Basic authentication</span></span>

<span data-ttu-id="6135a-104">O Outlook Social Connector (OSC) chama o método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) para determinar as funcionalidades do provedor do OSC para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="6135a-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="6135a-105">O OSC usa os recursos retornados para determinar como dar suporte a um usuário do Office que está fazendo logon nesta rede social.</span><span class="sxs-lookup"><span data-stu-id="6135a-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="6135a-106">Se o elemento **useLogonWebAuth** no XML de **funcionalidades** retornado indicar que o provedor OSC dá suporte à autenticação básica, o OSC poderá fazer a seguinte sequência de chamada para permitir que um usuário faça logon na rede social:</span><span class="sxs-lookup"><span data-stu-id="6135a-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="6135a-107">[ISocialProvider:: Load](isocialprovider-load.md) – o OSC carrega o provedor.</span><span class="sxs-lookup"><span data-stu-id="6135a-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="6135a-108">[ISocialProvider:: Version](isocialprovider-version.md) – o OSC Obtém uma cadeia de caracteres que representa o número da versão do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="6135a-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="6135a-109">[ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) – o OSC Obtém uma cadeia de caracteres que representa o nome da rede social.</span><span class="sxs-lookup"><span data-stu-id="6135a-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="6135a-110">[ISocialProvider:: SocialNetworkGuid](isocialprovider-socialnetworkguid.md) – o OSC Obtém um GUID imutável que representa a rede social.</span><span class="sxs-lookup"><span data-stu-id="6135a-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="6135a-111">[ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) – o OSC Obtém uma cadeia de caracteres que representa as funcionalidades do provedor e que está em conformidade com a definição de esquema para o elemento **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="6135a-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="6135a-112">[ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) – o OSC Obtém uma matriz de bytes que representa o ícone do site de rede social.</span><span class="sxs-lookup"><span data-stu-id="6135a-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="6135a-113">[ISocialProvider:: GetSession](isocialprovider-getsession.md) — o OSC Obtém uma interface [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="6135a-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="6135a-114">[ISocialSession:: logon](isocialsession-logon.md) — o OSC registra o usuário no site de rede social usando o nome de usuário e senha especificados.</span><span class="sxs-lookup"><span data-stu-id="6135a-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="6135a-115">[ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) – o OSC Obtém uma interface [métodoisocialprofile](isocialprovideriunknown.md) que representa o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="6135a-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="6135a-116">[ISocialSession:: GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) – o OSC Obtém uma cadeia de caracteres que representa um identificador exclusivo para um site de rede social.</span><span class="sxs-lookup"><span data-stu-id="6135a-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="6135a-117">O identificador de rede pode ser equivalente ao nome da rede.</span><span class="sxs-lookup"><span data-stu-id="6135a-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6135a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="6135a-118">See also</span></span>

- [<span data-ttu-id="6135a-119">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="6135a-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="6135a-120">Sequências de chamada típicas do OSC</span><span class="sxs-lookup"><span data-stu-id="6135a-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

