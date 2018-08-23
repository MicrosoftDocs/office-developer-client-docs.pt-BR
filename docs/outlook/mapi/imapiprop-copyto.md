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
ms.openlocfilehash: bbc9dcf2218907b5d31ce1fc9f904e6ae1da47d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594009"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="c0626-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="c0626-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="c0626-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0626-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0626-105">Copia ou move todas as propriedades, exceto especificamente propriedades excluídas.</span><span class="sxs-lookup"><span data-stu-id="c0626-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="c0626-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0626-106">Parameters</span></span>

 <span data-ttu-id="c0626-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="c0626-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="c0626-108">[in] A contagem de interfaces a serem excluídos quando as propriedades são copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="c0626-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="c0626-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="c0626-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="c0626-110">[in] Uma matriz de identificadores de interface (IIDs) que especificam as interfaces que não devem ser usados quando informações complementares são copiadas ou movidas para o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c0626-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="c0626-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="c0626-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="c0626-112">[in] Um ponteiro para uma matriz de marca de propriedade que identifica as marcas de propriedade que devem ser excluídas da cópia ou a operação de movimentação.</span><span class="sxs-lookup"><span data-stu-id="c0626-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="c0626-113">Passando o parâmetro _lpExcludeProps_ **Nulo** indica que todas as propriedades do objeto devem ser copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="c0626-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="c0626-114">**CopyTo** retorna MAPI_E_INVALID_PARAMETER quando o membro **cValues** da estrutura [SPropProblemArray](spropproblemarray.md) apontado pela _lpExcludeProps_ estiver definido como 0.</span><span class="sxs-lookup"><span data-stu-id="c0626-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="c0626-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c0626-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="c0626-116">[in] Um identificador para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="c0626-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="c0626-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="c0626-117">_lpProgress_</span></span>
  
> <span data-ttu-id="c0626-118">[in] Um ponteiro para uma implementação do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="c0626-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="c0626-119">Se **Nulo** é passado no parâmetro _lpProgress_ , MAPI fornece a implementação de andamento.</span><span class="sxs-lookup"><span data-stu-id="c0626-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="c0626-120">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="c0626-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c0626-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c0626-121">_lpInterface_</span></span>
  
