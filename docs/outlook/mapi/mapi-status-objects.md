---
title: Objetos de status MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406742"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="d31ef-103">Objetos de status MAPI</span><span class="sxs-lookup"><span data-stu-id="d31ef-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="d31ef-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d31ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d31ef-105">Os objetos de status relatam informações sobre recursos MAPI.</span><span class="sxs-lookup"><span data-stu-id="d31ef-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="d31ef-106">Por exemplo, um provedor de serviços, o processo de envio/recebimento MAPI ou o livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="d31ef-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="d31ef-107">Há um objeto de status que fornece informações sobre cada provedor de serviços individual no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="d31ef-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="d31ef-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span><span class="sxs-lookup"><span data-stu-id="d31ef-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="d31ef-109">O objeto de status do subsistema fornece informações globais.</span><span class="sxs-lookup"><span data-stu-id="d31ef-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="d31ef-110">O objeto de status do livro de endereços integrado fornece o status de todos os provedores de agendas que operam no momento.</span><span class="sxs-lookup"><span data-stu-id="d31ef-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="d31ef-111">Cada objeto de status é incluído na tabela de status, uma tabela mantida pela MAPI que fornece aos clientes todas as informações de status da sessão.</span><span class="sxs-lookup"><span data-stu-id="d31ef-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="d31ef-112">Para obter mais informações, consulte [Tabelas de Status.](status-tables.md)</span><span class="sxs-lookup"><span data-stu-id="d31ef-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="d31ef-113">Os clientes podem acessar um objeto de status específico por meio da tabela ou, para um provedor de serviços, por meio de seu objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="d31ef-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="d31ef-114">Por exemplo, para acessar o objeto de status de um provedor de agendamento de endereços, um cliente pode chamar **IABLogon::OpenStatusEntry**.</span><span class="sxs-lookup"><span data-stu-id="d31ef-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="d31ef-115">Para obter mais informações, consulte [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span><span class="sxs-lookup"><span data-stu-id="d31ef-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="d31ef-116">Os clientes podem usar objetos de status para:</span><span class="sxs-lookup"><span data-stu-id="d31ef-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="d31ef-117">Saiba mais sobre o estado de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="d31ef-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="d31ef-118">Monitore um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="d31ef-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="d31ef-119">Controlar a transmissão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d31ef-119">Control message transmission.</span></span>
    
- <span data-ttu-id="d31ef-120">Exibir ou alterar a configuração e o status de um recurso.</span><span class="sxs-lookup"><span data-stu-id="d31ef-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="d31ef-121">Cada objeto de status implementa a interface **IMAPIStatus.**</span><span class="sxs-lookup"><span data-stu-id="d31ef-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="d31ef-122">Para obter mais informações, [consulte IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="d31ef-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="d31ef-123">No entanto, nem todos os objetos de status são compatíveis com todos **os métodos IMAPIStatus.**</span><span class="sxs-lookup"><span data-stu-id="d31ef-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="d31ef-124">Como há variação nos métodos suportados por um objeto de status, os clientes precisam aprender sobre um objeto de status específico antes de poder usá-lo.</span><span class="sxs-lookup"><span data-stu-id="d31ef-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="d31ef-125">Os objetos de status são necessários para publicar informações sobre seus recursos nas três propriedades a seguir:</span><span class="sxs-lookup"><span data-stu-id="d31ef-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="d31ef-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d31ef-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="d31ef-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d31ef-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="d31ef-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d31ef-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="d31ef-129">Para obter mais informações sobre a implementação de um objeto de status, consulte [Implementação de objeto de status.](status-object-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="d31ef-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="d31ef-130">Para obter mais informações sobre como usar um objeto de status, consulte [Status Table and Status Objects](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d31ef-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

