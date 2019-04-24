---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348829"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="65dbf-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="65dbf-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="65dbf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65dbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65dbf-105">Acessa recursos em um provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="65dbf-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65dbf-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="65dbf-106">Header file:</span></span>  <br/> |<span data-ttu-id="65dbf-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="65dbf-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="65dbf-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="65dbf-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="65dbf-109">Objetos de logon do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="65dbf-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="65dbf-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="65dbf-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="65dbf-111">Provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="65dbf-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="65dbf-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="65dbf-112">Called by:</span></span>  <br/> |<span data-ttu-id="65dbf-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="65dbf-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="65dbf-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="65dbf-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="65dbf-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="65dbf-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="65dbf-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="65dbf-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="65dbf-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="65dbf-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="65dbf-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="65dbf-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="65dbf-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="65dbf-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="65dbf-120">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="65dbf-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="65dbf-121">Fazer logoff</span><span class="sxs-lookup"><span data-stu-id="65dbf-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="65dbf-122">Inicia o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="65dbf-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="65dbf-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="65dbf-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="65dbf-124">Abre um contêiner, um usuário de mensagens ou uma lista de distribuição e retorna um ponteiro para uma implementação de interface para fornecer acesso adicional.</span><span class="sxs-lookup"><span data-stu-id="65dbf-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="65dbf-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="65dbf-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="65dbf-126">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="65dbf-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="65dbf-127">Utilizar</span><span class="sxs-lookup"><span data-stu-id="65dbf-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="65dbf-128">Registra o chamador para receber notificações de eventos específicos que afetam um contêiner, usuário de mensagens ou lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="65dbf-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="65dbf-129">Cancelar</span><span class="sxs-lookup"><span data-stu-id="65dbf-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="65dbf-130">Cancela as notificações que foram configuradas anteriormente com uma chamada para o método **Advise** .</span><span class="sxs-lookup"><span data-stu-id="65dbf-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="65dbf-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="65dbf-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="65dbf-132">Abre o objeto status do provedor.</span><span class="sxs-lookup"><span data-stu-id="65dbf-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="65dbf-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="65dbf-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="65dbf-134">Abre uma entrada de destinatário que tem dados residindo em um provedor de catálogo de endereços de host.</span><span class="sxs-lookup"><span data-stu-id="65dbf-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="65dbf-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="65dbf-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="65dbf-136">Retorna uma tabela de modelos únicos para a criação de destinatários a serem adicionados à lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="65dbf-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="65dbf-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="65dbf-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="65dbf-138">Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="65dbf-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65dbf-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="65dbf-139">Remarks</span></span>

<span data-ttu-id="65dbf-140">Para obter informações gerais sobre os métodos da interface **IABLogon** , consulte [Implementing Service Provider logon](implementing-service-provider-logon.md).</span><span class="sxs-lookup"><span data-stu-id="65dbf-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="65dbf-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="65dbf-141">See also</span></span>



[<span data-ttu-id="65dbf-142">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="65dbf-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

