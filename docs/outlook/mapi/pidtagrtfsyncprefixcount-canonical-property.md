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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389810"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="c9d31-103">Propriedade canônica PidTagRtfSyncPrefixCount</span><span class="sxs-lookup"><span data-stu-id="c9d31-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="c9d31-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9d31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9d31-105">Contém uma contagem dos caracteres ignorável que aparecem antes dos caracteres significativos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c9d31-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9d31-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c9d31-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9d31-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="c9d31-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="c9d31-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c9d31-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9d31-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="c9d31-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="c9d31-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c9d31-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9d31-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c9d31-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c9d31-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c9d31-112">Area:</span></span>  <br/> |<span data-ttu-id="c9d31-113">Mensagem MAPI</span><span class="sxs-lookup"><span data-stu-id="c9d31-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9d31-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9d31-114">Remarks</span></span>

<span data-ttu-id="c9d31-115">A contagem de caracteres de prefixo não inclui espaços em branco.</span><span class="sxs-lookup"><span data-stu-id="c9d31-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="c9d31-116">Essa propriedade é uma propriedade de auxiliar formato Rich Text (RTF).</span><span class="sxs-lookup"><span data-stu-id="c9d31-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="c9d31-117">Propriedades de auxiliar RTF são usadas pela função [RTFSync](rtfsync.md) e não se destina a ser usado diretamente por aplicativos do cliente.</span><span class="sxs-lookup"><span data-stu-id="c9d31-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c9d31-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9d31-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c9d31-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c9d31-119">Protocol specifications</span></span>

<span data-ttu-id="c9d31-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9d31-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9d31-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c9d31-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c9d31-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9d31-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9d31-123">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="c9d31-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9d31-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c9d31-124">Header files</span></span>

<span data-ttu-id="c9d31-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9d31-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9d31-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c9d31-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9d31-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9d31-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c9d31-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c9d31-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9d31-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9d31-129">See also</span></span>



[<span data-ttu-id="c9d31-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c9d31-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9d31-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c9d31-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9d31-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c9d31-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9d31-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c9d31-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

