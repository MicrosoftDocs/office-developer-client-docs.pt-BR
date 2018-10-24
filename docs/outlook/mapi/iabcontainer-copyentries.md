---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382943"
---
# <a name="iabcontainercopyentries"></a><span data-ttu-id="53185-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="53185-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="53185-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53185-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53185-105">Copia uma ou mais entradas, os usuários geralmente mensagens ou listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="53185-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="53185-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53185-106">Parameters</span></span>

 <span data-ttu-id="53185-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="53185-107">_lpEntries_</span></span>
  
> <span data-ttu-id="53185-108">[in] Um ponteiro para uma matriz de estruturas [ENTRYLIST](entrylist.md) que contém os identificadores de entrada das entradas para copiar.</span><span class="sxs-lookup"><span data-stu-id="53185-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="53185-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="53185-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="53185-110">[in] O identificador para a janela pai de todas as caixas de diálogo ou windows esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="53185-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="53185-111">O parâmetro _ulUIParam_ deve ser zero se o sinalizador AB_NO_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="53185-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="53185-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="53185-112">_lpProgress_</span></span>
  
> <span data-ttu-id="53185-113">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso ou nulo.</span><span class="sxs-lookup"><span data-stu-id="53185-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="53185-114">Se _lpProgress_ for NULL, um indicador de progresso deve ser exibido usando o objeto de progresso fornecido pelo MAPI por meio do método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="53185-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="53185-115">O parâmetro _lpProgress_ será ignorado se o sinalizador AB_NO_DIALOG está definido na _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="53185-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="53185-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53185-116">_ulFlags_</span></span>
  
> <span data-ttu-id="53185-117">[in] Uma bitmask dos sinalizadores que controla como a operação de cópia é executada.</span><span class="sxs-lookup"><span data-stu-id="53185-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="53185-118">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="53185-118">The following flags can be set:</span></span>
    
<span data-ttu-id="53185-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="53185-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="53185-120">Suprime a exibição de um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="53185-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="53185-121">Se esse sinalizador não estiver definida, um indicador de progresso é exibido.</span><span class="sxs-lookup"><span data-stu-id="53185-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="53185-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="53185-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="53185-123">Indica que um afastado nível de verificação de entrada duplicada deve ser realizado.</span><span class="sxs-lookup"><span data-stu-id="53185-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="53185-124">A implementação de verificação de entrada duplicada afastada é específico do provedor.</span><span class="sxs-lookup"><span data-stu-id="53185-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="53185-125">Por exemplo, um provedor pode definir uma correspondência afastada conforme qualquer duas entradas que têm o mesmo nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="53185-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="53185-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="53185-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="53185-127">Indica que um nível estrito de verificação de entrada duplicada deve ser realizado.</span><span class="sxs-lookup"><span data-stu-id="53185-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="53185-128">A implementação de verificação de entrada duplicada strict é específico do provedor.</span><span class="sxs-lookup"><span data-stu-id="53185-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="53185-129">Por exemplo, um provedor pode definir uma correspondência estrita como qualquer duas entradas que têm ambas o mesmo nome e endereço de mensagens são exibidos.</span><span class="sxs-lookup"><span data-stu-id="53185-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="53185-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="53185-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="53185-131">Indica que uma nova entrada deve substituir um existente, se for determinado que as duas versões sejam duplicatas.</span><span class="sxs-lookup"><span data-stu-id="53185-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53185-132">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="53185-132">Return value</span></span>

<span data-ttu-id="53185-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="53185-133">S_OK</span></span> 
  
> <span data-ttu-id="53185-134">A operação de cópia foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="53185-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="53185-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="53185-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="53185-136">A operação de cópia bem-sucedida, mas um ou mais das entradas não pôde ser copiado.</span><span class="sxs-lookup"><span data-stu-id="53185-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="53185-137">Quando este valor é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="53185-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="53185-138">Para testar esse valor, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="53185-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="53185-139">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="53185-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53185-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="53185-140">Remarks</span></span>

