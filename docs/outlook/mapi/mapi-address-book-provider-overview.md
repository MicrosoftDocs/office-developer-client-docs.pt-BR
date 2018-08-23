---
title: Visão geral de provedor de catálogo de endereços MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 855b145bcca8007601eb8e841665306d4c58982f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576558"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="f2204-103">Visão geral de provedor de catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="f2204-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="f2204-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2204-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2204-105">No catálogo de endereços provedores alça acesso às informações de diretório.</span><span class="sxs-lookup"><span data-stu-id="f2204-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="f2204-106">Informações sobre o diretório dados consiste de dois tipos de destinatários da mensagem: individuais de usuários e grupos de usuários de mensagens que são geralmente resolvidos juntos em listas de distribuição de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f2204-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="f2204-107">Dependendo do tipo de destinatário e o provedor de catálogo de endereços, há uma ampla gama de informações que podem ser disponibilizadas.</span><span class="sxs-lookup"><span data-stu-id="f2204-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="f2204-108">Por exemplo, todos os provedores de catálogo de endereços armazenam o nome, endereço e tipo de endereço do destinatário.</span><span class="sxs-lookup"><span data-stu-id="f2204-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="f2204-109">Cada provedor de catálogo de endereços organiza esses dados usando um ou mais contêineres.</span><span class="sxs-lookup"><span data-stu-id="f2204-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="f2204-110">O número e a estrutura dos contêineres depende da implementação do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="f2204-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="f2204-111">Por exemplo, um provedor de catálogo de endereços pode usar um único recipiente para armazenar todas as informações de outro pode utilizar um contêiner de nível superior que armazena subcontêineres e um terceiro pode usar vários contêineres de nível superior, cada subcontêineres fornecerá.</span><span class="sxs-lookup"><span data-stu-id="f2204-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="f2204-112">Uma hierarquia de contêiner de catálogo de endereços pode ser bastante profunda; Não há nenhum limite no número de subcontêineres que podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="f2204-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="f2204-113">A ilustração a seguir mostra uma organização típica de catálogo de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="f2204-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="f2204-114">**Address book organization**</span><span class="sxs-lookup"><span data-stu-id="f2204-114">**Address book organization**</span></span>
  
<span data-ttu-id="f2204-115">![Organização de catálogo de endereços] (media/amapi_04.gif "Organização de catálogo de endereços")</span><span class="sxs-lookup"><span data-stu-id="f2204-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="f2204-116">MAPI integra todas as informações fornecidas pelos provedores de catálogo de endereços instalada em um único catálogo de endereços, apresentando uma exibição unificada para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="f2204-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="f2204-117">A lista integrada mostra os contêineres de nível superior indicados por cada um dos provedores de catálogo de endereços instalada.</span><span class="sxs-lookup"><span data-stu-id="f2204-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="f2204-118">A maioria dos provedores de catálogo de endereços expor somente alguns contêineres (normalmente um a três) no nível superior para inclusão em um nível superior do catálogo de endereços integrado do MAPI.</span><span class="sxs-lookup"><span data-stu-id="f2204-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="f2204-119">Por exemplo, um fornecedor de catálogo de endereços pode tornar "disponível todos os usuários" e "Local" como dois contêineres de nível superior.</span><span class="sxs-lookup"><span data-stu-id="f2204-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="f2204-120">Os usuários de aplicativos cliente podem exibir o conteúdo dos contêineres do catálogo de endereços e, em alguns casos, modificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f2204-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="f2204-121">Contêineres de catálogo de endereços podem ser criados com os níveis de acesso diferente, dependendo do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="f2204-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f2204-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2204-122">See also</span></span>

- [<span data-ttu-id="f2204-123">Arquitetura e os recursos MAPI</span><span class="sxs-lookup"><span data-stu-id="f2204-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

