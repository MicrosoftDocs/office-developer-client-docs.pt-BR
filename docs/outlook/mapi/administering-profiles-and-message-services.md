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
ms.openlocfilehash: 1e64241008a4adde4431b2c9683199294f21e396
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330230"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="2a29c-103">Administrar perfis e serviços de mensagens</span><span class="sxs-lookup"><span data-stu-id="2a29c-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="2a29c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a29c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a29c-105">O perfil e a administração do serviço de mensagens podem envolver a criação de novos perfis, a exclusão de perfis antigos e a modificação do conteúdo de perfis existentes alterando os serviços de mensagens e provedores de serviços contidos neles.</span><span class="sxs-lookup"><span data-stu-id="2a29c-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="2a29c-106">Nem todos os clientes dão suporte à administração de perfis e serviços de mensagens como recursos padrão.</span><span class="sxs-lookup"><span data-stu-id="2a29c-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="2a29c-107">Alguns clientes não têm mais a ver com perfis do que permitem que os usuários selecionem um no momento do logon.</span><span class="sxs-lookup"><span data-stu-id="2a29c-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="2a29c-108">Se você oferecer suporte à administração de perfil ou serviço de mensagens, é provável que você use as seguintes interfaces implementadas por MAPI:</span><span class="sxs-lookup"><span data-stu-id="2a29c-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="2a29c-109">[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) para administrar um serviço de mensagens em um perfil, acessível por meio de [IMAPISession: adminservices](imapisession-adminservices.md) ou [IProfAdmin:: adminservices](iprofadmin-adminservices.md).</span><span class="sxs-lookup"><span data-stu-id="2a29c-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="2a29c-110">Os clientes de mensagens normalmente chamam o **IMAPISession** de clientes de configuração, ou clientes que não enviam ou recebem mensagens, chamam **IProfAdmin**.</span><span class="sxs-lookup"><span data-stu-id="2a29c-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="2a29c-111">Sempre que possível, chame o método **IProfAdmin** porque ele não faz com que o serviço de mensagem seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="2a29c-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="2a29c-112">Para obter mais informações sobre como usar a interface **IMsgServiceAdmin** , consulte os seguintes tópicos: Configurando [um serviço de mensagens](configuring-a-message-service.md), [copiando um serviço de mensagens](copying-a-message-service.md)e excluindo [um serviço de mensagens](deleting-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="2a29c-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="2a29c-113">[IProfAdmin: IUnknown](iprofadminiunknown.md) para administrar um perfil, acessível através da função [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="2a29c-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="2a29c-114">Para obter mais informações sobre como usar a interface **IProfAdmin** , consulte os seguintes tópicos: [criando um perfil usando código personalizado](creating-a-profile-by-using-custom-code.md), [copiando](copying-a-profile.md)um perfil, excluindo um [perfil](deleting-a-profile.md), [encontrando um nome de perfil](finding-a-profile-name.md)e [definindo um Perfil padrão](setting-a-default-profile.md).</span><span class="sxs-lookup"><span data-stu-id="2a29c-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="2a29c-115">[IProfSect: IMAPIProp](iprofsectimapiprop.md) para manter as propriedades em uma seção de perfil, acessível através do método [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md) ou [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="2a29c-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="2a29c-116">Para obter mais informações sobre seções de perfil, consulte [MAPI](mapi-profiles.md)Profiles.</span><span class="sxs-lookup"><span data-stu-id="2a29c-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="2a29c-117">[IProviderAdmin: IUnknown](iprovideradminiunknown.md) para administrar os provedores de serviço em um serviço de mensagens, acessível através de [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md).</span><span class="sxs-lookup"><span data-stu-id="2a29c-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="2a29c-118">Para obter mais informações sobre como usar a interface **IProviderAdmin** , confira [Adicionar ou excluir provedores em um serviço de mensagens](adding-or-deleting-providers-in-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="2a29c-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="2a29c-119">Tenha cuidado ao dar suporte à administração de perfis e serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2a29c-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="2a29c-120">Não há garantias de proteção contra a modificação adversa de um perfil que está em uso.</span><span class="sxs-lookup"><span data-stu-id="2a29c-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="2a29c-121">O MAPI pode impedir a exclusão de um perfil em uso, mas não pode impedir a exclusão de todos os serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2a29c-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="2a29c-122">Se você excluir todos os serviços de mensagens em um perfil, todos os provedores de serviços desses serviços serão interrompidos, fazendo com que ocorram resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="2a29c-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="2a29c-123">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2a29c-123">In this section</span></span>

[<span data-ttu-id="2a29c-124">Criar um perfil</span><span class="sxs-lookup"><span data-stu-id="2a29c-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="2a29c-125">Descreve como criar um perfil.</span><span class="sxs-lookup"><span data-stu-id="2a29c-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="2a29c-126">Copiar um perfil</span><span class="sxs-lookup"><span data-stu-id="2a29c-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="2a29c-127">Descreve como copiar um perfil.</span><span class="sxs-lookup"><span data-stu-id="2a29c-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="2a29c-128">Excluir um perfil</span><span class="sxs-lookup"><span data-stu-id="2a29c-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="2a29c-129">Descreve como excluir um perfil.</span><span class="sxs-lookup"><span data-stu-id="2a29c-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="2a29c-130">ConFigurando um perfil padrão</span><span class="sxs-lookup"><span data-stu-id="2a29c-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="2a29c-131">Descreve como definir um perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="2a29c-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="2a29c-132">Localizar um nome de perfil</span><span class="sxs-lookup"><span data-stu-id="2a29c-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="2a29c-133">Descreve como localizar o nome de um perfil.</span><span class="sxs-lookup"><span data-stu-id="2a29c-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="2a29c-134">Adicionar um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="2a29c-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="2a29c-135">Descreve como adicionar um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2a29c-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="2a29c-136">ConFigurando um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="2a29c-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="2a29c-137">Descreve como configurar um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2a29c-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="2a29c-138">Copiar um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="2a29c-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="2a29c-139">Descreve como copiar um serviço de mensagens para um perfil.</span><span class="sxs-lookup"><span data-stu-id="2a29c-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="2a29c-140">Excluir um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="2a29c-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="2a29c-141">Descreve como excluir um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2a29c-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="2a29c-142">Adicionar ou excluir provedores em um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="2a29c-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="2a29c-143">Descreve como adicionar ou excluir provedores em um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2a29c-143">Describes how to add or delete providers in a message service.</span></span>
    

