---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 81f9388b67d3194fe1442091b9f4f75a7671cb6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579645"
---
# <a name="itnefsetprops"></a><span data-ttu-id="f0874-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="f0874-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="f0874-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0874-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0874-105">Define o valor de uma ou mais propriedades para uma mensagem encapsulada ou um anexo sem modificar a mensagem original ou um anexo.</span><span class="sxs-lookup"><span data-stu-id="f0874-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="f0874-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0874-106">Parameters</span></span>

 <span data-ttu-id="f0874-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f0874-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f0874-108">[in] Uma bitmask dos sinalizadores que controla como os valores de propriedade são definidos.</span><span class="sxs-lookup"><span data-stu-id="f0874-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="f0874-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="f0874-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f0874-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="f0874-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="f0874-111">Codifica apenas as propriedades da mensagem ou anexo especificado pelo parâmetro _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="f0874-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="f0874-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="f0874-112">_ulElemID_</span></span>
  
> <span data-ttu-id="f0874-113">[in] Propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo, que contém um número de forma exclusiva identifica o anexo na mensagem de seu pai.</span><span class="sxs-lookup"><span data-stu-id="f0874-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="f0874-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="f0874-114">_cValues_</span></span>
  
> <span data-ttu-id="f0874-115">[in] O número de valores de propriedade na estrutura [SPropValue](spropvalue.md) apontado pelo parâmetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="f0874-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="f0874-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="f0874-116">_lpProps_</span></span>
  
> <span data-ttu-id="f0874-117">[in] Um ponteiro para uma estrutura **SPropValue** que contém os valores de propriedade para definir as propriedades.</span><span class="sxs-lookup"><span data-stu-id="f0874-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f0874-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f0874-118">Return value</span></span>

<span data-ttu-id="f0874-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0874-119">S_OK</span></span> 
  
> <span data-ttu-id="f0874-120">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="f0874-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0874-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0874-121">Remarks</span></span>

<span data-ttu-id="f0874-122">Provedores, provedores de armazenamento de mensagem e o método **ITnef::SetProps** de chamada de gateways para definir propriedades para incluir no encapsulamento de uma mensagem ou um anexo sem modificar a mensagem original ou um anexo de transporte.</span><span class="sxs-lookup"><span data-stu-id="f0874-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="f0874-123">Todas as propriedades definidas com esta chamada substituiem propriedades existentes na mensagem encapsulada.</span><span class="sxs-lookup"><span data-stu-id="f0874-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="f0874-124">**SetProps** é suportado somente para os objetos TNEF abertos com o sinalizador TNEF_ENCODE para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="f0874-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="f0874-125">Qualquer número de propriedades pode ser definido com esta chamada.</span><span class="sxs-lookup"><span data-stu-id="f0874-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f0874-126">Nenhuma codificação TNEF real para **SetProps** acontece até depois que o método [ITnef::Finish](itnef-finish.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="f0874-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="f0874-127">Essa funcionalidade significa que os ponteiros passados para **SetProps** devem permanecer válidos até após a chamada para **Concluir a** é feita.</span><span class="sxs-lookup"><span data-stu-id="f0874-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="f0874-128">Nesse momento, todos os objetos e dados passados para **SetProps** chamadas podem ser lançados ou liberados.</span><span class="sxs-lookup"><span data-stu-id="f0874-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0874-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0874-129">See also</span></span>



[<span data-ttu-id="f0874-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="f0874-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="f0874-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="f0874-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="f0874-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="f0874-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="f0874-133">Propriedade canônico de PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="f0874-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="f0874-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f0874-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="f0874-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f0874-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

