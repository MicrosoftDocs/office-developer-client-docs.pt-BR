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
ms.openlocfilehash: ec1db68d9168e7260a32aaf7708897df6124725a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360505"
---
# <a name="pidtagattachcontentbase-canonical-property"></a><span data-ttu-id="4a0ff-103">Propriedade canônica PidTagAttachContentBase</span><span class="sxs-lookup"><span data-stu-id="4a0ff-103">PidTagAttachContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="4a0ff-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a0ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a0ff-105">Contém o cabeçalho base de conteúdo de um anexo de mensagem MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="4a0ff-105">Contains the content base header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a0ff-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4a0ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a0ff-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span><span class="sxs-lookup"><span data-stu-id="4a0ff-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span></span>  <br/> |
|<span data-ttu-id="4a0ff-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4a0ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a0ff-109">0x3711</span><span class="sxs-lookup"><span data-stu-id="4a0ff-109">0x3711</span></span>  <br/> |
|<span data-ttu-id="4a0ff-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4a0ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a0ff-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4a0ff-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4a0ff-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4a0ff-112">Area:</span></span>  <br/> |<span data-ttu-id="4a0ff-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="4a0ff-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a0ff-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a0ff-114">Remarks</span></span>

<span data-ttu-id="4a0ff-115">Essas propriedades são usadas para suporte a MHTML.</span><span class="sxs-lookup"><span data-stu-id="4a0ff-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="4a0ff-116">Eles representam o cabeçalho base de conteúdo para a parte apropriada do corpo MIME.</span><span class="sxs-lookup"><span data-stu-id="4a0ff-116">They represent the content base header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4a0ff-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a0ff-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a0ff-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="4a0ff-118">Protocol specifications</span></span>

<span data-ttu-id="4a0ff-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a0ff-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a0ff-120">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="4a0ff-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a0ff-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4a0ff-121">Header files</span></span>

<span data-ttu-id="4a0ff-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4a0ff-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a0ff-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4a0ff-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a0ff-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4a0ff-124">Mapitags.h</span></span>
  
> <span data-ttu-id="4a0ff-125">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="4a0ff-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a0ff-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a0ff-126">See also</span></span>



[<span data-ttu-id="4a0ff-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4a0ff-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a0ff-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4a0ff-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a0ff-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4a0ff-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a0ff-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4a0ff-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

