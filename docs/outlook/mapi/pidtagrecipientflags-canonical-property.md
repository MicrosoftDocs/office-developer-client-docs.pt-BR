---
title: Propriedade canônica PidTagRecipientFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356697"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="903f9-103">Propriedade canônica PidTagRecipientFlags</span><span class="sxs-lookup"><span data-stu-id="903f9-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="903f9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="903f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="903f9-105">Especifica um campo de bits que descreve o status do destinatário.</span><span class="sxs-lookup"><span data-stu-id="903f9-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="903f9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="903f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="903f9-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="903f9-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="903f9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="903f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="903f9-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="903f9-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="903f9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="903f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="903f9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="903f9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="903f9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="903f9-112">Area:</span></span>  <br/> |<span data-ttu-id="903f9-113">Destinatário de transporte</span><span class="sxs-lookup"><span data-stu-id="903f9-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="903f9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="903f9-114">Remarks</span></span>

<span data-ttu-id="903f9-115">Esta propriedade não é obrigatória.</span><span class="sxs-lookup"><span data-stu-id="903f9-115">This property is not required.</span></span> <span data-ttu-id="903f9-116">Estes são os sinalizadores individuais que podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="903f9-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="903f9-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="903f9-117">**Value**</span></span>|<span data-ttu-id="903f9-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="903f9-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="903f9-119">S (recipSendable, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="903f9-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="903f9-120">O destinatário é um participante que é **enviado** .</span><span class="sxs-lookup"><span data-stu-id="903f9-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="903f9-121">Este sinalizador é usado apenas na propriedade **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="903f9-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="903f9-122">O (recipOrganizer, 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="903f9-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="903f9-123">O **RecipientRow** no qual este sinalizador é definido representa o organizador da reunião.</span><span class="sxs-lookup"><span data-stu-id="903f9-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="903f9-124">ER (recipExceptionalResponse, 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="903f9-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="903f9-125">Indica que o participante deu uma resposta para a exceção na qual esse **RecipientRow** reside.</span><span class="sxs-lookup"><span data-stu-id="903f9-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="903f9-126">Este sinalizador é usado apenas em um **RecipientRow** de um objeto de mensagem incorporado de exceção do objeto de reunião do organizador.</span><span class="sxs-lookup"><span data-stu-id="903f9-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="903f9-127">ED (recipExceptionalDeleted, 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="903f9-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="903f9-128">Indica que, apesar da **RecipientRow** existir, ela deve ser tratada como se o destinatário correspondente não.</span><span class="sxs-lookup"><span data-stu-id="903f9-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="903f9-129">Este sinalizador é usado apenas em um **RecipientRow** de um objeto de mensagem incorporado de exceção do objeto de reunião do organizador.</span><span class="sxs-lookup"><span data-stu-id="903f9-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="903f9-130">X (reservado, 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="903f9-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="903f9-131">Não deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="903f9-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="903f9-132">X (reservado, 0x00000080)</span><span class="sxs-lookup"><span data-stu-id="903f9-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="903f9-133">Não deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="903f9-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="903f9-134">G (recipOriginal, 0x00000100)</span><span class="sxs-lookup"><span data-stu-id="903f9-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="903f9-135">Indica que o destinatário é um participante original.</span><span class="sxs-lookup"><span data-stu-id="903f9-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="903f9-136">Este sinalizador é usado apenas na propriedade **dispidApptUnsendableRecips** .</span><span class="sxs-lookup"><span data-stu-id="903f9-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="903f9-137">X (reservado, 0x00000200)</span><span class="sxs-lookup"><span data-stu-id="903f9-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="903f9-138">Reservado.</span><span class="sxs-lookup"><span data-stu-id="903f9-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="903f9-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="903f9-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="903f9-140">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="903f9-140">Protocol specifications</span></span>

<span data-ttu-id="903f9-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="903f9-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="903f9-142">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="903f9-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="903f9-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="903f9-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="903f9-144">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="903f9-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="903f9-145">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="903f9-145">Header files</span></span>

<span data-ttu-id="903f9-146">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="903f9-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="903f9-147">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="903f9-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="903f9-148">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="903f9-148">Mapitags.h</span></span>
  
> <span data-ttu-id="903f9-149">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="903f9-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="903f9-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="903f9-150">See also</span></span>



[<span data-ttu-id="903f9-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="903f9-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="903f9-152">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="903f9-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="903f9-153">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="903f9-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="903f9-154">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="903f9-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

