---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405580"
---
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="a5567-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="a5567-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="a5567-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5567-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5567-105">Copia ou move uma ou mais propriedades de um objeto para outro objeto.</span><span class="sxs-lookup"><span data-stu-id="a5567-105">Copies or moves one or more properties of an object to another object.</span></span>
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="a5567-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5567-106">Parameters</span></span>

 <span data-ttu-id="a5567-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="a5567-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="a5567-108">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto com as propriedades a serem copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="a5567-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="a5567-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="a5567-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="a5567-110">no Um ponteiro para o objeto que contém as propriedades a serem copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="a5567-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="a5567-111">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="a5567-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="a5567-112">no Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz contada de marcas de propriedade que indicam as propriedades a serem copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="a5567-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="a5567-113">O parâmetro _lpIncludeProps_ não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="a5567-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="a5567-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a5567-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="a5567-115">no Uma alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="a5567-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="a5567-116">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a5567-116">_lpProgress_</span></span>
  
> <span data-ttu-id="a5567-117">no Um ponteiro para uma implementação de um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="a5567-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="a5567-118">Se NULL for passado no parâmetro _lpProgress_ , o indicador de progresso será exibido usando a implementação MAPI.</span><span class="sxs-lookup"><span data-stu-id="a5567-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="a5567-119">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="a5567-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a5567-120">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="a5567-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="a5567-121">no Um ponteiro para o identificador de interface que representa a interface a ser usada para acessar o objeto para receber as propriedades que são copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="a5567-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="a5567-122">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="a5567-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="a5567-123">no Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="a5567-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="a5567-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a5567-124">_ulFlags_</span></span>
  
> <span data-ttu-id="a5567-125">no Uma bitmask de sinalizadores que controlam como a operação de cópia ou movimentação é executada.</span><span class="sxs-lookup"><span data-stu-id="a5567-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="a5567-126">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a5567-126">The following flags can be set:</span></span>
    
<span data-ttu-id="a5567-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a5567-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a5567-128">Exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="a5567-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="a5567-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="a5567-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="a5567-130">**DoCopyProps** deve executar uma operação de movimentação em vez de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="a5567-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="a5567-131">Quando esse sinalizador não é definido, o **DoCopyProps** realiza uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="a5567-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="a5567-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="a5567-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="a5567-133">As propriedades existentes no objeto de destino não devem ser substituídas.</span><span class="sxs-lookup"><span data-stu-id="a5567-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="a5567-134">Quando esse sinalizador não é definido, **DoCopyProps** substitui as propriedades existentes.</span><span class="sxs-lookup"><span data-stu-id="a5567-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="a5567-135">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="a5567-135">_lppProblems_</span></span>
  
> <span data-ttu-id="a5567-136">[in, out] Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; caso contrário, NULL, que não indica nenhuma necessidade de informações de erro.</span><span class="sxs-lookup"><span data-stu-id="a5567-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="a5567-137">Se _lppProblems_ for um ponteiro válido na entrada, **DoCopyProps** retornará informações detalhadas sobre erros ao copiar uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="a5567-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a5567-138">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a5567-138">Return value</span></span>

<span data-ttu-id="a5567-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5567-139">S_OK</span></span> 
  
> <span data-ttu-id="a5567-140">As propriedades foram copiadas ou movidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="a5567-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="a5567-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="a5567-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="a5567-142">Uma propriedade a ser copiada ou movida já existe no objeto de destino e o sinalizador MAPI_NOREPLACE está definido.</span><span class="sxs-lookup"><span data-stu-id="a5567-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="a5567-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="a5567-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="a5567-144">O objeto de origem direta ou indiretamente contém o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="a5567-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="a5567-145">Um trabalho significativo pode ter sido realizado antes da descoberta dessa condição, portanto, os objetos de origem e de destino podem ser parcialmente modificados.</span><span class="sxs-lookup"><span data-stu-id="a5567-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="a5567-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="a5567-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="a5567-147">A interface identificada pelo parâmetro _lpSrcInterface_ não é suportada pelo objeto de origem ou a interface identificada pelo parâmetro _lpDestInterface_ não é suportada pelo objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="a5567-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="a5567-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a5567-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="a5567-149">Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="a5567-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="a5567-150">Esse erro será retornado se o objeto de destino for o mesmo que o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="a5567-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="a5567-151">Os valores a seguir podem ser retornados na estrutura **SPropProblemArray** , mas não como valores de retorno para **DoCopyProps**.</span><span class="sxs-lookup"><span data-stu-id="a5567-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="a5567-152">Esses erros se aplicam a uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="a5567-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="a5567-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a5567-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a5567-154">O sinalizador MAPI_UNICODE foi definido e o **DoCopyProps** não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e **DoCopyProps** suporta apenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="a5567-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="a5567-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="a5567-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="a5567-156">A propriedade não pode ser modificada pelo chamador porque é uma propriedade somente leitura, calculada pelo proprietário do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="a5567-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="a5567-157">Esse erro não é grave; o chamador deve permitir que a operação de cópia continue.</span><span class="sxs-lookup"><span data-stu-id="a5567-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="a5567-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="a5567-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="a5567-159">O tipo de propriedade é inválido.</span><span class="sxs-lookup"><span data-stu-id="a5567-159">The property type is invalid.</span></span>
    
