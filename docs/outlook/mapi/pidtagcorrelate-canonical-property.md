---
title: Propriedade canônica PidTagCorrelate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ea217808a163c7f16bbaa3c5a959fd32c8cbe10c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405216"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="a4454-103">Propriedade canônica PidTagCorrelate</span><span class="sxs-lookup"><span data-stu-id="a4454-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="a4454-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4454-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4454-105">Contém TRUE se o remetente de uma mensagem solicita o recurso de correlação do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a4454-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4454-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a4454-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4454-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="a4454-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="a4454-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a4454-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4454-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="a4454-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="a4454-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a4454-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4454-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a4454-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a4454-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a4454-112">Area:</span></span>  <br/> |<span data-ttu-id="a4454-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="a4454-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4454-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4454-114">Remarks</span></span>

<span data-ttu-id="a4454-115">Essa propriedade é usada para solicitar a correlação de relatórios de entrada com a mensagem enviada original.</span><span class="sxs-lookup"><span data-stu-id="a4454-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="a4454-116">Quando um provedor de transporte encontra  uma mensagem enviada com PR_CORRELATE definida como TRUE, ele define a propriedade **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) como o identificador do sistema de transferência de mensagens (MTS) para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="a4454-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="a4454-117">**PR_CORRELATE** deve ser usado com sistemas de mensagens que suportam correlação por identificador MTS, como X.400.</span><span class="sxs-lookup"><span data-stu-id="a4454-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a4454-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4454-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a4454-119">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="a4454-119">Header files</span></span>

<span data-ttu-id="a4454-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4454-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4454-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a4454-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="a4454-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a4454-122">Mapitags.h</span></span>
  
> <span data-ttu-id="a4454-123">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="a4454-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4454-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4454-124">See also</span></span>



[<span data-ttu-id="a4454-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a4454-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4454-126">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a4454-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4454-127">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a4454-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4454-128">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a4454-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

