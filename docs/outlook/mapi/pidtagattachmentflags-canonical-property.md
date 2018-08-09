---
title: Propriedade canônica PidTagAttachmentFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentFlags
api_type:
- HeaderDef
ms.assetid: 42981aac-f9e7-45dd-91a2-15d9784f30aa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 825f6f1eff94635ca2d0f5226cfc3f421d41bcce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768987"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="0154b-103">Propriedade canônica PidTagAttachmentFlags</span><span class="sxs-lookup"><span data-stu-id="0154b-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="0154b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0154b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0154b-105">Indica a ação especial para este objeto Attachment.</span><span class="sxs-lookup"><span data-stu-id="0154b-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0154b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0154b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0154b-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="0154b-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="0154b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0154b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0154b-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="0154b-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="0154b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0154b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0154b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0154b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0154b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0154b-112">Area:</span></span>  <br/> |<span data-ttu-id="0154b-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="0154b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0154b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0154b-114">Remarks</span></span>

<span data-ttu-id="0154b-115">Deve ser 0x00000000, a menos que substituída por outros protocolos que estendem a mensagem e o protocolo do objeto Attachment conforme indicado no [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0154b-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0154b-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0154b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0154b-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0154b-117">Protocol specifications</span></span>

<span data-ttu-id="0154b-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0154b-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0154b-119">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="0154b-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="0154b-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0154b-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0154b-121">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="0154b-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0154b-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0154b-122">Header files</span></span>

<span data-ttu-id="0154b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0154b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0154b-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0154b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0154b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0154b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0154b-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0154b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0154b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0154b-127">See also</span></span>



[<span data-ttu-id="0154b-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0154b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0154b-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0154b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0154b-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0154b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0154b-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0154b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

