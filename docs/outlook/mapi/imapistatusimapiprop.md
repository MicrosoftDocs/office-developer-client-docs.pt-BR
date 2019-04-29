---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408296"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="b7ac9-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b7ac9-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="b7ac9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7ac9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7ac9-105">Fornece informações de status sobre o subsistema MAPI, o catálogo de endereços integrado e o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7ac9-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="b7ac9-106">Um provedor de serviços implementa o **IMAPIStatus** para fornecer informações sobre seu próprio status.</span><span class="sxs-lookup"><span data-stu-id="b7ac9-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7ac9-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b7ac9-107">Header file:</span></span>  <br/> |<span data-ttu-id="b7ac9-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b7ac9-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b7ac9-109">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="b7ac9-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="b7ac9-110">Objetos de status</span><span class="sxs-lookup"><span data-stu-id="b7ac9-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="b7ac9-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b7ac9-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="b7ac9-112">Provedores de serviços e MAPI</span><span class="sxs-lookup"><span data-stu-id="b7ac9-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="b7ac9-113">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="b7ac9-113">Called by:</span></span>  <br/> |<span data-ttu-id="b7ac9-114">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="b7ac9-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="b7ac9-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="b7ac9-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b7ac9-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="b7ac9-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="b7ac9-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="b7ac9-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="b7ac9-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="b7ac9-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="b7ac9-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="b7ac9-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="b7ac9-120">Não-Transacted</span><span class="sxs-lookup"><span data-stu-id="b7ac9-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b7ac9-121">Vtable order</span><span class="sxs-lookup"><span data-stu-id="b7ac9-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b7ac9-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="b7ac9-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="b7ac9-123">Confirma as informações de status externas disponíveis para o recurso MAPI ou provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="b7ac9-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="b7ac9-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="b7ac9-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="b7ac9-125">Exibe uma folha de propriedades que permite que o usuário altere a configuração de um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="b7ac9-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="b7ac9-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="b7ac9-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="b7ac9-127">Modifica a senha de um provedor de serviços sem exibir uma interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="b7ac9-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="b7ac9-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="b7ac9-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="b7ac9-129">Força todas as mensagens aguardando para serem enviadas ou recebidas para serem carregadas ou baixadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="b7ac9-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="b7ac9-130">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="b7ac9-130">**Required properties**</span></span>|<span data-ttu-id="b7ac9-131">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="b7ac9-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7ac9-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b7ac9-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b7ac9-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b7ac9-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="b7ac9-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b7ac9-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b7ac9-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b7ac9-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="b7ac9-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b7ac9-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b7ac9-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7ac9-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="b7ac9-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b7ac9-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b7ac9-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7ac9-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="b7ac9-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b7ac9-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b7ac9-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7ac9-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="b7ac9-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b7ac9-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b7ac9-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7ac9-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="b7ac9-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b7ac9-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b7ac9-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7ac9-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7ac9-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7ac9-146">Remarks</span></span>

<span data-ttu-id="b7ac9-147">Os objetos de status que o MAPI implementa suporta os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="b7ac9-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="b7ac9-148">**Objeto status**</span><span class="sxs-lookup"><span data-stu-id="b7ac9-148">**Status object**</span></span>|<span data-ttu-id="b7ac9-149">**Métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="b7ac9-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7ac9-150">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="b7ac9-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="b7ac9-151">**ValidateState** somente</span><span class="sxs-lookup"><span data-stu-id="b7ac9-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="b7ac9-152">Catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="b7ac9-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="b7ac9-153">**ValidateState** somente</span><span class="sxs-lookup"><span data-stu-id="b7ac9-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="b7ac9-154">Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="b7ac9-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="b7ac9-155">**ValidateState** e **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="b7ac9-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="b7ac9-156">Os objetos de status que o MAPI implementa precisam ter uma versão somente leitura dos métodos da interface [IMAPIProp](imapipropiunknown.md) e para dar suporte ao método **ValidateState** .</span><span class="sxs-lookup"><span data-stu-id="b7ac9-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="b7ac9-157">Os provedores de transporte também devem oferecer suporte a **FlushQueues**.</span><span class="sxs-lookup"><span data-stu-id="b7ac9-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="b7ac9-158">Todos os provedores devem suportar o **SettingsDialog**; o suporte para **ChangePassword** é opcional.</span><span class="sxs-lookup"><span data-stu-id="b7ac9-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="b7ac9-159">Os clientes usam objetos de status para executar a configuração e para saber mais sobre o estado da sessão.</span><span class="sxs-lookup"><span data-stu-id="b7ac9-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="b7ac9-160">Eles acessam um objeto status chamando o método **OpenStatusEntry** de um objeto de logon do provedor de serviços ou o método [IMAPISession::](imapisession-getstatustable.md) getstatustable para recuperar o objeto status.</span><span class="sxs-lookup"><span data-stu-id="b7ac9-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7ac9-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7ac9-161">See also</span></span>



[<span data-ttu-id="b7ac9-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b7ac9-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

