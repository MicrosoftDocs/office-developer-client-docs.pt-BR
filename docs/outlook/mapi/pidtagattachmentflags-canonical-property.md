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
ms.openlocfilehash: d494f1f14daff75be55e910da56204ecb3dbcf83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345793"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="55fde-103">Propriedade canônica PidTagAttachmentFlags</span><span class="sxs-lookup"><span data-stu-id="55fde-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="55fde-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55fde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55fde-105">Indica uma manipulação especial para este objeto Attachment.</span><span class="sxs-lookup"><span data-stu-id="55fde-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55fde-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="55fde-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55fde-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="55fde-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="55fde-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="55fde-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55fde-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="55fde-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="55fde-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="55fde-110">Data type:</span></span>  <br/> |<span data-ttu-id="55fde-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="55fde-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="55fde-112">Área:</span><span class="sxs-lookup"><span data-stu-id="55fde-112">Area:</span></span>  <br/> |<span data-ttu-id="55fde-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="55fde-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55fde-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="55fde-114">Remarks</span></span>

<span data-ttu-id="55fde-115">Deve ser 0x00000000, a menos que seja substituído por outros protocolos que estendem o Protocolo de Objeto de Anexo e Mensagem, conforme notado [em [MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55fde-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55fde-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="55fde-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55fde-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="55fde-117">Protocol specifications</span></span>

<span data-ttu-id="55fde-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55fde-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55fde-119">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="55fde-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="55fde-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55fde-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55fde-121">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="55fde-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55fde-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="55fde-122">Header files</span></span>

<span data-ttu-id="55fde-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55fde-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="55fde-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="55fde-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="55fde-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55fde-125">Mapitags.h</span></span>
  
> <span data-ttu-id="55fde-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="55fde-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55fde-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="55fde-127">See also</span></span>



[<span data-ttu-id="55fde-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="55fde-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55fde-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="55fde-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55fde-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="55fde-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55fde-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="55fde-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

