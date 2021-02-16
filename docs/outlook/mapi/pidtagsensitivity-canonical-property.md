---
title: Propriedade canônica PidTagSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eab8ce71d28a672d7069a1c16da5cd2cc2e149f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342501"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="780bc-103">Propriedade canônica PidTagSensitivity</span><span class="sxs-lookup"><span data-stu-id="780bc-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="780bc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="780bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="780bc-105">Contém um valor que indica a opinião do remetente da mensagem sobre a sensibilidade de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="780bc-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="780bc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="780bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="780bc-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="780bc-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="780bc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="780bc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="780bc-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="780bc-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="780bc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="780bc-110">Data type:</span></span>  <br/> |<span data-ttu-id="780bc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="780bc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="780bc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="780bc-112">Area:</span></span>  <br/> |<span data-ttu-id="780bc-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="780bc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="780bc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="780bc-114">Remarks</span></span>

<span data-ttu-id="780bc-115">É recomendável que os objetos de mensagem exponham essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="780bc-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="780bc-116">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="780bc-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="780bc-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="780bc-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="780bc-118">A mensagem não tem sensibilidade especial.</span><span class="sxs-lookup"><span data-stu-id="780bc-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="780bc-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="780bc-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="780bc-120">A mensagem é pessoal.</span><span class="sxs-lookup"><span data-stu-id="780bc-120">The message is personal.</span></span>
    
<span data-ttu-id="780bc-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="780bc-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="780bc-122">A mensagem é particular.</span><span class="sxs-lookup"><span data-stu-id="780bc-122">The message is private.</span></span>
    
<span data-ttu-id="780bc-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="780bc-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="780bc-124">A mensagem é designada como confidencial da empresa.</span><span class="sxs-lookup"><span data-stu-id="780bc-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="780bc-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="780bc-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="780bc-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="780bc-126">Protocol specifications</span></span>

<span data-ttu-id="780bc-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="780bc-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="780bc-128">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="780bc-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="780bc-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="780bc-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="780bc-130">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="780bc-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="780bc-131">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="780bc-131">Header files</span></span>

<span data-ttu-id="780bc-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="780bc-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="780bc-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="780bc-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="780bc-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="780bc-134">Mapitags.h</span></span>
  
> <span data-ttu-id="780bc-135">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="780bc-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="780bc-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="780bc-136">See also</span></span>



[<span data-ttu-id="780bc-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="780bc-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="780bc-138">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="780bc-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="780bc-139">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="780bc-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="780bc-140">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="780bc-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