> <span data-ttu-id="c0626-122">[in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar o objeto apontado pelo parâmetro _lpDestObj_ .</span><span class="sxs-lookup"><span data-stu-id="c0626-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="c0626-123">O parâmetro _lpInterface_ não deve ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="c0626-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="c0626-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="c0626-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="c0626-125">[in] Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="c0626-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="c0626-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c0626-126">_ulFlags_</span></span>
  
> <span data-ttu-id="c0626-127">[in] Uma bitmask dos sinalizadores que controla a operação de cópia ou movimentação.</span><span class="sxs-lookup"><span data-stu-id="c0626-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="c0626-128">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c0626-128">The following flags can be set:</span></span>
    
<span data-ttu-id="c0626-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="c0626-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="c0626-130">Se **CopyTo** chama o método [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) para lidar com a cópia ou a operação de movimentação, ele em vez disso, deve retornar imediatamente com o valor de erro MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="c0626-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="c0626-131">O sinalizador MAPI_DECLINE_OK é definido por MAPI para limitar a recursão.</span><span class="sxs-lookup"><span data-stu-id="c0626-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="c0626-132">Os clientes não definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="c0626-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="c0626-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c0626-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="c0626-134">Exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="c0626-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="c0626-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="c0626-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="c0626-136">**CopyTo** deve realizar uma operação de movimentação, em vez de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="c0626-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="c0626-137">Quando esse sinalizador não estiver definida, **CopyTo** executa uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="c0626-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="c0626-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="c0626-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="c0626-139">Propriedades existentes no objeto de destino não devem ser substituídas.</span><span class="sxs-lookup"><span data-stu-id="c0626-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="c0626-140">Quando esse sinalizador não estiver definida, **CopyTo** substitui as propriedades existentes.</span><span class="sxs-lookup"><span data-stu-id="c0626-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="c0626-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="c0626-141">_lppProblems_</span></span>
  
> <span data-ttu-id="c0626-142">[além, out] Na entrada, um ponteiro para um ponteiro para uma estrutura **SPropProblemArray** ; Caso contrário, **null**, indicando sem a necessidade de informações de erro.</span><span class="sxs-lookup"><span data-stu-id="c0626-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="c0626-143">Se _lppProblems_ for um ponteiro válido na entrada, **CopyTo** retorna informações detalhadas sobre erros no copiando uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="c0626-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c0626-144">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c0626-144">Return value</span></span>

<span data-ttu-id="c0626-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0626-145">S_OK</span></span> 
  
> <span data-ttu-id="c0626-146">As propriedades foi copiadas ou movidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="c0626-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="c0626-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="c0626-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="c0626-148">Não é possível copiar um Subobjeto porque um Subobjeto com o mesmo nome para exibição — especificado pela propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) — já existe no objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c0626-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="c0626-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="c0626-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="c0626-150">O provedor de serviços não implementa a operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="c0626-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="c0626-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="c0626-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="c0626-152">O objeto de origem executando a operação de cópia ou movimentação direta ou indiretamente contém o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c0626-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="c0626-153">Trabalho significativo pode ter sido executado antes que esta condição foi descoberta, para que os objetos de origem e destino podem ser modificados parcialmente.</span><span class="sxs-lookup"><span data-stu-id="c0626-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="c0626-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="c0626-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="c0626-155">Não há suporte para a interface identificada pelo parâmetro _lpInterface_ pelo objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c0626-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="c0626-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c0626-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c0626-157">Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="c0626-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="c0626-158">Esse erro será retornado se o objeto de destino é o mesmo que o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="c0626-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="c0626-159">Os seguintes valores podem ser retornados na estrutura de **SPropProblemArray** , mas não como valores de retorno para **CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="c0626-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="c0626-160">Os seguintes erros se aplicam a uma única propriedade:</span><span class="sxs-lookup"><span data-stu-id="c0626-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="c0626-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c0626-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c0626-162">Tanto o sinalizador MAPI_UNICODE foi definido e **CopyTo** não oferece suporte a Unicode, ou MAPI_UNICODE não foi definido e **CopyTo** suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="c0626-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="c0626-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="c0626-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="c0626-164">A propriedade não pode ser modificada pelo chamador porque ele é uma propriedade somente leitura, computada pelo proprietário do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c0626-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="c0626-165">Esse erro não é grave; o chamador deve permitir que a operação de cópia continuar.</span><span class="sxs-lookup"><span data-stu-id="c0626-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="c0626-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="c0626-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="c0626-167">O tipo de propriedade é inválido.</span><span class="sxs-lookup"><span data-stu-id="c0626-167">The property type is invalid.</span></span>
    
<span data-ttu-id="c0626-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="c0626-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="c0626-169">O tipo de propriedade não é o tipo esperado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="c0626-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0626-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0626-170">Remarks</span></span>

<span data-ttu-id="c0626-171">Por padrão, o método **IMAPIProp::CopyTo** copia ou move todas as propriedades do objeto atual a um objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c0626-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="c0626-172">**CopyTo** é usado quando um objeto deve ser copiado ou movido exatamente, com todos ou a maioria de suas propriedades intactas.</span><span class="sxs-lookup"><span data-stu-id="c0626-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="c0626-173">Qualquer subobjetos no objeto de origem automaticamente estão incluídos na operação e são copiados ou movidos na íntegra.</span><span class="sxs-lookup"><span data-stu-id="c0626-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="c0626-174">Por padrão, **CopyTo** substitui quaisquer propriedades no objeto de destino que corresponde às propriedades do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="c0626-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="c0626-175">Se qualquer uma das propriedades movidas ou copiadas já existir no objeto de destino, as propriedades existentes são sobrescritas por novas propriedades, exceto se o sinalizador MAPI_NOREPLACE estiver definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="c0626-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="c0626-176">As informações existentes no objeto de destino que não será substituído são permanecem inalteradas.</span><span class="sxs-lookup"><span data-stu-id="c0626-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c0626-177">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="c0626-177">Notes to implementers</span></span>

<span data-ttu-id="c0626-178">Você pode fornecer uma implementação total de **CopyTo** ou baseiam-se na implementação de MAPI fornece em seu objeto de suporte.</span><span class="sxs-lookup"><span data-stu-id="c0626-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="c0626-179">Se você quiser usar a implementação de MAPI, chame **IMAPISupport::DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="c0626-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="c0626-180">No entanto, se você delega o processamento para **DoCopyTo** e você é passadas o sinalizador MAPI_DECLINE_OK, evitar a chamada de suporte e retornar MAPI_E_DECLINE_COPY em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c0626-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="c0626-181">MAPI chamará com esse sinalizador para evitar a recursão possível que pode acontecer quando as pastas são copiadas.</span><span class="sxs-lookup"><span data-stu-id="c0626-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="c0626-182">Como a operação de cópia pode ser demorada, você deve exibir um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="c0626-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="c0626-183">Use a implementação de [IMAPIProgress](imapiprogressiunknown.md) passada no parâmetro _lpProgress_ , se houver uma.</span><span class="sxs-lookup"><span data-stu-id="c0626-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="c0626-184">Se _lpProgress_ for **nula**, chame o método de [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para usar a implementação de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c0626-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="c0626-185">Não tente definir quaisquer propriedades conhecidas de somente leitura no objeto de destino; retorne MAPI_E_NO_ACCESS em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c0626-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="c0626-186">Os objetos de origem e destino devem usar as mesmas interfaces.</span><span class="sxs-lookup"><span data-stu-id="c0626-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="c0626-187">Retorne MAPI_E_INVALID_PARAMETER se _lpInterface_ não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="c0626-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="c0626-188">Retorne MAPI_E_INTERFACE_NOT_SUPPORTED se todas as interfaces conhecidas serão excluídas.</span><span class="sxs-lookup"><span data-stu-id="c0626-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c0626-189">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="c0626-189">Notes to callers</span></span>

<span data-ttu-id="c0626-190">Não definir o sinalizador MAPI_DECLINE_OK; MAPI usa em suas chamadas para implementações de **CopyTo** do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c0626-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="c0626-191">Porque as operações de movimentação e cópia podem demorar, você deve solicitar a exibição de um indicador de progresso, definindo o sinalizador MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="c0626-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="c0626-192">Você pode definir o parâmetro _lpProgress_ à sua implementação do **IMAPIProgress**, se você tiver um, ou como **Nulo**.</span><span class="sxs-lookup"><span data-stu-id="c0626-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="c0626-193">Se _lpProgress_ for **nula**, **CopyTo** usará o indicador de progresso padrão que fornece de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c0626-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="c0626-194">Você pode suprimir a exibição de um indicador de progresso, não definindo o sinalizador MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="c0626-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="c0626-195">**CopyTo** irá ignorar os parâmetros _ulUIParam_ e _lpProgress_ e não exibirá o indicador.</span><span class="sxs-lookup"><span data-stu-id="c0626-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="c0626-196">**CopyTo** possível denunciar global e individual ou erros que ocorrem com uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="c0626-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="c0626-197">Esses erros individuais são colocados em uma estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="c0626-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="c0626-198">Você pode suprimir relatório no nível de propriedade passando **Nulo**, em vez de um ponteiro válido, para o parâmetro de estrutura de matriz de problema de propriedade de erros.</span><span class="sxs-lookup"><span data-stu-id="c0626-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="c0626-199">Se você desejar receber informações sobre erros, passe um ponteiro de estrutura de **SPropProblemArray** válido no parâmetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="c0626-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="c0626-200">Quando **CopyTo** Retorna S_OK, verifique se há erros possíveis com as propriedades individuais na estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0626-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="c0626-201">Quando **CopyTo** retornará um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="c0626-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="c0626-202">Em vez disso, chame [IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar informações de erro detalhadas.</span><span class="sxs-lookup"><span data-stu-id="c0626-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="c0626-203">Se **CopyTo** Retorna S_OK, livre a estrutura de **SPropProblemArray** retornada ao chamar a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c0626-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="c0626-204">Se você copiar propriedades que são exclusivas para o tipo de objeto de origem, certifique-se de que o objeto de destino é do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="c0626-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="c0626-205">**CopyTo** não impede que você associar propriedades que geralmente pertencem a um tipo de objeto com outro tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="c0626-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="c0626-206">Cabe a você copie as propriedades que fazem sentido para o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c0626-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="c0626-207">Por exemplo, você não deve copiar propriedades da mensagem para um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="c0626-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="c0626-208">Para garantir que você copie entre os objetos do mesmo tipo, verifique se o objeto de origem e destino são do mesmo tipo, por comparando ponteiros de objeto ou chamar [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c0626-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="c0626-209">Defina o identificador de interface apontado pela _lpInterface_ para a interface padrão para o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="c0626-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="c0626-210">Além disso, certifique-se de que o tipo de objeto ou a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) é o mesmo para os dois objetos.</span><span class="sxs-lookup"><span data-stu-id="c0626-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="c0626-211">Por exemplo, se você copiar de uma mensagem, defina _lpInterface_ IID_IMessage e o **PR_OBJECT_TYPE** para ambos os objetos para MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="c0626-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="c0626-212">Se um ponteiro inválido é passado no parâmetro _lpDestObj_ , os resultados serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="c0626-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="c0626-213">Excluindo propriedades em uma chamada **CopyTo** pode ser útil.</span><span class="sxs-lookup"><span data-stu-id="c0626-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="c0626-214">Por exemplo, alguns objetos têm propriedades que são específicas para uma única instância do objeto, a data e hora da entrega da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c0626-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="c0626-215">Para evitar copiando o tempo de entrega da mensagem quando você copia a mensagem para uma pasta diferente, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) na matriz propriedade tag exclude.</span><span class="sxs-lookup"><span data-stu-id="c0626-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="c0626-216">Para excluir a lista de destinatários da mensagem, adicione a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) à matriz exclude.</span><span class="sxs-lookup"><span data-stu-id="c0626-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="c0626-217">Para excluir anexos da mensagem, adicione a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) à matriz.</span><span class="sxs-lookup"><span data-stu-id="c0626-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="c0626-218">Impedir da mesma forma, as cópias ou movimentações de uma pasta ou da tabela de hierarquia ou conteúdo do contêiner de catálogo de endereços, incluindo **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na propriedade tag Excluir matriz.</span><span class="sxs-lookup"><span data-stu-id="c0626-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="c0626-219">Para excluir propriedades da cópia ou operação de movimentação, inclua suas marcas de propriedade no parâmetro _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="c0626-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="c0626-220">Se você passar os resultados da macro **PROP_TAG** para criar uma marca de propriedade de um identificador específico na matriz de marca de propriedade, todas as propriedades com esse identificador não serão excluídas.</span><span class="sxs-lookup"><span data-stu-id="c0626-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="c0626-221">Por exemplo, a seguinte entrada na matriz de marca de propriedade faz com que todas as propriedades com um identificador do 0x8002 sejam excluídos, independentemente do tipo:</span><span class="sxs-lookup"><span data-stu-id="c0626-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="c0626-222">A marca de propriedade **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não pode ser incluída na matriz _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="c0626-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="c0626-223">A utilidade do recurso **CopyTo** para excluindo interfaces talvez não é tão óbvia como a utilidade dos excluindo propriedades.</span><span class="sxs-lookup"><span data-stu-id="c0626-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="c0626-224">Você pode excluir uma interface quando você copia a um objeto que não tem conhecimento de um grupo de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c0626-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="c0626-225">Por exemplo, se você copiar propriedades de uma pasta em um anexo, as únicas propriedades que o anexo pode trabalhar com são as propriedades genéricas disponíveis com qualquer implementação [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="c0626-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="c0626-226">Excluindo [IMAPIFolder](imapifolderimapicontainer.md) da operação de cópia, o anexo não receberá qualquer uma das propriedades de pasta mais específicas.</span><span class="sxs-lookup"><span data-stu-id="c0626-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="c0626-227">Quando você usa o parâmetro _rgiidExclude_ para excluir uma interface, ele também exclui todas as interfaces derivadas essa interface.</span><span class="sxs-lookup"><span data-stu-id="c0626-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="c0626-228">Por exemplo, excluir [IMAPIContainer](imapicontainerimapiprop.md) faz com que pastas ou contêineres de catálogo de endereços a serem excluídos, dependendo do tipo de provedor.</span><span class="sxs-lookup"><span data-stu-id="c0626-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="c0626-229">Não exclua **IMAPIProp** ou [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) porque tantas interfaces derivam deles.</span><span class="sxs-lookup"><span data-stu-id="c0626-229">Do not exclude **IMAPIProp** or [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="c0626-230">Ignorar MAPI_E_COMPUTED erros retornados na estrutura de **SPropProblemArray** no parâmetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="c0626-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c0626-231">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c0626-231">MFCMAPI reference</span></span>

