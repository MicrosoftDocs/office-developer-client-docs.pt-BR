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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387108"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="007dd-103">Propriedade canônica PidTagJunkThreshold</span><span class="sxs-lookup"><span data-stu-id="007dd-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="007dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="007dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="007dd-105">Indica o quão agressivamente emails de entrada devem ser enviada para a pasta Lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="007dd-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="007dd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="007dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="007dd-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="007dd-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="007dd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="007dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="007dd-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="007dd-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="007dd-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="007dd-110">Data type:</span></span>  <br/> |<span data-ttu-id="007dd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="007dd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="007dd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="007dd-112">Area:</span></span>  <br/> |<span data-ttu-id="007dd-113">Spam</span><span class="sxs-lookup"><span data-stu-id="007dd-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="007dd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="007dd-114">Remarks</span></span>

<span data-ttu-id="007dd-115">Essa propriedade corresponde à alta / baixa / nenhuma configuração de filtro.</span><span class="sxs-lookup"><span data-stu-id="007dd-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="007dd-116">Um valor de "0xFFFFFFFF" indica que a filtragem de spam não deve ser aplicada, no entanto, listas de bloqueio ainda devem ser aplicadas.</span><span class="sxs-lookup"><span data-stu-id="007dd-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="007dd-117">Um valor igual a "0x80000000" indica que todos os emails de spam, exceto as mensagens de remetentes na lista de remetentes confiáveis ou enviadas aos destinatários na lista de destinatários confiáveis.</span><span class="sxs-lookup"><span data-stu-id="007dd-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="007dd-118">Valores são:</span><span class="sxs-lookup"><span data-stu-id="007dd-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="007dd-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="007dd-119">**Value**</span></span>|<span data-ttu-id="007dd-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="007dd-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="007dd-121">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="007dd-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="007dd-122">Nenhuma filtragem de spam</span><span class="sxs-lookup"><span data-stu-id="007dd-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="007dd-123">0x00000006</span><span class="sxs-lookup"><span data-stu-id="007dd-123">0x00000006</span></span>  <br/> |<span data-ttu-id="007dd-124">Filtragem de spam baixa</span><span class="sxs-lookup"><span data-stu-id="007dd-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="007dd-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="007dd-125">0x00000003</span></span>  <br/> |<span data-ttu-id="007dd-126">Filtragem de spam de alta</span><span class="sxs-lookup"><span data-stu-id="007dd-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="007dd-127">0x80000000</span><span class="sxs-lookup"><span data-stu-id="007dd-127">0x80000000</span></span>  <br/> |<span data-ttu-id="007dd-128">Somente listas confiáveis</span><span class="sxs-lookup"><span data-stu-id="007dd-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="007dd-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="007dd-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="007dd-130">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="007dd-130">Protocol specifications</span></span>

<span data-ttu-id="007dd-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="007dd-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="007dd-132">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="007dd-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="007dd-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="007dd-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="007dd-134">Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="007dd-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="007dd-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="007dd-135">Header files</span></span>

<span data-ttu-id="007dd-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="007dd-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="007dd-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="007dd-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="007dd-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="007dd-138">Mapitags.h</span></span>
  
> <span data-ttu-id="007dd-139">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="007dd-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="007dd-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="007dd-140">See also</span></span>



[<span data-ttu-id="007dd-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="007dd-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="007dd-142">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="007dd-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="007dd-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="007dd-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="007dd-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="007dd-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

