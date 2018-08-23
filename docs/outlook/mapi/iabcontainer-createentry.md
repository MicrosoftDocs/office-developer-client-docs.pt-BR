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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2f8a6baa9a910b91e633084f1d9cd8ac52b24d5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575599"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="84682-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="84682-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="84682-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84682-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84682-105">Cria uma nova entrada, que pode ser um usuário de mensagens, uma lista de distribuição ou outro contêiner.</span><span class="sxs-lookup"><span data-stu-id="84682-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="84682-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84682-106">Parameters</span></span>

 <span data-ttu-id="84682-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="84682-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="84682-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="84682-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="84682-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="84682-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="84682-110">[in] Um ponteiro para o identificador de entrada de um modelo para a criação de novas entradas de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="84682-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="84682-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="84682-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="84682-112">[in] Uma bitmask dos sinalizadores que controla como a criação de entrada é executada.</span><span class="sxs-lookup"><span data-stu-id="84682-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="84682-113">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="84682-113">The following flags can be set:</span></span>
    
<span data-ttu-id="84682-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="84682-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="84682-115">Um nível afastado de verificação de entrada duplicada deve ser realizado.</span><span class="sxs-lookup"><span data-stu-id="84682-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="84682-116">A implementação de verificação de entrada duplicada afastada é específico do provedor.</span><span class="sxs-lookup"><span data-stu-id="84682-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="84682-117">Por exemplo, um provedor pode definir uma correspondência afastada conforme qualquer duas entradas que têm o mesmo nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="84682-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="84682-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="84682-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="84682-119">Um nível estrito de verificação de entrada duplicada deve ser realizado.</span><span class="sxs-lookup"><span data-stu-id="84682-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="84682-120">A implementação de verificação de entrada duplicada strict é específico do provedor.</span><span class="sxs-lookup"><span data-stu-id="84682-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="84682-121">Por exemplo, um provedor pode definir uma correspondência estrita como qualquer duas entradas que têm ambas o mesmo nome e endereço de mensagens são exibidos.</span><span class="sxs-lookup"><span data-stu-id="84682-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="84682-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="84682-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="84682-123">Uma nova entrada deve substituir um já existente, se for determinado que as duas versões sejam duplicatas.</span><span class="sxs-lookup"><span data-stu-id="84682-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="84682-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="84682-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="84682-125">[out] Um ponteiro para um ponteiro para a entrada recém-criado.</span><span class="sxs-lookup"><span data-stu-id="84682-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84682-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="84682-126">Return value</span></span>

<span data-ttu-id="84682-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="84682-127">S_OK</span></span> 
  
> <span data-ttu-id="84682-128">A nova entrada foi criada com êxito.</span><span class="sxs-lookup"><span data-stu-id="84682-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84682-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="84682-129">Remarks</span></span>

<span data-ttu-id="84682-130">O método **IABContainer::CreateEntry** cria uma nova entrada de um determinado tipo no contêiner especificado, retornando um ponteiro para uma implementação de interface para acesso à entrada.</span><span class="sxs-lookup"><span data-stu-id="84682-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="84682-131">A nova entrada é criada usando um modelo que foi selecionado na lista do contêiner dos modelos disponíveis publicado em sua tabela único.</span><span class="sxs-lookup"><span data-stu-id="84682-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="84682-132">Os chamadores acessar a tabela de únicos de um contêiner chamando seu método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e solicitar a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="84682-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="84682-133">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="84682-133">Notes to implementers</span></span>

