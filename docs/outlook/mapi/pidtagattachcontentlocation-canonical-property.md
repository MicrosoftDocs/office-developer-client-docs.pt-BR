---
title: Propriedade canônica PidTagAttachContentLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentLocation
api_type:
- HeaderDef
ms.assetid: af2f776c-1b77-4942-827a-4363eda3924f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1d654c2a14728979146ef09618bfc4e9e618f9d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594765"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="cf0ff-103">Propriedade canônica PidTagAttachContentLocation</span><span class="sxs-lookup"><span data-stu-id="cf0ff-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="cf0ff-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf0ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf0ff-105">Contém o cabeçalho de local do conteúdo de anexo de uma mensagem de email extensões MIME (Multipurpose Internet).</span><span class="sxs-lookup"><span data-stu-id="cf0ff-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf0ff-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cf0ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf0ff-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="cf0ff-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="cf0ff-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cf0ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cf0ff-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="cf0ff-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="cf0ff-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cf0ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="cf0ff-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cf0ff-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cf0ff-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cf0ff-112">Area:</span></span>  <br/> |<span data-ttu-id="cf0ff-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="cf0ff-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf0ff-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf0ff-114">Remarks</span></span>

<span data-ttu-id="cf0ff-115">Essas propriedades são usadas para suporte MHTML.</span><span class="sxs-lookup"><span data-stu-id="cf0ff-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="cf0ff-116">Eles representam o cabeçalho de local do conteúdo para a parte apropriada do corpo MIME.</span><span class="sxs-lookup"><span data-stu-id="cf0ff-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cf0ff-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf0ff-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cf0ff-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cf0ff-118">Protocol specifications</span></span>

<span data-ttu-id="cf0ff-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf0ff-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf0ff-120">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="cf0ff-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cf0ff-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cf0ff-121">Header files</span></span>

<span data-ttu-id="cf0ff-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf0ff-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf0ff-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cf0ff-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="cf0ff-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cf0ff-124">Mapitags.h</span></span>
  
> <span data-ttu-id="cf0ff-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="cf0ff-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf0ff-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf0ff-126">See also</span></span>



[<span data-ttu-id="cf0ff-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cf0ff-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf0ff-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cf0ff-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf0ff-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cf0ff-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf0ff-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cf0ff-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

