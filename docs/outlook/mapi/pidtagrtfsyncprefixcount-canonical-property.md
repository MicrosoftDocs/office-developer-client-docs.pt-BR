---
title: Propriedade canônica PidTagRtfSyncPrefixCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncPrefixCount
api_type:
- COM
ms.assetid: c2b15ac5-9e89-4ee2-812d-102d0b2ac56e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 61683534504b7451f126591af149d11306cff1bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357859"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="0c3db-103">Propriedade canônica PidTagRtfSyncPrefixCount</span><span class="sxs-lookup"><span data-stu-id="0c3db-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="0c3db-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c3db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c3db-105">Contém uma contagem dos caracteres ignorable que aparecem antes dos caracteres significativos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0c3db-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c3db-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0c3db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c3db-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="0c3db-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="0c3db-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0c3db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0c3db-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="0c3db-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="0c3db-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0c3db-110">Data type:</span></span>  <br/> |<span data-ttu-id="0c3db-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0c3db-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0c3db-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0c3db-112">Area:</span></span>  <br/> |<span data-ttu-id="0c3db-113">Mensagem MAPI</span><span class="sxs-lookup"><span data-stu-id="0c3db-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c3db-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c3db-114">Remarks</span></span>

<span data-ttu-id="0c3db-115">A contagem de caracteres de prefixo não inclui espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="0c3db-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="0c3db-116">Esta propriedade é uma propriedade auxiliar do formato Rich Text (RTF).</span><span class="sxs-lookup"><span data-stu-id="0c3db-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="0c3db-117">As propriedades auxiliares de RTF são usadas pela função [RTFSync](rtfsync.md) e não se destinam a ser usadas diretamente por aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="0c3db-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0c3db-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c3db-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c3db-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="0c3db-119">Protocol specifications</span></span>

<span data-ttu-id="0c3db-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c3db-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c3db-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0c3db-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c3db-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c3db-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c3db-123">Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="0c3db-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c3db-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0c3db-124">Header files</span></span>

<span data-ttu-id="0c3db-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0c3db-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c3db-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0c3db-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0c3db-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0c3db-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0c3db-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0c3db-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c3db-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c3db-129">See also</span></span>



[<span data-ttu-id="0c3db-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0c3db-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c3db-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0c3db-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c3db-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0c3db-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c3db-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0c3db-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