<span data-ttu-id="84682-134">Todos os contêineres que suportam o método **IABContainer::CreateEntry** devem ser pode ser modificados.</span><span class="sxs-lookup"><span data-stu-id="84682-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="84682-135">Defina sinalizador AB_MODIFIABLE do seu contêiner na sua propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que ela é modificável.</span><span class="sxs-lookup"><span data-stu-id="84682-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="84682-136">Você deve oferecer suporte a todos os sinalizadores _ulCreateFlags_ .</span><span class="sxs-lookup"><span data-stu-id="84682-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="84682-137">No entanto, a interpretação e usar esses sinalizadores é específico da implementação — ou seja, você pode determinar o significado a semântica de CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT no contexto da sua implementação.</span><span class="sxs-lookup"><span data-stu-id="84682-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="84682-138">Se você não pode ou não determinam se uma entrada é uma duplicata, sempre permita a entrada a ser criado.</span><span class="sxs-lookup"><span data-stu-id="84682-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="84682-139">Alguns provedores de implementam estrita entrada verificação combinando o nome para exibição, mensagens de endereço e a chave de pesquisa em uma entrada; outros provedores de limitam a correspondência para exibir o nome e endereço.</span><span class="sxs-lookup"><span data-stu-id="84682-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="84682-140">Verificação de entrada afastada geralmente é implementado, verificando o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="84682-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="84682-141">Observações para implementadores de provedor de catálogo de endereço de Host</span><span class="sxs-lookup"><span data-stu-id="84682-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="84682-142">Se seu contêiner pode criar entradas de modelos de outros provedores, a implementação dos **CreateEntry** deverão fornecer armazenamento para algumas ou todas as propriedades associadas às entradas criadas.</span><span class="sxs-lookup"><span data-stu-id="84682-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="84682-143">Por exemplo, se você fornecer armazenamento para a propriedade de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de uma entrada, você poderá gerar sua caixa de diálogo detalhes sem ter que dependem do provedor estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="84682-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="84682-144">Se seu contêiner pode criar entradas que oferecem suporte à propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), a implementação dos **CreateEntry** deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="84682-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="84682-145">Chame o método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) .</span><span class="sxs-lookup"><span data-stu-id="84682-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="84682-146">**OpenTemplateID** permite que o código do provedor estrangeira para a entrada vincular para a nova entrada que está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="84682-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="84682-147">Provedores estrangeira oferecem suporte a esse processo de vinculação para manter o controle sobre entradas criados a partir de seus modelos nos contêineres de provedores de catálogo de endereço de host.</span><span class="sxs-lookup"><span data-stu-id="84682-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="84682-148">Realizar qualquer inicialização necessária e popular o novo objeto com todas as propriedades da entrada no provedor estrangeira que o objeto retornado no parâmetro _lppMAPIPropNew_ do **OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="84682-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="84682-149">Se **OpenTemplateID** tiver êxito, copie as propriedades para a implementação apontado pelo parâmetro _lppMAPIPropNew_ e não diretamente para a implementação apontado pelo parâmetro _lpMAPIPropData_ .</span><span class="sxs-lookup"><span data-stu-id="84682-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="84682-150">Inicialize a nova entrada para uso offline, como faria com qualquer outra entrada de um provedor estrangeira.</span><span class="sxs-lookup"><span data-stu-id="84682-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="84682-151">Se **OpenTemplateID** retornará um erro, **CreateEntry** deve falhar.</span><span class="sxs-lookup"><span data-stu-id="84682-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="84682-152">Não permita a entrada a ser criado.</span><span class="sxs-lookup"><span data-stu-id="84682-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="84682-153">Como o provedor estrangeiro pode fazer suposições sobre os dados em seu provedor, não crie uma entrada com um identificador de modelo que não tenha sido associado com êxito ao provedor estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="84682-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="84682-154">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="84682-154">Notes to callers</span></span>

<span data-ttu-id="84682-155">Quando **CreateEntry** retorna, você pode ou não ser capaz de acessar imediatamente o identificador de entrada para a nova entrada.</span><span class="sxs-lookup"><span data-stu-id="84682-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="84682-156">Alguns provedores de catálogo de endereços não disponibilizá-lo até depois de ter chamado o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da nova entrada.</span><span class="sxs-lookup"><span data-stu-id="84682-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="84682-157">Embora os sinalizadores de verificação duplicados são passados como parâmetros para **CreateEntry**, a operação de verificação de duplicata não ocorrerá até **SaveChanges** é chamado.</span><span class="sxs-lookup"><span data-stu-id="84682-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="84682-158">Portanto, os erros relacionados, como MAPI_E_COLLISION, que indica que foi feita uma tentativa para criar uma entrada já existente, são retornados pelo **SaveChanges** ao invés **CreateEntry**.</span><span class="sxs-lookup"><span data-stu-id="84682-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="84682-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="84682-159">See also</span></span>



[<span data-ttu-id="84682-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="84682-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="84682-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="84682-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="84682-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="84682-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="84682-163">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="84682-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="84682-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="84682-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

