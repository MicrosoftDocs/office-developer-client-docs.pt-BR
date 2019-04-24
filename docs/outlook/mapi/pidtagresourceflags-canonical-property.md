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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330181"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="25f9f-103">Propriedade canônica PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="25f9f-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="25f9f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25f9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25f9f-105">Contém uma bitmask de sinalizadores para serviços de mensagens e provedores.</span><span class="sxs-lookup"><span data-stu-id="25f9f-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25f9f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="25f9f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25f9f-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="25f9f-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="25f9f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="25f9f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25f9f-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="25f9f-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="25f9f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="25f9f-110">Data type:</span></span>  <br/> |<span data-ttu-id="25f9f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="25f9f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="25f9f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="25f9f-112">Area:</span></span>  <br/> |<span data-ttu-id="25f9f-113">MAPI comum</span><span class="sxs-lookup"><span data-stu-id="25f9f-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25f9f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="25f9f-114">Remarks</span></span>

<span data-ttu-id="25f9f-115">Esta propriedade descreve as características de um serviço de mensagens, um provedor de serviços ou um objeto status.</span><span class="sxs-lookup"><span data-stu-id="25f9f-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="25f9f-116">Os sinalizadores definidos para esta propriedade dependem do seu contexto.</span><span class="sxs-lookup"><span data-stu-id="25f9f-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="25f9f-117">Por exemplo, alguns sinalizadores são válidos somente para objetos status e outros sinalizadores somente para colunas na tabela de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="25f9f-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="25f9f-118">Os sinalizadores são de três classes: estática, modificável e dinâmica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="25f9f-119">Os sinalizadores estáticos são definidos por MAPI de dados em MAPISVC. INF e nunca alterado.</span><span class="sxs-lookup"><span data-stu-id="25f9f-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="25f9f-120">Os sinalizadores modificáveis são definidos por MAPI de MAPISVC. INF, mas pode ser alterado subsequentemente.</span><span class="sxs-lookup"><span data-stu-id="25f9f-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="25f9f-121">Sinalizadores dinâmicos podem ser definidos e redefinidos por métodos MAPI.</span><span class="sxs-lookup"><span data-stu-id="25f9f-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="25f9f-122">Para um serviço de mensagens, um ou mais dos seguintes sinalizadores podem ser definidos nesta propriedade:</span><span class="sxs-lookup"><span data-stu-id="25f9f-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="25f9f-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="25f9f-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="25f9f-124">Reservado.</span><span class="sxs-lookup"><span data-stu-id="25f9f-124">Reserved.</span></span> <span data-ttu-id="25f9f-125">Não usar.</span><span class="sxs-lookup"><span data-stu-id="25f9f-125">Do not use.</span></span>
    
