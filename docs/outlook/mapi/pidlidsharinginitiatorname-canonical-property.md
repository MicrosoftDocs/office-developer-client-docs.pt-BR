---
title: Propriedade canônica PidLidSharingInitiatorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorName
api_type:
- COM
ms.assetid: f2b126fc-41fa-4dc4-9f13-07bc4f621d0b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1b20c2171f77451d9b7e85573260acff3243238f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768652"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="f5c02-103">Propriedade canônica PidLidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="f5c02-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="f5c02-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5c02-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5c02-105">Designa como uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f5c02-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5c02-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f5c02-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5c02-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="f5c02-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="f5c02-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="f5c02-108">Property set:</span></span>  <br/> |<span data-ttu-id="f5c02-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="f5c02-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="f5c02-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="f5c02-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f5c02-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="f5c02-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="f5c02-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f5c02-112">Data type:</span></span>  <br/> |<span data-ttu-id="f5c02-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f5c02-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f5c02-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f5c02-114">Area:</span></span>  <br/> |<span data-ttu-id="f5c02-115">Sharing</span><span class="sxs-lookup"><span data-stu-id="f5c02-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5c02-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5c02-116">Remarks</span></span>

<span data-ttu-id="f5c02-117">Essa propriedade deve ser definida como o valor da **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do catálogo de endereços identificado pela **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) e deve ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="f5c02-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f5c02-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5c02-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5c02-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f5c02-119">Protocol specifications</span></span>

<span data-ttu-id="f5c02-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5c02-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5c02-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f5c02-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5c02-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5c02-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5c02-123">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="f5c02-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5c02-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f5c02-124">Header files</span></span>

<span data-ttu-id="f5c02-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5c02-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5c02-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f5c02-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5c02-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5c02-127">See also</span></span>



[<span data-ttu-id="f5c02-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f5c02-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5c02-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f5c02-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5c02-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f5c02-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5c02-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f5c02-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

