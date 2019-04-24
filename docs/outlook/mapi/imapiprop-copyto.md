---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356389"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="6dfc4-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="6dfc4-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="6dfc4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dfc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dfc4-105">Copia ou move todas as propriedades, exceto as propriedades especificamente excluídas.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="6dfc4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dfc4-106">Parameters</span></span>

 <span data-ttu-id="6dfc4-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="6dfc4-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="6dfc4-108">no A contagem de interfaces a serem excluídas quando as propriedades são copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="6dfc4-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="6dfc4-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="6dfc4-110">no Uma matriz de identificadores de interface (IIDs) que especificam interfaces que não devem ser usadas quando as informações suplementares são copiadas ou movidas para o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="6dfc4-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="6dfc4-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="6dfc4-112">no Um ponteiro para uma matriz de marca de propriedade que identifica as marcas de propriedade que devem ser excluídas da operação de cópia ou movimentação.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="6dfc4-113">Passar **NULL** no parâmetro _lpExcludeProps_ indica que todas as propriedades do objeto devem ser copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="6dfc4-114">**CopyTo** retorna MAPI_E_INVALID_PARAMETER quando o membro **CValues** da estrutura [SPropProblemArray](spropproblemarray.md) apontada por _lpExcludeProps_ é definida como 0.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="6dfc4-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6dfc4-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="6dfc4-116">no Uma alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="6dfc4-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="6dfc4-117">_lpProgress_</span></span>
  
> <span data-ttu-id="6dfc4-118">no Um ponteiro para uma implementação de indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="6dfc4-119">Se **NULL** for passado no parâmetro _lpProgress_ , MAPI fornecerá a implementação de progresso.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="6dfc4-120">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="6dfc4-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6dfc4-121">_lpInterface_</span></span>
  
> <span data-ttu-id="6dfc4-122">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto apontado pelo parâmetro _lpDestObj_ .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="6dfc4-123">O parâmetro _lpInterface_ não deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="6dfc4-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="6dfc4-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="6dfc4-125">no Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="6dfc4-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6dfc4-126">_ulFlags_</span></span>
  
> <span data-ttu-id="6dfc4-127">no Uma bitmask de sinalizadores que controlam a operação de cópia ou movimentação.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="6dfc4-128">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="6dfc4-128">The following flags can be set:</span></span>
    
<span data-ttu-id="6dfc4-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="6dfc4-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="6dfc4-130">Se **CopyTo** chamar o método [IMAPISupport::D ocopyto](imapisupport-docopyto.md) para manipular a operação de cópia ou movimentação, ele deverá retornar imediatamente com o valor de erro MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="6dfc4-131">O sinalizador MAPI_DECLINE_OK é definido por MAPI para limitar a recursividade.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="6dfc4-132">Os clientes não definem esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="6dfc4-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6dfc4-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6dfc4-134">Exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="6dfc4-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="6dfc4-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="6dfc4-136">**CopyTo** deve executar uma operação de movimentação em vez de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="6dfc4-137">Quando esse sinalizador não é definido, **CopyTo** executa uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="6dfc4-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="6dfc4-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="6dfc4-139">As propriedades existentes no objeto de destino não devem ser substituídas.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="6dfc4-140">Quando esse sinalizador não é definido, **CopyTo** substitui as propriedades existentes.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="6dfc4-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="6dfc4-141">_lppProblems_</span></span>
  
> <span data-ttu-id="6dfc4-142">[in, out] Na entrada, um ponteiro para um ponteiro para uma estrutura **SPropProblemArray** ; caso contrário, **NULL**, indicando que não há necessidade de informações de erro.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="6dfc4-143">Se _lppProblems_ for um ponteiro válido na entrada, **CopyTo** retornará informações detalhadas sobre erros ao copiar uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6dfc4-144">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6dfc4-144">Return value</span></span>

<span data-ttu-id="6dfc4-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="6dfc4-145">S_OK</span></span> 
  
