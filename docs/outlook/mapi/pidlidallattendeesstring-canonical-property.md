---
title: Propriedade canônica PidLidAllAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAllAttendeesString
api_type:
- COM
ms.assetid: 2ffc0609-341d-4e35-8f53-ed3096c6fa7f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a9580428cd985902d3af6320dd754947565b74e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768214"
---
# <a name="pidlidallattendeesstring-canonical-property"></a><span data-ttu-id="30c91-103">Propriedade canônica PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="30c91-103">PidLidAllAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="30c91-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30c91-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30c91-105">Especifica uma lista de todos os participantes, exceto o organizador, incluindo recursos e participantes de outro.</span><span class="sxs-lookup"><span data-stu-id="30c91-105">Specifies a list of all the attendees except for the organizer, including resources and unsendable attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30c91-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="30c91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30c91-107">dispidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="30c91-107">dispidAllAttendeesString</span></span>  <br/> |
|<span data-ttu-id="30c91-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="30c91-108">Property set:</span></span>  <br/> |<span data-ttu-id="30c91-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="30c91-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="30c91-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="30c91-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="30c91-111">0x00008238</span><span class="sxs-lookup"><span data-stu-id="30c91-111">0x00008238</span></span>  <br/> |
|<span data-ttu-id="30c91-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="30c91-112">Data type:</span></span>  <br/> |<span data-ttu-id="30c91-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="30c91-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="30c91-114">Área:</span><span class="sxs-lookup"><span data-stu-id="30c91-114">Area:</span></span>  <br/> |<span data-ttu-id="30c91-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="30c91-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30c91-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="30c91-116">Remarks</span></span>

<span data-ttu-id="30c91-117">O valor para cada participante é o nome de exibição do participante.</span><span class="sxs-lookup"><span data-stu-id="30c91-117">The value for each attendee is the attendee's display name.</span></span> <span data-ttu-id="30c91-118">Entradas separadas devem ser delimitadas por ponto e vírgula seguido por um espaço.</span><span class="sxs-lookup"><span data-stu-id="30c91-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="30c91-119">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="30c91-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="30c91-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="30c91-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30c91-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="30c91-121">Protocol specifications</span></span>

<span data-ttu-id="30c91-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30c91-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30c91-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="30c91-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="30c91-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30c91-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30c91-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="30c91-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30c91-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="30c91-126">Header files</span></span>

<span data-ttu-id="30c91-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30c91-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="30c91-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="30c91-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30c91-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="30c91-129">See also</span></span>



[<span data-ttu-id="30c91-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="30c91-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30c91-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="30c91-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30c91-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="30c91-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30c91-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="30c91-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

