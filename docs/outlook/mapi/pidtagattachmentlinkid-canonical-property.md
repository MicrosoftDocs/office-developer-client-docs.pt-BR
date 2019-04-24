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
ms.openlocfilehash: 623b4195b7128667b9aaa6bc97d03c21d62c690a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345693"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="0a8c3-103">Propriedade canônica PidTagAttachmentLinkId</span><span class="sxs-lookup"><span data-stu-id="0a8c3-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="0a8c3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a8c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a8c3-105">Indica o tipo de objeto Message ao qual esse anexo está vinculado.</span><span class="sxs-lookup"><span data-stu-id="0a8c3-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a8c3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0a8c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a8c3-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="0a8c3-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="0a8c3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0a8c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0a8c3-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="0a8c3-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="0a8c3-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0a8c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="0a8c3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0a8c3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0a8c3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0a8c3-112">Area:</span></span>  <br/> |<span data-ttu-id="0a8c3-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="0a8c3-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a8c3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a8c3-114">Remarks</span></span>

<span data-ttu-id="0a8c3-115">Deve ser 0, a menos que seja substituído por outros protocolos que estendem o protocolo de objeto Message e Attachment, conforme observado em [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0a8c3-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0a8c3-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a8c3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a8c3-117">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="0a8c3-117">Protocol specifications</span></span>

<span data-ttu-id="0a8c3-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a8c3-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a8c3-119">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="0a8c3-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="0a8c3-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a8c3-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a8c3-121">Especifica as propriedades e as operações que são permitidas para objetos de diário.</span><span class="sxs-lookup"><span data-stu-id="0a8c3-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="0a8c3-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a8c3-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a8c3-123">Especifica as propriedades e o modelo de interação para email e outros lembretes de objeto.</span><span class="sxs-lookup"><span data-stu-id="0a8c3-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a8c3-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0a8c3-124">Header files</span></span>

<span data-ttu-id="0a8c3-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0a8c3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a8c3-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0a8c3-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0a8c3-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0a8c3-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0a8c3-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0a8c3-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a8c3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a8c3-129">See also</span></span>



[<span data-ttu-id="0a8c3-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0a8c3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a8c3-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0a8c3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a8c3-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0a8c3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a8c3-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0a8c3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

