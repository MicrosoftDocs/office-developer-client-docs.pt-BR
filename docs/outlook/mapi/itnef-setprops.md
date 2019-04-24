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
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315040"
---
# <a name="itnefsetprops"></a><span data-ttu-id="dbaef-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="dbaef-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="dbaef-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbaef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbaef-105">Define o valor de uma ou mais propriedades de uma mensagem encapsulada ou anexo sem modificar a mensagem original ou o anexo.</span><span class="sxs-lookup"><span data-stu-id="dbaef-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="dbaef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbaef-106">Parameters</span></span>

 <span data-ttu-id="dbaef-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dbaef-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dbaef-108">no Uma bitmask de sinalizadores que controla como os valores de propriedade são definidos.</span><span class="sxs-lookup"><span data-stu-id="dbaef-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="dbaef-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="dbaef-109">The following flag can be set:</span></span>
    
<span data-ttu-id="dbaef-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="dbaef-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="dbaef-111">Codifica somente as propriedades da mensagem ou do anexo especificado pelo parâmetro _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="dbaef-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="dbaef-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="dbaef-112">_ulElemID_</span></span>
  
> <span data-ttu-id="dbaef-113">no A propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo, que contém um número que identifica exclusivamente o anexo em sua mensagem pai.</span><span class="sxs-lookup"><span data-stu-id="dbaef-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="dbaef-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="dbaef-114">_cValues_</span></span>
  
> <span data-ttu-id="dbaef-115">no O número de valores de propriedade na estrutura [SPropValue](spropvalue.md) apontados pelo parâmetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="dbaef-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="dbaef-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="dbaef-116">_lpProps_</span></span>
  
> <span data-ttu-id="dbaef-117">no Um ponteiro para uma estrutura **SPropValue** que contém os valores de propriedade das propriedades a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="dbaef-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dbaef-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dbaef-118">Return value</span></span>

<span data-ttu-id="dbaef-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="dbaef-119">S_OK</span></span> 
  
> <span data-ttu-id="dbaef-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="dbaef-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dbaef-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbaef-121">Remarks</span></span>

<span data-ttu-id="dbaef-122">Provedores de transporte, provedores de repositórios de mensagens e gateways chamam o método **ITnef::** SetProps para definir propriedades a serem incluídas no encapsulamento de uma mensagem ou anexo sem modificar a mensagem original ou o anexo.</span><span class="sxs-lookup"><span data-stu-id="dbaef-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="dbaef-123">Todas as propriedades definidas com essa chamada substituem as propriedades existentes na mensagem encapsulada.</span><span class="sxs-lookup"><span data-stu-id="dbaef-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="dbaef-124">\*\*\*\* SetProps tem suporte apenas para objetos TNEF que são abertos com o sinalizador TNEF_ENCODE para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="dbaef-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="dbaef-125">Qualquer número de propriedades pode ser definido com esta chamada.</span><span class="sxs-lookup"><span data-stu-id="dbaef-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="dbaef-126">Nenhuma codificação TNEF real para \*\*\*\* SetProps acontece até após o método [ITnef:: Finish](itnef-finish.md) ser chamado.</span><span class="sxs-lookup"><span data-stu-id="dbaef-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="dbaef-127">Essa funcionalidade significa que os ponteiros \*\*\*\* passados para SetProps devem permanecer válidos até que a chamada para **término** seja feita.</span><span class="sxs-lookup"><span data-stu-id="dbaef-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="dbaef-128">Nesse ponto, todos os objetos e dados passados para \*\*\*\* as chamadas de SetProps podem ser liberados ou liberados.</span><span class="sxs-lookup"><span data-stu-id="dbaef-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dbaef-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbaef-129">See also</span></span>



[<span data-ttu-id="dbaef-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="dbaef-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="dbaef-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="dbaef-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="dbaef-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="dbaef-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="dbaef-133">Propriedade canônica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="dbaef-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="dbaef-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dbaef-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="dbaef-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dbaef-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

