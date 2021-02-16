---
title: Propriedade canônica PidTagResourceFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436227"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="c9451-103">Propriedade canônica PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="c9451-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="c9451-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9451-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9451-105">Contém uma máscara de bits de sinalizadores para provedores e serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c9451-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9451-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c9451-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9451-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c9451-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="c9451-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c9451-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9451-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="c9451-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="c9451-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c9451-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9451-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c9451-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c9451-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c9451-112">Area:</span></span>  <br/> |<span data-ttu-id="c9451-113">MAPI comum</span><span class="sxs-lookup"><span data-stu-id="c9451-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9451-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9451-114">Remarks</span></span>

<span data-ttu-id="c9451-115">Essa propriedade descreve as características de um serviço de mensagem, um provedor de serviços ou um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="c9451-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="c9451-116">Os sinalizadores definidos para essa propriedade dependem de seu contexto.</span><span class="sxs-lookup"><span data-stu-id="c9451-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="c9451-117">Por exemplo, alguns sinalizadores são válidos apenas para objetos de status e outros sinalizadores somente para colunas na tabela de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c9451-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="c9451-118">Os sinalizadores são de três classes: estática, modificável e dinâmica.</span><span class="sxs-lookup"><span data-stu-id="c9451-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="c9451-119">Sinalizadores estáticos são definidos por MAPI a partir de dados em MAPISVC. INF e nunca alterado.</span><span class="sxs-lookup"><span data-stu-id="c9451-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="c9451-120">Sinalizadores modificáveis são definidos por MAPI de MAPISVC. INF, mas pode ser alterado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="c9451-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="c9451-121">Sinalizadores dinâmicos podem ser definidos e redefinidos por métodos MAPI.</span><span class="sxs-lookup"><span data-stu-id="c9451-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="c9451-122">Para um serviço de mensagens, um ou mais dos seguintes sinalizadores podem ser definidos nesta propriedade:</span><span class="sxs-lookup"><span data-stu-id="c9451-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="c9451-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="c9451-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="c9451-124">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c9451-124">Reserved.</span></span> <span data-ttu-id="c9451-125">Não usar.</span><span class="sxs-lookup"><span data-stu-id="c9451-125">Do not use.</span></span>
    
