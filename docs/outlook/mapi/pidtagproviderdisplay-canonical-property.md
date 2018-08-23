---
title: Propriedade canônica PidTagProviderDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDisplay
api_type:
- COM
ms.assetid: 62e96db8-4c3e-4f73-b695-99eb4b2396fd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9a37382cda1a96025f950d941f83fb5b6a0497bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565498"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="a2acd-103">Propriedade canônica PidTagProviderDisplay</span><span class="sxs-lookup"><span data-stu-id="a2acd-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="a2acd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2acd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2acd-105">Contém o nome de exibição de fornecedor definido para um provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="a2acd-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a2acd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a2acd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a2acd-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="a2acd-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="a2acd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a2acd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a2acd-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="a2acd-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="a2acd-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a2acd-110">Data type:</span></span>  <br/> |<span data-ttu-id="a2acd-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a2acd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a2acd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a2acd-112">Area:</span></span>  <br/> |<span data-ttu-id="a2acd-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="a2acd-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2acd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2acd-114">Remarks</span></span>

<span data-ttu-id="a2acd-115">Essas propriedades e **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) são definidas apenas em seções de perfil que pertencem a provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="a2acd-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="a2acd-116">Elas devem estar presentes em MAPISVC.</span><span class="sxs-lookup"><span data-stu-id="a2acd-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a2acd-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2acd-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a2acd-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a2acd-118">Header files</span></span>

<span data-ttu-id="a2acd-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2acd-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="a2acd-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a2acd-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="a2acd-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a2acd-121">Mapitags.h</span></span>
  
> <span data-ttu-id="a2acd-122">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a2acd-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2acd-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2acd-123">See also</span></span>



[<span data-ttu-id="a2acd-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a2acd-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a2acd-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a2acd-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a2acd-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a2acd-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a2acd-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a2acd-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

