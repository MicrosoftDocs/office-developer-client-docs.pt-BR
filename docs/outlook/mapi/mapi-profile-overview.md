---
title: Visão geral do perfil MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a34c21e20fa45cd3265ec42c9d992eb828203f66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563909"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="dbfb4-103">Visão geral do perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="dbfb4-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="dbfb4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbfb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbfb4-105">Um perfil é uma coleção de informações sobre os serviços de mensagens e provedores de serviços que um usuário de um aplicativo cliente quer esteja disponível durante uma determinada sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="dbfb4-106">Cada usuário tenha pelo menos um perfil; muitos usuários manter vários.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="dbfb4-107">Por exemplo, um usuário pode ter um perfil para trabalhar com um serviço de repositório de mensagens baseado em servidor e outro perfil para trabalhar com um serviço de repositório de mensagem no computador local.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="dbfb4-108">Um usuário talvez queira acessar um conjunto de sistemas de mensagens usando os serviços de transporte adequado para a parte do dia e outro conjunto para o restante do dia.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="dbfb4-109">Perfis fornecem uma maneira flexível para selecionar combinações de serviços do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="dbfb4-110">Perfis podem ter até 64 caracteres alfanuméricos os nomes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="dbfb4-111">Os nomes podem incluir espaços incorporados, o sublinhado e ênfase caracteres e não podem conter espaços à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="dbfb4-112">Perfis são organizados hierarquicamente e divididos em seções, com uma seção para cada serviço de mensagem e uma seção para cada provedor de serviços em um serviço.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="dbfb4-113">As seções relacionadas são vinculadas, tornando mais fácil navegar as informações.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="dbfb4-114">Cada seção contém uma série de entradas MAPI ou um aplicativo cliente usa para configuração.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="dbfb4-115">As entradas incluídas em um perfil variam de serviço de mensagem para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="dbfb4-116">Algumas das entradas comuns incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dbfb4-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="dbfb4-117">O nome de cada serviço de mensagem ou o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="dbfb4-118">O nome de DLLs que contêm os provedores de serviço e serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="dbfb4-119">O nome da função do ponto de entrada do serviço de cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="dbfb4-120">Uma lista dos provedores de serviços que constituem cada serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="dbfb4-121">Perfis podem ser criados no momento da instalação, quando o MAPI ou um serviço de mensagem for carregado em um computador, ou a qualquer momento posterior.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="dbfb4-122">MAPI fornece o Assistente de perfil para administração de perfil.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="dbfb4-123">O Assistente de perfil é um aplicativo que cria novos perfis com uma quantidade mínima de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="dbfb4-124">O assistente usa valores padrão para configurações sempre que possível, economizando esforço e tempo dos usuários.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="dbfb4-125">Os usuários inserem valores somente quando absolutamente necessário.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="dbfb4-126">Para obter mais informações, consulte o [tópico Criando um perfil usando o Assistente de perfil](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="dbfb4-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="dbfb4-127">Você também pode usar a ferramenta de personalização do Office para criar um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="dbfb4-128">Para obter mais informações, consulte [Office Customization Tool](http://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="dbfb4-128">For more information, see [Office Customization Tool](http://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dbfb4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbfb4-129">See also</span></span>



[<span data-ttu-id="dbfb4-130">Arquitetura e os recursos MAPI</span><span class="sxs-lookup"><span data-stu-id="dbfb4-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

