---
title: Propriedade canônica PidTagAttachContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentBase
api_type:
- HeaderDef
ms.assetid: 35c10264-6998-4c46-8cef-82708c96d9c7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cff0e2a5ffdb3b85e73b24ec8a30b7d88637ce48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768951"
---
# <a name="pidtagattachcontentbase-canonical-property"></a><span data-ttu-id="f6fe6-103">Propriedade canônica PidTagAttachContentBase</span><span class="sxs-lookup"><span data-stu-id="f6fe6-103">PidTagAttachContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="f6fe6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6fe6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f6fe6-105">Contém o cabeçalho de base de conteúdo de anexo de uma mensagem de email extensões MIME (Multipurpose Internet).</span><span class="sxs-lookup"><span data-stu-id="f6fe6-105">Contains the content base header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6fe6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f6fe6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6fe6-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span><span class="sxs-lookup"><span data-stu-id="f6fe6-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span></span>  <br/> |
|<span data-ttu-id="f6fe6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f6fe6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6fe6-109">0x3711</span><span class="sxs-lookup"><span data-stu-id="f6fe6-109">0x3711</span></span>  <br/> |
|<span data-ttu-id="f6fe6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f6fe6-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6fe6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f6fe6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f6fe6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f6fe6-112">Area:</span></span>  <br/> |<span data-ttu-id="f6fe6-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="f6fe6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6fe6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6fe6-114">Remarks</span></span>

<span data-ttu-id="f6fe6-115">Essas propriedades são usadas para suporte MHTML.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="f6fe6-116">Eles representam o cabeçalho de base de conteúdo para a parte apropriada do corpo MIME.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-116">They represent the content base header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f6fe6-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6fe6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f6fe6-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f6fe6-118">Protocol specifications</span></span>

<span data-ttu-id="f6fe6-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6fe6-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6fe6-120">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f6fe6-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f6fe6-121">Header files</span></span>

<span data-ttu-id="f6fe6-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6fe6-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6fe6-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6fe6-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f6fe6-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f6fe6-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6fe6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6fe6-126">See also</span></span>



[<span data-ttu-id="f6fe6-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f6fe6-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6fe6-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f6fe6-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6fe6-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f6fe6-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6fe6-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f6fe6-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