> <span data-ttu-id="6dfc4-146">As propriedades foram copiadas ou movidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="6dfc4-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="6dfc4-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="6dfc4-148">Um subobjeto não pode ser copiado porque um subobjeto com o mesmo nome de exibição, especificado pela propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), já existe no objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="6dfc4-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="6dfc4-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="6dfc4-150">O provedor de serviços não implementa a operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="6dfc4-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="6dfc4-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="6dfc4-152">O objeto de origem executando a operação copiar ou mover direta ou indiretamente contém o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="6dfc4-153">Um trabalho significativo pode ter sido realizado antes da descoberta dessa condição, portanto, os objetos de origem e de destino podem ser parcialmente modificados.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="6dfc4-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="6dfc4-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="6dfc4-155">A interface identificada pelo parâmetro _lpInterface_ não é suportada pelo objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="6dfc4-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6dfc4-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6dfc4-157">Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="6dfc4-158">Esse erro será retornado se o objeto de destino for o mesmo que o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="6dfc4-159">Os valores a seguir podem ser retornados na estrutura **SPropProblemArray** , mas não como valores de retorno para **CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="6dfc4-160">Os seguintes erros se aplicam a uma única propriedade:</span><span class="sxs-lookup"><span data-stu-id="6dfc4-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="6dfc4-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6dfc4-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6dfc4-162">O sinalizador MAPI_UNICODE foi definido e **CopyTo** não dá suporte a Unicode, ou o MAPI_UNICODE não foi definido e o **CopyTo** suporta apenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="6dfc4-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="6dfc4-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="6dfc4-164">A propriedade não pode ser modificada pelo chamador porque é uma propriedade somente leitura, calculada pelo proprietário do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="6dfc4-165">Esse erro não é grave; o chamador deve permitir que a operação de cópia continue.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="6dfc4-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="6dfc4-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="6dfc4-167">O tipo de propriedade é inválido.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-167">The property type is invalid.</span></span>
    
<span data-ttu-id="6dfc4-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="6dfc4-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="6dfc4-169">O tipo de propriedade não é o tipo esperado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6dfc4-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="6dfc4-170">Remarks</span></span>

<span data-ttu-id="6dfc4-171">Por padrão, o método **IMAPIProp:: CopyTo** copia ou move todas as propriedades do objeto atual para um objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="6dfc4-172">**CopyTo** é usado quando um objeto deve ser copiado ou movido exatamente, com todas ou a maioria de suas propriedades intacta.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="6dfc4-173">Todos os subobjetos no objeto de origem são automaticamente incluídos na operação e são copiados ou movidos completamente.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="6dfc4-174">Por padrão, **CopyTo** substitui quaisquer propriedades no objeto de destino que correspondam às propriedades do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="6dfc4-175">Se qualquer uma das propriedades copiadas ou movidas já existir no objeto de destino, as propriedades existentes serão sobrescritas pelas novas propriedades, a menos que o sinalizador MAPI_NOREPLACE seja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="6dfc4-176">As informações existentes no objeto de destino que não estão sobrescritas são deixadas inalteradas.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6dfc4-177">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="6dfc4-177">Notes to implementers</span></span>

<span data-ttu-id="6dfc4-178">Você pode fornecer uma implementação completa de **CopyTo** ou depender da implementação que a MAPI fornece em seu objeto support.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="6dfc4-179">Se você quiser usar a implementação MAPI, chame **IMAPISupport::D ocopyto**.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="6dfc4-180">No enTanto, se você fizer o \*\*\*\* processamento de representante para docopyto e passar o sinalizador MAPI_DECLINE_OK, evite a chamada de suporte e retorne MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="6dfc4-181">O MAPI chamará com esse sinalizador para evitar a possível recursão que pode ocorrer quando pastas são copiadas.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="6dfc4-182">Como a operação de cópia pode ser demorada, você deve exibir um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="6dfc4-183">Use a implementação [método imapiprogress](imapiprogressiunknown.md) passada no parâmetro _lpProgress_ , se houver um.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="6dfc4-184">Se _lpProgress_ for **NULL**, chame o método [IMAPISupport::D OPROGRESSDIALOG](imapisupport-doprogressdialog.md) para usar a implementação MAPI.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="6dfc4-185">Não tente definir nenhuma propriedade somente leitura conhecida no objeto de destino; em vez disso, retorne MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="6dfc4-186">Os objetos de origem e destino devem usar as mesmas interfaces.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="6dfc4-187">Retornar MAPI_E_INVALID_PARAMETER se _lpInterface_ não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="6dfc4-188">Retornar MAPI_E_INTERFACE_NOT_SUPPORTED se todas as interfaces conhecidas forem excluídas.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="6dfc4-189">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="6dfc4-189">Notes to callers</span></span>

