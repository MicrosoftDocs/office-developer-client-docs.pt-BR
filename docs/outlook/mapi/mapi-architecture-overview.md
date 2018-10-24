---
title: Visão geral da arquitetura do MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a0f2efc17ca8790502f11d677498013cbe10205d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579351"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="ca741-103">Visão geral da arquitetura do MAPI</span><span class="sxs-lookup"><span data-stu-id="ca741-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="ca741-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca741-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca741-105">MAPI define uma arquitetura modular, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca741-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="ca741-106">![Arquitetura do Outlook 2010] (media/amapi_43.gif "Arquitetura do Outlook 2010")</span><span class="sxs-lookup"><span data-stu-id="ca741-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="ca741-107">O aplicativo de MAPI é conhecido como um aplicativo cliente porque ele é um cliente do subsistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ca741-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="ca741-108">Aplicativos baseados em mensagens empregam como parte central do seu processamento de mensagens e oferecem recursos de mensagens extensivo, como a troca de informações de diversos tipos em vários formatos e a capacidade de salvar e organizar as informações localmente.</span><span class="sxs-lookup"><span data-stu-id="ca741-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="ca741-109">Envie um email, agendar, e aplicativos de fluxo de trabalho são exemplos de aplicativos baseados em mensagens.</span><span class="sxs-lookup"><span data-stu-id="ca741-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="ca741-110">O subsistema de MAPI é composto por uma interface de usuário comum e as interfaces de programação.</span><span class="sxs-lookup"><span data-stu-id="ca741-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="ca741-111">A interface de usuário comum é um conjunto de caixas de diálogo que proporciona aos aplicativos cliente uma aparência consistente e usuários uma maneira consistente de trabalhar.</span><span class="sxs-lookup"><span data-stu-id="ca741-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="ca741-112">MAPI tem interfaces de programação que são usados pelo subsistema de MAPI, por desenvolvedores de software do cliente e por desenvolvedores de provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="ca741-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="ca741-113">A interface de programação de MAPI é a interface de programação baseada no objeto principal.</span><span class="sxs-lookup"><span data-stu-id="ca741-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="ca741-114">A interface de programação de MAPI é semelhante ao OLE Component Object Model e é usada pelo subsistema MAPI e aplicativos de cliente baseado em mensagens escritos em C ou C++.</span><span class="sxs-lookup"><span data-stu-id="ca741-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="ca741-115">Como um desenvolvedor de software do cliente, você pode fazer chamadas MAPI diretamente por meio da interface de programação de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ca741-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="ca741-116">Você pode implementar a mensagens com uma única interface de cliente MAPI ou uma combinação das interfaces.</span><span class="sxs-lookup"><span data-stu-id="ca741-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="ca741-117">Um único aplicativo pode fazer chamadas para métodos ou funções que pertencem a qualquer uma das interfaces.</span><span class="sxs-lookup"><span data-stu-id="ca741-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ca741-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca741-118">See also</span></span>

<span data-ttu-id="ca741-119">-[Arquitetura e os recursos MAPI](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="ca741-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

