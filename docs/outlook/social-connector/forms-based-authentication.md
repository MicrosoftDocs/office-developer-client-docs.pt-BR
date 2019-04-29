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
# <a name="forms-based-authentication"></a><span data-ttu-id="c5ee8-103">Autenticação baseada em formulários</span><span class="sxs-lookup"><span data-stu-id="c5ee8-103">Forms-based authentication</span></span>

<span data-ttu-id="c5ee8-104">O Outlook Social Connector (OSC) chama o método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) para determinar as funcionalidades do provedor do OSC para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="c5ee8-105">O OSC usa os recursos retornados para determinar como dar suporte a um usuário do Office que está fazendo logon nesta rede social.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> 

<span data-ttu-id="c5ee8-106">Se o elemento **useLogonWebAuth** no XML de **funcionalidades** retornado indicar que o provedor OSC dá suporte à autenticação baseada em formulários, o OSC poderá fazer a seguinte sequência de chamada para permitir que um usuário faça logon na rede social:</span><span class="sxs-lookup"><span data-stu-id="c5ee8-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports forms-based authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="c5ee8-107">[ISocialProvider:: Load](isocialprovider-load.md) &ndash; O OSC carrega o provedor.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="c5ee8-108">[ISocialProvider:: versão](isocialprovider-version.md) &ndash; O OSC Obtém uma cadeia de caracteres que representa o número da versão do provedor para esta rede social.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; The OSC gets a string that represents the version number of the provider for this social network.</span></span> 
    
3. <span data-ttu-id="c5ee8-109">[ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; O OSC Obtém uma cadeia de caracteres que representa o nome da rede social.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="c5ee8-110">[ISocialProvider:: SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; O OSC Obtém um GUID imutável que representa a rede social.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="c5ee8-111">[ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) &ndash; O OSC Obtém uma cadeia de caracteres que representa as funcionalidades do provedor e que está em conformidade com a definição de esquema para o elemento **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="c5ee8-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="c5ee8-112">[ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; O OSC Obtém uma matriz de bytes que representa o ícone do site de rede social.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="c5ee8-113">[ISocialProvider:: GetSession](isocialprovider-getsession.md) &ndash; O OSC Obtém uma interface [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="c5ee8-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="c5ee8-114">[ISocialSession:: LogonWeb](isocialsession-logonweb.md) &ndash; O OSC Inicializa o logon no site de rede social por autenticação baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC initializes logging on to the social network site by forms-based authentication.</span></span> <span data-ttu-id="c5ee8-115">Para essa chamada de logon inicial, o OSC passa **NULL** para o parâmetro _connectem_ .</span><span class="sxs-lookup"><span data-stu-id="c5ee8-115">For this initial logon call, the OSC passes **null** for the  _connectIn_ parameter.</span></span> 
    
9. <span data-ttu-id="c5ee8-116">[ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md) &ndash; O OSC Obtém a URL para exibir um formulário baseado em navegador para o usuário durante a autenticação da Web.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; The OSC gets the URL to display a browser-based form to the user during web authentication.</span></span> 
    
10. <span data-ttu-id="c5ee8-117">[ISocialSession:: LogonWeb](isocialsession-logonweb.md) &ndash; O OSC conclui o logon no site de rede social usando a autenticação baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC completes the logon to the social network site by using forms-based authentication.</span></span> <span data-ttu-id="c5ee8-118">O OSC chama esse método uma segunda vez, passando a URL do formulário de logon para o provedor no parâmetro _connectem_ .</span><span class="sxs-lookup"><span data-stu-id="c5ee8-118">The OSC calls this method a second time, passing the URL of the logon form to the provider in the  _connectIn_ parameter.</span></span> 
    
11. <span data-ttu-id="c5ee8-119">[ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; O OSC Obtém uma interface [métodoisocialprofile](isocialprovideriunknown.md) que representa o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
12. <span data-ttu-id="c5ee8-120">[ISocialSession:: GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; O OSC Obtém uma cadeia de caracteres que representa um identificador exclusivo para um site de rede social.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="c5ee8-121">O identificador de rede pode ser equivalente ao nome da rede.</span><span class="sxs-lookup"><span data-stu-id="c5ee8-121">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c5ee8-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5ee8-122">See also</span></span>

- [<span data-ttu-id="c5ee8-123">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="c5ee8-123">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="c5ee8-124">Sequências de chamada típicas do OSC</span><span class="sxs-lookup"><span data-stu-id="c5ee8-124">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

