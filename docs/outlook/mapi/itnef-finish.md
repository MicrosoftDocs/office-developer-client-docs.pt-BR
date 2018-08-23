---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aff805f7868ec0c2adc55ece94c45b76368ba6eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583761"
---
# <a name="itneffinish"></a><span data-ttu-id="4c97d-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="4c97d-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="4c97d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c97d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c97d-105">Tiver terminado de processamento de todas as operações de Transport-Neutral Encapsulation Format (TNEF) que estão enfileiradas e em espera.</span><span class="sxs-lookup"><span data-stu-id="4c97d-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="4c97d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c97d-106">Parameters</span></span>

 <span data-ttu-id="4c97d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c97d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4c97d-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4c97d-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4c97d-109">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="4c97d-109">_lpKey_</span></span>
  
> <span data-ttu-id="4c97d-110">[out] Um ponteiro para a propriedade de chave **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo.</span><span class="sxs-lookup"><span data-stu-id="4c97d-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="4c97d-111">O objeto de encapsulamento TNEF usa essa chave para coincidir com um anexo para sua tag de posicionamento de anexo em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="4c97d-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="4c97d-112">Essa chave deve ser exclusivo para cada anexo.</span><span class="sxs-lookup"><span data-stu-id="4c97d-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="4c97d-113">_lpProblem_</span><span class="sxs-lookup"><span data-stu-id="4c97d-113">_lpProblem_</span></span>
  
> <span data-ttu-id="4c97d-114">[out] Um ponteiro para um ponteiro para uma estrutura de [STnefProblemArray](stnefproblemarray.md) retornado.</span><span class="sxs-lookup"><span data-stu-id="4c97d-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="4c97d-115">A estrutura **STnefProblemArray** indica quais propriedades, se houver, não foram codificadas adequadamente.</span><span class="sxs-lookup"><span data-stu-id="4c97d-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="4c97d-116">Se NULL é passada no parâmetro _lpProblem_ , nenhuma matriz de problema da propriedade será retornado.</span><span class="sxs-lookup"><span data-stu-id="4c97d-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4c97d-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4c97d-117">Return value</span></span>

<span data-ttu-id="4c97d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c97d-118">S_OK</span></span> 
  
> <span data-ttu-id="4c97d-119">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="4c97d-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c97d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c97d-120">Remarks</span></span>

<span data-ttu-id="4c97d-121">Chamada de gateways, o método **ITnef::Finish** para executar a codificação de todas as propriedades para a qual codificação foi solicitado em chamadas para os métodos [ITnef::AddProps](itnef-addprops.md) e [ITnef::SetProps](itnef-setprops.md) , provedores de armazenamento de mensagem e provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="4c97d-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="4c97d-122">Se o objeto TNEF foi aberto com o sinalizador TNEF_ENCODE para a função [OpenTnefStreamEx](opentnefstreamex.md) ou [OpenTnefStream](opentnefstream.md) , o método **término** codifica as propriedades solicitadas no fluxo encapsulamento passado para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="4c97d-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="4c97d-123">Se o objeto TNEF foi aberto com o sinalizador TNEF_DECODE, o método **término** decodifica as propriedades do fluxo de TNEF e grava-os de volta à mensagem que pertencem.</span><span class="sxs-lookup"><span data-stu-id="4c97d-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="4c97d-124">Após a chamada de **término** , o ponteiro para o fluxo de encapsulamento aponta para o final dos dados TNEF.</span><span class="sxs-lookup"><span data-stu-id="4c97d-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="4c97d-125">Se o provedor ou o gateway precisa usar os dados de fluxo TNEF após o **término** de chamada, ele deverá redefinir o ponteiro do fluxo ao início dos dados stream TNEF.</span><span class="sxs-lookup"><span data-stu-id="4c97d-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="4c97d-126">A implementação de TNEF relata problemas de codificação de fluxo TNEF sem interromper o processamento de **término** .</span><span class="sxs-lookup"><span data-stu-id="4c97d-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="4c97d-127">A estrutura de [STnefProblemArray](stnefproblemarray.md) retornada no parâmetro _lpProblem_ indica quais atributos TNEF ou propriedades MAPI, se houver, não pôde ser processadas.</span><span class="sxs-lookup"><span data-stu-id="4c97d-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="4c97d-128">O valor retornado no membro **scode** um das estruturas **STnefProblem** contidos no **STnefProblemArray** indica que o problema específico.</span><span class="sxs-lookup"><span data-stu-id="4c97d-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="4c97d-129">O provedor ou o gateway pode trabalhar no pressuposto de que todas as propriedades ou os atributos para os quais a **Concluir** , não retorna um relatório de problema foram processados com êxito.</span><span class="sxs-lookup"><span data-stu-id="4c97d-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="4c97d-130">Se um provedor ou gateway não funciona com matrizes de problema, ele pode passar NULL em _lpProblem_; Nesse caso, a matriz nenhum problema é retornado.</span><span class="sxs-lookup"><span data-stu-id="4c97d-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="4c97d-131">O valor retornado em _lpProblem_ é válido somente se a chamada Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="4c97d-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="4c97d-132">Quando for retornado S_OK, o provedor ou gateway deve verificar os valores retornados na estrutura **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="4c97d-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="4c97d-133">Se ocorrer um erro na chamada, a estrutura de **STnefProblemArray** não for preenchida e o gateway ou provedor de chamada não deve usar ou livre a estrutura.</span><span class="sxs-lookup"><span data-stu-id="4c97d-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="4c97d-134">Se nenhum erro ocorrer na chamada, o provedor de chamada ou gateway deve liberar a memória para o **STnefProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="4c97d-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4c97d-135">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4c97d-135">MFCMAPI reference</span></span>

<span data-ttu-id="4c97d-136">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c97d-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4c97d-137">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="4c97d-137">**File**</span></span>|<span data-ttu-id="4c97d-138">**Function**</span><span class="sxs-lookup"><span data-stu-id="4c97d-138">**Function**</span></span>|<span data-ttu-id="4c97d-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="4c97d-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4c97d-140">CPP</span><span class="sxs-lookup"><span data-stu-id="4c97d-140">File.cpp</span></span>  <br/> |<span data-ttu-id="4c97d-141">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="4c97d-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="4c97d-142">MFCMAPI usa o método **ITnef::Finish** para concluir o processamento do novo fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="4c97d-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c97d-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c97d-143">See also</span></span>



[<span data-ttu-id="4c97d-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="4c97d-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="4c97d-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4c97d-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4c97d-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="4c97d-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="4c97d-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="4c97d-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="4c97d-148">Propriedade canônica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="4c97d-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="4c97d-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="4c97d-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="4c97d-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c97d-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="4c97d-151">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="4c97d-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

