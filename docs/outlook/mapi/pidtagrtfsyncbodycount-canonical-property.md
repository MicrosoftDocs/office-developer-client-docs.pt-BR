---
title: Propriedade canônica PidTagRtfSyncBodyCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b88c036b3bc9b29962204ea0b90bd460ee1cf90f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585168"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="45694-103">Propriedade canônica PidTagRtfSyncBodyCount</span><span class="sxs-lookup"><span data-stu-id="45694-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="45694-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45694-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45694-105">Contém uma contagem dos caracteres significativos do texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="45694-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45694-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="45694-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45694-107">PR_RTF_SYNC_BODY_COUNT</span><span class="sxs-lookup"><span data-stu-id="45694-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="45694-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="45694-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45694-109">0x1007</span><span class="sxs-lookup"><span data-stu-id="45694-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="45694-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="45694-110">Data type:</span></span>  <br/> |<span data-ttu-id="45694-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="45694-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="45694-112">Área:</span><span class="sxs-lookup"><span data-stu-id="45694-112">Area:</span></span>  <br/> |<span data-ttu-id="45694-113">Mensagem MAPI</span><span class="sxs-lookup"><span data-stu-id="45694-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45694-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="45694-114">Remarks</span></span>

<span data-ttu-id="45694-115">A função [RTFSync](rtfsync.md) calcula a contagem de caracteres no texto usando apenas aqueles que ele considera como significativo à mensagem.</span><span class="sxs-lookup"><span data-stu-id="45694-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="45694-116">Por exemplo, alguns espaços em branco e outros caracteres ignorável forem omitidos da contagem.</span><span class="sxs-lookup"><span data-stu-id="45694-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="45694-117">Essa propriedade é uma propriedade de auxiliar formato Rich Text (RTF).</span><span class="sxs-lookup"><span data-stu-id="45694-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="45694-118">Essas propriedades são usadas pela função **RTFSync** e não se destina a ser usado diretamente por aplicativos do cliente.</span><span class="sxs-lookup"><span data-stu-id="45694-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="45694-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="45694-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45694-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="45694-120">Protocol specifications</span></span>

<span data-ttu-id="45694-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45694-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45694-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="45694-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45694-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45694-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45694-124">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="45694-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45694-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="45694-125">Header files</span></span>

<span data-ttu-id="45694-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45694-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="45694-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="45694-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="45694-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45694-128">Mapitags.h</span></span>
  
> <span data-ttu-id="45694-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="45694-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45694-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="45694-130">See also</span></span>



[<span data-ttu-id="45694-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="45694-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45694-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="45694-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45694-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="45694-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45694-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="45694-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

