---
title: Propriedade canônico de PidTagProviderDisplay
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 1546ee1aa970be71d853dba59ce0fab7cc5a4dac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769699"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="59952-103">Propriedade canônico de PidTagProviderDisplay</span><span class="sxs-lookup"><span data-stu-id="59952-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="59952-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="59952-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="59952-105">Contém o nome de exibição de fornecedor definido para um provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="59952-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59952-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="59952-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59952-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="59952-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="59952-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="59952-108">Identifier:</span></span>  <br/> |<span data-ttu-id="59952-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="59952-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="59952-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="59952-110">Data type:</span></span>  <br/> |<span data-ttu-id="59952-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="59952-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="59952-112">Área:</span><span class="sxs-lookup"><span data-stu-id="59952-112">Area:</span></span>  <br/> |<span data-ttu-id="59952-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="59952-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59952-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="59952-114">Remarks</span></span>

<span data-ttu-id="59952-115">Essas propriedades e **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) são definidas apenas em seções de perfil que pertencem a provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="59952-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="59952-116">Elas devem estar presentes em MAPISVC.</span><span class="sxs-lookup"><span data-stu-id="59952-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="59952-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="59952-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="59952-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="59952-118">Header files</span></span>

<span data-ttu-id="59952-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59952-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="59952-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="59952-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="59952-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="59952-121">Mapitags.h</span></span>
  
> <span data-ttu-id="59952-122">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="59952-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59952-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="59952-123">See also</span></span>



[<span data-ttu-id="59952-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="59952-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59952-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="59952-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59952-126">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="59952-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59952-127">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="59952-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

