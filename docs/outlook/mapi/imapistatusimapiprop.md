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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e36a987174ffb2abb4c0f5fc95bf695f31af942e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767211"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="03713-103">IMAPIStatus: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="03713-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="03713-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03713-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03713-105">Fornece informações de status sobre o MAPI spooler, o catálogo de endereços integrada e o subsistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="03713-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="03713-106">Um provedor de serviços implementa **IMAPIStatus** para fornecer informações sobre seu próprio status.</span><span class="sxs-lookup"><span data-stu-id="03713-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03713-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="03713-107">Header file:</span></span>  <br/> |<span data-ttu-id="03713-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03713-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="03713-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="03713-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="03713-110">Objetos de status</span><span class="sxs-lookup"><span data-stu-id="03713-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="03713-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="03713-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="03713-112">Provedores de serviços e MAPI</span><span class="sxs-lookup"><span data-stu-id="03713-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="03713-113">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="03713-113">Called by:</span></span>  <br/> |<span data-ttu-id="03713-114">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="03713-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="03713-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="03713-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="03713-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="03713-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="03713-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="03713-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="03713-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="03713-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="03713-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="03713-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="03713-120">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="03713-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="03713-121">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="03713-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="03713-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="03713-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="03713-123">Confirma as informações de status externos disponíveis para o recurso MAPI ou o provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="03713-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="03713-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="03713-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="03713-125">Exibe uma folha de propriedades que permite ao usuário alterar a configuração de um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="03713-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="03713-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="03713-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="03713-127">Modifica a senha de um provedor de serviços sem exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="03713-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="03713-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="03713-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="03713-129">Força todas as mensagens aguardando para ser enviado ou recebido para ser carregadas ou baixadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="03713-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="03713-130">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="03713-130">**Required properties**</span></span>|<span data-ttu-id="03713-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="03713-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="03713-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03713-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="03713-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="03713-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="03713-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03713-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="03713-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="03713-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="03713-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03713-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="03713-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03713-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="03713-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03713-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="03713-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03713-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="03713-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03713-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="03713-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03713-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="03713-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03713-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="03713-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03713-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="03713-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03713-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="03713-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03713-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03713-146">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="03713-146">Remarks</span></span>

<span data-ttu-id="03713-147">Os objetos de status que implementa MAPI suportam os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="03713-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="03713-148">**Objeto de status**</span><span class="sxs-lookup"><span data-stu-id="03713-148">**Status object**</span></span>|<span data-ttu-id="03713-149">**Métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="03713-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="03713-150">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="03713-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="03713-151">**ValidateState** apenas</span><span class="sxs-lookup"><span data-stu-id="03713-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="03713-152">Catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="03713-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="03713-153">**ValidateState** apenas</span><span class="sxs-lookup"><span data-stu-id="03713-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="03713-154">Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="03713-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="03713-155">**ValidateState** e **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="03713-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="03713-156">Os objetos de status que implementa MAPI são necessários para ter uma versão somente leitura dos métodos da interface [IMAPIProp](imapipropiunknown.md) e suporte ao método **ValidateState** .</span><span class="sxs-lookup"><span data-stu-id="03713-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="03713-157">Provedores de transporte também devem oferecer suporte a **FlushQueues**.</span><span class="sxs-lookup"><span data-stu-id="03713-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="03713-158">Todos os provedores devem oferecer suporte a **SettingsDialog**; o suporte para **ChangePassword** é opcional.</span><span class="sxs-lookup"><span data-stu-id="03713-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="03713-159">Clientes usam objetos de status para executar a configuração e para saber mais sobre o estado da sessão.</span><span class="sxs-lookup"><span data-stu-id="03713-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="03713-160">Eles acessar um objeto de status chamando o método **OpenStatusEntry** de um objeto de logon do provedor de serviço ou o método [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para recuperar o objeto de status.</span><span class="sxs-lookup"><span data-stu-id="03713-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03713-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="03713-161">See also</span></span>



[<span data-ttu-id="03713-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="03713-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

