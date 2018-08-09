---
title: Objetos de Status MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f5b48f8cd4ef6ff41733ec9a18d1ab682f5e6bcb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767963"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="906ee-103">Objetos de Status MAPI</span><span class="sxs-lookup"><span data-stu-id="906ee-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="906ee-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="906ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="906ee-105">Objetos de status relatar informações sobre os recursos MAPI.</span><span class="sxs-lookup"><span data-stu-id="906ee-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="906ee-106">Por exemplo, um provedor de serviços, o processo de envio/recebimento de MAPI ou o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="906ee-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="906ee-107">Não há um objeto de status, fornecendo informações sobre cada provedor de serviços individuais no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="906ee-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="906ee-108">MAPI é responsável por implementar objetos de status para o catálogo de endereços, o processo de envio/recebimento de MAPI e o subsistema.</span><span class="sxs-lookup"><span data-stu-id="906ee-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="906ee-109">O objeto de status do subsistema fornece informações globais.</span><span class="sxs-lookup"><span data-stu-id="906ee-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="906ee-110">O objeto de status para o catálogo de endereços integrada fornece o status de todos os provedores de catálogo de endereços funcionando no momento.</span><span class="sxs-lookup"><span data-stu-id="906ee-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="906ee-111">Cada objeto de status é incluído na tabela de status, na tabela mantida pelo MAPI que fornece aos clientes com todas as informações de status para a sessão.</span><span class="sxs-lookup"><span data-stu-id="906ee-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="906ee-112">Para obter mais informações, consulte as [Tabelas de Status](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="906ee-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="906ee-113">Clientes podem acessar um objeto de status específico por meio da tabela ou, para um provedor de serviço, por meio de seu objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="906ee-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="906ee-114">Por exemplo, para acessar o objeto de status de um provedor catálogo de endereços, um cliente pode chamar **IABLogon::OpenStatusEntry**.</span><span class="sxs-lookup"><span data-stu-id="906ee-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="906ee-115">Para obter mais informações, consulte [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span><span class="sxs-lookup"><span data-stu-id="906ee-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="906ee-116">Os clientes podem usar os objetos de status para:</span><span class="sxs-lookup"><span data-stu-id="906ee-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="906ee-117">Saiba mais sobre o estado da sessão.</span><span class="sxs-lookup"><span data-stu-id="906ee-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="906ee-118">Monitore a um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="906ee-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="906ee-119">Controle de transmissão da mensagem.</span><span class="sxs-lookup"><span data-stu-id="906ee-119">Control message transmission.</span></span>
    
- <span data-ttu-id="906ee-120">Exibir ou alterar a configuração e o status do recurso.</span><span class="sxs-lookup"><span data-stu-id="906ee-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="906ee-121">Cada objeto de status implementa a interface de **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="906ee-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="906ee-122">Para obter mais informações, consulte [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="906ee-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="906ee-123">No entanto, não a cada objeto de status totalmente fornece suporte a cada método **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="906ee-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="906ee-124">Como há variação nos métodos suportados por um objeto de status, os clientes precisam aprender sobre um objeto determinado status antes que eles podem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="906ee-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="906ee-125">Objetos de status são necessários para publicar informações sobre seus recursos nas seguintes três propriedades:</span><span class="sxs-lookup"><span data-stu-id="906ee-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="906ee-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="906ee-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="906ee-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="906ee-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="906ee-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="906ee-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="906ee-129">Para obter mais informações sobre como implementar um objeto de status, consulte o [Status de implementação de objeto](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="906ee-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="906ee-130">Para obter mais informações sobre como usar um objeto de status, consulte a [tabela de Status e objetos de Status](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="906ee-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
