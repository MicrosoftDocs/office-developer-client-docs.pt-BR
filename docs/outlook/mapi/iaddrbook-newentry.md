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
# <a name="iaddrbooknewentry"></a><span data-ttu-id="34be1-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="34be1-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="34be1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34be1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34be1-105">Adiciona um novo destinatário a um contêiner de livro de endereços ou à lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="34be1-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="34be1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34be1-106">Parameters</span></span>

 <span data-ttu-id="34be1-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="34be1-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="34be1-108">[in] Um alça para a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="34be1-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="34be1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="34be1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="34be1-110">[in] Uma máscara de bits de sinalizadores que controla o tipo de texto usado.</span><span class="sxs-lookup"><span data-stu-id="34be1-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="34be1-111">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="34be1-111">The following flag can be set:</span></span>
    
<span data-ttu-id="34be1-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="34be1-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="34be1-113">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="34be1-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="34be1-114">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="34be1-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="34be1-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="34be1-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="34be1-116">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEIDContainer._</span><span class="sxs-lookup"><span data-stu-id="34be1-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="34be1-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="34be1-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="34be1-118">[in] Um ponteiro para o identificador de entrada do contêiner ao qual o novo destinatário deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="34be1-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="34be1-119">Se o parâmetro  _cbEIDContainer_ for zero, o método **NewEntry** retornará um identificador de entrada de destinatário e uma lista de modelos como se o método [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) tivesse sido chamado.</span><span class="sxs-lookup"><span data-stu-id="34be1-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="34be1-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="34be1-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="34be1-121">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEIDNewEntryTpl._</span><span class="sxs-lookup"><span data-stu-id="34be1-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="34be1-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="34be1-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="34be1-123">[in] Um ponteiro para um modelo único que será usado para criar o novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="34be1-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="34be1-124">Se  _cbEIDNewEntryTpl_ for zero e  _lpEIDNewEntryTpl_ for NULL, **NewEntry** exibirá uma caixa de diálogo com a qual o usuário poderá selecionar em uma lista de modelos para adicionar novas entradas.</span><span class="sxs-lookup"><span data-stu-id="34be1-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="34be1-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="34be1-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="34be1-126">[out] Um ponteiro para a contagem de byte no identificador de entrada apontado pelo _parâmetro lppEIDNewEntry._</span><span class="sxs-lookup"><span data-stu-id="34be1-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="34be1-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="34be1-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="34be1-128">[out] Um ponteiro para um ponteiro para o identificador de entrada do novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="34be1-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34be1-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="34be1-129">Return value</span></span>

<span data-ttu-id="34be1-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="34be1-130">S_OK</span></span> 
  
> <span data-ttu-id="34be1-131">A nova entrada do livro de endereços foi criada com êxito.</span><span class="sxs-lookup"><span data-stu-id="34be1-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34be1-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="34be1-132">Remarks</span></span>

<span data-ttu-id="34be1-133">O **método NewEntry** cria uma nova entrada de livro de endereços, a ser adicionada diretamente a um contêiner ou a ser usada para tratar de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="34be1-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="34be1-134">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="34be1-134">Notes to callers</span></span>

<span data-ttu-id="34be1-135">Se você quiser que a nova entrada seja adicionada a um contêiner específico, de conjunto  _lpEIDContainer_ para o identificador de entrada do contêiner e  _cbEIDContainer_ para a contagem de byte no identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="34be1-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="34be1-136">Se você quiser que a nova entrada seja adicionada à lista de destinatários de uma mensagem de saída, de definida  _lpEIDContainer_ como NULL e  _cbEIDContainer_ como zero.</span><span class="sxs-lookup"><span data-stu-id="34be1-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="34be1-137">Se você quiser permitir que o usuário de um aplicativo cliente selecione o tipo de entrada a ser criado, passe zero em  _cbEIDNewEntryTpl_ e NULL em  _lpEIDNewEntryTpl_.</span><span class="sxs-lookup"><span data-stu-id="34be1-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="34be1-138">O **método NewEntry** exibe a tabela única MAPI, uma lista de modelos com suporte por MAPI e por cada provedor de agenda na sessão.</span><span class="sxs-lookup"><span data-stu-id="34be1-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="34be1-139">Cada modelo pode criar uma entrada de destinatário para um ou mais tipos de endereço.</span><span class="sxs-lookup"><span data-stu-id="34be1-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="34be1-140">Se você quiser manter o identificador de entrada da nova entrada, passe ponteiros válidos nos parâmetros _lpcbEIDNewEntry_ e _lppEIDNewEntry._</span><span class="sxs-lookup"><span data-stu-id="34be1-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="34be1-141">Você é responsável por liberar esse identificador de entrada quando terminar de chamá-lo chamando a [função MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="34be1-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="34be1-142">Para usar um modelo específico para adicionar uma nova entrada a um contêiner modificável, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="34be1-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="34be1-143">Chame o [método IMAPISession::OpenEntry](imapisession-openentry.md) para abrir o contêiner de destino e de definir o parâmetro  _lpEntryID_ como o identificador de entrada do contêiner.</span><span class="sxs-lookup"><span data-stu-id="34be1-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="34be1-144">Chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner de destino e de definir o parâmetro  _ulPropTag_ como **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) e o parâmetro  _lpiid_ como IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="34be1-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="34be1-145">O contêiner retornará uma tabela única que lista todos os modelos compatíveis com a criação de novas entradas.</span><span class="sxs-lookup"><span data-stu-id="34be1-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="34be1-146">Recupere a linha que representa o modelo para o tipo específico de entrada que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="34be1-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="34be1-147">A **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica o tipo de endereço suportado pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="34be1-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="34be1-148">Chame o **método NewEntry** e de set  _lpEIDNewEntryTpl_ para o identificador de entrada do modelo selecionado.</span><span class="sxs-lookup"><span data-stu-id="34be1-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="34be1-149">O identificador de entrada **será a PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do modelo na tabela one-off.</span><span class="sxs-lookup"><span data-stu-id="34be1-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="34be1-150">Passe zero em  _cbEIDContainer_ e NULL em  _lpEIDContainer_.</span><span class="sxs-lookup"><span data-stu-id="34be1-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="34be1-151">Passe um ponteiro válido no parâmetro  _lppEIDNewEntry_ se quiser manter o identificador de entrada da nova entrada.</span><span class="sxs-lookup"><span data-stu-id="34be1-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="34be1-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="34be1-152">See also</span></span>



[<span data-ttu-id="34be1-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="34be1-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="34be1-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="34be1-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="34be1-155">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="34be1-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="34be1-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="34be1-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

