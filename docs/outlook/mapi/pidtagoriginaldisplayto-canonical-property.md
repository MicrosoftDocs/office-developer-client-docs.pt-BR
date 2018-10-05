---
title: Propriedade canônica PidTagOriginalDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayTo
api_type:
- COM
ms.assetid: 8c1cf14c-0339-4ced-8f68-4bfaa1e4d3e9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5a2f60051e5cb0717926a5c3e2f878a49919b04c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385064"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a><span data-ttu-id="d6e3c-103">Propriedade canônica PidTagOriginalDisplayTo</span><span class="sxs-lookup"><span data-stu-id="d6e3c-103">PidTagOriginalDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="d6e3c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6e3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6e3c-105">Contém os nomes de exibição dos (destinatários da mensagem original para) primário.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-105">Contains the display names of the primary (To) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6e3c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d6e3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6e3c-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="d6e3c-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="d6e3c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d6e3c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6e3c-109">0x0074</span><span class="sxs-lookup"><span data-stu-id="d6e3c-109">0x0074</span></span>  <br/> |
|<span data-ttu-id="d6e3c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d6e3c-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6e3c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6e3c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d6e3c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d6e3c-112">Area:</span></span>  <br/> |<span data-ttu-id="d6e3c-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="d6e3c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6e3c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6e3c-114">Remarks</span></span>

<span data-ttu-id="d6e3c-115">Essas propriedades contêm uma lista de ASCII, separada por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-115">These properties contain an ASCII list separated by semicolons.</span></span> <span data-ttu-id="d6e3c-116">Ele é fornecido pela MAPI e é copiado diretamente do **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) quando uma entrega ou o relatório de não entrega ou uma leitura ou nonread relatório é gerado.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="d6e3c-117">Essa propriedade pode estar presente em outras mensagens, conforme definido pelas suas classes de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d6e3c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6e3c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6e3c-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d6e3c-119">Protocol specifications</span></span>

<span data-ttu-id="d6e3c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6e3c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6e3c-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6e3c-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6e3c-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6e3c-123">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6e3c-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d6e3c-124">Header files</span></span>

<span data-ttu-id="d6e3c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6e3c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6e3c-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6e3c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d6e3c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d6e3c-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6e3c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6e3c-129">See also</span></span>



[<span data-ttu-id="d6e3c-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d6e3c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6e3c-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d6e3c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6e3c-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d6e3c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6e3c-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d6e3c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

