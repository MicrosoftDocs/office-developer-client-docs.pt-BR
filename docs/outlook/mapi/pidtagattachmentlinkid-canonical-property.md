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
ms.openlocfilehash: cd5a6071674dce97215bbeb7027752bfcedc94ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578070"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="eb856-103">Propriedade canônica PidTagAttachmentLinkId</span><span class="sxs-lookup"><span data-stu-id="eb856-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="eb856-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb856-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb856-105">Indica o tipo de objeto de mensagem à qual este anexo está vinculado.</span><span class="sxs-lookup"><span data-stu-id="eb856-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb856-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="eb856-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb856-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="eb856-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="eb856-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="eb856-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb856-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="eb856-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="eb856-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="eb856-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb856-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="eb856-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="eb856-112">Área:</span><span class="sxs-lookup"><span data-stu-id="eb856-112">Area:</span></span>  <br/> |<span data-ttu-id="eb856-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="eb856-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb856-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb856-114">Remarks</span></span>

<span data-ttu-id="eb856-115">Deve ser 0, a menos que substituída por outros protocolos que estendem a mensagem e o protocolo do objeto Attachment conforme indicado no [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="eb856-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eb856-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb856-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb856-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="eb856-117">Protocol specifications</span></span>

<span data-ttu-id="eb856-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb856-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb856-119">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="eb856-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="eb856-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb856-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb856-121">Especifica as propriedades e operações que são permitidas para os objetos de diário.</span><span class="sxs-lookup"><span data-stu-id="eb856-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="eb856-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb856-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb856-123">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="eb856-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eb856-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="eb856-124">Header files</span></span>

<span data-ttu-id="eb856-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb856-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb856-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="eb856-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb856-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eb856-127">Mapitags.h</span></span>
  
> <span data-ttu-id="eb856-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="eb856-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb856-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb856-129">See also</span></span>



[<span data-ttu-id="eb856-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="eb856-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb856-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="eb856-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb856-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="eb856-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb856-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="eb856-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

