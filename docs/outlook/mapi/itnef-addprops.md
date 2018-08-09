---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2d37898b100398218d4f8762cdd3a16943d8f11a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767718"
---
# <a name="itnefaddprops"></a><span data-ttu-id="80e6b-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="80e6b-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="80e6b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80e6b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80e6b-105">Permite que o provedor de serviços de chamada ou gateway adicionar propriedades ao encapsulamento de uma mensagem ou um anexo.</span><span class="sxs-lookup"><span data-stu-id="80e6b-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="80e6b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80e6b-106">Parameters</span></span>

 <span data-ttu-id="80e6b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80e6b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="80e6b-108">[in] Uma bitmask dos sinalizadores que controla como propriedades são incluídas em ou excluídas de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="80e6b-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="80e6b-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="80e6b-109">The following flags can be set:</span></span>
    
<span data-ttu-id="80e6b-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="80e6b-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="80e6b-111">Codifica apenas as propriedades no parâmetro _lpPropList_ que fazem parte de anexos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="80e6b-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="80e6b-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="80e6b-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="80e6b-113">Codifica apenas as propriedades do anexo especificado pelo parâmetro _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="80e6b-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="80e6b-114">Se o parâmetro _lpvData_ não for nulo, os dados apontados são gravados para encapsulamento do anexo no arquivo indicado pela propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="80e6b-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="80e6b-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="80e6b-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="80e6b-116">Codifica apenas as propriedades da mensagem ou anexo especificado pelo parâmetro _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="80e6b-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="80e6b-117">Se esse sinalizador estiver definido, o valor em _lpvData_ deve ser um ponteiro [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="80e6b-117">If this flag is set, the value in  _lpvData_ must be an [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) pointer.</span></span> 
    
<span data-ttu-id="80e6b-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="80e6b-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="80e6b-119">Codifica todas as propriedades não especificadas no parâmetro _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="80e6b-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="80e6b-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="80e6b-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="80e6b-121">Codifica todas as propriedades especificadas na _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="80e6b-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="80e6b-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="80e6b-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="80e6b-123">Codifica apenas as propriedades especificadas na _lpPropList_ que fazem parte da mensagem em si.</span><span class="sxs-lookup"><span data-stu-id="80e6b-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="80e6b-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="80e6b-124">_ulElemID_</span></span>
  
> <span data-ttu-id="80e6b-125">[in] Propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo, que contém um número de forma exclusiva identifica o anexo na mensagem de seu pai.</span><span class="sxs-lookup"><span data-stu-id="80e6b-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="80e6b-126">O parâmetro _ulElemID_ é usado quando a ação especial é solicitada para um anexo.</span><span class="sxs-lookup"><span data-stu-id="80e6b-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="80e6b-127">O parâmetro _ulElemID_ deve ser 0 a menos que o sinalizador TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="80e6b-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="80e6b-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="80e6b-128">_lpvData_</span></span>
  
> <span data-ttu-id="80e6b-129">[in] Um ponteiro para dados de anexo usados para substituir os dados do anexo especificado em _ulElemID_.</span><span class="sxs-lookup"><span data-stu-id="80e6b-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="80e6b-130">O parâmetro _lpvData_ deve ser NULL, a menos que TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF está definida na _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="80e6b-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="80e6b-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="80e6b-131">_lpPropList_</span></span>
  
> <span data-ttu-id="80e6b-132">[in] Um ponteiro para a lista de propriedades para incluir ou excluir do encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="80e6b-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="80e6b-133">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="80e6b-133">Return value</span></span>

<span data-ttu-id="80e6b-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="80e6b-134">S_OK</span></span> 
  
> <span data-ttu-id="80e6b-135">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="80e6b-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80e6b-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="80e6b-136">Remarks</span></span>

<span data-ttu-id="80e6b-137">Provedores de transporte, provedores de armazenamento de mensagem e gateways chame o método de **ITnef::AddProps** às propriedades de lista para ser incluídos ou excluídos do processamento de uma mensagem ou um anexo Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="80e6b-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="80e6b-138">Usando sucessivas chamadas, o provedor ou o gateway pode especificar uma lista de propriedades para adicionar e codificar ou excluídos da sendo codificado.</span><span class="sxs-lookup"><span data-stu-id="80e6b-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="80e6b-139">Provedores e gateways também podem usar **AddProps** para fornecer informações sobre todos os anexos manipulação especial devem ser dada.</span><span class="sxs-lookup"><span data-stu-id="80e6b-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="80e6b-140">**AddProps** é suportado somente para os objetos TNEF abertos com o sinalizador TNEF_ENCODE para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="80e6b-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="80e6b-141">Observe que nenhuma real a codificação TNEF acontece para **AddProps** até que o método [ITnef::Finish](itnef-finish.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="80e6b-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="80e6b-142">Essa funcionalidade significa que os ponteiros passados para **AddProps** devem permanecer válidos até após a chamada para **Concluir a** é feita.</span><span class="sxs-lookup"><span data-stu-id="80e6b-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="80e6b-143">Nesse momento, todos os objetos e dados passados com **AddProps** chamadas podem ser lançados ou liberados.</span><span class="sxs-lookup"><span data-stu-id="80e6b-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="80e6b-144">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="80e6b-144">MFCMAPI reference</span></span>

<span data-ttu-id="80e6b-145">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="80e6b-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="80e6b-146">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="80e6b-146">**File**</span></span>|<span data-ttu-id="80e6b-147">**Function**</span><span class="sxs-lookup"><span data-stu-id="80e6b-147">**Function**</span></span>|<span data-ttu-id="80e6b-148">**Comment**</span><span class="sxs-lookup"><span data-stu-id="80e6b-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80e6b-149">CPP</span><span class="sxs-lookup"><span data-stu-id="80e6b-149">File.cpp</span></span>  <br/> |<span data-ttu-id="80e6b-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="80e6b-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="80e6b-151">MFCMAPI usa o método **ITnef::AddProps** para copiar propriedades de uma mensagem para um fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="80e6b-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80e6b-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="80e6b-152">See also</span></span>



[<span data-ttu-id="80e6b-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="80e6b-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="80e6b-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="80e6b-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="80e6b-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="80e6b-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="80e6b-156">Propriedade canônica PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="80e6b-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="80e6b-157">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80e6b-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="80e6b-158">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="80e6b-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
