---
title: Objetos implementada de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fe5549e41008dbf5b5f50f9f32769f1a820e3bc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767878"
---
# <a name="mapi-implemented-objects"></a><span data-ttu-id="6aee5-103">Objetos implementada de MAPI</span><span class="sxs-lookup"><span data-stu-id="6aee5-103">MAPI-implemented objects</span></span>
  
<span data-ttu-id="6aee5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6aee5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6aee5-105">MAPI implementa vários objetos para uso por provedores de serviços e aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="6aee5-105">MAPI implements several objects for use by client applications and service providers.</span></span> <span data-ttu-id="6aee5-106">O objeto de sessão permite aos clientes utilizarem serviços de sessão, para acessar tabelas e se comuniquem com provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="6aee5-106">The session object allows clients to use session services, to access tables, and to communicate with service providers.</span></span> <span data-ttu-id="6aee5-107">O objeto de catálogo de endereços fornece clientes com acesso integrado para todos os provedores de catálogo de endereço diferente.</span><span class="sxs-lookup"><span data-stu-id="6aee5-107">The address book object provides clients with integrated access to all of the different address book providers.</span></span> 
  
<span data-ttu-id="6aee5-108">MAPI fornece vários objetos de tabela e status para clientes usarem para exibição e informações do provedor de sessão e o serviço de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="6aee5-108">MAPI supplies multiple table and status objects for clients to use for viewing and monitoring session and service provider information.</span></span> <span data-ttu-id="6aee5-109">Por exemplo, MAPI fornece uma tabela de perfil com informações sobre todos os perfis que estão instalados no computador e uma tabela de serviço de mensagem com informações sobre todos os serviços de mensagem no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="6aee5-109">For example, MAPI provides a profile table with information about all of the profiles that are installed on the computer and a message service table with information about all of the message services in the current profile.</span></span> <span data-ttu-id="6aee5-110">MAPI fornece três objetos diferentes status: uma que representa o subsistema de geral, um para o spooler MAPI e outro para o catálogo de endereços integrada.</span><span class="sxs-lookup"><span data-stu-id="6aee5-110">MAPI provides three different status objects: one that represents the overall subsystem, one for the MAPI spooler, and one for the integrated address book.</span></span> 
  
<span data-ttu-id="6aee5-111">MAPI implementa quatro objetos diferentes para gerenciar a configuração de serviços de mensagens, provedores de serviços e perfis.</span><span class="sxs-lookup"><span data-stu-id="6aee5-111">MAPI implements four different objects for managing the configuration of message services, service providers, and profiles.</span></span> <span data-ttu-id="6aee5-112">Provedores de serviços e clientes usam a administração do provedor e objetos de seção perfil; Esses objetos habilitá-los configurar provedores de serviços e acessar propriedades de perfil.</span><span class="sxs-lookup"><span data-stu-id="6aee5-112">Both clients and service providers use provider administration and profile section objects; these objects enable them to configure service providers and access profile properties.</span></span> <span data-ttu-id="6aee5-113">Os clientes usam apenas o serviço de mensagem e objetos de administração de perfil, os objetos que permitem a administração dos serviços de mensagem e perfis.</span><span class="sxs-lookup"><span data-stu-id="6aee5-113">Clients use only message service and profile administration objects, the objects that support the administration of message services and profiles.</span></span> 
  
<span data-ttu-id="6aee5-114">MAPI fornece dois objetos para provedores de serviço: um objeto de suporte e um objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="6aee5-114">MAPI provides two objects for service providers: a support object and a TNEF object.</span></span> <span data-ttu-id="6aee5-115">Todos os provedores de serviços usam um ou mais objetos de suporte; Há quatro implementações de objeto de suporte de diferentes.</span><span class="sxs-lookup"><span data-stu-id="6aee5-115">All service providers use one or more support objects; there are four different support object implementations.</span></span> <span data-ttu-id="6aee5-116">MAPI fornece uma implementação para oferecer suporte a configuração, bem como implementações específicas para dar suporte ao catálogo de endereços, armazenamento de mensagens e provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="6aee5-116">MAPI supplies an implementation to support configuration as well as specific implementations to support address book, message store, and transport providers.</span></span> <span data-ttu-id="6aee5-117">O objeto TNEF é usado pelos provedores de transporte que suportam o TNEF Transport Neutral Encapsulation Format ().</span><span class="sxs-lookup"><span data-stu-id="6aee5-117">The TNEF object is used by transport providers that support the Transport Neutral Encapsulation Format (TNEF).</span></span>
  
