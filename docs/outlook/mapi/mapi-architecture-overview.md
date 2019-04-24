---
title: Visão geral da arquitetura MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 98a723528a714918ad7e0f10534efb0d38ef139a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297884"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="1d350-103">Visão geral da arquitetura MAPI</span><span class="sxs-lookup"><span data-stu-id="1d350-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="1d350-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d350-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d350-105">O MAPI define uma arquitetura modular, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="1d350-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="1d350-106">![Arquitetura do Outlook 2010] (media/amapi_43.gif "Arquitetura do Outlook 2010")</span><span class="sxs-lookup"><span data-stu-id="1d350-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="1d350-107">O aplicativo MAPI é conhecido como um aplicativo cliente porque é um cliente do subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="1d350-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="1d350-108">Os aplicativos baseados em mensagens empregam mensagens como uma parte central do processamento e oferecem recursos de mensagens abrangentes, como a troca de informações de vários tipos em vários formatos e a capacidade de salvar e organizar as informações localmente.</span><span class="sxs-lookup"><span data-stu-id="1d350-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="1d350-109">Os aplicativos de email, agendamento e fluxo de trabalho são exemplos de aplicativos baseados em mensagens.</span><span class="sxs-lookup"><span data-stu-id="1d350-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="1d350-110">O subsistema MAPI é composto por uma interface de usuário comum e as interfaces de programação.</span><span class="sxs-lookup"><span data-stu-id="1d350-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="1d350-111">A interface de usuário comum é um conjunto de caixas de diálogo que oferece aos aplicativos cliente uma aparência consistente e os usuários uma maneira consistente de trabalhar.</span><span class="sxs-lookup"><span data-stu-id="1d350-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="1d350-112">O MAPI tem interfaces de programação que são usadas pelo subsistema MAPI, por desenvolvedores de software de cliente e por desenvolvedores de provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="1d350-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="1d350-113">A interface de programação MAPI é a principal interface de programação baseada em objeto.</span><span class="sxs-lookup"><span data-stu-id="1d350-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="1d350-114">A interface de programação MAPI é semelhante ao modelo de objeto de componente OLE e é usada pelo subsistema MAPI e por aplicativos clientes baseados em mensagens escritas em C ou C++.</span><span class="sxs-lookup"><span data-stu-id="1d350-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="1d350-115">Como desenvolvedor de software cliente, você faz chamadas MAPI diretamente por meio da interface de programação MAPI.</span><span class="sxs-lookup"><span data-stu-id="1d350-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="1d350-116">Você pode implementar o sistema de mensagens com uma única interface de cliente MAPI ou uma combinação de interfaces.</span><span class="sxs-lookup"><span data-stu-id="1d350-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="1d350-117">Um único aplicativo pode fazer chamadas para métodos ou funções pertencentes a qualquer uma das interfaces.</span><span class="sxs-lookup"><span data-stu-id="1d350-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1d350-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d350-118">See also</span></span>

<span data-ttu-id="1d350-119">-[Recursos e arquitetura MAPI](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="1d350-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

