---
title: Propriedade canônica PidLidSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0333f0c309d89436c50a58124500f1b359584954
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768646"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="dca6e-103">Propriedade canônica PidLidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="dca6e-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="dca6e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dca6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dca6e-105">Designa como uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="dca6e-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dca6e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dca6e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dca6e-107">dispidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="dca6e-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="dca6e-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="dca6e-108">Property set:</span></span>  <br/> |<span data-ttu-id="dca6e-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="dca6e-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="dca6e-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="dca6e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dca6e-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="dca6e-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="dca6e-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dca6e-112">Data type:</span></span>  <br/> |<span data-ttu-id="dca6e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dca6e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dca6e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="dca6e-114">Area:</span></span>  <br/> |<span data-ttu-id="dca6e-115">Sharing</span><span class="sxs-lookup"><span data-stu-id="dca6e-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dca6e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="dca6e-116">Remarks</span></span>

<span data-ttu-id="dca6e-117">O valor dessa propriedade deve ser um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="dca6e-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="dca6e-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="dca6e-118">**Value**</span></span>|<span data-ttu-id="dca6e-119">**Tipo de objeto de mensagem de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="dca6e-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dca6e-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="dca6e-120">0x00020310</span></span>  <br/> |<span data-ttu-id="dca6e-121">Um convite de compartilhamento para uma pasta especial.</span><span class="sxs-lookup"><span data-stu-id="dca6e-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="dca6e-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="dca6e-122">0x00000310</span></span>  <br/> |<span data-ttu-id="dca6e-123">Um convite de compartilhamento para uma pasta que não é uma pasta especial.</span><span class="sxs-lookup"><span data-stu-id="dca6e-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="dca6e-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="dca6e-124">0x00020500</span></span>  <br/> |<span data-ttu-id="dca6e-125">Uma solicitação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="dca6e-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="dca6e-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="dca6e-126">0x00020710</span></span>  <br/> |<span data-ttu-id="dca6e-127">Ambos os um convite de compartilhamento para uma pasta especial e uma solicitação de compartilhamento de pasta especial do equivalente do destinatário.</span><span class="sxs-lookup"><span data-stu-id="dca6e-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="dca6e-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="dca6e-128">0x00025100</span></span>  <br/> |<span data-ttu-id="dca6e-129">Uma resposta de compartilhamento a negação uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="dca6e-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="dca6e-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="dca6e-130">0x00023310</span></span>  <br/> |<span data-ttu-id="dca6e-131">Uma resposta de compartilhamento aceitar uma solicitação (também um tipo de convite de compartilhamento).</span><span class="sxs-lookup"><span data-stu-id="dca6e-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="dca6e-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dca6e-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dca6e-133">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="dca6e-133">Protocol specifications</span></span>

<span data-ttu-id="dca6e-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dca6e-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dca6e-135">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="dca6e-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dca6e-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dca6e-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dca6e-137">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="dca6e-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dca6e-138">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dca6e-138">Header files</span></span>

<span data-ttu-id="dca6e-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dca6e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="dca6e-140">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dca6e-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dca6e-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="dca6e-141">See also</span></span>



[<span data-ttu-id="dca6e-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dca6e-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dca6e-143">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="dca6e-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dca6e-144">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dca6e-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dca6e-145">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dca6e-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

