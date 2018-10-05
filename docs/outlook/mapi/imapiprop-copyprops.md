---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398399"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="b1067-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="b1067-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="b1067-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1067-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1067-105">Cópias ou movimentações de propriedades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="b1067-105">Copies or moves selected properties.</span></span> 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="b1067-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1067-106">Parameters</span></span>

 <span data-ttu-id="b1067-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="b1067-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="b1067-108">[in] Um ponteiro para uma matriz de marca de propriedade que especifica as propriedades para copiar ou mover.</span><span class="sxs-lookup"><span data-stu-id="b1067-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="b1067-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não podem ser incluídos na matriz.</span><span class="sxs-lookup"><span data-stu-id="b1067-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="b1067-110">O parâmetro _lpIncludeProps_ não pode ser **Nulo**.</span><span class="sxs-lookup"><span data-stu-id="b1067-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="b1067-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b1067-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="b1067-112">[in] Um identificador para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="b1067-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="b1067-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="b1067-113">_lpProgress_</span></span>
  
> <span data-ttu-id="b1067-114">[in] Um ponteiro para uma implementação de um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="b1067-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="b1067-115">Se **Nulo** é passado no parâmetro _lpProgress_ , o indicador de progresso é exibido, usando a implementação de MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1067-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="b1067-116">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b1067-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b1067-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b1067-117">_lpInterface_</span></span>
  
> <span data-ttu-id="b1067-118">[in] Um ponteiro para o identificador de interface (IID) que representa a interface que deve ser usada para acessar o objeto apontado pelo parâmetro _lpDestObj_ .</span><span class="sxs-lookup"><span data-stu-id="b1067-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="b1067-119">O parâmetro _lpInterface_ não deve ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="b1067-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="b1067-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="b1067-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="b1067-121">[in] Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="b1067-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="b1067-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1067-122">_ulFlags_</span></span>
  
> <span data-ttu-id="b1067-123">[in] Uma bitmask dos sinalizadores que controla a operação de cópia ou movimentação.</span><span class="sxs-lookup"><span data-stu-id="b1067-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="b1067-124">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="b1067-124">The following flags can be set:</span></span>
    
<span data-ttu-id="b1067-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="b1067-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="b1067-126">Se **CopyProps** chama o método [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) para lidar com a cópia ou a operação de movimentação, ele em vez disso, deve retornar imediatamente com o valor de erro MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="b1067-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="b1067-127">O sinalizador MAPI_DECLINE_OK é definido por MAPI para limitar a recursão.</span><span class="sxs-lookup"><span data-stu-id="b1067-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="b1067-128">Os clientes não definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="b1067-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="b1067-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b1067-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b1067-130">Exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="b1067-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="b1067-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="b1067-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="b1067-132">**CopyProps** deve realizar uma operação de movimentação, em vez de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="b1067-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="b1067-133">Quando esse sinalizador não estiver definida, **CopyProps** executa uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="b1067-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="b1067-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="b1067-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="b1067-135">Propriedades existentes no objeto de destino não devem ser substituídas.</span><span class="sxs-lookup"><span data-stu-id="b1067-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="b1067-136">Quando esse sinalizador não estiver definida, **CopyProps** substitui as propriedades existentes.</span><span class="sxs-lookup"><span data-stu-id="b1067-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="b1067-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="b1067-137">_lppProblems_</span></span>
  
> <span data-ttu-id="b1067-138">[além, out] Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; Caso contrário, **null**, indicando que não há nenhuma necessidade de informações de erro.</span><span class="sxs-lookup"><span data-stu-id="b1067-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="b1067-139">Se _lppProblems_ for um ponteiro válido na entrada, **CopyProps** retorna informações detalhadas sobre erros no copiando uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="b1067-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b1067-140">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b1067-140">Return value</span></span>

<span data-ttu-id="b1067-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1067-141">S_OK</span></span> 
  
> <span data-ttu-id="b1067-142">Propriedades foi copiadas ou movidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="b1067-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="b1067-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="b1067-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="b1067-144">Não é possível copiar um Subobjeto porque já existe um Subobjeto com o mesmo nome de exibição, definido pela propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), no objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b1067-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="b1067-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="b1067-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="b1067-146">O provedor de serviços não implementa a operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="b1067-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="b1067-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="b1067-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="b1067-148">O objeto de origem executando a operação de cópia ou movimentação direta ou indiretamente contém o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b1067-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="b1067-149">Trabalho significativo pode ter sido executado antes que esta condição foi descoberta, para que os objetos de origem e destino podem ser modificados parcialmente.</span><span class="sxs-lookup"><span data-stu-id="b1067-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="b1067-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="b1067-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="b1067-151">Não há suporte para a interface identificada pelo parâmetro _lpInterface_ pelo objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b1067-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="b1067-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b1067-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b1067-153">Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="b1067-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="b1067-154">Esse erro será retornado se o objeto de destino é o mesmo que o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="b1067-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="b1067-155">Os seguintes valores podem ser retornados na estrutura de **SPropProblemArray** , mas não como valores de retorno para **CopyProps**.</span><span class="sxs-lookup"><span data-stu-id="b1067-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="b1067-156">Esses erros se aplicam a uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="b1067-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="b1067-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b1067-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b1067-158">Tanto o sinalizador MAPI_UNICODE foi definido e **CopyProps** não oferece suporte a Unicode, ou MAPI_UNICODE não foi definido e **CopyProps** suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="b1067-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="b1067-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="b1067-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="b1067-160">A propriedade não pode ser modificada pelo chamador porque ele é uma propriedade somente leitura, computada pelo proprietário do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b1067-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="b1067-161">Esse erro não é grave; o chamador deve permitir que a operação de cópia continuar.</span><span class="sxs-lookup"><span data-stu-id="b1067-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="b1067-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="b1067-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="b1067-163">O tipo de propriedade é inválido.</span><span class="sxs-lookup"><span data-stu-id="b1067-163">The property type is invalid.</span></span>
    
