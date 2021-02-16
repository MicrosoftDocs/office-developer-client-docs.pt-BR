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
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348619"
---
# <a name="itnefaddprops"></a><span data-ttu-id="d575d-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="d575d-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="d575d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d575d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d575d-105">Permite que o provedor de serviços de chamada ou gateway adicione propriedades ao encapsulamento de uma mensagem ou anexo.</span><span class="sxs-lookup"><span data-stu-id="d575d-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="d575d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d575d-106">Parameters</span></span>

 <span data-ttu-id="d575d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d575d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d575d-108">[in] Uma bitmask de sinalizadores que controla como as propriedades são incluídas ou excluídas do encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="d575d-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="d575d-109">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="d575d-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d575d-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="d575d-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="d575d-111">Codifica somente as propriedades no  _parâmetro lpPropList_ que fazem parte dos anexos na mensagem.</span><span class="sxs-lookup"><span data-stu-id="d575d-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="d575d-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="d575d-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="d575d-113">Codifica somente as propriedades do anexo especificado pelo _parâmetro ulElemID._</span><span class="sxs-lookup"><span data-stu-id="d575d-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="d575d-114">Se o parâmetro  _lpvData_ não for NULL, os dados apontados serão gravados no encapsulamento do anexo no arquivo indicado pela propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d575d-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="d575d-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="d575d-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="d575d-116">Codifica somente as propriedades da mensagem ou do anexo especificados pelo _parâmetro ulElemID._</span><span class="sxs-lookup"><span data-stu-id="d575d-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="d575d-117">Se esse sinalizador estiver definido, o valor em _lpvData_ deverá ser um [ponteiro IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream)</span><span class="sxs-lookup"><span data-stu-id="d575d-117">If this flag is set, the value in  _lpvData_ must be an [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) pointer.</span></span> 
    
<span data-ttu-id="d575d-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="d575d-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="d575d-119">Codifica todas as propriedades não especificadas no _parâmetro lpPropList._</span><span class="sxs-lookup"><span data-stu-id="d575d-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="d575d-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="d575d-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="d575d-121">Codifica todas as propriedades especificadas em  _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="d575d-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="d575d-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="d575d-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="d575d-123">Codifica somente as propriedades especificadas em  _lpPropList_ que fazem parte da mensagem em si.</span><span class="sxs-lookup"><span data-stu-id="d575d-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="d575d-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="d575d-124">_ulElemID_</span></span>
  
> <span data-ttu-id="d575d-125">[in] A propriedade **PR_ATTACH_NUM** de um anexo ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), que contém um número que identifica exclusivamente o anexo em sua mensagem pai.</span><span class="sxs-lookup"><span data-stu-id="d575d-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="d575d-126">O  _parâmetro ulElemID_ é usado quando uma manipulação especial é solicitada para um anexo.</span><span class="sxs-lookup"><span data-stu-id="d575d-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="d575d-127">O _parâmetro ulElemID_ deve ser 0, a menos que o sinalizador TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF seja definido no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="d575d-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="d575d-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="d575d-128">_lpvData_</span></span>
  
> <span data-ttu-id="d575d-129">[in] Um ponteiro para dados de anexo usados para substituir os dados do anexo especificado em  _ulElemID_.</span><span class="sxs-lookup"><span data-stu-id="d575d-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="d575d-130">O  _parâmetro lpvData_ deve ser NULL, a menos que TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF seja definido em  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="d575d-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="d575d-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="d575d-131">_lpPropList_</span></span>
  
> <span data-ttu-id="d575d-132">[in] Um ponteiro para a lista de propriedades a incluir ou excluir do encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="d575d-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d575d-133">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d575d-133">Return value</span></span>

<span data-ttu-id="d575d-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="d575d-134">S_OK</span></span> 
  
> <span data-ttu-id="d575d-135">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="d575d-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d575d-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="d575d-136">Remarks</span></span>

<span data-ttu-id="d575d-137">Provedores de transporte, provedores de armazenamento de mensagens e gateways chamam o método **ITnef::AddProps** para listar propriedades a serem incluídas ou excluídas do processamento de formato de encapsulamento Transport-Neutral (TNEF) de uma mensagem ou um anexo.</span><span class="sxs-lookup"><span data-stu-id="d575d-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="d575d-138">Usando chamadas sucessivas, o provedor ou gateway pode especificar uma lista de propriedades para adicionar e codificar ou excluir da codificação.</span><span class="sxs-lookup"><span data-stu-id="d575d-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="d575d-139">Os provedores e gateways também podem usar **AddProps** para fornecer informações sobre qualquer tratamento especial de anexos que devem ser dados.</span><span class="sxs-lookup"><span data-stu-id="d575d-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="d575d-140">**AddProps** é suportado apenas para objetos TNEF que são abertos com o sinalizador TNEF_ENCODE para as funções [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="d575d-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="d575d-141">Observe que nenhuma codificação TNEF real acontece para **AddProps** até que o método [ITnef::Finish](itnef-finish.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="d575d-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="d575d-142">Essa funcionalidade significa que os ponteiros passados para **AddProps** devem permanecer válidos até que a chamada para **Concluir** seja feita.</span><span class="sxs-lookup"><span data-stu-id="d575d-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="d575d-143">Nesse ponto, todos os objetos e dados passados com **chamadas AddProps** podem ser liberados ou liberados.</span><span class="sxs-lookup"><span data-stu-id="d575d-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d575d-144">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d575d-144">MFCMAPI reference</span></span>

<span data-ttu-id="d575d-145">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d575d-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d575d-146">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d575d-146">**File**</span></span>|<span data-ttu-id="d575d-147">**Função**</span><span class="sxs-lookup"><span data-stu-id="d575d-147">**Function**</span></span>|<span data-ttu-id="d575d-148">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="d575d-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d575d-149">File.cpp</span><span class="sxs-lookup"><span data-stu-id="d575d-149">File.cpp</span></span>  <br/> |<span data-ttu-id="d575d-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="d575d-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="d575d-151">MFCMAPI usa o **método ITnef::AddProps** para copiar propriedades de uma mensagem para um fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="d575d-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d575d-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="d575d-152">See also</span></span>



[<span data-ttu-id="d575d-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="d575d-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="d575d-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="d575d-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="d575d-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="d575d-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="d575d-156">Propriedade canônica PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="d575d-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="d575d-157">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d575d-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="d575d-158">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d575d-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

