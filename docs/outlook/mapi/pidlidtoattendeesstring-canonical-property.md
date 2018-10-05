---
title: Propriedade canônica PidLidToAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToAttendeesString
api_type:
- COM
ms.assetid: ca1eedba-c617-4403-8490-315ab75f2edb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ea0cd256b025ae519272f32522bebbe6e9e17b5e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383699"
---
# <a name="pidlidtoattendeesstring-canonical-property"></a><span data-ttu-id="e6b9b-103">Propriedade canônica PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="e6b9b-103">PidLidToAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="e6b9b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6b9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6b9b-105">Contém uma lista de todos os participantes sendable que também são participantes necessários.</span><span class="sxs-lookup"><span data-stu-id="e6b9b-105">Contains a list of all the sendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6b9b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e6b9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e6b9b-107">dispidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="e6b9b-107">dispidToAttendeesString</span></span>  <br/> |
|<span data-ttu-id="e6b9b-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="e6b9b-108">Property set:</span></span>  <br/> |<span data-ttu-id="e6b9b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e6b9b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e6b9b-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="e6b9b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e6b9b-111">0x0000823B</span><span class="sxs-lookup"><span data-stu-id="e6b9b-111">0x0000823B</span></span>  <br/> |
|<span data-ttu-id="e6b9b-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e6b9b-112">Data type:</span></span>  <br/> |<span data-ttu-id="e6b9b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e6b9b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e6b9b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e6b9b-114">Area:</span></span>  <br/> |<span data-ttu-id="e6b9b-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="e6b9b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6b9b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6b9b-116">Remarks</span></span>

<span data-ttu-id="e6b9b-117">O valor para cada participante é a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do participante catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="e6b9b-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="e6b9b-118">Entradas separadas devem ser delimitadas por ponto e vírgula seguido por um espaço.</span><span class="sxs-lookup"><span data-stu-id="e6b9b-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="e6b9b-119">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="e6b9b-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e6b9b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6b9b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e6b9b-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e6b9b-121">Protocol specifications</span></span>

<span data-ttu-id="e6b9b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6b9b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6b9b-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e6b9b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e6b9b-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6b9b-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6b9b-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="e6b9b-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e6b9b-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e6b9b-126">Header files</span></span>

<span data-ttu-id="e6b9b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6b9b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e6b9b-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e6b9b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6b9b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6b9b-129">See also</span></span>



[<span data-ttu-id="e6b9b-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e6b9b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e6b9b-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e6b9b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e6b9b-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e6b9b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e6b9b-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e6b9b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

