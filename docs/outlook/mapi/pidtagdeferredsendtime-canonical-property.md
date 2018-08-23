---
title: Propriedade canônica PidTagDeferredSendTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f636c0a49d6ad96ab157d00780fa6ffc5c8f3236
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588269"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="560ba-103">Propriedade canônica PidTagDeferredSendTime</span><span class="sxs-lookup"><span data-stu-id="560ba-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="560ba-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="560ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="560ba-105">Indica um horário quando um cliente gostaria para adiar a enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="560ba-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="560ba-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="560ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="560ba-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="560ba-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="560ba-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="560ba-108">Identifier:</span></span>  <br/> |<span data-ttu-id="560ba-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="560ba-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="560ba-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="560ba-110">Data type:</span></span>  <br/> |<span data-ttu-id="560ba-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="560ba-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="560ba-112">Área:</span><span class="sxs-lookup"><span data-stu-id="560ba-112">Area:</span></span>  <br/> |<span data-ttu-id="560ba-113">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="560ba-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="560ba-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="560ba-114">Remarks</span></span>

<span data-ttu-id="560ba-115">Se as propriedades de **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) e o **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) estiverem presentes, o valor dessa propriedade é recalculado usando a seguinte fórmula e o valor antigo será ignorado.</span><span class="sxs-lookup"><span data-stu-id="560ba-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="560ba-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf (**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="560ba-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="560ba-117">Se o valor **PR_DEFERRED_SEND_TIME** for anterior a hora atual (em UTC), a mensagem é enviada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="560ba-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="560ba-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="560ba-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="560ba-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="560ba-119">Protocol specifications</span></span>

<span data-ttu-id="560ba-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="560ba-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="560ba-121">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="560ba-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="560ba-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="560ba-122">Header files</span></span>

<span data-ttu-id="560ba-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="560ba-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="560ba-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="560ba-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="560ba-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="560ba-125">Mapitags.h</span></span>
  
> <span data-ttu-id="560ba-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="560ba-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="560ba-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="560ba-127">See also</span></span>



[<span data-ttu-id="560ba-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="560ba-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="560ba-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="560ba-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="560ba-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="560ba-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="560ba-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="560ba-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

