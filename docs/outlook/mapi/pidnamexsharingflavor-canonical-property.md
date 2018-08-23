---
title: Propriedade canônica PidNameXSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bcdca783778e1a310be638ce376d408acf0b247f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580037"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="425f3-103">Propriedade canônica PidNameXSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="425f3-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="425f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="425f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="425f3-105">Representa o valor da propriedade **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="425f3-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="425f3-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="425f3-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="425f3-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="425f3-107">None</span></span>  <br/> |
|<span data-ttu-id="425f3-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="425f3-108">Property set:</span></span>  <br/> |<span data-ttu-id="425f3-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="425f3-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="425f3-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="425f3-110">Property name:</span></span>  <br/> |<span data-ttu-id="425f3-111">Tipo de compartilhamento X</span><span class="sxs-lookup"><span data-stu-id="425f3-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="425f3-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="425f3-112">Data type:</span></span>  <br/> |<span data-ttu-id="425f3-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="425f3-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="425f3-114">Área:</span><span class="sxs-lookup"><span data-stu-id="425f3-114">Area:</span></span>  <br/> |<span data-ttu-id="425f3-115">Sharing</span><span class="sxs-lookup"><span data-stu-id="425f3-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="425f3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="425f3-116">Remarks</span></span>

<span data-ttu-id="425f3-117">A propriedade **dispidSharingFlavor** deve ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="425f3-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="425f3-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="425f3-118">**Value**</span></span>|<span data-ttu-id="425f3-119">**Tipo de mensagem de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="425f3-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="425f3-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="425f3-120">0x00020310</span></span>  <br/> |<span data-ttu-id="425f3-121">Um convite de compartilhamento para uma pasta especial.</span><span class="sxs-lookup"><span data-stu-id="425f3-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="425f3-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="425f3-122">0x00000310</span></span>  <br/> |<span data-ttu-id="425f3-123">Um convite de compartilhamento para uma pasta que não é uma pasta especial.</span><span class="sxs-lookup"><span data-stu-id="425f3-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="425f3-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="425f3-124">0x00020500</span></span>  <br/> |<span data-ttu-id="425f3-125">Uma solicitação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="425f3-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="425f3-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="425f3-126">0x00020710</span></span>  <br/> |<span data-ttu-id="425f3-127">Ambos os um convite de compartilhamento para uma pasta especial e uma solicitação de compartilhamento de pasta especial do equivalente do destinatário.</span><span class="sxs-lookup"><span data-stu-id="425f3-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="425f3-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="425f3-128">0x00025100</span></span>  <br/> |<span data-ttu-id="425f3-129">Uma resposta de compartilhamento que nega uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="425f3-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="425f3-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="425f3-130">0x00023310</span></span>  <br/> |<span data-ttu-id="425f3-131">Uma resposta de compartilhamento que aceita uma solicitação (também um tipo de convite de compartilhamento).</span><span class="sxs-lookup"><span data-stu-id="425f3-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="425f3-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="425f3-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="425f3-133">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="425f3-133">Protocol specifications</span></span>

<span data-ttu-id="425f3-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="425f3-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="425f3-135">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="425f3-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="425f3-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="425f3-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="425f3-137">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="425f3-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="425f3-138">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="425f3-138">Header files</span></span>

<span data-ttu-id="425f3-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="425f3-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="425f3-140">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="425f3-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="425f3-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="425f3-141">See also</span></span>



[<span data-ttu-id="425f3-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="425f3-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="425f3-143">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="425f3-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="425f3-144">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="425f3-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="425f3-145">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="425f3-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

