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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355619"
---
# <a name="pidtagoriginaldisplaycc-canonical-property"></a><span data-ttu-id="a7825-103">Propriedade canônica PidTagOriginalDisplayCc</span><span class="sxs-lookup"><span data-stu-id="a7825-103">PidTagOriginalDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="a7825-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7825-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7825-105">Contém os nomes de exibição de todos os destinatários de cópia carbono (CC) da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="a7825-105">Contains the display names of any carbon copy (CC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7825-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a7825-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7825-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="a7825-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="a7825-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a7825-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7825-109">0x0073</span><span class="sxs-lookup"><span data-stu-id="a7825-109">0x0073</span></span>  <br/> |
|<span data-ttu-id="a7825-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a7825-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7825-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a7825-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a7825-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a7825-112">Area:</span></span>  <br/> |<span data-ttu-id="a7825-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="a7825-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7825-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7825-114">Remarks</span></span>

<span data-ttu-id="a7825-115">Essas propriedades contêm uma lista separada por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="a7825-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="a7825-116">Ele é fornecido por MAPI e é copiado diretamente do **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) quando um relatório de entrega ou não entrega ou um relatório de leitura ou não leitura é gerado.</span><span class="sxs-lookup"><span data-stu-id="a7825-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="a7825-117">Essa propriedade pode estar presente em outras mensagens, conforme definido por suas classes de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a7825-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7825-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7825-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7825-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="a7825-119">Protocol specifications</span></span>

<span data-ttu-id="a7825-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7825-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7825-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a7825-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7825-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7825-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7825-123">Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a7825-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7825-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a7825-124">Header files</span></span>

<span data-ttu-id="a7825-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a7825-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7825-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a7825-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7825-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a7825-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a7825-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a7825-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7825-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7825-129">See also</span></span>



[<span data-ttu-id="a7825-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a7825-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7825-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a7825-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7825-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a7825-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7825-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a7825-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

