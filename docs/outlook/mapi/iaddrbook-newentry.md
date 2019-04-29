---
title: IAddrBookNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405097"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="78ea5-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="78ea5-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="78ea5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78ea5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78ea5-105">Adiciona um novo destinatário a um contêiner de catálogo de endereços ou à lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="78ea5-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a><span data-ttu-id="78ea5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78ea5-106">Parameters</span></span>

 <span data-ttu-id="78ea5-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="78ea5-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="78ea5-108">no Uma alça para a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="78ea5-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="78ea5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78ea5-109">_ulFlags_</span></span>
  
> <span data-ttu-id="78ea5-110">no Uma bitmask de sinalizadores que controla o tipo de texto que é usado.</span><span class="sxs-lookup"><span data-stu-id="78ea5-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="78ea5-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="78ea5-111">The following flag can be set:</span></span>
    
<span data-ttu-id="78ea5-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="78ea5-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="78ea5-113">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="78ea5-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="78ea5-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="78ea5-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="78ea5-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="78ea5-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="78ea5-116">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEIDContainer_ .</span><span class="sxs-lookup"><span data-stu-id="78ea5-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="78ea5-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="78ea5-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="78ea5-118">no Um ponteiro para o identificador de entrada do contêiner onde o novo destinatário deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="78ea5-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="78ea5-119">Se o parâmetro _cbEIDContainer_ for zero, o método **NewEntry** retornará um identificador de entrada de destinatário e uma lista de modelos como se o método [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) fosse chamado.</span><span class="sxs-lookup"><span data-stu-id="78ea5-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="78ea5-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="78ea5-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="78ea5-121">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEIDNewEntryTpl_ .</span><span class="sxs-lookup"><span data-stu-id="78ea5-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="78ea5-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="78ea5-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="78ea5-123">no Um ponteiro para um modelo one-off que será usado para criar o novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="78ea5-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="78ea5-124">Se _cbEIDNewEntryTpl_ for zero e _lpEIDNewEntryTpl_ for nulo, **NewEntry** exibirá uma caixa de diálogo com a qual o usuário pode selecionar a partir de uma lista de modelos para adicionar novas entradas.</span><span class="sxs-lookup"><span data-stu-id="78ea5-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="78ea5-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="78ea5-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="78ea5-126">bota Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEIDNewEntry_ .</span><span class="sxs-lookup"><span data-stu-id="78ea5-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="78ea5-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="78ea5-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="78ea5-128">bota Um ponteiro para um ponteiro para o novo identificador de entrada do destinatário.</span><span class="sxs-lookup"><span data-stu-id="78ea5-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78ea5-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="78ea5-129">Return value</span></span>

<span data-ttu-id="78ea5-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="78ea5-130">S_OK</span></span> 
  
> <span data-ttu-id="78ea5-131">A nova entrada do catálogo de endereços foi criada com êxito.</span><span class="sxs-lookup"><span data-stu-id="78ea5-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78ea5-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="78ea5-132">Remarks</span></span>

<span data-ttu-id="78ea5-133">O método **NewEntry** cria uma nova entrada de catálogo de endereços, a ser adicionada diretamente a um contêiner ou usada para endereçar uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="78ea5-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="78ea5-134">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="78ea5-134">Notes to callers</span></span>

<span data-ttu-id="78ea5-135">Se você deseja que a nova entrada seja adicionada a um contêiner específico, defina _lpEIDContainer_ para o identificador de entrada do contêiner e _cbEIDContainer_ para a contagem de bytes no identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="78ea5-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="78ea5-136">Se quiser que a nova entrada seja adicionada à lista de destinatários de uma mensagem de saída, defina _lpEIDContainer_ como nulo e _cbEIDContainer_ como zero.</span><span class="sxs-lookup"><span data-stu-id="78ea5-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="78ea5-137">Se você deseja permitir que o usuário de um aplicativo cliente selecione o tipo de entrada a ser criado, passe zero em _cbEIDNewEntryTpl_ e nulo no _lpEIDNewEntryTpl_.</span><span class="sxs-lookup"><span data-stu-id="78ea5-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="78ea5-138">O método **NewEntry** exibe a tabela de one-off MAPI, uma lista de modelos suportados pelo MAPI e por cada provedor de catálogo de endereços na sessão.</span><span class="sxs-lookup"><span data-stu-id="78ea5-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="78ea5-139">Cada modelo pode criar uma entrada de destinatário para um ou mais tipos de endereço.</span><span class="sxs-lookup"><span data-stu-id="78ea5-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="78ea5-140">Se você quiser manter o identificador de entrada da nova entrada, passe os ponteiros válidos nos parâmetros _lpcbEIDNewEntry_ e _lppEIDNewEntry_ .</span><span class="sxs-lookup"><span data-stu-id="78ea5-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="78ea5-141">Você é responsável por liberar esse identificador de entrada quando terminar de fazê-lo chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="78ea5-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="78ea5-142">Para usar um modelo específico para adicionar uma nova entrada a um contêiner modificável, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="78ea5-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="78ea5-143">Chame o método [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir o contêiner de destino e defina o parâmetro _lpEntryID_ para o identificador de entrada do contêiner.</span><span class="sxs-lookup"><span data-stu-id="78ea5-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="78ea5-144">Chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do contêiner de destino e defina o _parâmetro ulPropTag_ como **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) e o parâmetro _lpiid_ para IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="78ea5-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="78ea5-145">O contêiner retornará uma tabela única que lista todos os modelos compatíveis com a criação de novas entradas.</span><span class="sxs-lookup"><span data-stu-id="78ea5-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="78ea5-146">Recupere a linha que representa o modelo para o tipo específico de entrada que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="78ea5-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="78ea5-147">A coluna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica o tipo de endereço que tem suporte no modelo.</span><span class="sxs-lookup"><span data-stu-id="78ea5-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="78ea5-148">Chame o método **NewEntry** e defina _lpEIDNewEntryTpl_ para o identificador de entrada do modelo selecionado.</span><span class="sxs-lookup"><span data-stu-id="78ea5-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="78ea5-149">O identificador de entrada será a coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do modelo na tabela one-off.</span><span class="sxs-lookup"><span data-stu-id="78ea5-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="78ea5-150">Passe zero em _cbEIDContainer_ e nulo no _lpEIDContainer_.</span><span class="sxs-lookup"><span data-stu-id="78ea5-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="78ea5-151">Passe um ponteiro válido no parâmetro _lppEIDNewEntry_ se você quiser manter o identificador de entrada da nova entrada.</span><span class="sxs-lookup"><span data-stu-id="78ea5-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="78ea5-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="78ea5-152">See also</span></span>



[<span data-ttu-id="78ea5-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="78ea5-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="78ea5-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="78ea5-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="78ea5-155">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="78ea5-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="78ea5-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="78ea5-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

