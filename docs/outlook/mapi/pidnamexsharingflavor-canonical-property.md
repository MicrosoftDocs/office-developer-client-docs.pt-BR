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
ms.openlocfilehash: d2afa598bf9b7949f2e9142611570ebbd048f7e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360883"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="ddad4-103">Propriedade canônica PidNameXSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="ddad4-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="ddad4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddad4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddad4-105">Representa o valor da propriedade **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ddad4-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ddad4-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="ddad4-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="ddad4-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ddad4-107">None</span></span>  <br/> |
|<span data-ttu-id="ddad4-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="ddad4-108">Property set:</span></span>  <br/> |<span data-ttu-id="ddad4-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="ddad4-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="ddad4-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="ddad4-110">Property name:</span></span>  <br/> |<span data-ttu-id="ddad4-111">X-Sharing-flavor</span><span class="sxs-lookup"><span data-stu-id="ddad4-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="ddad4-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ddad4-112">Data type:</span></span>  <br/> |<span data-ttu-id="ddad4-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ddad4-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ddad4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ddad4-114">Area:</span></span>  <br/> |<span data-ttu-id="ddad4-115">Compartilhamento</span><span class="sxs-lookup"><span data-stu-id="ddad4-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddad4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ddad4-116">Remarks</span></span>

<span data-ttu-id="ddad4-117">A propriedade **dispidSharingFlavor** deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ddad4-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="ddad4-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ddad4-118">**Value**</span></span>|<span data-ttu-id="ddad4-119">**Tipo de mensagem de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="ddad4-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ddad4-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="ddad4-120">0x00020310</span></span>  <br/> |<span data-ttu-id="ddad4-121">Um convite de compartilhamento para uma pasta especial.</span><span class="sxs-lookup"><span data-stu-id="ddad4-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="ddad4-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="ddad4-122">0x00000310</span></span>  <br/> |<span data-ttu-id="ddad4-123">Um convite de compartilhamento para uma pasta que não é uma pasta especial.</span><span class="sxs-lookup"><span data-stu-id="ddad4-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="ddad4-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="ddad4-124">0x00020500</span></span>  <br/> |<span data-ttu-id="ddad4-125">Uma solicitação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ddad4-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="ddad4-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="ddad4-126">0x00020710</span></span>  <br/> |<span data-ttu-id="ddad4-127">Um convite de compartilhamento para uma pasta especial e uma solicitação de compartilhamento para a pasta especial equivalente do destinatário.</span><span class="sxs-lookup"><span data-stu-id="ddad4-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="ddad4-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="ddad4-128">0x00025100</span></span>  <br/> |<span data-ttu-id="ddad4-129">Uma resposta de compartilhamento que nega uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="ddad4-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="ddad4-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="ddad4-130">0x00023310</span></span>  <br/> |<span data-ttu-id="ddad4-131">Uma resposta de compartilhamento que aceita uma solicitação (também um tipo de convite de compartilhamento).</span><span class="sxs-lookup"><span data-stu-id="ddad4-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ddad4-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddad4-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ddad4-133">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="ddad4-133">Protocol specifications</span></span>

<span data-ttu-id="ddad4-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ddad4-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ddad4-135">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ddad4-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ddad4-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ddad4-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ddad4-137">Compartilha pastas de caixa de correio entre os clientes.</span><span class="sxs-lookup"><span data-stu-id="ddad4-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ddad4-138">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ddad4-138">Header files</span></span>

<span data-ttu-id="ddad4-139">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ddad4-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="ddad4-140">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ddad4-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ddad4-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddad4-141">See also</span></span>



[<span data-ttu-id="ddad4-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ddad4-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ddad4-143">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ddad4-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ddad4-144">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ddad4-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ddad4-145">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ddad4-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

