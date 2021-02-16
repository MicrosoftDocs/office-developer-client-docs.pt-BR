---
title: Visão geral do perfil MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328158"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="6d812-103">Visão geral do perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="6d812-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="6d812-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d812-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d812-105">Um perfil é um conjunto de informações sobre os serviços de mensagens e provedores de serviços que um usuário de um aplicativo cliente deseja disponibilizar durante uma sessão MAPI específica.</span><span class="sxs-lookup"><span data-stu-id="6d812-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="6d812-106">Cada usuário tem pelo menos um perfil; muitos usuários mantêm vários.</span><span class="sxs-lookup"><span data-stu-id="6d812-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="6d812-107">Por exemplo, um usuário pode ter um perfil para trabalhar com um serviço de armazenamento de mensagens baseado em servidor e outro perfil para trabalhar com um serviço de armazenamento de mensagens no computador local.</span><span class="sxs-lookup"><span data-stu-id="6d812-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="6d812-108">Um usuário pode querer acessar um conjunto de sistemas de mensagens usando os serviços de transporte apropriados para parte do dia e outro conjunto para o restante do dia.</span><span class="sxs-lookup"><span data-stu-id="6d812-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="6d812-109">Os perfis fornecem uma maneira flexível de selecionar combinações de serviços do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6d812-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="6d812-110">Os perfis podem ter nomes de até 64 caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="6d812-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="6d812-111">Os nomes podem incluir caracteres de destaque, sublinhado e espaços incorporados e não podem incluir espaços à frente ou à final.</span><span class="sxs-lookup"><span data-stu-id="6d812-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="6d812-112">Os perfis são organizados hierarquicamente e divididos em seções, com uma seção para cada serviço de mensagens e uma seção para cada provedor de serviços em um serviço.</span><span class="sxs-lookup"><span data-stu-id="6d812-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="6d812-113">As seções relacionadas são vinculadas, facilitando a navegação pelas informações.</span><span class="sxs-lookup"><span data-stu-id="6d812-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="6d812-114">Cada seção contém uma série de entradas que MAPI ou um aplicativo cliente usa para configuração.</span><span class="sxs-lookup"><span data-stu-id="6d812-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="6d812-115">As entradas incluídas em um perfil variam de serviço de mensagens para serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6d812-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="6d812-116">Algumas das entradas comuns incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6d812-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="6d812-117">O nome de cada serviço de mensagens ou provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="6d812-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="6d812-118">O nome das DLLs que contêm provedores de serviços e serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6d812-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="6d812-119">O nome da função de ponto de entrada de cada serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6d812-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="6d812-120">Uma lista dos provedores de serviços que comem cada serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6d812-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="6d812-121">Os perfis podem ser criados no momento da instalação, quando MAPI ou um serviço de mensagens é carregado em um computador ou a qualquer momento posterior.</span><span class="sxs-lookup"><span data-stu-id="6d812-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="6d812-122">MAPI provides the Profile Wizard for profile administration.</span><span class="sxs-lookup"><span data-stu-id="6d812-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="6d812-123">O Assistente de Perfil é um aplicativo que cria novos perfis com uma quantidade mínima de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6d812-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="6d812-124">O assistente usa valores padrão para configurações sempre que possível, economizando tempo e esforço dos usuários.</span><span class="sxs-lookup"><span data-stu-id="6d812-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="6d812-125">Os usuários ins insiram valores somente quando absolutamente necessário.</span><span class="sxs-lookup"><span data-stu-id="6d812-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="6d812-126">Para obter mais informações, [consulte Criando um perfil usando o Assistente de Perfil.](creating-a-profile-by-using-the-profile-wizard.md)</span><span class="sxs-lookup"><span data-stu-id="6d812-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="6d812-127">Você também pode usar a Ferramenta de Personalização do Office para criar um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="6d812-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="6d812-128">Para obter mais informações, consulte [Ferramenta de Personalização do Office](https://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="6d812-128">For more information, see [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d812-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d812-129">See also</span></span>



[<span data-ttu-id="6d812-130">Recursos e arquitetura MAPI</span><span class="sxs-lookup"><span data-stu-id="6d812-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

