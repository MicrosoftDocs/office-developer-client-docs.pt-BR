---
title: Propriedade canônica PidTagOwnerAppointmentId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnerAppointmentId
api_type:
- COM
ms.assetid: b5eea554-6bca-42d1-b943-1327f0d70584
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7ad68a8ba527879871e79dd85e79d577291d32a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335438"
---
# <a name="pidtagownerappointmentid-canonical-property"></a><span data-ttu-id="8393b-103">Propriedade canônica PidTagOwnerAppointmentId</span><span class="sxs-lookup"><span data-stu-id="8393b-103">PidTagOwnerAppointmentId Canonical Property</span></span>

  
  
<span data-ttu-id="8393b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8393b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8393b-105">Contém um identificador para um compromisso na agenda do proprietário.</span><span class="sxs-lookup"><span data-stu-id="8393b-105">Contains an identifier for an appointment in the owner's schedule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8393b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8393b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8393b-107">PR_OWNER_APPT_ID</span><span class="sxs-lookup"><span data-stu-id="8393b-107">PR_OWNER_APPT_ID</span></span>  <br/> |
|<span data-ttu-id="8393b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8393b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8393b-109">0x0062</span><span class="sxs-lookup"><span data-stu-id="8393b-109">0x0062</span></span>  <br/> |
|<span data-ttu-id="8393b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8393b-110">Data type:</span></span>  <br/> |<span data-ttu-id="8393b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8393b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8393b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8393b-112">Area:</span></span>  <br/> |<span data-ttu-id="8393b-113">Compromisso</span><span class="sxs-lookup"><span data-stu-id="8393b-113">Appointment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8393b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8393b-114">Remarks</span></span>

<span data-ttu-id="8393b-115">Essa propriedade é usada em solicitações de reunião.</span><span class="sxs-lookup"><span data-stu-id="8393b-115">This property is used in meeting requests.</span></span> <span data-ttu-id="8393b-116">Ele não representa um identificador de entrada, mas um inteiro longo que identifica exclusivamente o compromisso dentro da agenda do remetente.</span><span class="sxs-lookup"><span data-stu-id="8393b-116">It does not represent an entry identifier, but a long integer that uniquely identifies the appointment within the sender's schedule.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8393b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8393b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8393b-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8393b-118">Protocol specifications</span></span>

<span data-ttu-id="8393b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8393b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8393b-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8393b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8393b-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8393b-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8393b-122">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="8393b-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8393b-123">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8393b-123">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8393b-124">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="8393b-124">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8393b-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8393b-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8393b-126">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente de fluxo.</span><span class="sxs-lookup"><span data-stu-id="8393b-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8393b-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="8393b-127">Header files</span></span>

<span data-ttu-id="8393b-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8393b-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="8393b-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8393b-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="8393b-130">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8393b-130">mapitags.h</span></span>
  
> <span data-ttu-id="8393b-131">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="8393b-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8393b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8393b-132">See also</span></span>



[<span data-ttu-id="8393b-133">Propriedade canônica PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="8393b-133">PidTagOriginalAuthorSearchKey Canonical Property</span></span>](pidtagoriginalauthorsearchkey-canonical-property.md)


[<span data-ttu-id="8393b-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8393b-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8393b-135">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8393b-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8393b-136">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8393b-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8393b-137">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8393b-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

