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
# <a name="basic-authentication"></a><span data-ttu-id="4a197-103">Autenticação básica</span><span class="sxs-lookup"><span data-stu-id="4a197-103">Basic authentication</span></span>

<span data-ttu-id="4a197-104">Outlook Social Connector (OSC) chama o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar os recursos do provedor de OSC para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="4a197-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="4a197-105">O OSC usa os recursos retornados para determinar como oferecer suporte a um usuário do Office que está fazendo logon com essa rede social.</span><span class="sxs-lookup"><span data-stu-id="4a197-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="4a197-106">Se o elemento de **useLogonWebAuth** em **recursos** retornado XML indica que o provedor do OSC suporta a autenticação básica, o OSC pode fazer a seguinte sequência de chamada para permitir que um usuário fazer logon na rede social:</span><span class="sxs-lookup"><span data-stu-id="4a197-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="4a197-107">[ISocialProvider::Load](isocialprovider-load.md) — o OSC carrega o provedor.</span><span class="sxs-lookup"><span data-stu-id="4a197-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="4a197-108">[ISocialProvider::Version](isocialprovider-version.md) — o OSC obtém uma string que representa o número da versão do provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="4a197-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="4a197-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — o OSC obtém uma string que representa o nome de rede social.</span><span class="sxs-lookup"><span data-stu-id="4a197-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="4a197-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) — o OSC obtém uma GUID imutável que representa a rede social.</span><span class="sxs-lookup"><span data-stu-id="4a197-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="4a197-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) — o OSC obtém uma string que representa os recursos do provedor e que está em conformidade com a definição de esquema para o elemento de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="4a197-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="4a197-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — o OSC obtém uma matriz de bytes que representa o ícone para o site de rede social.</span><span class="sxs-lookup"><span data-stu-id="4a197-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="4a197-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) — o OSC obtém uma interface [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="4a197-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="4a197-114">[ISocialSession::Logon](isocialsession-logon.md) — o OSC logs do usuário no site de rede social usando o nome de usuário especificado e a senha.</span><span class="sxs-lookup"><span data-stu-id="4a197-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="4a197-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — o OSC obtém uma interface [ISocialProfile](isocialprovideriunknown.md) que representa o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="4a197-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="4a197-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — o OSC obtém uma string que representa um identificador exclusivo para um site de rede social.</span><span class="sxs-lookup"><span data-stu-id="4a197-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="4a197-117">O identificador de rede pode ser equivalente ao nome de rede.</span><span class="sxs-lookup"><span data-stu-id="4a197-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4a197-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a197-118">See also</span></span>

- [<span data-ttu-id="4a197-119">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="4a197-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="4a197-120">Sequências de chamadas comuns do OSC</span><span class="sxs-lookup"><span data-stu-id="4a197-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