<span data-ttu-id="c9451-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="c9451-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="c9451-127">Dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c9451-127">Dynamic.</span></span> <span data-ttu-id="c9451-128">O serviço de mensagens contém o armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="c9451-128">The message service contains the default store.</span></span> <span data-ttu-id="c9451-129">Uma interface do usuário deve ser exibida solicitando que o usuário confirme antes de excluir ou mover esse serviço para fora do perfil.</span><span class="sxs-lookup"><span data-stu-id="c9451-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="c9451-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="c9451-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="c9451-131">Estático.</span><span class="sxs-lookup"><span data-stu-id="c9451-131">Static.</span></span> <span data-ttu-id="c9451-132">O sinalizador de nível de serviço que deve ser definido para indicar que nenhum dos provedores no serviço de mensagens pode ser usado para fornecer uma identidade.</span><span class="sxs-lookup"><span data-stu-id="c9451-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="c9451-133">Esse sinalizador ou SERVICE_PRIMARY_IDENTITY deve ser definido, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="c9451-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="c9451-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="c9451-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="c9451-135">Modificável.</span><span class="sxs-lookup"><span data-stu-id="c9451-135">Modifiable.</span></span> <span data-ttu-id="c9451-136">O serviço de mensagens correspondente contém o provedor usado para a identidade principal desta sessão.</span><span class="sxs-lookup"><span data-stu-id="c9451-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="c9451-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="c9451-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="c9451-138">Esse sinalizador ou SERVICE_NO_PRIMARY_IDENTITY devem ser definidos, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="c9451-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="c9451-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="c9451-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="c9451-140">Estático.</span><span class="sxs-lookup"><span data-stu-id="c9451-140">Static.</span></span> <span data-ttu-id="c9451-141">Qualquer tentativa de criar ou copiar esse serviço de mensagem em um perfil onde o serviço já existe falhará.</span><span class="sxs-lookup"><span data-stu-id="c9451-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="c9451-142">Para criar um serviço de mensagem de cópia **única, PR_RESOURCE_FLAGS** a propriedade PR_RESOURCE_FLAGS seção do serviço no MAPISVC. INF e de definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="c9451-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="c9451-143">Para um provedor de serviços, um ou mais dos seguintes sinalizadores podem ser definidos **PR_RESOURCE_FLAGS:**</span><span class="sxs-lookup"><span data-stu-id="c9451-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="c9451-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="c9451-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="c9451-145">Estático.</span><span class="sxs-lookup"><span data-stu-id="c9451-145">Static.</span></span> <span data-ttu-id="c9451-146">O gancho do spooler precisa processar mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="c9451-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="c9451-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="c9451-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="c9451-148">Estático.</span><span class="sxs-lookup"><span data-stu-id="c9451-148">Static.</span></span> <span data-ttu-id="c9451-149">O gancho do spooler precisa processar mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="c9451-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="c9451-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="c9451-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="c9451-151">Modificável.</span><span class="sxs-lookup"><span data-stu-id="c9451-151">Modifiable.</span></span> <span data-ttu-id="c9451-152">Essa identidade deve ser aplicada a mensagens de saída se o perfil contiver várias instâncias deste provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c9451-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="c9451-153">Isso pode acontecer se várias instâncias de um único provedor de transporte aparecerem no perfil.</span><span class="sxs-lookup"><span data-stu-id="c9451-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="c9451-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="c9451-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="c9451-155">Modificável.</span><span class="sxs-lookup"><span data-stu-id="c9451-155">Modifiable.</span></span> <span data-ttu-id="c9451-156">Esse armazenamento de mensagens é o armazenamento padrão do perfil.</span><span class="sxs-lookup"><span data-stu-id="c9451-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="c9451-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="c9451-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="c9451-158">Dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c9451-158">Dynamic.</span></span> <span data-ttu-id="c9451-159">As pastas padrão nesse armazenamento de mensagens, incluindo a pasta raiz da mensagem interpersonal (IPM), ainda não foram verificadas.</span><span class="sxs-lookup"><span data-stu-id="c9451-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="c9451-160">MAPI define e limpa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="c9451-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="c9451-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="c9451-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="c9451-162">Estático.</span><span class="sxs-lookup"><span data-stu-id="c9451-162">Static.</span></span> <span data-ttu-id="c9451-163">Esse armazenamento de mensagens não consegue se tornar o armazenamento de mensagens padrão para o perfil.</span><span class="sxs-lookup"><span data-stu-id="c9451-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="c9451-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="c9451-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="c9451-165">Estático.</span><span class="sxs-lookup"><span data-stu-id="c9451-165">Static.</span></span> <span data-ttu-id="c9451-166">Esse provedor não fornece uma identidade em sua linha de status.</span><span class="sxs-lookup"><span data-stu-id="c9451-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="c9451-167">Esse sinalizador ou STATUS_PRIMARY_IDENTITY deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="c9451-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="c9451-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="c9451-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="c9451-169">Estático.</span><span class="sxs-lookup"><span data-stu-id="c9451-169">Static.</span></span> <span data-ttu-id="c9451-170">Esse provedor de transporte está fortemente unido a um repositório de mensagens e fornece a PR_OWN_STORE_ENTRYID **(** [PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) em sua linha de status.</span><span class="sxs-lookup"><span data-stu-id="c9451-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="c9451-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="c9451-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="c9451-172">Modificável.</span><span class="sxs-lookup"><span data-stu-id="c9451-172">Modifiable.</span></span> <span data-ttu-id="c9451-173">Esse provedor fornece a identidade principal da sessão; o identificador de entrada do objeto que fornece a identidade é retornado de [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="c9451-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="c9451-174">Esse sinalizador ou **STATUS_NO_PRIMARY_IDENTITY** deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="c9451-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="c9451-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="c9451-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="c9451-176">Modificável.</span><span class="sxs-lookup"><span data-stu-id="c9451-176">Modifiable.</span></span> <span data-ttu-id="c9451-177">Esse armazenamento de mensagens deve ser usado quando um aplicativo cliente faz o login.</span><span class="sxs-lookup"><span data-stu-id="c9451-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="c9451-178">Depois de aberto, esse armazenamento deve ser definido como o armazenamento padrão para o perfil.</span><span class="sxs-lookup"><span data-stu-id="c9451-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="c9451-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="c9451-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="c9451-180">Modificável.</span><span class="sxs-lookup"><span data-stu-id="c9451-180">Modifiable.</span></span> <span data-ttu-id="c9451-181">Esse armazenamento de mensagens deve ser usado se o armazenamento principal não estiver disponível quando um aplicativo cliente faz o login.</span><span class="sxs-lookup"><span data-stu-id="c9451-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="c9451-182">Depois de aberto, esse armazenamento deve ser definido como o armazenamento padrão para o perfil.</span><span class="sxs-lookup"><span data-stu-id="c9451-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="c9451-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="c9451-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="c9451-184">Dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c9451-184">Dynamic.</span></span> <span data-ttu-id="c9451-185">Esse armazenamento de mensagens será usado pelo Simple MAPI como seu armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="c9451-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="c9451-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="c9451-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="c9451-187">Dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c9451-187">Dynamic.</span></span> <span data-ttu-id="c9451-188">Esse armazenamento de mensagens não deve ser publicado na tabela do armazenamento de mensagens e será excluído do perfil após o logoff.</span><span class="sxs-lookup"><span data-stu-id="c9451-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="c9451-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="c9451-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="c9451-190">Estático.</span><span class="sxs-lookup"><span data-stu-id="c9451-190">Static.</span></span> <span data-ttu-id="c9451-191">Esse transporte espera ser o último transporte selecionado para enviar uma mensagem quando vários provedores de transporte são capazes de transmitir a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c9451-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="c9451-192">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9451-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c9451-193">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="c9451-193">Header files</span></span>

<span data-ttu-id="c9451-194">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9451-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9451-195">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c9451-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9451-196">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9451-196">Mapitags.h</span></span>
  
> <span data-ttu-id="c9451-197">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c9451-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9451-198">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9451-198">See also</span></span>



[<span data-ttu-id="c9451-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="c9451-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="c9451-200">Propriedade canônica PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="c9451-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="c9451-201">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c9451-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9451-202">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c9451-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9451-203">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c9451-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9451-204">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c9451-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

