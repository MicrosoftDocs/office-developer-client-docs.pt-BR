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
ms.openlocfilehash: 40e2efbf512265dffeee43d09e85879e8c3a0e56
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582417"
---
# <a name="pidtagattachcontentbase-canonical-property"></a><span data-ttu-id="10b5b-103">Propriedade canônica PidTagAttachContentBase</span><span class="sxs-lookup"><span data-stu-id="10b5b-103">PidTagAttachContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="10b5b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10b5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10b5b-105">Contém o cabeçalho de base de conteúdo de anexo de uma mensagem de email extensões MIME (Multipurpose Internet).</span><span class="sxs-lookup"><span data-stu-id="10b5b-105">Contains the content base header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10b5b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="10b5b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10b5b-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span><span class="sxs-lookup"><span data-stu-id="10b5b-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span></span>  <br/> |
|<span data-ttu-id="10b5b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="10b5b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="10b5b-109">0x3711</span><span class="sxs-lookup"><span data-stu-id="10b5b-109">0x3711</span></span>  <br/> |
|<span data-ttu-id="10b5b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="10b5b-110">Data type:</span></span>  <br/> |<span data-ttu-id="10b5b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="10b5b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="10b5b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="10b5b-112">Area:</span></span>  <br/> |<span data-ttu-id="10b5b-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="10b5b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10b5b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="10b5b-114">Remarks</span></span>

<span data-ttu-id="10b5b-115">Essas propriedades são usadas para suporte MHTML.</span><span class="sxs-lookup"><span data-stu-id="10b5b-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="10b5b-116">Eles representam o cabeçalho de base de conteúdo para a parte apropriada do corpo MIME.</span><span class="sxs-lookup"><span data-stu-id="10b5b-116">They represent the content base header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="10b5b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="10b5b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10b5b-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="10b5b-118">Protocol specifications</span></span>

<span data-ttu-id="10b5b-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10b5b-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10b5b-120">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="10b5b-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10b5b-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="10b5b-121">Header files</span></span>

<span data-ttu-id="10b5b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10b5b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="10b5b-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="10b5b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="10b5b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="10b5b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="10b5b-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="10b5b-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10b5b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="10b5b-126">See also</span></span>



[<span data-ttu-id="10b5b-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="10b5b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10b5b-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="10b5b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10b5b-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="10b5b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10b5b-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="10b5b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

