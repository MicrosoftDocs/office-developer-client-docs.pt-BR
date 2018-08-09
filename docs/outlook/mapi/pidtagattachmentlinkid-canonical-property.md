---
title: Propriedade canônica PidTagAttachmentLinkId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentLinkId
api_type:
- HeaderDef
ms.assetid: 5d0daae7-248d-459f-9d96-cb949b86f590
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e467fb7c05a647265d007429930ee522fd77b2fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768968"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="9f73e-103">Propriedade canônica PidTagAttachmentLinkId</span><span class="sxs-lookup"><span data-stu-id="9f73e-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="9f73e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f73e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f73e-105">Indica o tipo de objeto de mensagem à qual este anexo está vinculado.</span><span class="sxs-lookup"><span data-stu-id="9f73e-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f73e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9f73e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f73e-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="9f73e-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="9f73e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9f73e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f73e-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="9f73e-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="9f73e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9f73e-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f73e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9f73e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9f73e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9f73e-112">Area:</span></span>  <br/> |<span data-ttu-id="9f73e-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="9f73e-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f73e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f73e-114">Remarks</span></span>

<span data-ttu-id="9f73e-115">Deve ser 0, a menos que substituída por outros protocolos que estendem a mensagem e o protocolo do objeto Attachment conforme indicado no [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f73e-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9f73e-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f73e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f73e-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9f73e-117">Protocol specifications</span></span>

<span data-ttu-id="9f73e-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f73e-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f73e-119">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="9f73e-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9f73e-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f73e-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f73e-121">Especifica as propriedades e operações que são permitidas para os objetos de diário.</span><span class="sxs-lookup"><span data-stu-id="9f73e-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="9f73e-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f73e-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f73e-123">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="9f73e-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f73e-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9f73e-124">Header files</span></span>

<span data-ttu-id="9f73e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f73e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f73e-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9f73e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9f73e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9f73e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9f73e-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9f73e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f73e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f73e-129">See also</span></span>



[<span data-ttu-id="9f73e-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9f73e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f73e-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="9f73e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f73e-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9f73e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f73e-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9f73e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

