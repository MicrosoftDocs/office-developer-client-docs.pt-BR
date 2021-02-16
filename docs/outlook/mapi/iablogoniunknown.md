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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431075"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="ee5c9-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee5c9-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="ee5c9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee5c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee5c9-105">Acessa recursos em um provedor de agendamento de endereços.</span><span class="sxs-lookup"><span data-stu-id="ee5c9-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee5c9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ee5c9-106">Header file:</span></span>  <br/> |<span data-ttu-id="ee5c9-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="ee5c9-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="ee5c9-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="ee5c9-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ee5c9-109">Objetos de logon do livro de endereços</span><span class="sxs-lookup"><span data-stu-id="ee5c9-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="ee5c9-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ee5c9-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ee5c9-111">Provedores de lista de endereços</span><span class="sxs-lookup"><span data-stu-id="ee5c9-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="ee5c9-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="ee5c9-112">Called by:</span></span>  <br/> |<span data-ttu-id="ee5c9-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="ee5c9-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="ee5c9-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="ee5c9-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ee5c9-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="ee5c9-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="ee5c9-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="ee5c9-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ee5c9-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="ee5c9-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ee5c9-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="ee5c9-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ee5c9-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="ee5c9-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="ee5c9-120">Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro do provedor de agendas anterior.</span><span class="sxs-lookup"><span data-stu-id="ee5c9-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="ee5c9-121">Fazer logoff</span><span class="sxs-lookup"><span data-stu-id="ee5c9-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="ee5c9-122">Inicia o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="ee5c9-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="ee5c9-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ee5c9-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="ee5c9-124">Abre um contêiner, um usuário de mensagens ou uma lista de distribuição e retorna um ponteiro para uma implementação de interface para fornecer mais acesso.</span><span class="sxs-lookup"><span data-stu-id="ee5c9-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="ee5c9-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ee5c9-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="ee5c9-126">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="ee5c9-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="ee5c9-127">Advise</span><span class="sxs-lookup"><span data-stu-id="ee5c9-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="ee5c9-128">Registra o chamador para receber notificação de eventos especificados que afetam um contêiner, um usuário de mensagens ou uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="ee5c9-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="ee5c9-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="ee5c9-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="ee5c9-130">Cancela notificações que foram configuradas anteriormente com uma chamada para o **método Advise.**</span><span class="sxs-lookup"><span data-stu-id="ee5c9-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="ee5c9-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="ee5c9-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="ee5c9-132">Abre o objeto de status do provedor.</span><span class="sxs-lookup"><span data-stu-id="ee5c9-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="ee5c9-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="ee5c9-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="ee5c9-134">Abre uma entrada de destinatário que tem dados residindo em um provedor de agendamento de endereço de host.</span><span class="sxs-lookup"><span data-stu-id="ee5c9-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="ee5c9-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="ee5c9-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="ee5c9-136">Retorna uma tabela de modelos one-off para a criação de destinatários a serem adicionados à lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="ee5c9-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="ee5c9-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="ee5c9-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="ee5c9-138">Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ee5c9-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee5c9-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee5c9-139">Remarks</span></span>

<span data-ttu-id="ee5c9-140">Para obter informações gerais sobre os métodos da interface **IABLogon,** consulte Implementando o [logon do provedor de serviços.](implementing-service-provider-logon.md)</span><span class="sxs-lookup"><span data-stu-id="ee5c9-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee5c9-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee5c9-141">See also</span></span>



[<span data-ttu-id="ee5c9-142">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ee5c9-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

