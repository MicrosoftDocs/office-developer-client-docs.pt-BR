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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355640"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="21199-103">Propriedade canônica PidTagOriginalDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="21199-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="21199-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21199-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21199-105">Contém os nomes de exibição de qualquer destinatário de cópia oculta (Cco) da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="21199-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21199-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="21199-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21199-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="21199-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="21199-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="21199-108">Identifier:</span></span>  <br/> |<span data-ttu-id="21199-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="21199-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="21199-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="21199-110">Data type:</span></span>  <br/> |<span data-ttu-id="21199-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="21199-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="21199-112">Área:</span><span class="sxs-lookup"><span data-stu-id="21199-112">Area:</span></span>  <br/> |<span data-ttu-id="21199-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="21199-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21199-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="21199-114">Remarks</span></span>

<span data-ttu-id="21199-115">Essas propriedades contêm uma lista separada por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="21199-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="21199-116">Eles são fornecidos pelo MAPI e são copiados diretamente do **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) quando um relatório de entrega ou não entrega ou um relatório de leitura ou não leitura é gerado.</span><span class="sxs-lookup"><span data-stu-id="21199-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="21199-117">Essas propriedades podem estar presentes em outras mensagens, conforme definido por suas classes de mensagens.</span><span class="sxs-lookup"><span data-stu-id="21199-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="21199-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="21199-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="21199-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="21199-119">Protocol specifications</span></span>

<span data-ttu-id="21199-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21199-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21199-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="21199-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="21199-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21199-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21199-123">Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="21199-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="21199-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="21199-124">Header files</span></span>

<span data-ttu-id="21199-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="21199-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="21199-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="21199-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="21199-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="21199-127">Mapitags.h</span></span>
  
> <span data-ttu-id="21199-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="21199-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21199-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="21199-129">See also</span></span>



[<span data-ttu-id="21199-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="21199-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21199-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="21199-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21199-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="21199-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21199-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="21199-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