<span data-ttu-id="b1067-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="b1067-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="b1067-165">O tipo de propriedade não é o tipo esperado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="b1067-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1067-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1067-166">Remarks</span></span>

<span data-ttu-id="b1067-167">O método **IMAPIProp::CopyProps** copia ou move propriedades selecionadas do objeto atual para um objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b1067-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="b1067-168">**CopyProps** é usado principalmente para responder e encaminhar mensagens, onde apenas algumas das propriedades da mensagem original com a resposta de viagem ou encaminhadas a cópia.</span><span class="sxs-lookup"><span data-stu-id="b1067-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="b1067-169">Qualquer subobjetos no objeto de origem automaticamente estão incluídos na operação e copiados ou movidos na íntegra, independentemente do uso das propriedades indicados pela estrutura [SPropTagArray](sproptagarray.md) .</span><span class="sxs-lookup"><span data-stu-id="b1067-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="b1067-170">Por padrão, **CopyProps** substitui quaisquer propriedades no objeto de destino que corresponde às propriedades do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="b1067-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="b1067-171">Se qualquer uma das propriedades movidas ou copiadas já existir no objeto de destino, as propriedades existentes são sobrescritas por novas propriedades, exceto se o sinalizador MAPI_NOREPLACE estiver definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b1067-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="b1067-172">As informações existentes no objeto de destino que não será substituído são permanecem inalteradas.</span><span class="sxs-lookup"><span data-stu-id="b1067-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b1067-173">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="b1067-173">Notes to implementers</span></span>

