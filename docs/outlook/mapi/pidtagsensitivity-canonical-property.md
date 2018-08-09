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
ms.openlocfilehash: 93be3351749ac3e9d285fb214f746d58b55fb5b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770013"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="27478-103">Propriedade canônica PidTagSensitivity</span><span class="sxs-lookup"><span data-stu-id="27478-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="27478-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27478-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27478-105">Contém um valor que indica a opinião do remetente da mensagem da sensibilidade de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="27478-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27478-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="27478-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27478-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="27478-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="27478-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="27478-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27478-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="27478-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="27478-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="27478-110">Data type:</span></span>  <br/> |<span data-ttu-id="27478-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="27478-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="27478-112">Área:</span><span class="sxs-lookup"><span data-stu-id="27478-112">Area:</span></span>  <br/> |<span data-ttu-id="27478-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="27478-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27478-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="27478-114">Remarks</span></span>

<span data-ttu-id="27478-115">É recomendável que os objetos de mensagem exponham essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="27478-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="27478-116">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="27478-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="27478-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="27478-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="27478-118">A mensagem não tem nenhuma sensibilidade especial.</span><span class="sxs-lookup"><span data-stu-id="27478-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="27478-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="27478-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="27478-120">A mensagem é pessoal.</span><span class="sxs-lookup"><span data-stu-id="27478-120">The message is personal.</span></span>
    
<span data-ttu-id="27478-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="27478-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="27478-122">A mensagem é particular.</span><span class="sxs-lookup"><span data-stu-id="27478-122">The message is private.</span></span>
    
<span data-ttu-id="27478-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="27478-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="27478-124">A mensagem é designada confidencial da empresa.</span><span class="sxs-lookup"><span data-stu-id="27478-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="27478-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="27478-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27478-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="27478-126">Protocol specifications</span></span>

<span data-ttu-id="27478-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27478-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27478-128">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="27478-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27478-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27478-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27478-130">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="27478-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27478-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="27478-131">Header files</span></span>

<span data-ttu-id="27478-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27478-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="27478-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="27478-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="27478-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="27478-134">Mapitags.h</span></span>
  
> <span data-ttu-id="27478-135">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="27478-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27478-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="27478-136">See also</span></span>



[<span data-ttu-id="27478-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="27478-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27478-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="27478-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27478-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="27478-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27478-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="27478-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