<span data-ttu-id="6dfc4-190">Não defina o sinalizador MAPI_DECLINE_OK; MAPI usa-o em suas chamadas para implementações **CopyTo** de provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="6dfc4-191">Como as operações de cópia e movimentação podem demorar um pouco, você deve solicitar a exibição de um indicador de progresso Configurando o sinalizador MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="6dfc4-192">Você pode definir o parâmetro _lpProgress_ para sua implementação do **método imapiprogress**, se você tiver um, ou como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="6dfc4-193">Se _lpProgress_ for **NULL**, **CopyTo** usará o indicador de progresso padrão que o MAPI fornece.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="6dfc4-194">Você pode suprimir a exibição de um indicador de progresso não definindo o sinalizador MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="6dfc4-195">**CopyTo** ignorará os parâmetros _ulUIParam_ e _lpProgress_ e não exibirá o indicador.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="6dfc4-196">**CopyTo** pode relatar erros globais e individuais, ou erros que ocorrem com uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="6dfc4-197">Esses erros individuais são colocados em uma estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="6dfc4-198">Você pode suprimir o relatório de erros no nível da propriedade passando **NULL**, em vez de um ponteiro válido, para o parâmetro da estrutura da matriz do problema da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="6dfc4-199">Se você quiser receber informações sobre erros, passe um ponteiro de estrutura **SPropProblemArray** válido no parâmetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="6dfc4-200">Quando **CopyTo** retornar S_OK, verifique possíveis erros com propriedades individuais na estrutura.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="6dfc4-201">Quando **CopyTo** retorna um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="6dfc4-202">Em vez disso, chame [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) para recuperar informações de erro detalhadas.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="6dfc4-203">Se **CopyTo** retornar S_OK, libere a estrutura **SPropProblemArray** retornada chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="6dfc4-204">Se você copiar propriedades que são exclusivas para o tipo de objeto de origem, você deve garantir que o objeto de destino seja do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="6dfc4-205">**CopyTo** não impede que você associe propriedades que normalmente pertencem a um tipo de objeto com outro tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="6dfc4-206">Você pode copiar propriedades que fazem sentido para o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="6dfc4-207">Por exemplo, você não deve copiar as propriedades de mensagem para um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="6dfc4-208">Para garantir que você copie entre objetos do mesmo tipo, verifique se o objeto de origem e destino são do mesmo tipo, comparando ponteiros de objeto ou chamando [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="6dfc4-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="6dfc4-209">Defina o identificador de interface apontado por _lpInterface_ para a interface padrão do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="6dfc4-210">Além disso, certifique-se de que o tipo de objeto ou a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) seja a mesma dos dois objetos.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="6dfc4-211">Por exemplo, se você copiar de uma mensagem, defina _lpInterface_ como IID_IMessage e o **PR_OBJECT_TYPE** para ambos os objetos como MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="6dfc4-212">Se um ponteiro inválido for passado no parâmetro _lpDestObj_ , os resultados serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="6dfc4-213">Excluir propriedades em uma chamada **CopyTo** pode ser útil.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="6dfc4-214">Por exemplo, alguns objetos têm propriedades específicas para uma única instância do objeto, como data e hora da entrega da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="6dfc4-215">Para evitar a cópia do tempo de entrega de uma mensagem quando você copia a mensagem para uma pasta diferente, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) na marca de propriedade Exclude array.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="6dfc4-216">Para excluir a lista de destinatários de uma mensagem, adicione a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) à matriz Exclude.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="6dfc4-217">Para excluir os anexos de uma mensagem, adicione a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) à matriz.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="6dfc4-218">Da mesma forma, evite a cópia ou a movimentação de uma pasta ou hierarquia de um contêiner de catálogo de endereços ou uma tabela de conteúdo incluindo **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na marca Property Exclude array.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="6dfc4-219">Para excluir propriedades da operação de cópia ou movimentação, inclua suas marcas de propriedade no parâmetro _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="6dfc4-220">Se você passar os resultados da macro **PROP_TAG** para criar uma marca de propriedade a partir de um identificador específico na matriz de marca de propriedade, todas as propriedades com esse identificador serão excluídas.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="6dfc4-221">Por exemplo, a seguinte entrada na matriz de marca de propriedade faz com que todas as propriedades com um identificador de 0x8002 sejam excluídas, independentemente do tipo:</span><span class="sxs-lookup"><span data-stu-id="6dfc4-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="6dfc4-222">A marca de propriedade **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não pode ser incluída na matriz _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="6dfc4-223">A utilidade do recurso **CopyTo** para excluir interfaces talvez não seja tão óbvia quanto a utilidade de excluir propriedades.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="6dfc4-224">Você pode excluir uma interface ao copiar para um objeto que não tenha conhecimento de um grupo de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="6dfc4-225">Por exemplo, se você copiar propriedades de uma pasta para um anexo, as únicas propriedades com as quais o anexo pode trabalhar são as propriedades genéricas disponíveis em qualquer implementação do [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="6dfc4-226">Ao excluir [IMAPIFolder](imapifolderimapicontainer.md) da operação de cópia, o anexo não receberá nenhuma das propriedades de pasta mais específicas.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="6dfc4-227">Quando você usa o parâmetro _rgiidExclude_ para excluir uma interface, ele também exclui todas as interfaces derivadas dessa interface.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="6dfc4-228">Por exemplo, a exclusão de [IMAPIContainer](imapicontainerimapiprop.md) faz com que as pastas ou contêineres do catálogo de endereços sejam excluídos, dependendo do tipo de provedor.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="6dfc4-229">Não exclua **IMAPIProp** ou [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , pois muitas interfaces derivam deles.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-229">Do not exclude **IMAPIProp** or [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="6dfc4-230">Ignore os erros de MAPI_E_COMPUTED retornados na estrutura **SPropProblemArray** no parâmetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6dfc4-231">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6dfc4-231">MFCMAPI reference</span></span>

<span data-ttu-id="6dfc4-232">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6dfc4-233">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-233">**File**</span></span>|<span data-ttu-id="6dfc4-234">**Função**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-234">**Function**</span></span>|<span data-ttu-id="6dfc4-235">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6dfc4-236">Arquivo. cpp</span><span class="sxs-lookup"><span data-stu-id="6dfc4-236">File.cpp</span></span>  <br/> |<span data-ttu-id="6dfc4-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="6dfc4-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="6dfc4-238">MFCMAPI usa o método **IMAPIProp:: CopyTo** para copiar as propriedades de um arquivo. msg para um objeto [IMAPIMessageSite](imapimessagesiteiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="6dfc4-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="6dfc4-239">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="6dfc4-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="6dfc4-240">CFolderDlg:: HandlePaste</span><span class="sxs-lookup"><span data-stu-id="6dfc4-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="6dfc4-241">MFCMAPI usa o método **IMAPIProp:: CopyTo** para copiar as propriedades de uma mensagem de origem para uma mensagem de destino durante uma operação de colagem.</span><span class="sxs-lookup"><span data-stu-id="6dfc4-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6dfc4-242">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dfc4-242">See also</span></span>



[<span data-ttu-id="6dfc4-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="6dfc4-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="6dfc4-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6dfc4-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="6dfc4-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6dfc4-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="6dfc4-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6dfc4-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="6dfc4-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="6dfc4-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="6dfc4-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="6dfc4-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="6dfc4-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6dfc4-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6dfc4-250">Propriedade canônica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="6dfc4-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="6dfc4-251">Propriedade canônica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="6dfc4-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="6dfc4-252">Propriedade canônica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="6dfc4-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="6dfc4-253">Propriedade canônica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="6dfc4-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="6dfc4-254">Propriedade canônica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="6dfc4-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="6dfc4-255">Propriedade canônica PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="6dfc4-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="6dfc4-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="6dfc4-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="6dfc4-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="6dfc4-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="6dfc4-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6dfc4-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="6dfc4-259">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="6dfc4-259">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

