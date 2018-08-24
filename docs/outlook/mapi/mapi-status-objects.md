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
ms.openlocfilehash: 69a4d25fc6a7abec68c94cc947e5944322d230a6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594947"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="fce03-103">Objetos de Status MAPI</span><span class="sxs-lookup"><span data-stu-id="fce03-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="fce03-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fce03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fce03-105">Objetos de status relatar informações sobre os recursos MAPI.</span><span class="sxs-lookup"><span data-stu-id="fce03-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="fce03-106">Por exemplo, um provedor de serviços, o processo de envio/recebimento de MAPI ou o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="fce03-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="fce03-107">Não há um objeto de status, fornecendo informações sobre cada provedor de serviços individuais no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="fce03-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="fce03-108">MAPI é responsável por implementar objetos de status para o catálogo de endereços, o processo de envio/recebimento de MAPI e o subsistema.</span><span class="sxs-lookup"><span data-stu-id="fce03-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="fce03-109">O objeto de status do subsistema fornece informações globais.</span><span class="sxs-lookup"><span data-stu-id="fce03-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="fce03-110">O objeto de status para o catálogo de endereços integrada fornece o status de todos os provedores de catálogo de endereços funcionando no momento.</span><span class="sxs-lookup"><span data-stu-id="fce03-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="fce03-111">Cada objeto de status é incluído na tabela de status, na tabela mantida pelo MAPI que fornece aos clientes com todas as informações de status para a sessão.</span><span class="sxs-lookup"><span data-stu-id="fce03-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="fce03-112">Para obter mais informações, consulte as [Tabelas de Status](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="fce03-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="fce03-113">Clientes podem acessar um objeto de status específico por meio da tabela ou, para um provedor de serviço, por meio de seu objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="fce03-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="fce03-114">Por exemplo, para acessar o objeto de status de um provedor catálogo de endereços, um cliente pode chamar **IABLogon::OpenStatusEntry**.</span><span class="sxs-lookup"><span data-stu-id="fce03-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="fce03-115">Para obter mais informações, consulte [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span><span class="sxs-lookup"><span data-stu-id="fce03-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="fce03-116">Os clientes podem usar os objetos de status para:</span><span class="sxs-lookup"><span data-stu-id="fce03-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="fce03-117">Saiba mais sobre o estado da sessão.</span><span class="sxs-lookup"><span data-stu-id="fce03-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="fce03-118">Monitore a um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="fce03-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="fce03-119">Controle de transmissão da mensagem.</span><span class="sxs-lookup"><span data-stu-id="fce03-119">Control message transmission.</span></span>
    
- <span data-ttu-id="fce03-120">Exibir ou alterar a configuração e o status do recurso.</span><span class="sxs-lookup"><span data-stu-id="fce03-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="fce03-121">Cada objeto de status implementa a interface de **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="fce03-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="fce03-122">Para obter mais informações, consulte [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="fce03-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="fce03-123">No entanto, não a cada objeto de status totalmente fornece suporte a cada método **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="fce03-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="fce03-124">Como há variação nos métodos suportados por um objeto de status, os clientes precisam aprender sobre um objeto determinado status antes que eles podem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="fce03-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="fce03-125">Objetos de status são necessários para publicar informações sobre seus recursos nas seguintes três propriedades:</span><span class="sxs-lookup"><span data-stu-id="fce03-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="fce03-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fce03-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fce03-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fce03-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fce03-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fce03-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="fce03-129">Para obter mais informações sobre como implementar um objeto de status, consulte o [Status de implementação de objeto](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="fce03-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="fce03-130">Para obter mais informações sobre como usar um objeto de status, consulte a [tabela de Status e objetos de Status](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="fce03-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

