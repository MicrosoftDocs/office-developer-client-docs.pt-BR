---
title: Propriedade canônica PidTagRecipientTrackStatusTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatusTime
api_type:
- COM
ms.assetid: f14dfe47-a9f8-4475-bb26-7da3411d8c6f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8b7263fc408bd2c3f6838e571407ed8984c61427
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582760"
---
# <a name="pidtagrecipienttrackstatustime-canonical-property"></a><span data-ttu-id="32259-103">Propriedade canônica PidTagRecipientTrackStatusTime</span><span class="sxs-lookup"><span data-stu-id="32259-103">PidTagRecipientTrackStatusTime Canonical Property</span></span>

  
  
<span data-ttu-id="32259-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32259-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32259-105">Contém a data e hora de quando o participante respondido.</span><span class="sxs-lookup"><span data-stu-id="32259-105">Contains the date and time when the attendee responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="32259-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="32259-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="32259-107">PR_RECIPIENT_TRACKSTATUS_TIME</span><span class="sxs-lookup"><span data-stu-id="32259-107">PR_RECIPIENT_TRACKSTATUS_TIME</span></span>  <br/> |
|<span data-ttu-id="32259-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="32259-108">Identifier:</span></span>  <br/> |<span data-ttu-id="32259-109">0x5FFB</span><span class="sxs-lookup"><span data-stu-id="32259-109">0x5FFB</span></span>  <br/> |
|<span data-ttu-id="32259-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="32259-110">Data type:</span></span>  <br/> |<span data-ttu-id="32259-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="32259-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="32259-112">Área:</span><span class="sxs-lookup"><span data-stu-id="32259-112">Area:</span></span>  <br/> |<span data-ttu-id="32259-113">Destinatário de transporte</span><span class="sxs-lookup"><span data-stu-id="32259-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32259-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="32259-114">Remarks</span></span>

<span data-ttu-id="32259-115">O valor deve ser especificado no tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="32259-115">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="32259-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="32259-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="32259-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="32259-117">Protocol specifications</span></span>

<span data-ttu-id="32259-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32259-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32259-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="32259-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="32259-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32259-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32259-121">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="32259-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="32259-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="32259-122">Header files</span></span>

<span data-ttu-id="32259-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="32259-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="32259-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="32259-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="32259-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="32259-125">Mapitags.h</span></span>
  
> <span data-ttu-id="32259-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="32259-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32259-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="32259-127">See also</span></span>



[<span data-ttu-id="32259-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="32259-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="32259-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="32259-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="32259-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="32259-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="32259-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="32259-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

