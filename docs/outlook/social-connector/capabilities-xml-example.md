---
title: Exemplo de XML de recursos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: O exemplo de XML deste tópico é uma sequência de caracteres XML retornada para o Outlook Social Connector (OSC) depois de chamar o método ISocialProvider::GetCapabilities para uma rede social. O XML mostra como um provedor OSC Especifica seus recursos e requisitos para que o OSC.
ms.openlocfilehash: 5cafd6d29de8b4357e9e0ce6dab30b125f53b8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770827"
---
# <a name="capabilities-xml-example"></a><span data-ttu-id="4efdc-104">Exemplo de XML de recursos</span><span class="sxs-lookup"><span data-stu-id="4efdc-104">Capabilities XML example</span></span>

<span data-ttu-id="4efdc-105">O exemplo de XML deste tópico é uma sequência de caracteres XML retornada para o Outlook Social Connector (OSC) depois de chamar o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="4efdc-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="4efdc-106">O XML mostra como um provedor OSC Especifica seus recursos e requisitos para que o OSC.</span><span class="sxs-lookup"><span data-stu-id="4efdc-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="4efdc-107">Recursos para amigos</span><span class="sxs-lookup"><span data-stu-id="4efdc-107">Capabilities for friends</span></span>

<span data-ttu-id="4efdc-108">Neste exemplo, o provedor do OSC Especifica os seguintes elementos para mostrar seus recursos com suporte para o recurso de amigos:</span><span class="sxs-lookup"><span data-stu-id="4efdc-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="4efdc-109">**getFriends** como **true** para indicar o provedor do OSC oferece suporte ao método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obter informações de amigos dos programaticamente.</span><span class="sxs-lookup"><span data-stu-id="4efdc-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="4efdc-110">**cacheFriends** como **true** para informações do cache dos amigos de suporte em uma pasta de contatos do Outlook.</span><span class="sxs-lookup"><span data-stu-id="4efdc-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="4efdc-111">**contactSyncRestartInterval** como 60 para indicar esse erro diante, o OSC deve repetir a atualização do cache a cada 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="4efdc-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="4efdc-112">**followPerson** como **true** para indicar a capacidade de adicionar amigos na rede social.</span><span class="sxs-lookup"><span data-stu-id="4efdc-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="4efdc-113">**doNotFollowPerson** como **false** para indicar que o provedor do OSC não oferece suporte a remoção de uma pessoa como um amigo na rede social.</span><span class="sxs-lookup"><span data-stu-id="4efdc-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="4efdc-114">**dynamicContactsLookup** como **false** para indicar que o OSC não deve armazenar informações de amigos na memória.</span><span class="sxs-lookup"><span data-stu-id="4efdc-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="4efdc-115">Recursos para atividades</span><span class="sxs-lookup"><span data-stu-id="4efdc-115">Capabilities for activities</span></span>

<span data-ttu-id="4efdc-116">O provedor do OSC Especifica os seguintes elementos para mostrar sua capacidade de oferecer suporte às atividades:</span><span class="sxs-lookup"><span data-stu-id="4efdc-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="4efdc-117">**getActivities** como **true** para indicar que o provedor do OSC suporta o método [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) para fazer atividades dos amigos programaticamente.</span><span class="sxs-lookup"><span data-stu-id="4efdc-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="4efdc-118">**cacheActivities** como **false** para oferecer suporte a atividades de cache de amigos na pasta oculta o Feed de notícias do Outlook.</span><span class="sxs-lookup"><span data-stu-id="4efdc-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="4efdc-119">**dynamicActivitiesLookupEx** como **true** para indicar que o OSC deve armazenar atividades dos amigos na memória.</span><span class="sxs-lookup"><span data-stu-id="4efdc-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="4efdc-120">Recursos para configuração de conta e autenticação</span><span class="sxs-lookup"><span data-stu-id="4efdc-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="4efdc-121">O provedor do OSC Especifica os seguintes elementos para mostrar seu suporte para autenticação e a configuração de conta:</span><span class="sxs-lookup"><span data-stu-id="4efdc-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="4efdc-122">**useLogonWebAuth** como **false** para indicar que o provedor do OSC suporta a autenticação básica.</span><span class="sxs-lookup"><span data-stu-id="4efdc-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="4efdc-123">**supportsAutoConfigure** como **false** para indicar que o OSC não deve tentar configurar automaticamente e fazer logon rede social para o usuário.</span><span class="sxs-lookup"><span data-stu-id="4efdc-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="4efdc-124">**useLogonCached** e **hideRememberMyPassword** como **false** para indicar que o OSC deve solicitar senha cada vez e não deve usar o cache credenciais de logon para fazer logon.</span><span class="sxs-lookup"><span data-stu-id="4efdc-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="4efdc-125">**displayUrl** como **false** para indicar que o OSC não deve exibir a URL para a rede social na caixa de diálogo de configuração de conta.</span><span class="sxs-lookup"><span data-stu-id="4efdc-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="4efdc-126">**hideHyperlinks** como **false** para indicar que o provedor do OSC suporta somente contas existentes com senhas conhecidas e o OSC não deve exibir o **clique aqui para criar uma conta** e **Esqueceu sua senha?** hiperlinks na caixa de diálogo de configuração de conta.</span><span class="sxs-lookup"><span data-stu-id="4efdc-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="4efdc-127">Exemplo XML</span><span class="sxs-lookup"><span data-stu-id="4efdc-127">XML example</span></span>

<span data-ttu-id="4efdc-128">O exemplo a seguir mostra os **recursos de** XML de um provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="4efdc-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <getFriends>true</getFriends>
  <cacheFriends>true</cacheFriends>
  <followPerson>true</followPerson>
  <doNotFollowPerson>false</doNotFollowPerson>
  <getActivities>true</getActivities>
  <cacheActivities>false</cacheActivities>
  <displayUrl>false</displayUrl>
  <useLogonWebAuth>false</useLogonWebAuth>
  <hideHyperlinks>false</hideHyperlinks>
  <supportsAutoConfigure>false</supportsAutoConfigure>
  <contactSyncRestartInterval>60</contactSyncRestartInterval>
  <dynamicActivitiesLookupEx>true</dynamicActivitiesLookupEx>
  <dynamicContactsLookup>false</dynamicContactsLookup>
  <useLogonCached>false</useLogonCached>
  <hideRememberMyPassword>false</hideRememberMyPassword>
  <createAccountUrl>http://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>http://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a><span data-ttu-id="4efdc-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4efdc-129">See also</span></span>

- [<span data-ttu-id="4efdc-130">Exemplos XML de provedor do OSC</span><span class="sxs-lookup"><span data-stu-id="4efdc-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="4efdc-131">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="4efdc-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="4efdc-132">Exemplo de XML de amigos</span><span class="sxs-lookup"><span data-stu-id="4efdc-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="4efdc-133">Exemplo de XML de Feed de atividade</span><span class="sxs-lookup"><span data-stu-id="4efdc-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="4efdc-134">Esquema XML do Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="4efdc-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

