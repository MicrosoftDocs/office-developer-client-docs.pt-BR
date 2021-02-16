---
title: Propriedade canônica PidTagRecipientType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355255"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="e0e77-103">Propriedade canônica PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="e0e77-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="e0e77-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0e77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0e77-105">Contém o tipo de destinatário de um destinatário da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e0e77-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0e77-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e0e77-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0e77-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="e0e77-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="e0e77-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e0e77-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0e77-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="e0e77-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="e0e77-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e0e77-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0e77-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e0e77-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e0e77-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e0e77-112">Area:</span></span>  <br/> |<span data-ttu-id="e0e77-113">Destinatário MAPI</span><span class="sxs-lookup"><span data-stu-id="e0e77-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0e77-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0e77-114">Remarks</span></span>

<span data-ttu-id="e0e77-115">O tipo de destinatário contido nessa propriedade consiste em um valor obrigatório e um sinalizador opcional.</span><span class="sxs-lookup"><span data-stu-id="e0e77-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="e0e77-116">Essa propriedade deve conter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="e0e77-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="e0e77-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="e0e77-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="e0e77-118">O destinatário é um destinatário principal (Para).</span><span class="sxs-lookup"><span data-stu-id="e0e77-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="e0e77-119">Os clientes são necessários para lidar com destinatários primários.</span><span class="sxs-lookup"><span data-stu-id="e0e77-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="e0e77-120">Todos os outros tipos são opcionais.</span><span class="sxs-lookup"><span data-stu-id="e0e77-120">All other types are optional.</span></span>
    
