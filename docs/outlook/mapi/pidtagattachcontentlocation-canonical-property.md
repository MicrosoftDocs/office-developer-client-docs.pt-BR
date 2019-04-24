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
ms.openlocfilehash: f279d8ea305c0b1e609881b15e39653c41d5828e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345476"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="d81a3-103">Propriedade canônica PidTagAttachContentLocation</span><span class="sxs-lookup"><span data-stu-id="d81a3-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="d81a3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d81a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d81a3-105">Contém o cabeçalho de local de conteúdo de um anexo de mensagem MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="d81a3-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d81a3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d81a3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d81a3-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="d81a3-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="d81a3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d81a3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d81a3-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="d81a3-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="d81a3-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d81a3-110">Data type:</span></span>  <br/> |<span data-ttu-id="d81a3-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d81a3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d81a3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d81a3-112">Area:</span></span>  <br/> |<span data-ttu-id="d81a3-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="d81a3-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d81a3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d81a3-114">Remarks</span></span>

<span data-ttu-id="d81a3-115">Essas propriedades são usadas para suporte a MHTML.</span><span class="sxs-lookup"><span data-stu-id="d81a3-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="d81a3-116">Eles representam o cabeçalho de local de conteúdo para a parte de corpo MIME apropriada.</span><span class="sxs-lookup"><span data-stu-id="d81a3-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d81a3-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d81a3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d81a3-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="d81a3-118">Protocol specifications</span></span>

<span data-ttu-id="d81a3-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d81a3-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d81a3-120">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="d81a3-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d81a3-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d81a3-121">Header files</span></span>

<span data-ttu-id="d81a3-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d81a3-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="d81a3-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d81a3-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="d81a3-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d81a3-124">Mapitags.h</span></span>
  
> <span data-ttu-id="d81a3-125">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d81a3-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d81a3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d81a3-126">See also</span></span>



[<span data-ttu-id="d81a3-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d81a3-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d81a3-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d81a3-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d81a3-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d81a3-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d81a3-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d81a3-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

