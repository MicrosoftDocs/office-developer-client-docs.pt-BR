---
title: Propriedade canônica PidTagJunkThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326849"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="e009a-103">Propriedade canônica PidTagJunkThreshold</span><span class="sxs-lookup"><span data-stu-id="e009a-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="e009a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e009a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e009a-105">Indica o quão agressivamente as mensagens de entrada devem ser enviadas para a pasta lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="e009a-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e009a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e009a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e009a-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="e009a-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="e009a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e009a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e009a-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="e009a-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="e009a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e009a-110">Data type:</span></span>  <br/> |<span data-ttu-id="e009a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e009a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e009a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e009a-112">Area:</span></span>  <br/> |<span data-ttu-id="e009a-113">Spam</span><span class="sxs-lookup"><span data-stu-id="e009a-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e009a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e009a-114">Remarks</span></span>

<span data-ttu-id="e009a-115">Essa propriedade corresponde à configuração de filtro alto/baixo/nenhuma.</span><span class="sxs-lookup"><span data-stu-id="e009a-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="e009a-116">Um valor de "0xFFFFFFFF" indica que a filtragem de spam não deve ser aplicada, mas listas de bloqueios ainda devem ser aplicadas.</span><span class="sxs-lookup"><span data-stu-id="e009a-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="e009a-117">Um valor de "0x80000000" indica que todos os emails são spam, exceto as mensagens dos remetentes na lista de remetentes confiáveis ou enviados para os destinatários na lista de destinatários confiáveis.</span><span class="sxs-lookup"><span data-stu-id="e009a-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="e009a-118">Os valores para isso são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="e009a-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="e009a-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e009a-119">**Value**</span></span>|<span data-ttu-id="e009a-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e009a-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e009a-121">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="e009a-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="e009a-122">Sem filtragem de spam</span><span class="sxs-lookup"><span data-stu-id="e009a-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="e009a-123">0x00000006</span><span class="sxs-lookup"><span data-stu-id="e009a-123">0x00000006</span></span>  <br/> |<span data-ttu-id="e009a-124">Filtragem de spam baixa</span><span class="sxs-lookup"><span data-stu-id="e009a-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="e009a-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="e009a-125">0x00000003</span></span>  <br/> |<span data-ttu-id="e009a-126">Filtragem alta de spam</span><span class="sxs-lookup"><span data-stu-id="e009a-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="e009a-127">0x80000000</span><span class="sxs-lookup"><span data-stu-id="e009a-127">0x80000000</span></span>  <br/> |<span data-ttu-id="e009a-128">Somente listas confiáveis</span><span class="sxs-lookup"><span data-stu-id="e009a-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e009a-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e009a-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e009a-130">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="e009a-130">Protocol specifications</span></span>

<span data-ttu-id="e009a-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e009a-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e009a-132">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e009a-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e009a-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e009a-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e009a-134">Permite a manipulação de listas de permissões/bloqueios e a determinação de mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="e009a-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e009a-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e009a-135">Header files</span></span>

<span data-ttu-id="e009a-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e009a-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="e009a-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e009a-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="e009a-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e009a-138">Mapitags.h</span></span>
  
> <span data-ttu-id="e009a-139">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e009a-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e009a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="e009a-140">See also</span></span>



[<span data-ttu-id="e009a-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e009a-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e009a-142">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e009a-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e009a-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e009a-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e009a-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e009a-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

