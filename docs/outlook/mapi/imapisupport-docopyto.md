---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331805"
---
# <a name="imapisupportdocopyto"></a><span data-ttu-id="8d8ab-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="8d8ab-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="8d8ab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d8ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d8ab-105">Copia ou move todas as propriedades de um objeto, exceto as propriedades especificamente excluídas, para outro objeto.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="8d8ab-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d8ab-106">Parameters</span></span>

 <span data-ttu-id="8d8ab-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="8d8ab-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="8d8ab-108">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto que tem as propriedades a serem copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="8d8ab-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="8d8ab-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="8d8ab-110">no Um ponteiro para o objeto que tem as propriedades a serem copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="8d8ab-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="8d8ab-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="8d8ab-112">no A contagem de interfaces a serem excluídas quando você copia ou move Propriedades.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="8d8ab-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="8d8ab-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="8d8ab-114">no Uma matriz de identificadores de interface que indica interfaces que não devem ser usadas quando você copia ou move informações complementares para o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="8d8ab-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="8d8ab-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="8d8ab-116">no Um ponteiro para uma matriz de marca de propriedade que identifica as marcas de propriedade que devem ser excluídas da operação de cópia ou movimentação.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="8d8ab-117">Passar NULL no parâmetro _lpExcludeProps_ indica que todas as propriedades do objeto devem ser copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="8d8ab-118">\*\*\*\* Docopyto retorna MAPI_E_INVALID_PARAMETER quando o membro **CValues** da estrutura [SPropTagArray](sproptagarray.md) apontada por _lpExcludeProps_ é definida como 0.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="8d8ab-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8d8ab-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="8d8ab-120">no Uma alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="8d8ab-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="8d8ab-121">_lpProgress_</span></span>
  
> <span data-ttu-id="8d8ab-122">no Um ponteiro para uma implementação de indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="8d8ab-123">Se NULL for passado no parâmetro _lpProgress_ , MAPI fornecerá a implementação de progresso.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="8d8ab-124">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="8d8ab-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8d8ab-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="8d8ab-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="8d8ab-126">no Um ponteiro para o identificador de interface que representa a interface a ser usada para acessar o objeto para receber as propriedades copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="8d8ab-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="8d8ab-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="8d8ab-128">no Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="8d8ab-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d8ab-129">_ulFlags_</span></span>
  
> <span data-ttu-id="8d8ab-130">no Uma bitmask de sinalizadores que controlam a operação de cópia ou movimentação.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="8d8ab-131">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="8d8ab-131">The following flags can be set:</span></span>
    
<span data-ttu-id="8d8ab-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8d8ab-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="8d8ab-133">Exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="8d8ab-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="8d8ab-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="8d8ab-135">\*\*\*\* Docopyto deve executar uma operação de movimentação em vez de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="8d8ab-136">Quando esse sinalizador não é definido, \*\*\*\* docopyto realiza uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="8d8ab-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="8d8ab-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="8d8ab-138">As propriedades existentes no objeto de destino não devem ser substituídas.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="8d8ab-139">Quando esse sinalizador não é definido, \*\*\*\* docopyto substitui as propriedades existentes.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="8d8ab-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="8d8ab-140">_lppProblems_</span></span>
  
> <span data-ttu-id="8d8ab-141">bota Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; caso contrário, NULL, que não indica nenhuma necessidade de informações de erro.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="8d8ab-142">Se _lppProblems_ for um ponteiro válido na entrada, \*\*\*\* docopyto retornará informações detalhadas sobre erros ao copiar uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8d8ab-143">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8d8ab-143">Return value</span></span>

<span data-ttu-id="8d8ab-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d8ab-144">S_OK</span></span> 
  
