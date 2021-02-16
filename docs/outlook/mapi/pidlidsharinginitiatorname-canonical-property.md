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
ms.openlocfilehash: b9e3236affa9612356e68044d2943ea7b9276384
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336845"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="65133-103">Propriedade canônica PidLidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="65133-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="65133-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65133-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65133-105">Designa como uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="65133-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65133-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="65133-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="65133-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="65133-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="65133-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="65133-108">Property set:</span></span>  <br/> |<span data-ttu-id="65133-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="65133-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="65133-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="65133-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="65133-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="65133-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="65133-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="65133-112">Data type:</span></span>  <br/> |<span data-ttu-id="65133-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="65133-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="65133-114">Área:</span><span class="sxs-lookup"><span data-stu-id="65133-114">Area:</span></span>  <br/> |<span data-ttu-id="65133-115">Compartilhamento</span><span class="sxs-lookup"><span data-stu-id="65133-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65133-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="65133-116">Remarks</span></span>

<span data-ttu-id="65133-117">Essa propriedade deve ser definida como o valor de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do Address Book identificado por **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) e deve ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="65133-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="65133-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="65133-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="65133-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="65133-119">Protocol specifications</span></span>

<span data-ttu-id="65133-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65133-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65133-121">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="65133-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="65133-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65133-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65133-123">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="65133-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="65133-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="65133-124">Header files</span></span>

<span data-ttu-id="65133-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65133-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="65133-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="65133-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65133-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="65133-127">See also</span></span>



[<span data-ttu-id="65133-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="65133-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="65133-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="65133-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="65133-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="65133-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="65133-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="65133-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

