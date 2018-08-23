---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0242015680f11e5be6ae8ea9987e5778dc7cdf05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594359"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="5bb46-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="5bb46-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="5bb46-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bb46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bb46-105">Processa os componentes individuais de uma mensagem de um por vez em um fluxo de Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="5bb46-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="5bb46-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bb46-106">Parameters</span></span>

 <span data-ttu-id="5bb46-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5bb46-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5bb46-108">[in] Uma bitmask dos sinalizadores que controla o componente que vai ser concluída.</span><span class="sxs-lookup"><span data-stu-id="5bb46-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="5bb46-109">Um ou outro dos sinalizadores a seguir deve ser definido:</span><span class="sxs-lookup"><span data-stu-id="5bb46-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="5bb46-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="5bb46-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="5bb46-111">Processamento será concluído para um objeto attachment; o parâmetro _ulComponentID_ contém a propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.</span><span class="sxs-lookup"><span data-stu-id="5bb46-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="5bb46-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="5bb46-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="5bb46-113">Processamento vai ser concluído para um objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5bb46-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="5bb46-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="5bb46-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="5bb46-115">[in] 0 para indicar o processamento de uma mensagem ou a propriedade **PR_ATTACH_NUM** de um anexo a ser processado.</span><span class="sxs-lookup"><span data-stu-id="5bb46-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="5bb46-116">Se o sinalizador TNEF_COMPONENT_MESSAGE é definido no parâmetro _ulFlags_ , _ulComponentID_ deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="5bb46-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="5bb46-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="5bb46-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="5bb46-118">[in] Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém marcas de propriedade que identificam as propriedades passada no parâmetro _lpCustomProps_ .</span><span class="sxs-lookup"><span data-stu-id="5bb46-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="5bb46-119">Deve haver uma correspondência direta entre cada valor de propriedade em _lpCustomProps_ e uma marca de propriedade no parâmetro _lpCustomPropList_ .</span><span class="sxs-lookup"><span data-stu-id="5bb46-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="5bb46-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="5bb46-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="5bb46-121">[in] Um ponteiro para uma estrutura [SPropValue](spropvalue.md) que contém os valores de propriedade para as propriedades codificar.</span><span class="sxs-lookup"><span data-stu-id="5bb46-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="5bb46-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="5bb46-122">_lpPropList_</span></span>
  
> <span data-ttu-id="5bb46-123">[in] Um ponteiro para uma estrutura **SPropTagArray** que contém marcas de propriedade para as propriedades codificar.</span><span class="sxs-lookup"><span data-stu-id="5bb46-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="5bb46-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="5bb46-124">_lppProblems_</span></span>
  
> <span data-ttu-id="5bb46-125">[out] Um ponteiro para um ponteiro para uma estrutura de [STnefProblemArray](stnefproblemarray.md) retornado.</span><span class="sxs-lookup"><span data-stu-id="5bb46-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="5bb46-126">A estrutura **STnefProblemArray** indica quais propriedades, se houver, não foram codificadas adequadamente.</span><span class="sxs-lookup"><span data-stu-id="5bb46-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="5bb46-127">Se NULL é passada no parâmetro _lppProblems_ , nenhuma matriz de problema da propriedade será retornado.</span><span class="sxs-lookup"><span data-stu-id="5bb46-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5bb46-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5bb46-128">Return value</span></span>

<span data-ttu-id="5bb46-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="5bb46-129">S_OK</span></span> 
  
> <span data-ttu-id="5bb46-130">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="5bb46-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bb46-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bb46-131">Remarks</span></span>

<span data-ttu-id="5bb46-132">Transporte provedores, provedores de armazenamento de mensagem e o método **ITnef::FinishComponent** de chamada de gateways para executar o TNEF processamento para um componente, uma mensagem ou um anexo, conforme indicado pelo sinalizador definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="5bb46-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="5bb46-133">Para processamento de componente a ser habilitada, o provedor de chamada ou gateway passar o sinalizador TNEF_COMPONENT_ENCODING _ulFlags_ para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) que abriu o objeto para receber a codificação.</span><span class="sxs-lookup"><span data-stu-id="5bb46-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="5bb46-134">Passando valores nos parâmetros _lpCustomPropList_ e _lpCustomProps_ executa componente codificação equivalente à que feito pelo método [ITnef::SetProps](itnef-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="5bb46-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="5bb46-135">Passando um valor no parâmetro _lpPropList_ executa o equivalente de codificação de componente que feito pelo método [ITnef::AddProps](itnef-addprops.md) com o sinalizador TNEF_PROP_INCLUDE definido em _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="5bb46-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="5bb46-136">Passar esses valores, permite que você execute codificações com uma única chamada em vez de várias chamadas.</span><span class="sxs-lookup"><span data-stu-id="5bb46-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="5bb46-137">A implementação de TNEF relata problemas de codificação de fluxo TNEF sem interromper o processamento de **FinishComponent** .</span><span class="sxs-lookup"><span data-stu-id="5bb46-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="5bb46-138">A estrutura de **STnefProblemArray** retornada em _lppProblems_ indica quais atributos TNEF ou propriedades MAPI, se houver, não pôde ser processadas.</span><span class="sxs-lookup"><span data-stu-id="5bb46-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="5bb46-139">O valor retornado no membro **scode** um das estruturas **STnefProblem** contidos no **STnefProblemArray** indica que o problema específico.</span><span class="sxs-lookup"><span data-stu-id="5bb46-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="5bb46-140">O provedor ou o gateway pode trabalhar no pressuposto de que todas as propriedades ou os atributos para os quais **FinishComponent** não retorna um relatório de problema foram processados com êxito.</span><span class="sxs-lookup"><span data-stu-id="5bb46-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="5bb46-141">Se um provedor ou gateway não funciona com matrizes de problema, ele pode passar NULL em _lppProblems_; Nesse caso, a matriz nenhum problema é retornado.</span><span class="sxs-lookup"><span data-stu-id="5bb46-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="5bb46-142">O valor retornado em _lppProblems_ é válido somente se a chamada Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="5bb46-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="5bb46-143">Quando for retornado S_OK, o provedor ou gateway deve verificar os valores retornados na estrutura [STnefProblemArray](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="5bb46-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="5bb46-144">Se ocorrer um erro na chamada, a estrutura de **STnefProblemArray** não for preenchida e o gateway ou provedor de chamada não deve usar ou livre a estrutura.</span><span class="sxs-lookup"><span data-stu-id="5bb46-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="5bb46-145">Se nenhum erro ocorrer na chamada, o provedor de chamada ou gateway deve liberar a memória para o **STnefProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5bb46-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5bb46-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bb46-146">See also</span></span>



[<span data-ttu-id="5bb46-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="5bb46-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="5bb46-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="5bb46-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="5bb46-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5bb46-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5bb46-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="5bb46-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="5bb46-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="5bb46-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="5bb46-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="5bb46-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="5bb46-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="5bb46-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="5bb46-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bb46-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

