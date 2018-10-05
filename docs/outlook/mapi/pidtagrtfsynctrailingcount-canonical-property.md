---
title: Propriedade canônica PidTagRtfSyncTrailingCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncTrailingCount
api_type:
- COM
ms.assetid: 3f0e5b24-767e-46f5-bb3d-e9cb82cb935b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 67093cf456db9df5f9e939bdda9d2e44f248dadc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397916"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a><span data-ttu-id="1f49e-103">Propriedade canônica PidTagRtfSyncTrailingCount</span><span class="sxs-lookup"><span data-stu-id="1f49e-103">PidTagRtfSyncTrailingCount Canonical Property</span></span>

  
  
<span data-ttu-id="1f49e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f49e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f49e-105">Contém uma contagem dos caracteres ignorável que aparecem após os caracteres significativos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1f49e-105">Contains a count of the ignorable characters that appear after the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f49e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1f49e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f49e-107">PR_RTF_SYNC_TRAILING_COUNT</span><span class="sxs-lookup"><span data-stu-id="1f49e-107">PR_RTF_SYNC_TRAILING_COUNT</span></span>  <br/> |
|<span data-ttu-id="1f49e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1f49e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f49e-109">0x1011</span><span class="sxs-lookup"><span data-stu-id="1f49e-109">0x1011</span></span>  <br/> |
|<span data-ttu-id="1f49e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1f49e-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f49e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1f49e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1f49e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1f49e-112">Area:</span></span>  <br/> |<span data-ttu-id="1f49e-113">Mensagem MAPI</span><span class="sxs-lookup"><span data-stu-id="1f49e-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f49e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f49e-114">Remarks</span></span>

<span data-ttu-id="1f49e-115">Essa propriedade é uma propriedade auxiliar de formato de texto Rich (RFT).</span><span class="sxs-lookup"><span data-stu-id="1f49e-115">This property is a Rich Text Format (RFT) auxiliary property.</span></span> <span data-ttu-id="1f49e-116">Essas propriedades são usadas pela função [RTFSync](rtfsync.md) e não se destina a ser usado diretamente por aplicativos do cliente.</span><span class="sxs-lookup"><span data-stu-id="1f49e-116">These properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1f49e-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f49e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f49e-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1f49e-118">Protocol specifications</span></span>

<span data-ttu-id="1f49e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f49e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f49e-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1f49e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f49e-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f49e-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f49e-122">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="1f49e-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f49e-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1f49e-123">Header files</span></span>

<span data-ttu-id="1f49e-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f49e-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f49e-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1f49e-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f49e-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f49e-126">Mapitags.h</span></span>
  
> <span data-ttu-id="1f49e-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1f49e-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f49e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f49e-128">See also</span></span>



[<span data-ttu-id="1f49e-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1f49e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f49e-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1f49e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f49e-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1f49e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f49e-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1f49e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

