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
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327479"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="3478e-103">Propriedade canônica PidLidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="3478e-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="3478e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3478e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3478e-105">Designa como uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="3478e-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3478e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3478e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3478e-107">dispidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="3478e-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="3478e-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="3478e-108">Property set:</span></span>  <br/> |<span data-ttu-id="3478e-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="3478e-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="3478e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3478e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3478e-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="3478e-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="3478e-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3478e-112">Data type:</span></span>  <br/> |<span data-ttu-id="3478e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3478e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3478e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3478e-114">Area:</span></span>  <br/> |<span data-ttu-id="3478e-115">Compartilhamento</span><span class="sxs-lookup"><span data-stu-id="3478e-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3478e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3478e-116">Remarks</span></span>

<span data-ttu-id="3478e-117">O valor dessa propriedade deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="3478e-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="3478e-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3478e-118">**Value**</span></span>|<span data-ttu-id="3478e-119">**Tipo de objeto de mensagem de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="3478e-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3478e-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="3478e-120">0x00020310</span></span>  <br/> |<span data-ttu-id="3478e-121">Um convite de compartilhamento para uma pasta especial.</span><span class="sxs-lookup"><span data-stu-id="3478e-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="3478e-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="3478e-122">0x00000310</span></span>  <br/> |<span data-ttu-id="3478e-123">Um convite de compartilhamento para uma pasta que não é uma pasta especial.</span><span class="sxs-lookup"><span data-stu-id="3478e-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="3478e-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="3478e-124">0x00020500</span></span>  <br/> |<span data-ttu-id="3478e-125">Uma solicitação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="3478e-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="3478e-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="3478e-126">0x00020710</span></span>  <br/> |<span data-ttu-id="3478e-127">Um convite de compartilhamento para uma pasta especial e uma solicitação de compartilhamento para a pasta especial equivalente do destinatário.</span><span class="sxs-lookup"><span data-stu-id="3478e-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="3478e-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="3478e-128">0x00025100</span></span>  <br/> |<span data-ttu-id="3478e-129">Uma resposta de compartilhamento negando uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="3478e-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="3478e-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="3478e-130">0x00023310</span></span>  <br/> |<span data-ttu-id="3478e-131">Uma resposta de compartilhamento que aceita uma solicitação (também um tipo de convite de compartilhamento).</span><span class="sxs-lookup"><span data-stu-id="3478e-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3478e-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3478e-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3478e-133">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="3478e-133">Protocol specifications</span></span>

<span data-ttu-id="3478e-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3478e-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3478e-135">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3478e-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3478e-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3478e-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3478e-137">Compartilha pastas de caixa de correio entre os clientes.</span><span class="sxs-lookup"><span data-stu-id="3478e-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3478e-138">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3478e-138">Header files</span></span>

<span data-ttu-id="3478e-139">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3478e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="3478e-140">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3478e-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3478e-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="3478e-141">See also</span></span>



[<span data-ttu-id="3478e-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3478e-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3478e-143">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3478e-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3478e-144">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3478e-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3478e-145">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3478e-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

