---
title: Propriedade canônica PidTagOriginalDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayCc
api_type:
- COM
ms.assetid: f48d723c-3ad8-4617-952a-ba5216b2129c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9eb90d353705434803ff617ff2b355c7c96359b7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401528"
---
# <a name="pidtagoriginaldisplaycc-canonical-property"></a><span data-ttu-id="88820-103">Propriedade canônica PidTagOriginalDisplayCc</span><span class="sxs-lookup"><span data-stu-id="88820-103">PidTagOriginalDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="88820-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88820-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88820-105">Contém os nomes para exibição de qualquer destinatários de cópia carbono (CC) da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="88820-105">Contains the display names of any carbon copy (CC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88820-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="88820-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88820-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="88820-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="88820-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="88820-108">Identifier:</span></span>  <br/> |<span data-ttu-id="88820-109">0x0073</span><span class="sxs-lookup"><span data-stu-id="88820-109">0x0073</span></span>  <br/> |
|<span data-ttu-id="88820-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="88820-110">Data type:</span></span>  <br/> |<span data-ttu-id="88820-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="88820-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="88820-112">Área:</span><span class="sxs-lookup"><span data-stu-id="88820-112">Area:</span></span>  <br/> |<span data-ttu-id="88820-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="88820-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88820-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="88820-114">Remarks</span></span>

<span data-ttu-id="88820-115">Essas propriedades contêm uma lista separada por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="88820-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="88820-116">Ele é fornecido pela MAPI e é copiado diretamente do **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) quando uma entrega ou o relatório de não entrega ou uma leitura ou nonread relatório é gerado.</span><span class="sxs-lookup"><span data-stu-id="88820-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="88820-117">Essa propriedade pode estar presente em outras mensagens, conforme definido pelas suas classes de mensagens.</span><span class="sxs-lookup"><span data-stu-id="88820-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="88820-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="88820-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88820-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="88820-119">Protocol specifications</span></span>

<span data-ttu-id="88820-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88820-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88820-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="88820-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="88820-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88820-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88820-123">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="88820-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88820-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="88820-124">Header files</span></span>

<span data-ttu-id="88820-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88820-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="88820-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="88820-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="88820-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="88820-127">Mapitags.h</span></span>
  
> <span data-ttu-id="88820-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="88820-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88820-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="88820-129">See also</span></span>



[<span data-ttu-id="88820-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="88820-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88820-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="88820-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88820-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="88820-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88820-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="88820-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

