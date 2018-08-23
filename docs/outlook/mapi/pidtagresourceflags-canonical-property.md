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
ms.openlocfilehash: 875b37183134a6c5beca76ab7910cf601d1b6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567500"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="c1c34-103">Propriedade canônica PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="c1c34-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="c1c34-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1c34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1c34-105">Contém uma bitmask dos sinalizadores para serviços de mensagem e provedores.</span><span class="sxs-lookup"><span data-stu-id="c1c34-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1c34-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c1c34-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1c34-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c1c34-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="c1c34-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c1c34-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c1c34-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="c1c34-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="c1c34-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c1c34-110">Data type:</span></span>  <br/> |<span data-ttu-id="c1c34-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c1c34-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c1c34-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c1c34-112">Area:</span></span>  <br/> |<span data-ttu-id="c1c34-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="c1c34-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1c34-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1c34-114">Remarks</span></span>

<span data-ttu-id="c1c34-115">Essa propriedade descreve as características de um serviço de mensagem, um provedor de serviço ou um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="c1c34-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="c1c34-116">Os sinalizadores que estão definidos para esta propriedade dependem de seu contexto.</span><span class="sxs-lookup"><span data-stu-id="c1c34-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="c1c34-117">Por exemplo, alguns sinalizadores são válidos somente para objetos de status e outros sinalizadores apenas para colunas na tabela de serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c1c34-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="c1c34-118">Os sinalizadores são das três classes: modificável, estática e dinâmica.</span><span class="sxs-lookup"><span data-stu-id="c1c34-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="c1c34-119">Sinalizadores estáticos são definidos por MAPI de dados no MAPISVC. INF e nunca alteradas.</span><span class="sxs-lookup"><span data-stu-id="c1c34-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="c1c34-120">Sinalizadores modificáveis são definidos por MAPI do MAPISVC. INF, mas pode ser alterada posteriormente.</span><span class="sxs-lookup"><span data-stu-id="c1c34-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="c1c34-121">Sinalizadores dinâmicos podem ser definidas e redefinir pelos métodos MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1c34-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="c1c34-122">Para um serviço de mensagem, um ou mais dos seguintes sinalizadores podem ser definido nessa propriedade:</span><span class="sxs-lookup"><span data-stu-id="c1c34-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="c1c34-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="c1c34-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="c1c34-124">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c1c34-124">Reserved.</span></span> <span data-ttu-id="c1c34-125">Não a use.</span><span class="sxs-lookup"><span data-stu-id="c1c34-125">Do not use.</span></span>
    
