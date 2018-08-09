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
ms.openlocfilehash: b934f9694061e17118be35e3fabeeff3bbc61a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768959"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="614ae-103">Propriedade canônica PidTagAttachFlags</span><span class="sxs-lookup"><span data-stu-id="614ae-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="614ae-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="614ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="614ae-105">Contém uma bitmask dos sinalizadores para um anexo.</span><span class="sxs-lookup"><span data-stu-id="614ae-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="614ae-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="614ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="614ae-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="614ae-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="614ae-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="614ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="614ae-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="614ae-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="614ae-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="614ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="614ae-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="614ae-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="614ae-112">Área:</span><span class="sxs-lookup"><span data-stu-id="614ae-112">Area:</span></span>  <br/> |<span data-ttu-id="614ae-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="614ae-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="614ae-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="614ae-114">Remarks</span></span>

<span data-ttu-id="614ae-115">Essa propriedade é usada para suporte MHTML.</span><span class="sxs-lookup"><span data-stu-id="614ae-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="614ae-116">Um ou mais dos seguintes sinalizadores podem ser definidas para o bitmask **PR_ATTACH_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="614ae-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="614ae-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="614ae-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="614ae-118">Indica que este anexo não está disponível para aplicativos de renderização de HTML e deve ser ignorado em Multipurpose Internet Mail Extensions (MIME) processamento.</span><span class="sxs-lookup"><span data-stu-id="614ae-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="614ae-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="614ae-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="614ae-120">Indica que este anexo não está disponível para aplicativos de renderização em formato Rich Text (RTF) e deve ser ignorado pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="614ae-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="614ae-121">Se a propriedade **PR_ATTACH_FLAGS** for zero ou ausente, o anexo é a serem processados por todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="614ae-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="614ae-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="614ae-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="614ae-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="614ae-123">Protocol specifications</span></span>

<span data-ttu-id="614ae-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="614ae-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="614ae-125">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="614ae-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="614ae-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="614ae-126">Header files</span></span>

<span data-ttu-id="614ae-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="614ae-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="614ae-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="614ae-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="614ae-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="614ae-129">Mapitags.h</span></span>
  
> <span data-ttu-id="614ae-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="614ae-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="614ae-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="614ae-131">See also</span></span>



[<span data-ttu-id="614ae-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="614ae-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="614ae-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="614ae-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="614ae-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="614ae-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="614ae-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="614ae-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