<span data-ttu-id="e0e77-121">MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="e0e77-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="e0e77-122">O destinatário é um destinatário com cópia carbono (CC), um destinatário que recebe uma mensagem além dos destinatários primários.</span><span class="sxs-lookup"><span data-stu-id="e0e77-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="e0e77-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="e0e77-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="e0e77-124">O destinatário é um destinatário com cópia carbono (Cc).</span><span class="sxs-lookup"><span data-stu-id="e0e77-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="e0e77-125">Os destinatários de cópia primária e carbono não estão cientes da existência de destinatários Cc.</span><span class="sxs-lookup"><span data-stu-id="e0e77-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="e0e77-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="e0e77-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="e0e77-127">O destinatário não recebeu com êxito a mensagem na tentativa anterior.</span><span class="sxs-lookup"><span data-stu-id="e0e77-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="e0e77-128">Este é um resend de uma transmissão anterior.</span><span class="sxs-lookup"><span data-stu-id="e0e77-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="e0e77-129">Além disso, o sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="e0e77-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="e0e77-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="e0e77-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="e0e77-131">O destinatário já recebeu a mensagem e não precisa recebê-la novamente.</span><span class="sxs-lookup"><span data-stu-id="e0e77-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="e0e77-132">Este é um resend de uma transmissão anterior.</span><span class="sxs-lookup"><span data-stu-id="e0e77-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="e0e77-133">Esse sinalizador é definido em conjunto com os **MAPI_TO,** **MAPI_CC** e **MAPI_BCC** valores.</span><span class="sxs-lookup"><span data-stu-id="e0e77-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="e0e77-134">O MAPI_P1 e o **sinalizador MAPI_SUBMITTED** são usados quando uma mensagem está sendo retransmitida devido a um ou mais dos destinatários pretendidos.</span><span class="sxs-lookup"><span data-stu-id="e0e77-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="e0e77-135">Para essa retransmissão,  o cliente define MAPI_SUBMITTED em todos os destinatários que não precisam da mensagem novamente, mas que devem ser exibidos na lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="e0e77-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="e0e77-136">Para cada destinatário que não recebeu a mensagem anteriormente, o cliente mantém o destinatário original com seu valor **de PR_RECIPIENT_TYPE** inalterado, mas, além disso, envia uma cópia do destinatário com MAPI_P1 no lugar do valor original.</span><span class="sxs-lookup"><span data-stu-id="e0e77-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="e0e77-137">Essa cópia, que é descartada antes da entrega real, força o destinatário no envelope P1 e garante a retransmissão física para esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="e0e77-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="e0e77-138">A **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) é definida como FALSE para MAPI_P1 destinatários.</span><span class="sxs-lookup"><span data-stu-id="e0e77-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="e0e77-139">Quando um cliente exibe um formulário de reend, somente os MAPI_P1 destinatários ficam visíveis.</span><span class="sxs-lookup"><span data-stu-id="e0e77-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="e0e77-140">A menos que o usuário insira destinatários adicionais, quando a mensagem é entregue, a lista de destinatários aparece exatamente como era quando a mensagem foi enviada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="e0e77-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="e0e77-141">As **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) e **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) estão relacionadas ao tipo de destinatário.</span><span class="sxs-lookup"><span data-stu-id="e0e77-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="e0e77-142">Quando um cliente chama o **IMAPIProp::SaveChanges** de uma mensagem e há pelo menos um destinatário na lista de destinatários, o provedor de armazenamento de mensagens define essas propriedades da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="e0e77-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="e0e77-143">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="e0e77-143">**Property**</span></span>|<span data-ttu-id="e0e77-144">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e0e77-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0e77-145">PR_DISPLAY_TO</span><span class="sxs-lookup"><span data-stu-id="e0e77-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="e0e77-146">De definida como TRUE se um ou mais dos destinatários **MAPI_TO** destinatários.</span><span class="sxs-lookup"><span data-stu-id="e0e77-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="e0e77-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="e0e77-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="e0e77-148">De definida como TRUE se um ou mais dos destinatários **MAPI_CC** destinatários.</span><span class="sxs-lookup"><span data-stu-id="e0e77-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="e0e77-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="e0e77-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="e0e77-150">De definida como TRUE se um ou mais dos destinatários **MAPI_BCC** destinatários.</span><span class="sxs-lookup"><span data-stu-id="e0e77-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="e0e77-151">No X.400, o P1 ou o envelope de entrega são as informações necessárias para entregar uma mensagem, incluindo as propriedades de endereço do destinatário e quaisquer sinalizadores de opção que controlam a entrega e as respostas.</span><span class="sxs-lookup"><span data-stu-id="e0e77-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="e0e77-152">O envelope P2 ou de exibição é a informação normalmente exibida para cada destinatário que não seja o texto da mensagem em si.</span><span class="sxs-lookup"><span data-stu-id="e0e77-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="e0e77-153">Normalmente, ele inclui o assunto, a importância, a prioridade, a sensibilidade e o tempo de envio, bem como os nomes dos destinatários principais e copiados.</span><span class="sxs-lookup"><span data-stu-id="e0e77-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e0e77-154">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0e77-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0e77-155">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e0e77-155">Protocol specifications</span></span>

<span data-ttu-id="e0e77-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0e77-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0e77-157">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e0e77-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0e77-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0e77-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0e77-159">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="e0e77-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e0e77-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0e77-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0e77-161">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="e0e77-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="e0e77-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0e77-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0e77-163">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="e0e77-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0e77-164">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="e0e77-164">Header files</span></span>

<span data-ttu-id="e0e77-165">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0e77-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0e77-166">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e0e77-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0e77-167">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e0e77-167">Mapitags.h</span></span>
  
> <span data-ttu-id="e0e77-168">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e0e77-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0e77-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0e77-169">See also</span></span>



[<span data-ttu-id="e0e77-170">Propriedade canônica PidTagRecipientStatus</span><span class="sxs-lookup"><span data-stu-id="e0e77-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="e0e77-171">Propriedade canônica PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="e0e77-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="e0e77-172">Propriedade canônica PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="e0e77-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="e0e77-173">Propriedade canônica PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="e0e77-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="e0e77-174">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e0e77-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0e77-175">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e0e77-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0e77-176">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e0e77-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0e77-177">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e0e77-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

