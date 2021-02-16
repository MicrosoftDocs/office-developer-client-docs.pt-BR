---
title: Visão geral do provedor de agenda de endereços MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ee628f4b11cb174c05a16ca60c9ec830a0e9abbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426538"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="aba37-103">Visão geral do provedor de agenda de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="aba37-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="aba37-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aba37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aba37-105">Os provedores de agendas lidam com o acesso às informações do diretório.</span><span class="sxs-lookup"><span data-stu-id="aba37-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="aba37-106">As informações de diretório consistem em dados para dois tipos de destinatários de mensagens: usuários de mensagens individuais e grupos de usuários de mensagens que normalmente são abordados juntos em listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="aba37-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="aba37-107">Dependendo do tipo de destinatário e do provedor do livro de endereços, há uma ampla variedade de informações que podem ser disponibilizadas.</span><span class="sxs-lookup"><span data-stu-id="aba37-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="aba37-108">Por exemplo, todos os provedores de agendas armazenam o nome, o endereço e o tipo de endereço de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="aba37-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="aba37-109">Cada provedor de agendas organiza esses dados usando um ou mais contêineres.</span><span class="sxs-lookup"><span data-stu-id="aba37-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="aba37-110">O número e a estrutura dos contêineres dependem da implementação do provedor de agendas.</span><span class="sxs-lookup"><span data-stu-id="aba37-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="aba37-111">Por exemplo, um provedor de livro de endereços pode usar um único contêiner para reter todas as informações, outro pode usar um contêiner de nível superior que contém subcontentores e um terceiro pode usar vários contêineres de nível superior, cada um mantendo subcontainers.</span><span class="sxs-lookup"><span data-stu-id="aba37-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="aba37-112">Uma hierarquia de contêineres de um livro de endereços pode ser muito profunda; não há limite para o número de subcontainers que podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="aba37-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="aba37-113">A ilustração a seguir mostra uma organização típica do livro de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="aba37-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="aba37-114">**Address book organization**</span><span class="sxs-lookup"><span data-stu-id="aba37-114">**Address book organization**</span></span>
  
<span data-ttu-id="aba37-115">![Organização do address book Address](media/amapi_04.gif "book")</span><span class="sxs-lookup"><span data-stu-id="aba37-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="aba37-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span><span class="sxs-lookup"><span data-stu-id="aba37-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="aba37-117">A lista integrada mostra os contêineres de nível superior exibidos por cada um dos provedores de agendas instalados.</span><span class="sxs-lookup"><span data-stu-id="aba37-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="aba37-118">A maioria dos provedores de livro de endereços expõe apenas alguns contêineres (normalmente um a três) no nível superior para inclusão no nível superior do livro de endereços integrado MAPI.</span><span class="sxs-lookup"><span data-stu-id="aba37-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="aba37-119">Por exemplo, um provedor de agendas pode disponibilizar "Todos os Usuários" e "Usuários Locais" como dois contêineres no nível superior.</span><span class="sxs-lookup"><span data-stu-id="aba37-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="aba37-120">Os usuários de aplicativos cliente podem exibir o conteúdo dos contêineres do livro de endereços e, em alguns casos, modificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="aba37-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="aba37-121">Os contêineres de agenda podem ser criados com níveis de acesso diferentes, dependendo do provedor de agendas.</span><span class="sxs-lookup"><span data-stu-id="aba37-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aba37-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="aba37-122">See also</span></span>

- [<span data-ttu-id="aba37-123">Recursos e arquitetura MAPI</span><span class="sxs-lookup"><span data-stu-id="aba37-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