<span data-ttu-id="6aee5-118">Dois objetos utilitário, dados da tabela e dados de propriedade, geralmente são usados pelos provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="6aee5-118">Two utility objects, table data and property data, are typically used by service providers.</span></span> <span data-ttu-id="6aee5-119">Objetos de dados de tabela ajudam na implementação de objetos table; Ajuda de objetos de dados de propriedade para o acesso à propriedade definido e o modo de exibição e ajuda na implementação do [IMAPIProp: IUnknown](imapipropiunknown.md), a interface de propriedade base.</span><span class="sxs-lookup"><span data-stu-id="6aee5-119">Table data objects help in the implementation of table objects; property data objects help to set and view property access and help in the implementation of [IMAPIProp : IUnknown](imapipropiunknown.md), the base property interface.</span></span> 
  
<span data-ttu-id="6aee5-120">A tabela a seguir resume o objetivo de cada objeto que implementa de MAPI.</span><span class="sxs-lookup"><span data-stu-id="6aee5-120">The following table summarizes the purpose for each object that MAPI implements.</span></span>
  
|<span data-ttu-id="6aee5-121">**Objeto MAPI**</span><span class="sxs-lookup"><span data-stu-id="6aee5-121">**MAPI object**</span></span>|<span data-ttu-id="6aee5-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6aee5-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6aee5-123">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="6aee5-123">Address book</span></span>  <br/> |<span data-ttu-id="6aee5-124">Fornece acesso ao modo de exibição integrado de informações do destinatário que pertence a todos os provedores de catálogo de endereços no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="6aee5-124">Provides access to the integrated view of recipient information that belongs to all of the address book providers in the active profile.</span></span>  <br/> |
|<span data-ttu-id="6aee5-125">Administração do serviço de mensagem</span><span class="sxs-lookup"><span data-stu-id="6aee5-125">Message service administration</span></span>  <br/> |<span data-ttu-id="6aee5-126">Fornece acesso a informações de serviço de mensagem para a configuração.</span><span class="sxs-lookup"><span data-stu-id="6aee5-126">Provides access to message service information for configuration.</span></span>  <br/> |
|<span data-ttu-id="6aee5-127">Administração de perfil</span><span class="sxs-lookup"><span data-stu-id="6aee5-127">Profile administration</span></span>  <br/> |<span data-ttu-id="6aee5-128">Fornece acesso às informações de perfil de configuração.</span><span class="sxs-lookup"><span data-stu-id="6aee5-128">Provides access to profile information for configuration.</span></span>  <br/> |
|<span data-ttu-id="6aee5-129">Seção de perfil</span><span class="sxs-lookup"><span data-stu-id="6aee5-129">Profile section</span></span>  <br/> |<span data-ttu-id="6aee5-130">Uma parte de um perfil usado para descrever um serviço de mensagem específica ou de um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="6aee5-130">A part of a profile used to describe a particular message service or service provider.</span></span>  <br/> |
|<span data-ttu-id="6aee5-131">Dados de propriedade</span><span class="sxs-lookup"><span data-stu-id="6aee5-131">Property data</span></span>  <br/> |<span data-ttu-id="6aee5-132">Mantém o acesso às propriedades e ajuda a implementar **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="6aee5-132">Maintains access to properties and helps implement **IMAPIProp**.</span></span>  <br/> |
|<span data-ttu-id="6aee5-133">Administração do provedor</span><span class="sxs-lookup"><span data-stu-id="6aee5-133">Provider administration</span></span>  <br/> |<span data-ttu-id="6aee5-134">Oferece acesso a informações do provedor de serviço de configuração.</span><span class="sxs-lookup"><span data-stu-id="6aee5-134">Provides access to service provider information for configuration.</span></span>  <br/> |
|<span data-ttu-id="6aee5-135">Sessão</span><span class="sxs-lookup"><span data-stu-id="6aee5-135">Session</span></span>  <br/> |<span data-ttu-id="6aee5-136">Representa uma conexão aos sistemas de mensagens subjacentes e fornece aos clientes acesso aos recursos MAPI.</span><span class="sxs-lookup"><span data-stu-id="6aee5-136">Represents a connection to underlying messaging systems and provides clients with access to MAPI resources.</span></span>  <br/> |
|<span data-ttu-id="6aee5-137">Status</span><span class="sxs-lookup"><span data-stu-id="6aee5-137">Status</span></span>  <br/> |<span data-ttu-id="6aee5-138">Fornece acesso ao estado do subsistema de MAPI, o catálogo de endereços ou o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="6aee5-138">Provides access to the state of the MAPI subsystem, the address book, or the MAPI spooler.</span></span>  <br/> |
|<span data-ttu-id="6aee5-139">Suporte</span><span class="sxs-lookup"><span data-stu-id="6aee5-139">Support</span></span>  <br/> |<span data-ttu-id="6aee5-140">Ajuda a provedores de serviços de lidar com as solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="6aee5-140">Helps service providers handle client requests.</span></span>  <br/> |
|<span data-ttu-id="6aee5-141">Table</span><span class="sxs-lookup"><span data-stu-id="6aee5-141">Table</span></span>  <br/> |<span data-ttu-id="6aee5-142">Fornece acesso a um modo de exibição de resumo de dados de objeto no formato de linha e coluna, semelhante a uma tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6aee5-142">Provides access to a summary view of object data in row and column format, similar to a database table.</span></span>  <br/> |
|<span data-ttu-id="6aee5-143">Dados da tabela</span><span class="sxs-lookup"><span data-stu-id="6aee5-143">Table data</span></span>  <br/> |<span data-ttu-id="6aee5-144">Mantém o acesso a dados de tabela base e implementa objetos table.</span><span class="sxs-lookup"><span data-stu-id="6aee5-144">Maintains access to underlying table data and implements table objects.</span></span>  <br/> |
|<span data-ttu-id="6aee5-145">TNEF</span><span class="sxs-lookup"><span data-stu-id="6aee5-145">TNEF</span></span>  <br/> |<span data-ttu-id="6aee5-146">Suporta o uso do TNEF Transport Neutral Encapsulation Format ().</span><span class="sxs-lookup"><span data-stu-id="6aee5-146">Supports the use of the Transport Neutral Encapsulation Format (TNEF).</span></span>  <br/> |
   
<span data-ttu-id="6aee5-147">A ilustração a seguir mostra a relação entre os objetos que implementa MAPI, as interfaces do qual eles herdam e os componentes que usá-los.</span><span class="sxs-lookup"><span data-stu-id="6aee5-147">The following illustration shows the relationship between the objects that MAPI implements, the interfaces from which they inherit, and the components that use them.</span></span> 
  
<span data-ttu-id="6aee5-148">**Objects that MAPI implements**</span><span class="sxs-lookup"><span data-stu-id="6aee5-148">**Objects that MAPI implements**</span></span>
  
<span data-ttu-id="6aee5-149">![Objetos que implementa MAPI] (media/amapi_68.gif "Objetos que implementa MAPI")</span><span class="sxs-lookup"><span data-stu-id="6aee5-149">![Objects that MAPI implements](media/amapi_68.gif "Objects that MAPI implements")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6aee5-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="6aee5-150">See also</span></span>

- [<span data-ttu-id="6aee5-151">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6aee5-151">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="6aee5-152">Objeto MAPI e visão geral da Interface</span><span class="sxs-lookup"><span data-stu-id="6aee5-152">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)
