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
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435674"
---
# <a name="itneffinish"></a><span data-ttu-id="f5d4e-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="f5d4e-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="f5d4e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5d4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5d4e-105">Finaliza o processamento de todas as Transport-Neutral TNEF (Formato de Encapsulamento) que estão em fila e aguardando.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="f5d4e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5d4e-106">Parameters</span></span>

 <span data-ttu-id="f5d4e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f5d4e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f5d4e-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f5d4e-109">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="f5d4e-109">_lpKey_</span></span>
  
> <span data-ttu-id="f5d4e-110">[out] Um ponteiro para a **PR_ATTACH_NUM** chave ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="f5d4e-111">O objeto de encapsulamento TNEF usa essa chave para corresponder a um anexo à marca de posicionamento do anexo em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="f5d4e-112">Essa chave deve ser exclusiva para cada anexo.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="f5d4e-113">_lpProblem_</span><span class="sxs-lookup"><span data-stu-id="f5d4e-113">_lpProblem_</span></span>
  
> <span data-ttu-id="f5d4e-114">[out] Um ponteiro para um ponteiro para uma [estrutura STnefProblemArray](stnefproblemarray.md) retornada.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="f5d4e-115">A **estrutura STnefProblemArray** indica quais propriedades, se alguma, não foram codificadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="f5d4e-116">Se NULL for passado no  _parâmetro lpProblem,_ nenhuma matriz de problema de propriedade será retornada.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f5d4e-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f5d4e-117">Return value</span></span>

<span data-ttu-id="f5d4e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5d4e-118">S_OK</span></span> 
  
> <span data-ttu-id="f5d4e-119">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f5d4e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5d4e-120">Remarks</span></span>

<span data-ttu-id="f5d4e-121">Provedores de transporte, provedores de armazenamento de mensagens e gateways chamam o método **ITnef::Finish** para executar a codificação de todas as propriedades para as quais a codificação foi solicitada em chamadas para os métodos [ITnef::AddProps](itnef-addprops.md) e [ITnef::SetProps.](itnef-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="f5d4e-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="f5d4e-122">Se o objeto TNEF foi aberto com o sinalizador TNEF_ENCODE para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx,](opentnefstreamex.md) o método **Finish** codifica as propriedades solicitadas no fluxo de encapsulamento passado para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="f5d4e-123">Se o objeto TNEF tiver sido aberto com o sinalizador TNEF_DECODE, o método **Finish** decodificará as propriedades do fluxo TNEF e as grava novamente na mensagem à que pertencem.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="f5d4e-124">Após a **chamada Concluir,** o ponteiro para o fluxo de encapsulamento aponta para o final dos dados TNEF.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="f5d4e-125">Se o provedor ou o gateway precisar usar os dados de fluxo TNEF após a chamada **Concluir,** ele deverá redefinir o ponteiro de fluxo para o início dos dados de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="f5d4e-126">A implementação do TNEF relata problemas de codificação de fluxo TNEF sem interromper o **processo de** Concluir.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="f5d4e-127">A [estrutura STnefProblemArray](stnefproblemarray.md) retornada no parâmetro  _lpProblem_ indica quais atributos TNEF ou propriedades MAPI, se algum, não puderam ser processados.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="f5d4e-128">O valor retornado no membro **scode** de uma das estruturas **STnefProblem** contidas em **STnefProblemArray** indica o problema específico.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="f5d4e-129">O provedor ou gateway pode trabalhar na suposição de que todas as propriedades ou atributos para os quais **Finish** não retorna um relatório de problemas foram processados com êxito.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="f5d4e-130">Se um provedor ou gateway não funcionar com matrizes de problemas, ele poderá passar NULL em  _lpProblem_; nesse caso, nenhuma matriz do problema será retornada.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="f5d4e-131">O valor retornado em  _lpProblem_ só será válido se a chamada retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="f5d4e-132">Quando S_OK é retornado, o provedor ou gateway deve verificar os valores retornados na **estrutura STnefProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="f5d4e-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="f5d4e-133">Se ocorrer um erro na chamada, a estrutura **STnefProblemArray** não será preenchida e o provedor de chamada ou gateway não deverá usar ou liberar a estrutura.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="f5d4e-134">Se não ocorrer nenhum erro na chamada, o provedor de chamada ou gateway deverá liberar a memória para **o STnefProblemArray** chamando a [função MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="f5d4e-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f5d4e-135">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f5d4e-135">MFCMAPI reference</span></span>

<span data-ttu-id="f5d4e-136">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f5d4e-137">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f5d4e-137">**File**</span></span>|<span data-ttu-id="f5d4e-138">**Função**</span><span class="sxs-lookup"><span data-stu-id="f5d4e-138">**Function**</span></span>|<span data-ttu-id="f5d4e-139">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="f5d4e-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f5d4e-140">File.cpp</span><span class="sxs-lookup"><span data-stu-id="f5d4e-140">File.cpp</span></span>  <br/> |<span data-ttu-id="f5d4e-141">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="f5d4e-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="f5d4e-142">MFCMAPI usa o **método ITnef::Finish** para concluir o processamento do novo fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="f5d4e-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5d4e-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5d4e-143">See also</span></span>



[<span data-ttu-id="f5d4e-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="f5d4e-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="f5d4e-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f5d4e-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f5d4e-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="f5d4e-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="f5d4e-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="f5d4e-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="f5d4e-148">Propriedade canônica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="f5d4e-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="f5d4e-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="f5d4e-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="f5d4e-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f5d4e-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="f5d4e-151">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f5d4e-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

