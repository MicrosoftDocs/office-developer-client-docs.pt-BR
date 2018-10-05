---
title: Propriedade canônica PidTagOriginalDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayBcc
api_type:
- COM
ms.assetid: 7bf66f0c-3095-4b4a-a32e-db278e1adc5a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3fbd7205901616695bcdcd012601afd252ac05f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396706"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="ee0dd-103">Propriedade canônica PidTagOriginalDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="ee0dd-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="ee0dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee0dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee0dd-105">Contém os nomes para exibição de qualquer destinatários de cópia oculta (Cco) da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="ee0dd-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee0dd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ee0dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee0dd-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="ee0dd-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="ee0dd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ee0dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee0dd-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="ee0dd-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="ee0dd-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ee0dd-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee0dd-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee0dd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ee0dd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ee0dd-112">Area:</span></span>  <br/> |<span data-ttu-id="ee0dd-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="ee0dd-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee0dd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee0dd-114">Remarks</span></span>

<span data-ttu-id="ee0dd-115">Essas propriedades contêm uma lista separada por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="ee0dd-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="ee0dd-116">Eles são fornecidos por MAPI e são copiados diretamente do **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) quando uma entrega ou relatório de não entrega ou uma leitura ou nonread relatório é gerado.</span><span class="sxs-lookup"><span data-stu-id="ee0dd-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="ee0dd-117">Essas propriedades podem estar presentes em outras mensagens, conforme definido pelas suas classes de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ee0dd-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ee0dd-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee0dd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee0dd-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ee0dd-119">Protocol specifications</span></span>

<span data-ttu-id="ee0dd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee0dd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee0dd-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ee0dd-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ee0dd-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee0dd-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee0dd-123">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="ee0dd-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee0dd-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ee0dd-124">Header files</span></span>

<span data-ttu-id="ee0dd-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee0dd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee0dd-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ee0dd-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee0dd-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ee0dd-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ee0dd-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ee0dd-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee0dd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee0dd-129">See also</span></span>



[<span data-ttu-id="ee0dd-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ee0dd-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee0dd-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ee0dd-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee0dd-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ee0dd-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee0dd-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ee0dd-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

