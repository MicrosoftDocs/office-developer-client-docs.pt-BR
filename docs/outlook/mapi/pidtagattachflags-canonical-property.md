---
title: Propriedade canônica PidTagAttachFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339330"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="9fa8c-103">Propriedade canônica PidTagAttachFlags</span><span class="sxs-lookup"><span data-stu-id="9fa8c-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="9fa8c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fa8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fa8c-105">Contém uma bitmask de sinalizadores de um anexo.</span><span class="sxs-lookup"><span data-stu-id="9fa8c-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9fa8c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9fa8c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9fa8c-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="9fa8c-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="9fa8c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9fa8c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9fa8c-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="9fa8c-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="9fa8c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9fa8c-110">Data type:</span></span>  <br/> |<span data-ttu-id="9fa8c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9fa8c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9fa8c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9fa8c-112">Area:</span></span>  <br/> |<span data-ttu-id="9fa8c-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="9fa8c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fa8c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fa8c-114">Remarks</span></span>

<span data-ttu-id="9fa8c-115">Essa propriedade é usada para suporte a MHTML.</span><span class="sxs-lookup"><span data-stu-id="9fa8c-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="9fa8c-116">Um ou mais dos seguintes sinalizadores podem ser definidos para o bitmask **PR_ATTACH_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="9fa8c-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="9fa8c-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="9fa8c-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="9fa8c-118">Indica que esse anexo não está disponível para aplicativos de renderização HTML e deve ser ignorado no processamento MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="9fa8c-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="9fa8c-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="9fa8c-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="9fa8c-120">Indica que esse anexo não está disponível para processamento de aplicativos no formato Rich Text (RTF) e deve ser ignorado por MAPI.</span><span class="sxs-lookup"><span data-stu-id="9fa8c-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="9fa8c-121">Se a propriedade **PR_ATTACH_FLAGS** for zero ou ausente, o anexo será processado por todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9fa8c-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9fa8c-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fa8c-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9fa8c-123">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="9fa8c-123">Protocol specifications</span></span>

<span data-ttu-id="9fa8c-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9fa8c-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9fa8c-125">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="9fa8c-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9fa8c-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9fa8c-126">Header files</span></span>

<span data-ttu-id="9fa8c-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9fa8c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9fa8c-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9fa8c-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="9fa8c-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9fa8c-129">Mapitags.h</span></span>
  
> <span data-ttu-id="9fa8c-130">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9fa8c-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9fa8c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fa8c-131">See also</span></span>



[<span data-ttu-id="9fa8c-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9fa8c-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9fa8c-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9fa8c-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9fa8c-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9fa8c-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9fa8c-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9fa8c-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

