---
title: Propriedade canônica PidTagRtfSyncBodyTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bad754d21652d3f5278a6dad3ec06f4a0b533036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769893"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="547db-103">Propriedade canônica PidTagRtfSyncBodyTag</span><span class="sxs-lookup"><span data-stu-id="547db-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="547db-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="547db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="547db-105">Contém caracteres significativos que aparecem no início do texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="547db-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="547db-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="547db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="547db-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="547db-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="547db-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="547db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="547db-109">0x1008 configurar</span><span class="sxs-lookup"><span data-stu-id="547db-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="547db-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="547db-110">Data type:</span></span>  <br/> |<span data-ttu-id="547db-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="547db-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="547db-112">Área:</span><span class="sxs-lookup"><span data-stu-id="547db-112">Area:</span></span>  <br/> |<span data-ttu-id="547db-113">Mensagem MAPI</span><span class="sxs-lookup"><span data-stu-id="547db-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="547db-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="547db-114">Remarks</span></span>

<span data-ttu-id="547db-115">A função [RTFSync](rtfsync.md) usa o rótulo de texto para indicar o início do texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="547db-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="547db-116">Quando o texto é modificado, a marca é usada para localizar o início do texto anterior.</span><span class="sxs-lookup"><span data-stu-id="547db-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="547db-117">Essas propriedades são propriedades auxiliares de formato Rich Text.</span><span class="sxs-lookup"><span data-stu-id="547db-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="547db-118">Eles são usados pela função **RTFSync** e não se destina a ser usado diretamente por aplicativos do cliente.</span><span class="sxs-lookup"><span data-stu-id="547db-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="547db-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="547db-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="547db-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="547db-120">Protocol specifications</span></span>

<span data-ttu-id="547db-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="547db-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="547db-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="547db-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="547db-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="547db-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="547db-124">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="547db-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="547db-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="547db-125">Header files</span></span>

<span data-ttu-id="547db-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="547db-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="547db-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="547db-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="547db-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="547db-128">Mapitags.h</span></span>
  
> <span data-ttu-id="547db-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="547db-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="547db-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="547db-130">See also</span></span>



[<span data-ttu-id="547db-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="547db-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="547db-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="547db-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="547db-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="547db-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="547db-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="547db-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