> <span data-ttu-id="8d8ab-145">As propriedades foram copiadas ou movidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="8d8ab-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="8d8ab-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="8d8ab-147">Uma propriedade a ser copiada ou movida já existe no objeto de destino e o sinalizador MAPI_NOREPLACE está definido.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="8d8ab-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="8d8ab-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="8d8ab-149">O objeto de origem direta ou indiretamente contém o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="8d8ab-150">Um trabalho significativo pode ter sido realizado antes da descoberta dessa condição, portanto, os objetos de origem e de destino podem ser parcialmente modificados.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="8d8ab-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="8d8ab-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="8d8ab-152">A interface identificada pelo parâmetro _lpSrcInterface_ não é suportada pelo objeto apontado por _lpSrcObj_ou a interface identificada pelo parâmetro _lpDestInterface_ não é suportada pelo objeto apontado por _lpDestObj _.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="8d8ab-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8d8ab-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8d8ab-154">Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="8d8ab-155">Esse erro será retornado se o objeto de destino for o mesmo que o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="8d8ab-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8d8ab-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="8d8ab-157">O parâmetro _lpSrcInterface_ é NULL.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="8d8ab-158">Os valores a seguir podem ser retornados na estrutura **SPropProblemArray** , mas não como valores de retorno \*\*\*\* para docopyto.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="8d8ab-159">Esses erros se aplicam a uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="8d8ab-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8d8ab-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="8d8ab-161">O sinalizador MAPI_UNICODE foi definido e doCopyto não tem suporte para Unicode, ou MAPI_UNICODE não foi definido e **Docopyto** suporta apenas Unicode. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8d8ab-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="8d8ab-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="8d8ab-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="8d8ab-163">A propriedade não pode ser modificada pelo chamador porque é uma propriedade somente leitura, calculada pelo proprietário do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="8d8ab-164">Esse erro não é grave; o chamador deve permitir que a operação de cópia continue.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="8d8ab-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="8d8ab-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="8d8ab-166">O tipo de propriedade é inválido.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-166">The property type is invalid.</span></span>
    
<span data-ttu-id="8d8ab-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="8d8ab-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="8d8ab-168">O tipo de propriedade não é o tipo esperado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d8ab-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d8ab-169">Remarks</span></span>

<span data-ttu-id="8d8ab-170">O método **IMAPISupport::D ocopyto** é implementado para objetos de suporte do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="8d8ab-171">Os provedores de repositórios \*\*\*\* de mensagens podem chamar docopyto para implementar o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) para suas pastas e mensagens.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="8d8ab-172">Por padrão, \*\*\*\* docopyto copia ou move todas as propriedades de um objeto para outro objeto.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="8d8ab-173">Todos os subobjetos no objeto de origem são automaticamente incluídos na operação e copiados ou movidos completamente.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="8d8ab-174">Se qualquer uma das propriedades copiadas ou movidas já existir no objeto de destino, as propriedades existentes serão sobrescritas pelas novas propriedades, a menos que o sinalizador MAPI_NOREPLACE seja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="8d8ab-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="8d8ab-175">As informações existentes no objeto de destino que não estão sobrescritas são deixadas inalteradas.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8d8ab-176">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="8d8ab-176">Notes to callers</span></span>

