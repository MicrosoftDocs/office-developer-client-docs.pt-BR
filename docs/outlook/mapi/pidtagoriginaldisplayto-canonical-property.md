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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342698"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a><span data-ttu-id="37840-103">Propriedade canônica PidTagOriginalDisplayTo</span><span class="sxs-lookup"><span data-stu-id="37840-103">PidTagOriginalDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="37840-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37840-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37840-105">Contém os nomes de exibição dos destinatários primários (para) da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="37840-105">Contains the display names of the primary (To) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37840-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="37840-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37840-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="37840-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="37840-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="37840-108">Identifier:</span></span>  <br/> |<span data-ttu-id="37840-109">0x0074</span><span class="sxs-lookup"><span data-stu-id="37840-109">0x0074</span></span>  <br/> |
|<span data-ttu-id="37840-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="37840-110">Data type:</span></span>  <br/> |<span data-ttu-id="37840-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="37840-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="37840-112">Área:</span><span class="sxs-lookup"><span data-stu-id="37840-112">Area:</span></span>  <br/> |<span data-ttu-id="37840-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="37840-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37840-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="37840-114">Remarks</span></span>

<span data-ttu-id="37840-115">Essas propriedades contêm uma lista ASCII separada por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="37840-115">These properties contain an ASCII list separated by semicolons.</span></span> <span data-ttu-id="37840-116">Ele é fornecido por MAPI e é copiado diretamente do **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) quando um relatório de entrega ou não entrega ou um relatório de leitura ou não leitura é gerado.</span><span class="sxs-lookup"><span data-stu-id="37840-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="37840-117">Essa propriedade pode estar presente em outras mensagens, conforme definido por suas classes de mensagens.</span><span class="sxs-lookup"><span data-stu-id="37840-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37840-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="37840-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37840-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="37840-119">Protocol specifications</span></span>

<span data-ttu-id="37840-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37840-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37840-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="37840-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37840-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37840-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37840-123">Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="37840-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37840-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="37840-124">Header files</span></span>

<span data-ttu-id="37840-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="37840-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="37840-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="37840-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="37840-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="37840-127">Mapitags.h</span></span>
  
> <span data-ttu-id="37840-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="37840-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37840-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="37840-129">See also</span></span>



[<span data-ttu-id="37840-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="37840-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37840-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="37840-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37840-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="37840-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37840-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="37840-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