<span data-ttu-id="b1067-174">Você pode fornecer uma implementação total de **CopyProps** ou baseiam-se na implementação de MAPI fornece em seu objeto de suporte.</span><span class="sxs-lookup"><span data-stu-id="b1067-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="b1067-175">Se você quiser usar a implementação de MAPI, chame o método de **IMAPISupport::DoCopyProps** .</span><span class="sxs-lookup"><span data-stu-id="b1067-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="b1067-176">No entanto, se você delega o processamento para **DoCopyProps** e você é passadas o sinalizador MAPI_DECLINE_OK, evitar a chamada de suporte e retornar MAPI_E_DECLINE_COPY em vez disso.</span><span class="sxs-lookup"><span data-stu-id="b1067-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="b1067-177">Você será chamado com esse sinalizador por MAPI para evitar a recursão possível que pode ocorrer quando você copia pastas.</span><span class="sxs-lookup"><span data-stu-id="b1067-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="b1067-178">Como a operação de cópia pode ser demorada, você deve exibir um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="b1067-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="b1067-179">Use a implementação de [IMAPIProgress](imapiprogressiunknown.md) que é passada no parâmetro _lpProgress_ , se houver uma.</span><span class="sxs-lookup"><span data-stu-id="b1067-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="b1067-180">Se _lpProgress_ for **nula**, chame o método de [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para usar a implementação de MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1067-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b1067-181">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="b1067-181">Notes to callers</span></span>

<span data-ttu-id="b1067-182">Não definir o sinalizador MAPI_DECLINE_OK; ele é usado pelo MAPI em suas chamadas para a mensagem implementações de **CopyProps** do provedor de repositório.</span><span class="sxs-lookup"><span data-stu-id="b1067-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="b1067-183">Porque as operações de movimentação e cópia podem levar o tempo, é recomendável solicitar a exibição de um indicador de progresso, definindo o sinalizador MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="b1067-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="b1067-184">Você pode definir o parâmetro _lpProgress_ à sua implementação do **IMAPIProgress**, se você tiver um, ou como **Nulo**.</span><span class="sxs-lookup"><span data-stu-id="b1067-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="b1067-185">Se _lpProgress_ for **nula**, **CopyProps** usará o indicador de progresso padrão fornecido pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1067-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="b1067-186">Você pode suprimir a exibição de um indicador de progresso, não definindo o sinalizador MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="b1067-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="b1067-187">**CopyProps** ignorará os parâmetros _ulUIParam_ e _lpProgress_ e evitar exibindo o indicador.</span><span class="sxs-lookup"><span data-stu-id="b1067-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="b1067-188">**CopyProps** possível denunciar global e individual ou erros que ocorrem com uma ou mais das propriedades.</span><span class="sxs-lookup"><span data-stu-id="b1067-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="b1067-189">Esses erros individuais são colocados em uma estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="b1067-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="b1067-190">Você pode suprimir relatório no nível de propriedade passando **Nulo**, em vez de um ponteiro válido, para o parâmetro de estrutura de matriz de problema de propriedade de erros.</span><span class="sxs-lookup"><span data-stu-id="b1067-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="b1067-191">Se você desejar receber informações sobre erros, passe um ponteiro de estrutura de **SPropProblemArray** válido no parâmetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="b1067-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="b1067-192">Quando **CopyProps** Retorna S_OK, verifique se há erros possíveis com as propriedades individuais na estrutura.</span><span class="sxs-lookup"><span data-stu-id="b1067-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="b1067-193">Quando **CopyProps** retornará um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="b1067-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="b1067-194">Em vez disso, chame o método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar informações de erro detalhadas.</span><span class="sxs-lookup"><span data-stu-id="b1067-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="b1067-195">Se **CopyProps** Retorna S_OK, livre a estrutura de **SPropProblemArray** retornada ao chamar a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b1067-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="b1067-196">Se você estiver copiando propriedades que são exclusivas para o tipo de objeto de origem, você deve garantir que o objeto de destino é do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="b1067-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="b1067-197">**CopyProps** não impede que você associar propriedades que geralmente pertencem a um tipo de objeto com outro tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="b1067-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="b1067-198">Cabe a você copie as propriedades que fazem sentido para o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b1067-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="b1067-199">Por exemplo, você não deve copiar propriedades da mensagem para um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b1067-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="b1067-200">Para garantir que você está copiando entre os objetos do mesmo tipo, verifique se o objeto de origem e destino são do mesmo tipo, por comparando ponteiros de objeto ou chamar o método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b1067-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="b1067-201">Defina o identificador de interface apontado pela _lpInterface_ para a interface padrão para o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="b1067-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="b1067-202">Além disso, certifique-se de que o tipo de objeto ou a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) é o mesmo para os dois objetos.</span><span class="sxs-lookup"><span data-stu-id="b1067-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="b1067-203">Por exemplo, se você está copiando uma mensagem, defina _lpInterface_ IID_IMessage e o **PR_OBJECT_TYPE** para ambos os objetos para MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="b1067-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="b1067-204">Se um ponteiro inválido é passado no parâmetro _lpDestObj_ , os resultados serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="b1067-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="b1067-205">Para copiar a lista de destinatários da mensagem, chame o método **CopyProps** da mensagem e incluir a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) na matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b1067-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="b1067-206">Para copiar os anexos da mensagem, inclua a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b1067-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="b1067-207">Para copiar uma pasta, a hierarquia do contêiner de catálogo de endereços ou a tabela de conteúdo, incluem o **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou propriedades **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) o matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b1067-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="b1067-208">Para incluir a tabela de conteúdo associado de uma pasta, inclua a propriedade **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) na matriz.</span><span class="sxs-lookup"><span data-stu-id="b1067-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b1067-209">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b1067-209">MFCMAPI reference</span></span>

<span data-ttu-id="b1067-210">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1067-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b1067-211">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b1067-211">**File**</span></span>|<span data-ttu-id="b1067-212">**Função**</span><span class="sxs-lookup"><span data-stu-id="b1067-212">**Function**</span></span>|<span data-ttu-id="b1067-213">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="b1067-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b1067-214">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b1067-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b1067-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="b1067-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="b1067-216">MFCMAPI usa o método **IMAPIProp::CopyProps** para copiar propriedades nomeadas de uma mensagem para outro.</span><span class="sxs-lookup"><span data-stu-id="b1067-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="b1067-217">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="b1067-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b1067-218">CSingleMAPIPropListCtrl::OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="b1067-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="b1067-219">MFCMAPI usa o método **IMAPIProp::CopyProps** para colar uma propriedade que foi copiada de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="b1067-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1067-220">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1067-220">See also</span></span>



[<span data-ttu-id="b1067-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="b1067-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="b1067-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1067-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="b1067-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="b1067-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="b1067-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b1067-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="b1067-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="b1067-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="b1067-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="b1067-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="b1067-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b1067-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b1067-228">Propriedade canônica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="b1067-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="b1067-229">Propriedade canônica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="b1067-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="b1067-230">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="b1067-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="b1067-231">Propriedade canônica PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="b1067-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="b1067-232">Propriedade canônica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="b1067-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="b1067-233">Propriedade canônica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="b1067-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="b1067-234">Propriedade canônica PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="b1067-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="b1067-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="b1067-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="b1067-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b1067-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="b1067-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1067-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="b1067-238">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b1067-238">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

