---
title: Propriedade canônica PidLidBusyStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cb73a0e09436177b8b53a05588508886ee28a0a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383300"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="091a3-103">Propriedade canônica PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="091a3-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="091a3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="091a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="091a3-105">Representa a disponibilidade do usuário para um compromisso.</span><span class="sxs-lookup"><span data-stu-id="091a3-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="091a3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="091a3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="091a3-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="091a3-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="091a3-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="091a3-108">Property set:</span></span>  <br/> |<span data-ttu-id="091a3-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="091a3-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="091a3-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="091a3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="091a3-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="091a3-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="091a3-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="091a3-112">Data type:</span></span>  <br/> |<span data-ttu-id="091a3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="091a3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="091a3-114">Área:</span><span class="sxs-lookup"><span data-stu-id="091a3-114">Area:</span></span>  <br/> |<span data-ttu-id="091a3-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="091a3-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="091a3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="091a3-116">Remarks</span></span>

<span data-ttu-id="091a3-117">Essa propriedade especifica a disponibilidade de um usuário para o evento descrito pelo objeto e deve ser um dos valores especificados abaixo.</span><span class="sxs-lookup"><span data-stu-id="091a3-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="091a3-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="091a3-118">**Value**</span></span>|<span data-ttu-id="091a3-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="091a3-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="091a3-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="091a3-120">0x00000000</span></span>  <br/> |<span data-ttu-id="091a3-121">O usuário está disponível.</span><span class="sxs-lookup"><span data-stu-id="091a3-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="091a3-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="091a3-122">0x00000001</span></span>  <br/> |<span data-ttu-id="091a3-123">O usuário tem um evento provisório agendado.</span><span class="sxs-lookup"><span data-stu-id="091a3-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="091a3-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="091a3-124">0x00000002</span></span>  <br/> |<span data-ttu-id="091a3-125">O usuário está ocupado.</span><span class="sxs-lookup"><span data-stu-id="091a3-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="091a3-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="091a3-126">0x00000003</span></span>  <br/> |<span data-ttu-id="091a3-127">O usuário está fora do escritório em ausência temporária.</span><span class="sxs-lookup"><span data-stu-id="091a3-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="091a3-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="091a3-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="091a3-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="091a3-129">Protocol specifications</span></span>

<span data-ttu-id="091a3-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="091a3-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="091a3-131">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="091a3-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="091a3-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="091a3-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="091a3-133">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="091a3-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="091a3-134">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="091a3-134">Header files</span></span>

<span data-ttu-id="091a3-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="091a3-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="091a3-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="091a3-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="091a3-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="091a3-137">See also</span></span>



[<span data-ttu-id="091a3-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="091a3-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="091a3-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="091a3-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="091a3-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="091a3-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="091a3-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="091a3-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

