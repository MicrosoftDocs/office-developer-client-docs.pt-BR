---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9f80130279e3437dd9be947de97d3f0d4181165e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411271"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="37c38-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="37c38-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="37c38-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37c38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37c38-105">Cria uma nova entrada, que pode ser um usuário de mensagens, uma lista de distribuição ou outro contêiner.</span><span class="sxs-lookup"><span data-stu-id="37c38-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="37c38-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37c38-106">Parameters</span></span>

 <span data-ttu-id="37c38-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="37c38-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="37c38-108">no A contagem dos bytes no identificador de entrada apontados pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="37c38-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="37c38-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="37c38-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="37c38-110">no Um ponteiro para o identificador de entrada de um modelo para a criação de novas entradas de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="37c38-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="37c38-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="37c38-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="37c38-112">no Uma bitmask de sinalizadores que controla como a criação de entrada é realizada.</span><span class="sxs-lookup"><span data-stu-id="37c38-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="37c38-113">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="37c38-113">The following flags can be set:</span></span>
    
<span data-ttu-id="37c38-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="37c38-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="37c38-115">Um nível flexível de verificação de entrada duplicada deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="37c38-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="37c38-116">A implementação da verificação de entrada duplicada resolta é específica do provedor.</span><span class="sxs-lookup"><span data-stu-id="37c38-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="37c38-117">Por exemplo, um provedor pode definir uma correspondência frouxa como qualquer duas entradas com o mesmo nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="37c38-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="37c38-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="37c38-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="37c38-119">Um nível estrito de verificação de entrada duplicada deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="37c38-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="37c38-120">A implementação de verificação de entrada duplicada estrita é específica do provedor.</span><span class="sxs-lookup"><span data-stu-id="37c38-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="37c38-121">Por exemplo, um provedor pode definir uma correspondência estrita como qualquer duas entradas que tenham o mesmo nome de exibição e endereço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="37c38-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="37c38-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="37c38-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="37c38-123">Uma nova entrada deve substituir uma existente se for determinado que as duas são duplicatas.</span><span class="sxs-lookup"><span data-stu-id="37c38-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="37c38-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="37c38-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="37c38-125">bota Um ponteiro para um ponteiro para a entrada recém-criada.</span><span class="sxs-lookup"><span data-stu-id="37c38-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37c38-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="37c38-126">Return value</span></span>

<span data-ttu-id="37c38-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="37c38-127">S_OK</span></span> 
  
> <span data-ttu-id="37c38-128">A nova entrada foi criada com êxito.</span><span class="sxs-lookup"><span data-stu-id="37c38-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37c38-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="37c38-129">Remarks</span></span>

<span data-ttu-id="37c38-130">O método **IABContainer:: createentry** cria uma nova entrada de um tipo específico no contêiner especificado, retornando um ponteiro para uma implementação de interface para acesso adicional à entrada.</span><span class="sxs-lookup"><span data-stu-id="37c38-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="37c38-131">A nova entrada é criada usando um modelo que foi selecionado na lista de modelos disponíveis do contêiner publicada em sua tabela única.</span><span class="sxs-lookup"><span data-stu-id="37c38-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="37c38-132">Os chamadores acessam a tabela única de um contêiner chamando o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) e solicitando a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="37c38-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="37c38-133">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="37c38-133">Notes to implementers</span></span>

