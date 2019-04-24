---
title: Exemplo de XML de recursos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: O exemplo XML neste tópico é uma cadeia XML retornada para o Outlook Social Connector (OSC) depois de chamar o método ISocialProvider::GetCapabilities para uma rede social. O XML mostra como um provedor de OSC especifica seus recursos e os requisitos para a OSC.
ms.openlocfilehash: 53bd250432e7b27d984a846d206adc812c47898f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281227"
---
# <a name="capabilities-xml-example"></a><span data-ttu-id="e8b23-104">Exemplo de XML de recursos</span><span class="sxs-lookup"><span data-stu-id="e8b23-104">Capabilities XML example</span></span>

<span data-ttu-id="e8b23-105">O exemplo XML neste tópico é uma cadeia XML retornada para o Outlook Social Connector (OSC) depois de chamar o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="e8b23-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="e8b23-106">O XML mostra como um provedor de OSC especifica seus recursos e os requisitos para a OSC.</span><span class="sxs-lookup"><span data-stu-id="e8b23-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="e8b23-107">Recursos para amigos</span><span class="sxs-lookup"><span data-stu-id="e8b23-107">Capabilities for friends</span></span>

<span data-ttu-id="e8b23-108">Neste exemplo, o provedor OSC Especifica os seguintes elementos para mostrar os recursos de suporte no recurso amigos:</span><span class="sxs-lookup"><span data-stu-id="e8b23-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="e8b23-109">**getFriends** como **verdadeiro** para indicar que o provedor do OSC é compatível com o método[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obter informações dos amigos por programação.</span><span class="sxs-lookup"><span data-stu-id="e8b23-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="e8b23-110">**cacheFriends** como **verdadeiro** para dar suporte a informações sobre o cache de amigos em uma pasta de contatos do Outlook.</span><span class="sxs-lookup"><span data-stu-id="e8b23-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="e8b23-111">**contactSyncRestartInterval** como 60 para indicar que, em caso de erro, a OSC deve repetir a atualização do cache a cada 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="e8b23-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="e8b23-112">**followPerson** como **verdadeiro** para indicar a capacidade de adicionar amigos em rede social.</span><span class="sxs-lookup"><span data-stu-id="e8b23-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="e8b23-113">**doNotFollowPerson** como **falso** para indicar que o provedor OSC não oferece suporte para desfazer uma amizade em rede social.</span><span class="sxs-lookup"><span data-stu-id="e8b23-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="e8b23-114">**dynamicContactsLookup** como **falso** para indicar que o OSC não deve armazenar informações dos amigos na memória.</span><span class="sxs-lookup"><span data-stu-id="e8b23-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="e8b23-115">Recursos para atividades</span><span class="sxs-lookup"><span data-stu-id="e8b23-115">Capabilities for activities</span></span>

<span data-ttu-id="e8b23-116">O provedor OSC especifica os seguintes elementos para mostrar o recurso de atividades de suporte:</span><span class="sxs-lookup"><span data-stu-id="e8b23-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="e8b23-117">**getActivities** como **verdadeiro** para indicar que o provedor do OSC é compatível com o método[ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) para visualizar atividades dos amigos por programação.</span><span class="sxs-lookup"><span data-stu-id="e8b23-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="e8b23-118">**cacheActivities** como **falso** para dar suporte de atividades de cache de amigos na pasta oculta Feed de notícias do Outlook.</span><span class="sxs-lookup"><span data-stu-id="e8b23-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="e8b23-119">**dynamicActivitiesLookupEx** como **verdadeiro** para indicar que o OSC deverá ser armazenado nas atividades dos amigos na memória.</span><span class="sxs-lookup"><span data-stu-id="e8b23-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="e8b23-120">Testar recursos para autenticação e configuração de conta</span><span class="sxs-lookup"><span data-stu-id="e8b23-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="e8b23-121">O provedor OSC especifica os seguintes elementos para mostrar o suporte para autenticação e configuração de conta:</span><span class="sxs-lookup"><span data-stu-id="e8b23-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="e8b23-122">**useLogonWebAuth** como **falso** para indicar que o provedor OSC dá suporte à autenticação básica.</span><span class="sxs-lookup"><span data-stu-id="e8b23-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="e8b23-123">**supportsAutoConfigure** como **falso** para indicar que a OSC não deve tentar configurar automaticamente e fazer logon na rede social para o usuário.</span><span class="sxs-lookup"><span data-stu-id="e8b23-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="e8b23-124">**useLogonCached** e **hideRememberMyPassword** como **falso** para indicar que a OSC deve solicitar senha sempre e não deve usar credenciais de logon armazenadas em cache para fazer logon.</span><span class="sxs-lookup"><span data-stu-id="e8b23-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="e8b23-125">**displayUrl** como **falso** para indicar que o OSC não deverá exibir a URL para a rede social na caixa de diálogo da Configuração de conta.</span><span class="sxs-lookup"><span data-stu-id="e8b23-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="e8b23-126">**hideHyperlinks** como **falso** para indicar que o provedor OSC oferece suporte apenas para contas existentes com senhas conhecidas e o OSC não deve exibir os hyperlinks **clique aqui para criar uma conta** e \*\*Esqueceu sua senha? \*\* na caixa de diálogo da configuração de conta.</span><span class="sxs-lookup"><span data-stu-id="e8b23-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="e8b23-127">Exemplos de XML</span><span class="sxs-lookup"><span data-stu-id="e8b23-127">XML example</span></span>

<span data-ttu-id="e8b23-128">O exemplo a seguir mostra os**recursos** XML de um provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="e8b23-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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
  <createAccountUrl>https://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>https://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a><span data-ttu-id="e8b23-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8b23-129">See also</span></span>

- [<span data-ttu-id="e8b23-130">Exemplos de XML de provedor OSC</span><span class="sxs-lookup"><span data-stu-id="e8b23-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="e8b23-131">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="e8b23-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="e8b23-132">Exemplo de XML de amigos</span><span class="sxs-lookup"><span data-stu-id="e8b23-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="e8b23-133">Exemplo de XML de feed de atividades</span><span class="sxs-lookup"><span data-stu-id="e8b23-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="e8b23-134">Esquema XML do provedor Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="e8b23-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

