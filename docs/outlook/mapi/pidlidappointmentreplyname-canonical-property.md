---
title: Propriedade canônica PidLidAppointmentReplyName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyName
api_type:
- COM
ms.assetid: 2f3a44d1-600f-412e-bc89-078841db5308
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f6707c49c70804aeb757119aa411ca4059e378eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356039"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="3ceeb-103">Propriedade canônica PidLidAppointmentReplyName</span><span class="sxs-lookup"><span data-stu-id="3ceeb-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="3ceeb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ceeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ceeb-105">Especifica o último usuário que respondeu à solicitação de reunião ou ao objeto de atualização de reunião.</span><span class="sxs-lookup"><span data-stu-id="3ceeb-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ceeb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3ceeb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3ceeb-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="3ceeb-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="3ceeb-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="3ceeb-108">Property set:</span></span>  <br/> |<span data-ttu-id="3ceeb-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="3ceeb-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="3ceeb-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3ceeb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3ceeb-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="3ceeb-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="3ceeb-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3ceeb-112">Data type:</span></span>  <br/> |<span data-ttu-id="3ceeb-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3ceeb-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3ceeb-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3ceeb-114">Area:</span></span>  <br/> |<span data-ttu-id="3ceeb-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="3ceeb-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ceeb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ceeb-116">Remarks</span></span>

<span data-ttu-id="3ceeb-117">Esta propriedade só é definida para um delegante quando um representante responder.</span><span class="sxs-lookup"><span data-stu-id="3ceeb-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="3ceeb-118">O valor é igual à propriedade **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) para o repositório do representante.</span><span class="sxs-lookup"><span data-stu-id="3ceeb-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="3ceeb-119">Esta propriedade não tem significado para o organizador.</span><span class="sxs-lookup"><span data-stu-id="3ceeb-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="3ceeb-120">Para obter detalhes sobre o **PR_MAILBOX_OWNER_NAME**, consulte o protocolo de objeto de armazenamento especificado em [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ceeb-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3ceeb-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ceeb-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3ceeb-122">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="3ceeb-122">Protocol specifications</span></span>

<span data-ttu-id="3ceeb-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ceeb-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ceeb-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3ceeb-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3ceeb-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ceeb-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ceeb-126">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3ceeb-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3ceeb-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ceeb-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ceeb-128">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="3ceeb-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3ceeb-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3ceeb-129">Header files</span></span>

<span data-ttu-id="3ceeb-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3ceeb-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="3ceeb-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3ceeb-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3ceeb-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ceeb-132">See also</span></span>



[<span data-ttu-id="3ceeb-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3ceeb-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3ceeb-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3ceeb-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3ceeb-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3ceeb-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3ceeb-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3ceeb-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