<span data-ttu-id="c0626-232">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0626-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c0626-233">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c0626-233">**File**</span></span>|<span data-ttu-id="c0626-234">**Function**</span><span class="sxs-lookup"><span data-stu-id="c0626-234">**Function**</span></span>|<span data-ttu-id="c0626-235">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c0626-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c0626-236">CPP</span><span class="sxs-lookup"><span data-stu-id="c0626-236">File.cpp</span></span>  <br/> |<span data-ttu-id="c0626-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="c0626-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="c0626-238">MFCMAPI usa o método **IMAPIProp::CopyTo** para copiar as propriedades de um arquivo. msg a um objeto [IMAPIMessageSite](imapimessagesiteiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="c0626-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="c0626-239">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c0626-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="c0626-240">CFolderDlg::HandlePaste</span><span class="sxs-lookup"><span data-stu-id="c0626-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="c0626-241">MFCMAPI usa o método **IMAPIProp::CopyTo** para copiar propriedades de uma mensagem de origem para uma mensagem de destino durante uma operação de colar.</span><span class="sxs-lookup"><span data-stu-id="c0626-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0626-242">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0626-242">See also</span></span>



[<span data-ttu-id="c0626-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="c0626-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="c0626-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c0626-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="c0626-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0626-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="c0626-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0626-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="c0626-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="c0626-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="c0626-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="c0626-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="c0626-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c0626-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c0626-250">Propriedade canônica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="c0626-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="c0626-251">Propriedade canônica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="c0626-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="c0626-252">Propriedade canônica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="c0626-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="c0626-253">Propriedade canônica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="c0626-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="c0626-254">Propriedade canônica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="c0626-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="c0626-255">Propriedade canônica PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="c0626-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="c0626-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c0626-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="c0626-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c0626-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="c0626-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0626-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="c0626-259">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="c0626-259">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