<span data-ttu-id="53185-141">O método **IABContainer::CopyEntries** copia entradas do mesmo contêiner ou em um contêiner diferente.</span><span class="sxs-lookup"><span data-stu-id="53185-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="53185-142">Uma chamada para **CopyEntries** é funcionalmente equivalente à fazendo as seguintes chamadas para cada entrada a serem copiados:</span><span class="sxs-lookup"><span data-stu-id="53185-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="53185-143">O método [IABContainer::CreateEntry](iabcontainer-createentry.md) para criar a nova entrada.</span><span class="sxs-lookup"><span data-stu-id="53185-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="53185-144">O método [IMAPIProp::GetProps](imapiprop-getprops.md) para ler as propriedades da entrada a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="53185-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="53185-145">O método [IMAPIProp::SetProps](imapiprop-setprops.md) para gravar as propriedades para a nova entrada.</span><span class="sxs-lookup"><span data-stu-id="53185-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="53185-146">Método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da nova entrada para executar uma gravação.</span><span class="sxs-lookup"><span data-stu-id="53185-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="53185-147">Método de [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) da nova entrada ao lançamento de referência do contêiner.</span><span class="sxs-lookup"><span data-stu-id="53185-147">The new entry's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="53185-148">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="53185-148">Notes to implementers</span></span>

<span data-ttu-id="53185-149">Todos os contêineres que suportam o método **IABContainer::CopyEntries** devem ser pode ser modificados.</span><span class="sxs-lookup"><span data-stu-id="53185-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="53185-150">Defina sinalizador AB_MODIFIABLE do seu contêiner na sua propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que ela é modificável.</span><span class="sxs-lookup"><span data-stu-id="53185-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="53185-151">Você deve oferecer suporte a todos os sinalizadores; No entanto, a interpretação e usar esses sinalizadores é específico da implementação — ou seja, você pode determinar o significado a semântica dos sinalizadores CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT no contexto da sua implementação.</span><span class="sxs-lookup"><span data-stu-id="53185-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="53185-152">Se você não pode ou não determinam se uma entrada é uma duplicata, sempre permita a entrada a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="53185-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="53185-153">Se o sinalizador CREATE_REPLACE estiver definido, sempre copie a entrada independentemente se CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT é definida e se a entrada é uma duplicata.</span><span class="sxs-lookup"><span data-stu-id="53185-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="53185-154">Se CREATE_REPLACE não estiver definida e CREATE_CHECK_DUP_STRICT for definido, verificar duplicatas.</span><span class="sxs-lookup"><span data-stu-id="53185-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="53185-155">Se uma entrada é considerada uma duplicata, não copie a entrada.</span><span class="sxs-lookup"><span data-stu-id="53185-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="53185-156">Não é necessário dar suporte a CREATE_REPLACE; não oferece suporte à CREATE_REPLACE significa que você pode ignorá-la e executar sempre uma cópia.</span><span class="sxs-lookup"><span data-stu-id="53185-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="53185-157">Retorne o aviso MAPI_W_PARTIAL_COMPLETION somente se uma entrada não duplicada não pode ser copiada.</span><span class="sxs-lookup"><span data-stu-id="53185-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="53185-158">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="53185-158">Notes to callers</span></span>

<span data-ttu-id="53185-159">Use os sinalizadores CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT para indicar ao provedor de como você deseja que o contêiner para executar a verificação de duplicata-entrada.</span><span class="sxs-lookup"><span data-stu-id="53185-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="53185-160">Se você precisa ter uma entrada adicionada, independentemente se ele é uma duplicata, não defina nenhuma desses sinalizadores ou definir o sinalizador CREATE_REPLACE.</span><span class="sxs-lookup"><span data-stu-id="53185-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="53185-161">CREATE_REPLACE indica que não faz se uma entrada é uma duplicata; Você sempre deseja substituir a entrada original.</span><span class="sxs-lookup"><span data-stu-id="53185-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53185-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="53185-162">See also</span></span>



[<span data-ttu-id="53185-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="53185-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="53185-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="53185-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="53185-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53185-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="53185-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="53185-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="53185-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="53185-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

