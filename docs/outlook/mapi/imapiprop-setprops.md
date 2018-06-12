---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 304295e3ac77fb67ec5875620a7a269377b542c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767150"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="35988-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="35988-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="35988-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35988-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35988-105">Atualiza uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="35988-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="35988-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="35988-106">Parameters</span></span>

 <span data-ttu-id="35988-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="35988-107">_cValues_</span></span>
  
> <span data-ttu-id="35988-108">[in] A contagem dos valores de propriedade apontado pelo parâmetro _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="35988-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="35988-109">O parâmetro _cValues_ não deve ser de 0.</span><span class="sxs-lookup"><span data-stu-id="35988-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="35988-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="35988-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="35988-111">[in] Um ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) que contêm valores de propriedade a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="35988-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="35988-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="35988-112">_lppProblems_</span></span>
  
> <span data-ttu-id="35988-113">[além, out] Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; Caso contrário, NULL, indicando sem a necessidade de informações de erro.</span><span class="sxs-lookup"><span data-stu-id="35988-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="35988-114">Se _lppProblems_ for um ponteiro válido na entrada, **SetProps** retorna informações detalhadas sobre erros na atualização de uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="35988-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="35988-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="35988-115">Return value</span></span>

<span data-ttu-id="35988-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="35988-116">S_OK</span></span> 
  
> <span data-ttu-id="35988-117">As propriedades foram atualizadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="35988-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="35988-118">Os seguintes valores podem ser retornados na estrutura de **SPropProblemArray** , mas não como valores de retorno para **SetProps**:</span><span class="sxs-lookup"><span data-stu-id="35988-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="35988-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="35988-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="35988-120">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="35988-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="35988-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="35988-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="35988-122">A propriedade não pode ser atualizada porque ele é somente leitura, computado pelo provedor de serviços que é responsável pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="35988-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="35988-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="35988-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="35988-124">O tipo de propriedade é inválido.</span><span class="sxs-lookup"><span data-stu-id="35988-124">The property type is invalid.</span></span>
    
<span data-ttu-id="35988-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="35988-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="35988-126">Foi feita uma tentativa para modificar um objeto somente leitura ou para acessar um objeto para o qual o usuário tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="35988-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="35988-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="35988-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="35988-128">A propriedade não pode ser atualizada porque ela é maior que o tamanho do buffer do procedimento remoto (RPC) da chamada.</span><span class="sxs-lookup"><span data-stu-id="35988-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="35988-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="35988-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="35988-130">O tipo de propriedade não é o tipo esperado pela implementação de chamada.</span><span class="sxs-lookup"><span data-stu-id="35988-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="35988-131">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="35988-131">Notes to implementers</span></span>

<span data-ttu-id="35988-132">Ignore a marca de propriedade **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) e todas as propriedades com um tipo de **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="35988-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="35988-133">Não faça alterações ou relatar problemas na estrutura de **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="35988-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="35988-134">Retorne MAPI_E_INVALID_PARAMETER se uma propriedade do tipo **PT_OBJECT** é incluída na matriz de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="35988-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="35988-135">Também retorne esse erro se uma propriedade de valores múltiplos é incluída na matriz e sua lista de membros **cValues** estiver definido como 0.</span><span class="sxs-lookup"><span data-stu-id="35988-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="35988-136">Se a chamada tiver êxito geral, mas há problemas com a definição de algumas das propriedades, volte S_OK e coloque as informações sobre os problemas na entrada da estrutura **SPropProblemArray** que o parâmetro _lppProblems_ aponta para.</span><span class="sxs-lookup"><span data-stu-id="35988-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="35988-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="35988-137">Notes to callers</span></span>

<span data-ttu-id="35988-138">Dependendo do provedor de serviço, você também poderá alterar o tipo de propriedade passando-se uma marca de propriedade que contém um tipo diferente que foi usado anteriormente com um identificador de propriedade fornecida.</span><span class="sxs-lookup"><span data-stu-id="35988-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="35988-139">Se você incluir uma marca de propriedade para uma propriedade que não é suportada pelo objeto e a implementação do **SetProps** permite a criação de novas propriedades, a propriedade é adicionada ao objeto.</span><span class="sxs-lookup"><span data-stu-id="35988-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="35988-140">Qualquer valor anterior armazenado com o identificador de propriedade que foi usado para a nova propriedade é desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="35988-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="35988-141">Observe que o valor de retorno S_OK não garante que todas as propriedades foram atualizadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="35988-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="35988-142">Alguns provedores de cache **SetProps** chamadas até que recebam uma chamada que requer intervenção do provedor, como [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="35988-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="35988-143">Portanto, é possível receber valores de erro que se relacionam com a chamada de **SetProps** com as chamadas posteriores.</span><span class="sxs-lookup"><span data-stu-id="35988-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="35988-144">Se **SetProps** Retorna S_OK, verifique a estrutura de **SPropProblemArray** apontada pela _lppProblems_ para problemas na atualização propriedades individuais.</span><span class="sxs-lookup"><span data-stu-id="35988-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="35988-145">Se **SetProps** retornará um erro, não marque a matriz de problema de propriedade.</span><span class="sxs-lookup"><span data-stu-id="35988-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="35988-146">Em vez disso, chame o método do objeto [IMAPIProp::GetLastError](imapiprop-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="35988-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="35988-147">Ao atualizar as propriedades grandes, **SetProps** pode falhar e retornar MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="35988-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="35988-148">Não há nenhum tamanho máximo para propriedades e objetos de diferentes podem ter diferentes limites.</span><span class="sxs-lookup"><span data-stu-id="35988-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="35988-149">Se você lida com as propriedades potencialmente grandes, prepare-se para chamar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com IID_IStream como o identificador de interface se **SetProps** retornar esse valor de erro.</span><span class="sxs-lookup"><span data-stu-id="35988-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="35988-150">Chame a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="35988-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="35988-151">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="35988-151">MFCMAPI reference</span></span>

<span data-ttu-id="35988-152">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="35988-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="35988-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="35988-153">**File**</span></span>|<span data-ttu-id="35988-154">**Function**</span><span class="sxs-lookup"><span data-stu-id="35988-154">**Function**</span></span>|<span data-ttu-id="35988-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="35988-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="35988-156">PropertyEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="35988-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="35988-157">CPropertyEditor::WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="35988-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="35988-158">MFCMAPI usa o método **IMAPIProp::SetProps** para gravar uma propriedade de volta a um objeto após a propriedade ter sido editada.</span><span class="sxs-lookup"><span data-stu-id="35988-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35988-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="35988-159">See also</span></span>



[<span data-ttu-id="35988-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="35988-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="35988-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="35988-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="35988-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="35988-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="35988-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="35988-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="35988-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="35988-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="35988-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="35988-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="35988-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="35988-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="35988-167">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="35988-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