<span data-ttu-id="a5567-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="a5567-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="a5567-161">O tipo de propriedade não é o tipo esperado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="a5567-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5567-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5567-162">Remarks</span></span>

<span data-ttu-id="a5567-163">O método **IMAPISupport::D ocopyprops** é implementado para objetos de suporte do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a5567-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="a5567-164">Os provedores de repositórios de mensagens podem chamar o **DoCopyProps** para implementar o método [IMAPIProp:: CopyProps](imapiprop-copyprops.md) para suas pastas e mensagens.</span><span class="sxs-lookup"><span data-stu-id="a5567-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="a5567-165">**DoCopyProps** copia ou move as propriedades que são identificadas na matriz de marca de propriedade indicada por _lpIncludeProps_ e que estão presentes no objeto apontado por _lpSrcObj_.</span><span class="sxs-lookup"><span data-stu-id="a5567-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a5567-166">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a5567-166">Notes to callers</span></span>

<span data-ttu-id="a5567-167">Quando você copia Propriedades entre objetos do mesmo tipo, como duas mensagens, os parâmetros _lpSrcInterface_ e _lpDestInterface_ devem conter o mesmo identificador de interface e os parâmetros _lpSrcObj_ e _lpDestObj_ deve apontar para objetos do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="a5567-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="a5567-168">Se _lpDestInterface_ estiver definido como nulo, **DoCopyProps** retornará MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="a5567-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="a5567-169">Se você definir _lpDestInterface_ como um identificador de interface aceitável, mas definir _lpDestObj_ como um ponteiro inválido, os resultados serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="a5567-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="a5567-170">Provavelmente, o provedor falhará.</span><span class="sxs-lookup"><span data-stu-id="a5567-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="a5567-171">Defina o sinalizador MAPI_NOREPLACE se não quiser que nenhuma das propriedades no objeto de destino seja substituída.</span><span class="sxs-lookup"><span data-stu-id="a5567-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="a5567-172">As propriedades no objeto de destino que existem no objeto de origem e não são sobrescritas não são excluídas ou modificadas.</span><span class="sxs-lookup"><span data-stu-id="a5567-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="a5567-173">Para copiar a lista de destinatários de uma mensagem, inclua a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) na matriz de marca de propriedade apontada pelo parâmetro _lpIncludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="a5567-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="a5567-174">Para copiar os anexos da mensagem, inclua a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a5567-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="a5567-175">Para copiar uma pasta ou uma tabela de conteúdo ou hierarquia do contêiner de catálogo de endereços, inclua **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a5567-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="a5567-176">Para incluir a tabela de conteúdo associado de uma pasta, inclua a propriedade **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) na matriz.</span><span class="sxs-lookup"><span data-stu-id="a5567-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="a5567-177">Se as subpastas forem copiadas ou movidas, seu conteúdo será copiado ou movido totalmente, independentemente do uso das propriedades indicadas pela estrutura **SPropTagArray** .</span><span class="sxs-lookup"><span data-stu-id="a5567-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="a5567-178">**DoCopyProps** relata erros globais que ocorrem com a operação como um todo e erros individuais que ocorrem com uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="a5567-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="a5567-179">Esses erros individuais são colocados em uma estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="a5567-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="a5567-180">Você pode suprimir o relatório de erros no nível da propriedade passando NULL, em vez de um ponteiro válido, para o parâmetro da estrutura da matriz do problema da propriedade.</span><span class="sxs-lookup"><span data-stu-id="a5567-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="a5567-181">Se você quiser receber informações sobre erros, passe um ponteiro de estrutura **SPropProblemArray** válido no parâmetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="a5567-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="a5567-182">Quando **DoCopyProps** retorna S_OK, verifique se há possíveis erros com propriedades individuais na estrutura.</span><span class="sxs-lookup"><span data-stu-id="a5567-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="a5567-183">Quando **DoCopyProps** retorna um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="a5567-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="a5567-184">Em vez disso, chame o método [IMAPISupport:: GetLastError](imapisupport-getlasterror.md) para recuperar informações de erro detalhadas.</span><span class="sxs-lookup"><span data-stu-id="a5567-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="a5567-185">Se **DoCopyProps** retornar S_OK, libere a estrutura **SPropProblemArray** retornada chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a5567-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5567-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5567-186">See also</span></span>



[<span data-ttu-id="a5567-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="a5567-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="a5567-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="a5567-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="a5567-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="a5567-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="a5567-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a5567-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="a5567-191">Propriedade canônica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="a5567-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="a5567-192">Propriedade canônica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="a5567-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="a5567-193">Propriedade canônica PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="a5567-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="a5567-194">Propriedade canônica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="a5567-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="a5567-195">Propriedade canônica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="a5567-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="a5567-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="a5567-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="a5567-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a5567-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="a5567-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5567-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

