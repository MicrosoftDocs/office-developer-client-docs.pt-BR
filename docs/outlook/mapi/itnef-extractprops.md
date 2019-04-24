---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348647"
---
# <a name="itnefextractprops"></a><span data-ttu-id="8e658-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="8e658-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="8e658-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e658-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e658-105">Extrai as propriedades de um encapsulamento TNEF.</span><span class="sxs-lookup"><span data-stu-id="8e658-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="8e658-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e658-106">Parameters</span></span>

 <span data-ttu-id="8e658-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e658-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8e658-108">no Uma bitmask de sinalizadores que controla como as propriedades são decodificadas.</span><span class="sxs-lookup"><span data-stu-id="8e658-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="8e658-109">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="8e658-109">The following flags can be set:</span></span>
    
<span data-ttu-id="8e658-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="8e658-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="8e658-111">Decodifica todas as propriedades não especificadas no parâmetro _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="8e658-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="8e658-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="8e658-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="8e658-113">Decodifica todas as propriedades especificadas em _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="8e658-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="8e658-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="8e658-114">_lpPropList_</span></span>
  
> <span data-ttu-id="8e658-115">no Um ponteiro para a lista de propriedades para incluir ou excluir da operação de decodificação.</span><span class="sxs-lookup"><span data-stu-id="8e658-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="8e658-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="8e658-116">_lpProblems_</span></span>
  
> <span data-ttu-id="8e658-117">bota Um ponteiro para um ponteiro para uma estrutura [STnefProblemArray](stnefproblemarray.md) retornada.</span><span class="sxs-lookup"><span data-stu-id="8e658-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="8e658-118">A estrutura **STnefProblemArray** indica quais propriedades, se houver, não foram codificadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="8e658-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="8e658-119">Se NULL for passado no parâmetro _lpProblems_ , nenhuma matriz de problemas de propriedade será retornada.</span><span class="sxs-lookup"><span data-stu-id="8e658-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8e658-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8e658-120">Return value</span></span>

<span data-ttu-id="8e658-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e658-121">S_OK</span></span> 
  
> <span data-ttu-id="8e658-122">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="8e658-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="8e658-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="8e658-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="8e658-124">Os dados que estão sendo decodificados em um Stream estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="8e658-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e658-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e658-125">Remarks</span></span>

<span data-ttu-id="8e658-126">Provedores de transporte, provedores de repositórios de mensagens e gateways chamam o método **ITnef:: ExtractProps** para extrair (ou seja, decodificar) Propriedades do encapsulamento de uma mensagem ou de um anexo que foi passado para a função [OpenTnefStream](opentnefstream.md) .</span><span class="sxs-lookup"><span data-stu-id="8e658-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="8e658-127">O provedor de chamadas ou o gateway pode especificar uma lista de propriedades a serem decodificadas.</span><span class="sxs-lookup"><span data-stu-id="8e658-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="8e658-128">Provedores e gateways também podem usar o **ExtractProps** para fornecer informações sobre o tratamento especial de anexos.</span><span class="sxs-lookup"><span data-stu-id="8e658-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="8e658-129">**ExtractProps** preenche a mensagem original passada para **OpenTnefStream** com as propriedades decodificadas.</span><span class="sxs-lookup"><span data-stu-id="8e658-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="8e658-130">As chamadas **ExtractProps** subsequentes voltarão para a mensagem e extrairão a nova lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e658-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="8e658-131">Ao contrário do método [ITnef::](itnef-addprops.md) addprops, que enfileira as ações solicitadas até que o método **ITnef:: Finish** seja chamado, o método **ExtractProps** decodifica as propriedades encapsuladas imediatamente quando ele é chamado.</span><span class="sxs-lookup"><span data-stu-id="8e658-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="8e658-132">Por esse motivo, a mensagem de destino para decodificação de encapsulamento deve ser relativamente vazia.</span><span class="sxs-lookup"><span data-stu-id="8e658-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="8e658-133">As propriedades existentes na mensagem de destino são sobrescritas por Propriedades encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="8e658-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="8e658-134">**ExtractProps** só tem suporte para objetos abertos com o sinalizador TNEF_DECODE para a função **OpenTnefStream** ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="8e658-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="8e658-135">A implementação TNEF relata os problemas de codificação de fluxo TNEF sem interromper o processo **ExtractProps** .</span><span class="sxs-lookup"><span data-stu-id="8e658-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="8e658-136">A estrutura [STnefProblemArray](stnefproblemarray.md) retornada no _lpProblems_ indica quais atributos TNEF ou propriedades MAPI, se houver, não puderam ser processados.</span><span class="sxs-lookup"><span data-stu-id="8e658-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="8e658-137">O valor retornado no membro **SCODE** de uma das estruturas **STnefProblem** contidas no **STnefProblemArray** indica o problema específico.</span><span class="sxs-lookup"><span data-stu-id="8e658-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="8e658-138">O provedor ou gateway pode funcionar na pressuposição de que todas as propriedades ou atributos para os quais o **ExtractProps** não retorna um relatório de problemas foram processados com êxito.</span><span class="sxs-lookup"><span data-stu-id="8e658-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8e658-139">Se uma propriedade no bloco de encapsulamento MAPI não puder ser processada e deixar o fluxo não confiável durante a decodificação de um fluxo TNEF, a decodificação do bloco de encapsulamento será interrompida e um problema será relatado.</span><span class="sxs-lookup"><span data-stu-id="8e658-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="8e658-140">A matriz problemática para esse tipo de problema contém 0L para o membro **ulPropTag** `attMAPIProps` `attAttachment` ou para o membro **ulAttribute** e MAPI_E_UNABLE_TO_COMPLETE para o membro **SCODE** .</span><span class="sxs-lookup"><span data-stu-id="8e658-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="8e658-141">Observe que a decodificação do Stream não é interrompida, apenas a decodificação do bloco de encapsulamento MAPI.</span><span class="sxs-lookup"><span data-stu-id="8e658-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="8e658-142">A decodificação de fluxo continua com o próximo bloco de atributos.</span><span class="sxs-lookup"><span data-stu-id="8e658-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="8e658-143">Se um provedor ou gateway não funcionar com matrizes problemáticas, ele poderá passar NULL no _lppProblems_; Nesse caso, nenhum conjunto de problemas é retornado.</span><span class="sxs-lookup"><span data-stu-id="8e658-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="8e658-144">O valor retornado em _lpProblems_ é válido somente se a chamada retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="8e658-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="8e658-145">Quando S_OK é retornado, o provedor ou gateway deve verificar os valores retornados na estrutura **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="8e658-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="8e658-146">Se ocorrer um erro na chamada, a estrutura **STnefProblemArray** não será preenchida e o provedor de chamadas ou o gateway não deverá usar ou liberar a estrutura.</span><span class="sxs-lookup"><span data-stu-id="8e658-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="8e658-147">Se nenhum erro ocorrer na chamada, o provedor de chamada ou o gateway deve liberar a memória para a estrutura **STnefProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8e658-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e658-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e658-148">See also</span></span>



[<span data-ttu-id="8e658-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="8e658-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="8e658-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="8e658-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="8e658-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="8e658-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="8e658-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8e658-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8e658-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="8e658-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="8e658-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="8e658-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="8e658-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="8e658-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="8e658-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e658-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

