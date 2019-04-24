---
title: Propriedade canônica PidTagRtfSyncBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 85ac61d968243283e5ad9283730941adcd87cd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357866"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a><span data-ttu-id="fd801-103">Propriedade canônica PidTagRtfSyncBodyCrc</span><span class="sxs-lookup"><span data-stu-id="fd801-103">PidTagRtfSyncBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="fd801-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd801-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd801-105">Contém a verificação de redundância cíclica (CRC) calculada para o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="fd801-105">Contains the cyclical redundancy check (CRC) computed for the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd801-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fd801-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd801-107">PR_RTF_SYNC_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="fd801-107">PR_RTF_SYNC_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="fd801-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fd801-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fd801-109">0x1006</span><span class="sxs-lookup"><span data-stu-id="fd801-109">0x1006</span></span>  <br/> |
|<span data-ttu-id="fd801-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fd801-110">Data type:</span></span>  <br/> |<span data-ttu-id="fd801-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fd801-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fd801-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fd801-112">Area:</span></span>  <br/> |<span data-ttu-id="fd801-113">Mensagem MAPI</span><span class="sxs-lookup"><span data-stu-id="fd801-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd801-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd801-114">Remarks</span></span>

<span data-ttu-id="fd801-115">A função [RTFSync](rtfsync.md) COMPUTA o CRC usando apenas os caracteres que ele considera significativos para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="fd801-115">The [RTFSync](rtfsync.md) function computes the CRC by using only the characters that it considers to be significant to the message.</span></span> <span data-ttu-id="fd801-116">Por exemplo, alguns espaços em branco e outros caracteres ignoráveis são omitidos do CRC.</span><span class="sxs-lookup"><span data-stu-id="fd801-116">For example, some white space and other ignorable characters are omitted from the CRC.</span></span> 
  
<span data-ttu-id="fd801-117">Esta propriedade é uma propriedade auxiliar do formato Rich Text (RTF).</span><span class="sxs-lookup"><span data-stu-id="fd801-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="fd801-118">Essas propriedades são usadas pela função **RTFSync** e não devem ser usadas diretamente por aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="fd801-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fd801-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd801-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd801-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="fd801-120">Protocol specifications</span></span>

<span data-ttu-id="fd801-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd801-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd801-122">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fd801-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fd801-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd801-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd801-124">Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="fd801-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd801-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fd801-125">Header files</span></span>

<span data-ttu-id="fd801-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fd801-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd801-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fd801-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="fd801-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="fd801-128">Mapitags.h</span></span>
  
> <span data-ttu-id="fd801-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fd801-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd801-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd801-130">See also</span></span>



[<span data-ttu-id="fd801-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fd801-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd801-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fd801-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd801-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fd801-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd801-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fd801-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

