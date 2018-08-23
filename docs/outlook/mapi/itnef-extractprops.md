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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0765e46a6f0545682b16e484d08d296ea13e2136
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571343"
---
# <a name="itnefextractprops"></a><span data-ttu-id="ccf8f-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="ccf8f-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="ccf8f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccf8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccf8f-105">Extrai as propriedades de um encapsulamento TNEF.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="ccf8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccf8f-106">Parameters</span></span>

 <span data-ttu-id="ccf8f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ccf8f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ccf8f-108">[in] Uma bitmask dos sinalizadores que controla como as propriedades são decodificadas.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="ccf8f-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ccf8f-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ccf8f-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="ccf8f-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="ccf8f-111">Decodifica todas as propriedades não especificadas no parâmetro _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="ccf8f-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="ccf8f-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="ccf8f-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="ccf8f-113">Decodifica todas as propriedades especificadas na _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="ccf8f-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="ccf8f-114">_lpPropList_</span></span>
  
> <span data-ttu-id="ccf8f-115">[in] Um ponteiro para a lista de propriedades para incluir ou excluir a partir da operação de decodificação.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="ccf8f-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="ccf8f-116">_lpProblems_</span></span>
  
> <span data-ttu-id="ccf8f-117">[out] Um ponteiro para um ponteiro para uma estrutura de [STnefProblemArray](stnefproblemarray.md) retornado.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="ccf8f-118">A estrutura **STnefProblemArray** indica quais propriedades, se houver, não foram codificadas adequadamente.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="ccf8f-119">Se NULL é passada no parâmetro _lpProblems_ , nenhuma matriz de problema da propriedade será retornado.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ccf8f-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ccf8f-120">Return value</span></span>

<span data-ttu-id="ccf8f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccf8f-121">S_OK</span></span> 
  
> <span data-ttu-id="ccf8f-122">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="ccf8f-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="ccf8f-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="ccf8f-124">Sendo decodificados em um fluxo de dados estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ccf8f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccf8f-125">Remarks</span></span>

<span data-ttu-id="ccf8f-126">Provedores de transporte, provedores de armazenamento de mensagem e gateways chamar o método **ITnef::ExtractProps** para extrair (isto é, decodificar) propriedades a partir do encapsulamento de uma mensagem ou um anexo que foi passado para a função [OpenTnefStream](opentnefstream.md) .</span><span class="sxs-lookup"><span data-stu-id="ccf8f-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="ccf8f-127">O provedor ou gateway de chamada pode especificar uma lista de propriedades para decodificar.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="ccf8f-128">Provedores e gateways também podem usar **ExtractProps** para fornecer informações sobre qualquer ação especial para anexos.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="ccf8f-129">**ExtractProps** preenche a mensagem original passada para **OpenTnefStream** com as propriedades decodificadas.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="ccf8f-130">As chamadas subsequentes **ExtractProps** voltar à mensagem e extraia a nova lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="ccf8f-131">Ao contrário do método [ITnef::AddProps](itnef-addprops.md) , qual filas solicitada ações até que o método **ITnef::Finish** é chamado, o método **ExtractProps** decodifica as propriedades encapsuladas imediatamente quando for chamado.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="ccf8f-132">Por esse motivo, a mensagem de destino para decodificação encapsulamento deve ser relativamente vazia.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="ccf8f-133">As propriedades existentes na mensagem de destino são substituídas pelas propriedades encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="ccf8f-134">**ExtractProps** é suportado somente para os objetos que são abertos com o sinalizador TNEF_DECODE para a função **OpenTnefStream** ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="ccf8f-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="ccf8f-135">A implementação de TNEF relata problemas de codificação de fluxo TNEF sem interromper o processamento de **ExtractProps** .</span><span class="sxs-lookup"><span data-stu-id="ccf8f-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="ccf8f-136">A estrutura de [STnefProblemArray](stnefproblemarray.md) retornada em _lpProblems_ indica quais atributos TNEF ou propriedades MAPI, se houver, não pôde ser processadas.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="ccf8f-137">O valor retornado no membro **scode** um das estruturas **STnefProblem** contidos no **STnefProblemArray** indica que o problema específico.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="ccf8f-138">O provedor ou o gateway pode trabalhar no pressuposto de que todas as propriedades ou os atributos para os quais **ExtractProps** não retorna um relatório de problema foram processados com êxito.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ccf8f-139">Se uma propriedade no bloco de encapsulamento MAPI não pode ser processada e deixa o fluxo confiável durante a decodificação de um stream TNEF, decodificação do bloco de encapsulamento é interrompido e for informado um problema.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="ccf8f-140">A matriz de problema para esse tipo de problema contém L 0 para o membro **ulPropTag** , `attMAPIProps` ou `attAttachment` para o membro **ulAttribute** e MAPI_E_UNABLE_TO_COMPLETE para o membro **scode** .</span><span class="sxs-lookup"><span data-stu-id="ccf8f-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="ccf8f-141">Observe que a decodificação do fluxo não é interrompidas, apenas a decodificação do bloco de encapsulamento de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="ccf8f-142">O fluxo de decodificação continua com o próximo bloco de atributo.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="ccf8f-143">Se um provedor ou gateway não funciona com matrizes de problema, ele pode passar NULL em _lppProblems_; Nesse caso, a matriz nenhum problema é retornado.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="ccf8f-144">O valor retornado em _lpProblems_ é válido somente se a chamada Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="ccf8f-145">Quando for retornado S_OK, o provedor ou gateway deve verificar os valores retornados na estrutura **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="ccf8f-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="ccf8f-146">Se ocorrer um erro na chamada, a estrutura de **STnefProblemArray** não for preenchida e o gateway ou provedor de chamada não deve usar ou livre a estrutura.</span><span class="sxs-lookup"><span data-stu-id="ccf8f-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="ccf8f-147">Se nenhum erro ocorrer na chamada, o provedor de chamada ou gateway deve liberar a memória para a estrutura **STnefProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ccf8f-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ccf8f-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccf8f-148">See also</span></span>



[<span data-ttu-id="ccf8f-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="ccf8f-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="ccf8f-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="ccf8f-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="ccf8f-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="ccf8f-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="ccf8f-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ccf8f-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ccf8f-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="ccf8f-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="ccf8f-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="ccf8f-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="ccf8f-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="ccf8f-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="ccf8f-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ccf8f-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

