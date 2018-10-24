---
title: Administrar perfis e serviços de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 124f4875834e035e29d4c63e52789bf07f18258d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587541"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="32313-103">Administrar perfis e serviços de mensagens</span><span class="sxs-lookup"><span data-stu-id="32313-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="32313-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32313-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32313-105">Perfil e a mensagem de administração do serviço pode envolver a criação de novos perfis, excluindo perfis antigos e modificar o conteúdo de perfis existentes, alterando os serviços de mensagem e os provedores de serviço contidos neles.</span><span class="sxs-lookup"><span data-stu-id="32313-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="32313-106">Nem todos os clientes suportam administração do serviço de perfil e a mensagem como recursos padrão.</span><span class="sxs-lookup"><span data-stu-id="32313-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="32313-107">Alguns clientes têm nada mais fazer com os perfis de permitir que os usuários selecionem um momento de logon.</span><span class="sxs-lookup"><span data-stu-id="32313-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="32313-108">Caso você ofereça suporte a administração do serviço de perfil ou mensagem, as chances são que você usará as seguintes interfaces que são implementadas pelo MAPI:</span><span class="sxs-lookup"><span data-stu-id="32313-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="32313-109">[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) para administrar um serviço de mensagem em um perfil, acessível através do [IMAPISession::AdminServices](imapisession-adminservices.md) ou [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span><span class="sxs-lookup"><span data-stu-id="32313-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="32313-110">Clientes de mensagens normalmente chama **IMAPISession** durante a configuração de clientes ou clientes que não enviar ou receber mensagens, chame **IProfAdmin**.</span><span class="sxs-lookup"><span data-stu-id="32313-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="32313-111">Sempre que possível, chame o método de **IProfAdmin** porque ele não faz com que o serviço de mensagem a ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="32313-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="32313-112">Para obter mais informações sobre como usar a interface **IMsgServiceAdmin** , consulte os seguintes tópicos: [Configurar um serviço de mensagem](configuring-a-message-service.md), [copiando um serviço de mensagem](copying-a-message-service.md)e [Excluindo um serviço de mensagem](deleting-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="32313-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="32313-113">[IProfAdmin: IUnknown](iprofadminiunknown.md) para administrar um perfil, acessado por meio da função [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="32313-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="32313-114">Para obter mais informações sobre como usar a interface **IProfAdmin** , consulte os seguintes tópicos: [criação de um perfil usando código de sinalizador](creating-a-profile-by-using-custom-code.md), [copiando um perfil](copying-a-profile.md), [exclusão de um perfil](deleting-a-profile.md), [encontrando um nome de perfil](finding-a-profile-name.md)e [configuração um Perfil padrão](setting-a-default-profile.md).</span><span class="sxs-lookup"><span data-stu-id="32313-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="32313-115">[IProfSect: IMAPIProp](iprofsectimapiprop.md) para manter as propriedades em uma seção de perfil, acessada por meio do método [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="32313-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="32313-116">Para obter mais informações sobre as seções de perfil, consulte [Perfis MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="32313-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="32313-117">[IProviderAdmin: IUnknown](iprovideradminiunknown.md) para administrar os provedores de serviços em um serviço de mensagem, acessível através do [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span><span class="sxs-lookup"><span data-stu-id="32313-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="32313-118">Para obter mais informações sobre como usar a interface **IProviderAdmin** , consulte [adicionando ou excluindo provedores em um serviço de mensagem](adding-or-deleting-providers-in-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="32313-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="32313-119">Tenha cuidado no seu suporte da administração do serviço de perfil e mensagem.</span><span class="sxs-lookup"><span data-stu-id="32313-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="32313-120">Não há nenhuma proteções para proteger contra adversamente para modificar um perfil que está em uso.</span><span class="sxs-lookup"><span data-stu-id="32313-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="32313-121">MAPI pode impedir a exclusão de um perfil em uso, mas não pode impedir a exclusão de cada serviço de mensagem nela.</span><span class="sxs-lookup"><span data-stu-id="32313-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="32313-122">Se você excluir cada serviço de mensagem em um perfil, todos os provedores de serviço nesses serviços irá parar causando assim resultados imprevisíveis ocorra.</span><span class="sxs-lookup"><span data-stu-id="32313-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="32313-123">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="32313-123">In this section</span></span>

[<span data-ttu-id="32313-124">Criação de um perfil</span><span class="sxs-lookup"><span data-stu-id="32313-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="32313-125">Descreve como criar um perfil.</span><span class="sxs-lookup"><span data-stu-id="32313-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="32313-126">Copiando um perfil</span><span class="sxs-lookup"><span data-stu-id="32313-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="32313-127">Descreve como copiar um perfil.</span><span class="sxs-lookup"><span data-stu-id="32313-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="32313-128">Exclusão de um perfil</span><span class="sxs-lookup"><span data-stu-id="32313-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="32313-129">Descreve como excluir um perfil.</span><span class="sxs-lookup"><span data-stu-id="32313-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="32313-130">Definir um perfil padrão</span><span class="sxs-lookup"><span data-stu-id="32313-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="32313-131">Descreve como definir um perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="32313-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="32313-132">Localizando um nome de perfil</span><span class="sxs-lookup"><span data-stu-id="32313-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="32313-133">Descreve como localizar um nome de um perfil.</span><span class="sxs-lookup"><span data-stu-id="32313-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="32313-134">Adição de um serviço de mensagem</span><span class="sxs-lookup"><span data-stu-id="32313-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="32313-135">Descreve como adicionar um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="32313-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="32313-136">Configurando um serviço de mensagem</span><span class="sxs-lookup"><span data-stu-id="32313-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="32313-137">Descreve como configurar um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="32313-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="32313-138">Copiar um serviço de mensagem</span><span class="sxs-lookup"><span data-stu-id="32313-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="32313-139">Descreve como copiar um serviço de mensagem para um perfil.</span><span class="sxs-lookup"><span data-stu-id="32313-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="32313-140">Excluindo um serviço de mensagem</span><span class="sxs-lookup"><span data-stu-id="32313-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="32313-141">Descreve como excluir um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="32313-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="32313-142">Adicionando ou excluindo provedores em um serviço de mensagem</span><span class="sxs-lookup"><span data-stu-id="32313-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="32313-143">Descreve como adicionar ou excluir provedores em um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="32313-143">Describes how to add or delete providers in a message service.</span></span>
    

