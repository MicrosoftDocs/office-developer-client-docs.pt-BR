---
title: Propriedade canônica PidTagAttachContentId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentId
api_type:
- HeaderDef
ms.assetid: 46f31089-3b66-41a2-8094-e3db52464b9f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: edd0df690df6af47ed6db34dc4a658b24136077c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768964"
---
# <a name="pidtagattachcontentid-canonical-property"></a><span data-ttu-id="304df-103">Propriedade canônica PidTagAttachContentId</span><span class="sxs-lookup"><span data-stu-id="304df-103">PidTagAttachContentId Canonical Property</span></span>

  
  
<span data-ttu-id="304df-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="304df-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="304df-105">Contém o cabeçalho de identificação de conteúdo de anexo de uma mensagem de email extensões MIME (Multipurpose Internet).</span><span class="sxs-lookup"><span data-stu-id="304df-105">Contains the content identification header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="304df-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="304df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="304df-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span><span class="sxs-lookup"><span data-stu-id="304df-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span></span>  <br/> |
|<span data-ttu-id="304df-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="304df-108">Identifier:</span></span>  <br/> |<span data-ttu-id="304df-109">0x3712</span><span class="sxs-lookup"><span data-stu-id="304df-109">0x3712</span></span>  <br/> |
|<span data-ttu-id="304df-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="304df-110">Data type:</span></span>  <br/> |<span data-ttu-id="304df-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="304df-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="304df-112">Área:</span><span class="sxs-lookup"><span data-stu-id="304df-112">Area:</span></span>  <br/> |<span data-ttu-id="304df-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="304df-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="304df-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="304df-114">Remarks</span></span>

<span data-ttu-id="304df-115">Essas propriedades são usadas para suporte MHTML.</span><span class="sxs-lookup"><span data-stu-id="304df-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="304df-116">Eles representam o cabeçalho de identificação de conteúdo para a parte apropriada do corpo MIME.</span><span class="sxs-lookup"><span data-stu-id="304df-116">They represent the content identification header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="304df-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="304df-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="304df-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="304df-118">Protocol specifications</span></span>

<span data-ttu-id="304df-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="304df-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="304df-120">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="304df-120">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="304df-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="304df-121">Header Files</span></span>

<span data-ttu-id="304df-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="304df-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="304df-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="304df-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="304df-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="304df-124">Mapitags.h</span></span>
  
> <span data-ttu-id="304df-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="304df-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="304df-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="304df-126">See also</span></span>



[<span data-ttu-id="304df-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="304df-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="304df-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="304df-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="304df-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="304df-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="304df-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="304df-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