<span data-ttu-id="8d8ab-177">Para excluir propriedades da operação de cópia ou movimentação, inclua suas marcas de propriedade no parâmetro _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="8d8ab-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="8d8ab-178">Se você passar os resultados do uso da macro [PROP_TAG](prop_tag.md) para criar uma marca de propriedade a partir de um identificador específico na matriz de marca de propriedade, todas as propriedades com esse identificador serão excluídas.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="8d8ab-179">Por exemplo, a seguinte entrada na matriz de marca de propriedade faz com que todas as propriedades com um identificador de 0x8002 sejam excluídas, independentemente do tipo:</span><span class="sxs-lookup"><span data-stu-id="8d8ab-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="8d8ab-180">Para evitar a cópia do tempo de entrega de uma mensagem quando você copia a mensagem para uma pasta diferente, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) na marca de propriedade Exclude array.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="8d8ab-181">Para excluir a lista de destinatários de uma mensagem, adicione a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) à matriz Exclude.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="8d8ab-182">Para excluir os anexos de uma mensagem, adicione a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) à matriz.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="8d8ab-183">Da mesma forma, para impedir a cópia ou a movimentação de uma pasta ou hierarquia de um contêiner de catálogo de endereços ou uma tabela de conteúdo, inclua **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na marca Property Exclude array.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="8d8ab-184">Ignore os erros de MAPI_E_COMPUTED retornados na estrutura **SPropProblemArray** no parâmetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="8d8ab-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="8d8ab-185">O identificador de interface em que _lpSrcInterface_ aponta é geralmente o mesmo que o identificador de interface que o _lpDestInterface_ aponta.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="8d8ab-186">Se você passar um identificador de interface aceitável no _lpDestInterface_ , mas um ponteiro inválido no _lpDestObj_, os resultados serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="8d8ab-187">Provavelmente isso causará falha no provedor.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="8d8ab-188">Por outro lado, se você estiver ciente de informações complementares que não devem ser copiadas ou movidas, adicione os identificadores de interface para as interfaces a serem excluídas na matriz passadas no parâmetro _rgiidExclude_ .</span><span class="sxs-lookup"><span data-stu-id="8d8ab-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="8d8ab-189">Por exemplo, se você estiver copiando mensagens, mas não qualquer um de seus anexos de mensagem, passe IID_IMessage na matriz _rgiidExclude_ .</span><span class="sxs-lookup"><span data-stu-id="8d8ab-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="8d8ab-190">\*\*\*\* Docopyto ignora todas as interfaces listadas no _rgiidExclude_ que não são reconhecidas.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="8d8ab-191">Quando você usa o parâmetro _rgiidExclude_ para excluir uma interface, ele também exclui todas as interfaces derivadas dessa interface.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="8d8ab-192">Por exemplo, a exclusão da interface [IMAPIContainer](imapicontainerimapiprop.md) faz com que as pastas ou contêineres do catálogo de endereços sejam excluídos, dependendo do tipo de provedor.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="8d8ab-193">Não exclua [IMAPIProp](imapipropiunknown.md) ou [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) , pois muitas interfaces derivam deles.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="8d8ab-194">\*\*\*\* Docopyto relata erros globais que se aplicam à operação como um todo e erros individuais que se aplicam a propriedades individuais.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="8d8ab-195">Esses erros individuais são colocados em uma estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="8d8ab-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="8d8ab-196">Você pode suprimir o relatório de erros no nível da propriedade passando NULL, em vez de um ponteiro válido, para o parâmetro da estrutura da matriz do problema da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="8d8ab-197">Se você quiser receber informações sobre erros, passe um ponteiro de estrutura **SPropProblemArray** válido no parâmetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="8d8ab-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="8d8ab-198">Quando \*\*\*\* docopyto retorna S_OK, verifique se há possíveis erros com propriedades individuais na estrutura.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="8d8ab-199">Quando \*\*\*\* docopyto retorna um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="8d8ab-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="8d8ab-200">Em vez disso, chame o método [IMAPISupport:: GetLastError](imapisupport-getlasterror.md) para recuperar informações de erro detalhadas.</span><span class="sxs-lookup"><span data-stu-id="8d8ab-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="8d8ab-201">Se \*\*\*\* docopyto retornar S_OK, libere a estrutura **SPropProblemArray** retornada chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8d8ab-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="8d8ab-202">Se ocorrer um erro global na chamada \*\*\*\* docopyto, não use nem libere a estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="8d8ab-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="8d8ab-203">Os provedores devem ignorar o membro _ulIndex_ nas estruturas **SPropProblemArray** retornadas por docopyto. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8d8ab-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d8ab-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d8ab-204">See also</span></span>



[<span data-ttu-id="8d8ab-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="8d8ab-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="8d8ab-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="8d8ab-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="8d8ab-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="8d8ab-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="8d8ab-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8d8ab-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="8d8ab-209">Propriedade canônica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="8d8ab-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="8d8ab-210">Propriedade canônica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="8d8ab-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="8d8ab-211">Propriedade canônica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="8d8ab-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="8d8ab-212">Propriedade canônica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="8d8ab-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="8d8ab-213">Propriedade canônica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="8d8ab-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="8d8ab-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="8d8ab-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="8d8ab-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="8d8ab-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="8d8ab-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d8ab-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

