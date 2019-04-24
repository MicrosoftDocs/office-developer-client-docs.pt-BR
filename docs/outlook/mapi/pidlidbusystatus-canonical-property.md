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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342025"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="fe527-103">Propriedade canônica PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="fe527-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="fe527-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe527-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe527-105">Representa a disponibilidade do usuário para um compromisso.</span><span class="sxs-lookup"><span data-stu-id="fe527-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe527-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fe527-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe527-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="fe527-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="fe527-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="fe527-108">Property set:</span></span>  <br/> |<span data-ttu-id="fe527-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fe527-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fe527-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fe527-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fe527-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="fe527-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="fe527-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fe527-112">Data type:</span></span>  <br/> |<span data-ttu-id="fe527-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fe527-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fe527-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fe527-114">Area:</span></span>  <br/> |<span data-ttu-id="fe527-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="fe527-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe527-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe527-116">Remarks</span></span>

<span data-ttu-id="fe527-117">Esta propriedade especifica a disponibilidade de um usuário para o evento descrito pelo objeto e deve ser um dos valores especificados abaixo.</span><span class="sxs-lookup"><span data-stu-id="fe527-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="fe527-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fe527-118">**Value**</span></span>|<span data-ttu-id="fe527-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fe527-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe527-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe527-120">0x00000000</span></span>  <br/> |<span data-ttu-id="fe527-121">O usuário está disponível.</span><span class="sxs-lookup"><span data-stu-id="fe527-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="fe527-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fe527-122">0x00000001</span></span>  <br/> |<span data-ttu-id="fe527-123">O usuário tem um evento provisório agendado.</span><span class="sxs-lookup"><span data-stu-id="fe527-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="fe527-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fe527-124">0x00000002</span></span>  <br/> |<span data-ttu-id="fe527-125">O usuário está ocupado.</span><span class="sxs-lookup"><span data-stu-id="fe527-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="fe527-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="fe527-126">0x00000003</span></span>  <br/> |<span data-ttu-id="fe527-127">O usuário está fora do escritório em ausência temporária.</span><span class="sxs-lookup"><span data-stu-id="fe527-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fe527-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe527-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fe527-129">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="fe527-129">Protocol specifications</span></span>

<span data-ttu-id="fe527-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe527-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe527-131">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fe527-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fe527-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe527-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe527-133">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="fe527-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fe527-134">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fe527-134">Header files</span></span>

<span data-ttu-id="fe527-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fe527-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe527-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fe527-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe527-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe527-137">See also</span></span>



[<span data-ttu-id="fe527-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fe527-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe527-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fe527-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe527-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fe527-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe527-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fe527-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