<span data-ttu-id="25f9f-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="25f9f-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="25f9f-127">Dinâmica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-127">Dynamic.</span></span> <span data-ttu-id="25f9f-128">O serviço de mensagens contém o repositório padrão.</span><span class="sxs-lookup"><span data-stu-id="25f9f-128">The message service contains the default store.</span></span> <span data-ttu-id="25f9f-129">Uma interface do usuário deve ser exibida solicitando a confirmação do usuário antes de excluir ou mover esse serviço do perfil.</span><span class="sxs-lookup"><span data-stu-id="25f9f-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="25f9f-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="25f9f-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="25f9f-131">Estatistica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-131">Static.</span></span> <span data-ttu-id="25f9f-132">O sinalizador de nível de serviço que deve ser definido para indicar que nenhum dos provedores no serviço de mensagens pode ser usado para fornecer uma identidade.</span><span class="sxs-lookup"><span data-stu-id="25f9f-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="25f9f-133">Este sinalizador ou SERVICE_PRIMARY_IDENTITY deve ser definido, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="25f9f-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="25f9f-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="25f9f-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="25f9f-135">Modificável.</span><span class="sxs-lookup"><span data-stu-id="25f9f-135">Modifiable.</span></span> <span data-ttu-id="25f9f-136">O serviço de mensagens correspondente contém o provedor usado para a identidade principal desta sessão.</span><span class="sxs-lookup"><span data-stu-id="25f9f-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="25f9f-137">Use [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="25f9f-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="25f9f-138">Este sinalizador ou SERVICE_NO_PRIMARY_IDENTITY deve ser definido, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="25f9f-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="25f9f-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="25f9f-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="25f9f-140">Estatistica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-140">Static.</span></span> <span data-ttu-id="25f9f-141">Qualquer tentativa de criar ou copiar esse serviço de mensagens em um perfil onde o serviço já existe falhará.</span><span class="sxs-lookup"><span data-stu-id="25f9f-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="25f9f-142">Para criar um serviço de mensagem de cópia única, adicione a propriedade **PR_RESOURCE_FLAGS** à seção do serviço em MAPISVC. INF e defina esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="25f9f-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="25f9f-143">Para um provedor de serviços, um ou mais dos seguintes sinalizadores podem ser definidos no **PR_RESOURCE_FLAGS**:</span><span class="sxs-lookup"><span data-stu-id="25f9f-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="25f9f-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="25f9f-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="25f9f-145">Estatistica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-145">Static.</span></span> <span data-ttu-id="25f9f-146">O gancho do spooler precisa processar mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="25f9f-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="25f9f-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="25f9f-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="25f9f-148">Estatistica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-148">Static.</span></span> <span data-ttu-id="25f9f-149">O gancho do spooler precisa processar mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="25f9f-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="25f9f-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="25f9f-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="25f9f-151">Modificável.</span><span class="sxs-lookup"><span data-stu-id="25f9f-151">Modifiable.</span></span> <span data-ttu-id="25f9f-152">Essa identidade deve ser aplicada a mensagens de saída se o perfil contiver várias instâncias desse provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="25f9f-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="25f9f-153">Isso pode acontecer se várias instâncias de um único provedor de transporte aparecerem no perfil.</span><span class="sxs-lookup"><span data-stu-id="25f9f-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="25f9f-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="25f9f-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="25f9f-155">Modificável.</span><span class="sxs-lookup"><span data-stu-id="25f9f-155">Modifiable.</span></span> <span data-ttu-id="25f9f-156">Este repositório de mensagens é o repositório padrão para o perfil.</span><span class="sxs-lookup"><span data-stu-id="25f9f-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="25f9f-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="25f9f-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="25f9f-158">Dinâmica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-158">Dynamic.</span></span> <span data-ttu-id="25f9f-159">As pastas padrão neste repositório de mensagens, incluindo a pasta raiz da mensagem interpessoal (IPM), ainda não foram verificadas.</span><span class="sxs-lookup"><span data-stu-id="25f9f-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="25f9f-160">MAPI define e limpa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="25f9f-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="25f9f-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="25f9f-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="25f9f-162">Estatistica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-162">Static.</span></span> <span data-ttu-id="25f9f-163">Este repositório de mensagens é incapaz de se tornar o repositório de mensagens padrão para o perfil.</span><span class="sxs-lookup"><span data-stu-id="25f9f-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="25f9f-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="25f9f-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="25f9f-165">Estatistica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-165">Static.</span></span> <span data-ttu-id="25f9f-166">Esse provedor não fornece uma identidade na linha de status.</span><span class="sxs-lookup"><span data-stu-id="25f9f-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="25f9f-167">Este sinalizador ou STATUS_PRIMARY_IDENTITY deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="25f9f-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="25f9f-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="25f9f-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="25f9f-169">Estatistica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-169">Static.</span></span> <span data-ttu-id="25f9f-170">Esse provedor de transporte está rigidamente acoplado a um repositório de mensagens e fornece a propriedade **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) em sua linha de status.</span><span class="sxs-lookup"><span data-stu-id="25f9f-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="25f9f-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="25f9f-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="25f9f-172">Modificável.</span><span class="sxs-lookup"><span data-stu-id="25f9f-172">Modifiable.</span></span> <span data-ttu-id="25f9f-173">Este provedor fornece a identidade principal para a sessão; o identificador de entrada para o objeto que fornece a identidade é retornado de [IMAPISession:: QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="25f9f-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="25f9f-174">Este sinalizador ou **STATUS_NO_PRIMARY_IDENTITY** deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="25f9f-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="25f9f-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="25f9f-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="25f9f-176">Modificável.</span><span class="sxs-lookup"><span data-stu-id="25f9f-176">Modifiable.</span></span> <span data-ttu-id="25f9f-177">Este repositório de mensagens deve ser usado quando um aplicativo cliente faz logon.</span><span class="sxs-lookup"><span data-stu-id="25f9f-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="25f9f-178">Depois de aberto, esse repositório deverá ser definido como o repositório padrão para o perfil.</span><span class="sxs-lookup"><span data-stu-id="25f9f-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="25f9f-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="25f9f-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="25f9f-180">Modificável.</span><span class="sxs-lookup"><span data-stu-id="25f9f-180">Modifiable.</span></span> <span data-ttu-id="25f9f-181">Este repositório de mensagens será usado se o armazenamento principal não estiver disponível quando um aplicativo cliente fizer logon.</span><span class="sxs-lookup"><span data-stu-id="25f9f-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="25f9f-182">Depois de aberto, esse repositório deverá ser definido como o repositório padrão para o perfil.</span><span class="sxs-lookup"><span data-stu-id="25f9f-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="25f9f-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="25f9f-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="25f9f-184">Dinâmica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-184">Dynamic.</span></span> <span data-ttu-id="25f9f-185">Este repositório de mensagens será usado pelo Simple MAPI como o seu repositório de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="25f9f-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="25f9f-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="25f9f-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="25f9f-187">Dinâmica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-187">Dynamic.</span></span> <span data-ttu-id="25f9f-188">Este repositório de mensagens não deve ser publicado na tabela de repositório de mensagens e será excluído do perfil após o logoff.</span><span class="sxs-lookup"><span data-stu-id="25f9f-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="25f9f-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="25f9f-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="25f9f-190">Estatistica.</span><span class="sxs-lookup"><span data-stu-id="25f9f-190">Static.</span></span> <span data-ttu-id="25f9f-191">Esse transporte espera ser o último transporte selecionado para enviar uma mensagem quando vários provedores de transporte podem transmitir a mensagem.</span><span class="sxs-lookup"><span data-stu-id="25f9f-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="25f9f-192">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="25f9f-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="25f9f-193">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="25f9f-193">Header files</span></span>

<span data-ttu-id="25f9f-194">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="25f9f-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="25f9f-195">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="25f9f-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="25f9f-196">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="25f9f-196">Mapitags.h</span></span>
  
> <span data-ttu-id="25f9f-197">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="25f9f-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25f9f-198">Confira também</span><span class="sxs-lookup"><span data-stu-id="25f9f-198">See also</span></span>



[<span data-ttu-id="25f9f-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="25f9f-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="25f9f-200">Propriedade canônica PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="25f9f-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="25f9f-201">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="25f9f-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25f9f-202">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="25f9f-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25f9f-203">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="25f9f-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25f9f-204">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="25f9f-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