<span data-ttu-id="37c38-134">Todos os contêineres compatíveis com o método **IABContainer:: createentry** devem ser modificáveis.</span><span class="sxs-lookup"><span data-stu-id="37c38-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="37c38-135">Defina o sinalizador AB_MODIFIABLE de seu contêiner em sua propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que ele é modificável.</span><span class="sxs-lookup"><span data-stu-id="37c38-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="37c38-136">Você deve dar suporte a todos os sinalizadores _ulCreateFlags_ .</span><span class="sxs-lookup"><span data-stu-id="37c38-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="37c38-137">No enTanto, a interpretação e o uso desses sinalizadores são específicos de implementação, ou seja, você pode determinar quais são as semânticas de CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT no contexto da sua implementação.</span><span class="sxs-lookup"><span data-stu-id="37c38-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="37c38-138">Se você não puder ou não determinar se uma entrada é uma duplicata, sempre permita que a entrada seja criada.</span><span class="sxs-lookup"><span data-stu-id="37c38-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="37c38-139">Alguns provedores implementam a verificação de entrada estrita, combinando o nome para exibição, o endereço de mensagens e a chave de pesquisa em uma entrada; outros provedores limitam a correspondência para exibir o nome e o endereço.</span><span class="sxs-lookup"><span data-stu-id="37c38-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="37c38-140">A verificação de entrada flexível geralmente é implementada verificando apenas o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="37c38-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="37c38-141">Observações para implementadores do provedor de catálogo de endereços do host</span><span class="sxs-lookup"><span data-stu-id="37c38-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="37c38-142">Se o seu contêiner pode criar entradas dos modelos de outros provedores, sua implementação de **createentry** deve fornecer armazenamento para algumas ou todas as propriedades associadas às entradas criadas.</span><span class="sxs-lookup"><span data-stu-id="37c38-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="37c38-143">Por exemplo, se você fornecer armazenamento para a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de uma entrada, poderá gerar sua caixa de diálogo detalhes sem precisar depender do provedor estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="37c38-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="37c38-144">Se o seu contêiner pode criar entradas que suportam a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), sua implementação de createentry deve fazer o seguinte: \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="37c38-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="37c38-145">Chame o método [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) .</span><span class="sxs-lookup"><span data-stu-id="37c38-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="37c38-146">**OpenTemplateID** habilita o código do provedor estrangeiro para a entrada vincular à nova entrada que está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="37c38-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="37c38-147">Os provedores estrangeiros dão suporte a esse processo de associação para manter o controle sobre as entradas criadas de seus modelos nos contêineres de provedores de catálogo de endereços de host.</span><span class="sxs-lookup"><span data-stu-id="37c38-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="37c38-148">Execute qualquer inicialização necessária e preencha o novo objeto com todas as propriedades da entrada no provedor estrangeiro que o objeto retornou no parâmetro _lppMAPIPropNew_ de **OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="37c38-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="37c38-149">Se o **OpenTemplateID** tiver êxito, copie as propriedades para a implementação indicada pelo parâmetro _lppMAPIPropNew_ , em vez de diretamente na implementação indicada pelo parâmetro _lpMAPIPropData_ .</span><span class="sxs-lookup"><span data-stu-id="37c38-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="37c38-150">Inicialize a nova entrada para uso offline como faria com qualquer outra entrada de um provedor estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="37c38-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="37c38-151">Se **OpenTemplateID** retornar um erro, **createentry** deverá falhar.</span><span class="sxs-lookup"><span data-stu-id="37c38-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="37c38-152">Não permite que a entrada seja criada.</span><span class="sxs-lookup"><span data-stu-id="37c38-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="37c38-153">Como o provedor estrangeiro pode fazer suposições sobre os dados no seu provedor, não crie uma entrada com um identificador de modelo que não tenha sido vinculado com êxito ao provedor estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="37c38-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="37c38-154">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="37c38-154">Notes to callers</span></span>

<span data-ttu-id="37c38-155">Quando **createentry** retornar, você poderá ou não conseguir acessar imediatamente o identificador de entrada para a nova entrada.</span><span class="sxs-lookup"><span data-stu-id="37c38-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="37c38-156">Alguns provedores do catálogo de endereços não o disponibilizam até depois de chamar o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da nova entrada.</span><span class="sxs-lookup"><span data-stu-id="37c38-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="37c38-157">Embora os sinalizadores de verificação duplicados sejam passados \*\*\*\* como parâmetros para createentry, a operação de verificação de duplicatas não ocorre até que **SaveChanges** seja chamado.</span><span class="sxs-lookup"><span data-stu-id="37c38-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="37c38-158">Portanto, erros relacionados como MAPI_E_COLLISION, que indicam que uma tentativa foi feita para criar uma entrada já existente, são retornados por **SaveChanges** , e não \*\*\*\* por createentry.</span><span class="sxs-lookup"><span data-stu-id="37c38-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37c38-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="37c38-159">See also</span></span>



[<span data-ttu-id="37c38-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="37c38-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="37c38-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="37c38-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="37c38-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="37c38-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="37c38-163">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="37c38-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="37c38-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="37c38-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

