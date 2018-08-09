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
ms.openlocfilehash: 784430f1286c9a017337a0fae4b269757a56a3e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766860"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="72eb6-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72eb6-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="72eb6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72eb6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72eb6-105">Recursos de acessos em um provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="72eb6-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72eb6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="72eb6-106">Header file:</span></span>  <br/> |<span data-ttu-id="72eb6-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="72eb6-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="72eb6-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="72eb6-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="72eb6-109">Objetos de logon do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="72eb6-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="72eb6-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="72eb6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="72eb6-111">Provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="72eb6-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="72eb6-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="72eb6-112">Called by:</span></span>  <br/> |<span data-ttu-id="72eb6-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="72eb6-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="72eb6-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="72eb6-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="72eb6-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="72eb6-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="72eb6-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="72eb6-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="72eb6-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="72eb6-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="72eb6-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="72eb6-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="72eb6-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="72eb6-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="72eb6-120">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de provedor de catálogo de endereços anterior.</span><span class="sxs-lookup"><span data-stu-id="72eb6-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="72eb6-121">Fazer logoff</span><span class="sxs-lookup"><span data-stu-id="72eb6-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="72eb6-122">Inicia o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="72eb6-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="72eb6-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="72eb6-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="72eb6-124">Abre um contêiner, o usuário ou lista de distribuição de mensagens e retorna um ponteiro para uma implementação de interface para fornecer mais acesso.</span><span class="sxs-lookup"><span data-stu-id="72eb6-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="72eb6-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="72eb6-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="72eb6-126">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="72eb6-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="72eb6-127">Aviso</span><span class="sxs-lookup"><span data-stu-id="72eb6-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="72eb6-128">Registra o chamador para receber notificações de eventos especificados que afetam um contêiner, o usuário ou lista de distribuição de mensagens.</span><span class="sxs-lookup"><span data-stu-id="72eb6-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="72eb6-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="72eb6-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="72eb6-130">Cancela notificações que foram definidas com uma chamada ao método **Advise** anteriormente.</span><span class="sxs-lookup"><span data-stu-id="72eb6-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="72eb6-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="72eb6-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="72eb6-132">Abre o objeto de status do provedor.</span><span class="sxs-lookup"><span data-stu-id="72eb6-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="72eb6-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="72eb6-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="72eb6-134">Abre uma entrada do destinatário que possui dados que residem em um provedor de catálogo de endereço de host.</span><span class="sxs-lookup"><span data-stu-id="72eb6-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="72eb6-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="72eb6-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="72eb6-136">Retorna uma tabela de modelos únicos para a criação de destinatários a ser adicionado à lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="72eb6-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="72eb6-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="72eb6-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="72eb6-138">Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="72eb6-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72eb6-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="72eb6-139">Remarks</span></span>

<span data-ttu-id="72eb6-140">Para obter informações gerais sobre os métodos da interface **IABLogon** , consulte [Implementando Logon do provedor de serviço](implementing-service-provider-logon.md).</span><span class="sxs-lookup"><span data-stu-id="72eb6-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72eb6-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="72eb6-141">See also</span></span>



[<span data-ttu-id="72eb6-142">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="72eb6-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