<span data-ttu-id="c1c34-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="c1c34-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="c1c34-127">Dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c1c34-127">Dynamic.</span></span> <span data-ttu-id="c1c34-128">O serviço de mensagem contém o repositório padrão.</span><span class="sxs-lookup"><span data-stu-id="c1c34-128">The message service contains the default store.</span></span> <span data-ttu-id="c1c34-129">Uma interface do usuário deve ser exibida, solicitar a confirmação antes de excluir ou mover este serviço de perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="c1c34-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="c1c34-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="c1c34-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="c1c34-131">Estático.</span><span class="sxs-lookup"><span data-stu-id="c1c34-131">Static.</span></span> <span data-ttu-id="c1c34-132">O sinalizador nível de serviço que deve ser definido para indicar que nenhum dos provedores no serviço de mensagem pode ser usada para fornecer uma identidade.</span><span class="sxs-lookup"><span data-stu-id="c1c34-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="c1c34-133">Este sinalizador ou SERVICE_PRIMARY_IDENTITY deve ser definido, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="c1c34-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="c1c34-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="c1c34-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="c1c34-135">Pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="c1c34-135">Modifiable.</span></span> <span data-ttu-id="c1c34-136">O serviço correspondente da mensagem contém o provedor usado para a identidade principal nesta sessão.</span><span class="sxs-lookup"><span data-stu-id="c1c34-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="c1c34-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="c1c34-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="c1c34-138">Este sinalizador ou SERVICE_NO_PRIMARY_IDENTITY deve ser definido, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="c1c34-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="c1c34-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="c1c34-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="c1c34-140">Estático.</span><span class="sxs-lookup"><span data-stu-id="c1c34-140">Static.</span></span> <span data-ttu-id="c1c34-141">Qualquer tentativa de criar ou copiar esse serviço de mensagem para um perfil de onde o serviço já existe falhará.</span><span class="sxs-lookup"><span data-stu-id="c1c34-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="c1c34-142">Para criar uma única cópia o serviço de mensagem adicionar a propriedade **PR_RESOURCE_FLAGS** à seção do serviço em MAPISVC. INF e definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="c1c34-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="c1c34-143">Para um provedor de serviço, um ou mais dos seguintes sinalizadores podem ser definido em **PR_RESOURCE_FLAGS**:</span><span class="sxs-lookup"><span data-stu-id="c1c34-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="c1c34-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="c1c34-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="c1c34-145">Estático.</span><span class="sxs-lookup"><span data-stu-id="c1c34-145">Static.</span></span> <span data-ttu-id="c1c34-146">O gancho spooler deve processar mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="c1c34-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="c1c34-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="c1c34-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="c1c34-148">Estático.</span><span class="sxs-lookup"><span data-stu-id="c1c34-148">Static.</span></span> <span data-ttu-id="c1c34-149">O gancho spooler deve processar mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="c1c34-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="c1c34-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="c1c34-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="c1c34-151">Pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="c1c34-151">Modifiable.</span></span> <span data-ttu-id="c1c34-152">Essa identidade deve ser aplicada às mensagens de saída, se o perfil contiver várias instâncias desse provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c1c34-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="c1c34-153">Isso pode acontecer se várias instâncias de um provedor de transporte único aparecem no perfil.</span><span class="sxs-lookup"><span data-stu-id="c1c34-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="c1c34-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="c1c34-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="c1c34-155">Pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="c1c34-155">Modifiable.</span></span> <span data-ttu-id="c1c34-156">Este armazenamento de mensagem é o padrão para o perfil.</span><span class="sxs-lookup"><span data-stu-id="c1c34-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="c1c34-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="c1c34-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="c1c34-158">Dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c1c34-158">Dynamic.</span></span> <span data-ttu-id="c1c34-159">As pastas padrão no armazenamento de mensagens, incluindo a pasta raiz de mensagem interpessoais (IPM), ainda não foi verificadas.</span><span class="sxs-lookup"><span data-stu-id="c1c34-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="c1c34-160">Define e limpa esse sinalizador MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1c34-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="c1c34-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="c1c34-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="c1c34-162">Estático.</span><span class="sxs-lookup"><span data-stu-id="c1c34-162">Static.</span></span> <span data-ttu-id="c1c34-163">Este armazenamento de mensagens não é capaz de se tornando o armazenamento de mensagens para o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="c1c34-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="c1c34-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="c1c34-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="c1c34-165">Estático.</span><span class="sxs-lookup"><span data-stu-id="c1c34-165">Static.</span></span> <span data-ttu-id="c1c34-166">Esse provedor não forneça uma identidade em sua linha de status.</span><span class="sxs-lookup"><span data-stu-id="c1c34-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="c1c34-167">Este sinalizador ou STATUS_PRIMARY_IDENTITY deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="c1c34-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="c1c34-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="c1c34-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="c1c34-169">Estático.</span><span class="sxs-lookup"><span data-stu-id="c1c34-169">Static.</span></span> <span data-ttu-id="c1c34-170">Esse provedor de transporte está firmemente combinado com um armazenamento de mensagens e fornece a propriedade **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) em sua linha de status.</span><span class="sxs-lookup"><span data-stu-id="c1c34-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="c1c34-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="c1c34-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="c1c34-172">Pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="c1c34-172">Modifiable.</span></span> <span data-ttu-id="c1c34-173">Esse provedor representa a identidade principal para a sessão; o identificador de entrada para o objeto que forneçam a identidade é retornado por [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="c1c34-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="c1c34-174">Este sinalizador ou **STATUS_NO_PRIMARY_IDENTITY** deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="c1c34-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="c1c34-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="c1c34-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="c1c34-176">Pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="c1c34-176">Modifiable.</span></span> <span data-ttu-id="c1c34-177">Este armazenamento de mensagens deve ser usado quando um aplicativo cliente fizer logon.</span><span class="sxs-lookup"><span data-stu-id="c1c34-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="c1c34-178">Uma vez aberto, esse repositório deve ser definido como o repositório padrão para o perfil.</span><span class="sxs-lookup"><span data-stu-id="c1c34-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="c1c34-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="c1c34-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="c1c34-180">Pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="c1c34-180">Modifiable.</span></span> <span data-ttu-id="c1c34-181">Este armazenamento de mensagens deve ser usado se o repositório principal não está disponível quando um aplicativo cliente fizer logon.</span><span class="sxs-lookup"><span data-stu-id="c1c34-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="c1c34-182">Uma vez aberto, esse repositório deve ser definido como o repositório padrão para o perfil.</span><span class="sxs-lookup"><span data-stu-id="c1c34-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="c1c34-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="c1c34-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="c1c34-184">Dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c1c34-184">Dynamic.</span></span> <span data-ttu-id="c1c34-185">Este armazenamento de mensagens será usado pelo MAPI simples como seu armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="c1c34-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="c1c34-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="c1c34-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="c1c34-187">Dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c1c34-187">Dynamic.</span></span> <span data-ttu-id="c1c34-188">Este armazenamento de mensagens não deve ser publicado na tabela de repositório de mensagens e será excluído do perfil após o logoff.</span><span class="sxs-lookup"><span data-stu-id="c1c34-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="c1c34-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="c1c34-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="c1c34-190">Estático.</span><span class="sxs-lookup"><span data-stu-id="c1c34-190">Static.</span></span> <span data-ttu-id="c1c34-191">Espera-se que seja o último transporte selecionado para enviar uma mensagem quando vários provedores de transporte são capazes de transmitir a mensagem deste transporte.</span><span class="sxs-lookup"><span data-stu-id="c1c34-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="c1c34-192">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1c34-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c1c34-193">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c1c34-193">Header files</span></span>

<span data-ttu-id="c1c34-194">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1c34-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1c34-195">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c1c34-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="c1c34-196">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c1c34-196">Mapitags.h</span></span>
  
> <span data-ttu-id="c1c34-197">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c1c34-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1c34-198">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1c34-198">See also</span></span>



[<span data-ttu-id="c1c34-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="c1c34-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="c1c34-200">Propriedade canônica PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="c1c34-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="c1c34-201">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c1c34-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1c34-202">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c1c34-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1c34-203">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c1c34-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1c34-204">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c1c34-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

