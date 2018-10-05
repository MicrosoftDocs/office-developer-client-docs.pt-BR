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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385841"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="5be3c-103">Propriedade canônica PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="5be3c-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="5be3c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5be3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5be3c-105">Contém o tipo de destinatário para um destinatário de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5be3c-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5be3c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5be3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5be3c-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="5be3c-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="5be3c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5be3c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5be3c-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="5be3c-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="5be3c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5be3c-110">Data type:</span></span>  <br/> |<span data-ttu-id="5be3c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5be3c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5be3c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5be3c-112">Area:</span></span>  <br/> |<span data-ttu-id="5be3c-113">Destinatário MAPI</span><span class="sxs-lookup"><span data-stu-id="5be3c-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5be3c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5be3c-114">Remarks</span></span>

<span data-ttu-id="5be3c-115">O tipo de destinatário contido nesta propriedade consiste em um valor necessário e um sinalizador opcional.</span><span class="sxs-lookup"><span data-stu-id="5be3c-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="5be3c-116">Esta propriedade deve conter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5be3c-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="5be3c-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="5be3c-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="5be3c-118">O destinatário é primário (a) do destinatário.</span><span class="sxs-lookup"><span data-stu-id="5be3c-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="5be3c-119">Os clientes são necessários para lidar com destinatários principais.</span><span class="sxs-lookup"><span data-stu-id="5be3c-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="5be3c-120">Todos os outros tipos são opcionais.</span><span class="sxs-lookup"><span data-stu-id="5be3c-120">All other types are optional.</span></span>
    
<span data-ttu-id="5be3c-121">MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="5be3c-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="5be3c-122">O destinatário é um destinatário de cópia carbono (CC), um destinatário que recebe uma mensagem além dos destinatários principais.</span><span class="sxs-lookup"><span data-stu-id="5be3c-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="5be3c-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="5be3c-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="5be3c-124">O destinatário é um destinatário de cópia oculta (Cco).</span><span class="sxs-lookup"><span data-stu-id="5be3c-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="5be3c-125">Principal e cópia carbono destinatários estão cientes da existência de destinatários Cco.</span><span class="sxs-lookup"><span data-stu-id="5be3c-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="5be3c-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="5be3c-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="5be3c-127">O destinatário não recebeu com êxito a mensagem na tentativa anterior.</span><span class="sxs-lookup"><span data-stu-id="5be3c-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="5be3c-128">Este é um reenvio de uma transmissão anterior.</span><span class="sxs-lookup"><span data-stu-id="5be3c-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="5be3c-129">Além disso, o seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="5be3c-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="5be3c-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="5be3c-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="5be3c-131">O destinatário já tiver recebido a mensagem e não precisa recebê-la novamente.</span><span class="sxs-lookup"><span data-stu-id="5be3c-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="5be3c-132">Este é um reenvio de uma transmissão anterior.</span><span class="sxs-lookup"><span data-stu-id="5be3c-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="5be3c-133">Esse sinalizador é definido em conjunto com os valores **MAPI_TO**, **MAPI_CC**e **MAPI_BCC** .</span><span class="sxs-lookup"><span data-stu-id="5be3c-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="5be3c-134">O valor de MAPI_P1 e o sinalizador **MAPI_SUBMITTED** é usado quando uma mensagem está sendo retransmitida devido a não entrega a um ou mais dos destinatários pretendidos.</span><span class="sxs-lookup"><span data-stu-id="5be3c-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="5be3c-135">Para este tipo de retransmissão, o cliente define **MAPI_SUBMITTED** em cada destinatário que não precisa novamente a mensagem, mas deve ser exibido na lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="5be3c-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="5be3c-136">Para cada destinatário que não recebeu a mensagem anteriormente, o cliente retém o destinatário original com seu valor **PR_RECIPIENT_TYPE** inalterada, mas Além disso, envia uma cópia do destinatário com MAPI_P1 no lugar o valor original.</span><span class="sxs-lookup"><span data-stu-id="5be3c-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="5be3c-137">Essa cópia, que é descartada antes da entrega real, força o destinatário para o envelope P1 e garante a retransmissão físico para que o destinatário.</span><span class="sxs-lookup"><span data-stu-id="5be3c-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="5be3c-138">A propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) é definida como FALSE para destinatários MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="5be3c-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="5be3c-139">Quando um cliente exibe um formulário de reenvio, somente os destinatários MAPI_P1 estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="5be3c-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="5be3c-140">A menos que o usuário insere destinatários adicionais, quando a mensagem é entregue, a lista de destinatários é exibida exatamente como quando a mensagem foi enviada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="5be3c-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="5be3c-141">Os **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) e as propriedades de **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) estão relacionadas ao tipo de destinatário.</span><span class="sxs-lookup"><span data-stu-id="5be3c-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="5be3c-142">Quando um cliente chama **IMAPIProp::SaveChanges da mensagem** e há pelo menos um destinatário na lista de destinatários, o provedor de armazenamento de mensagem define essas propriedades da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5be3c-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="5be3c-143">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="5be3c-143">**Property**</span></span>|<span data-ttu-id="5be3c-144">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5be3c-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5be3c-145">PR_DISPLAY_TO</span><span class="sxs-lookup"><span data-stu-id="5be3c-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="5be3c-146">Definido como TRUE se um ou mais dos destinatários estão **MAPI_TO** destinatários.</span><span class="sxs-lookup"><span data-stu-id="5be3c-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="5be3c-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="5be3c-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="5be3c-148">Definido como TRUE se um ou mais dos destinatários estão **MAPI_CC** destinatários.</span><span class="sxs-lookup"><span data-stu-id="5be3c-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="5be3c-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="5be3c-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="5be3c-150">Definido como TRUE se um ou mais dos destinatários estão **MAPI_BCC** destinatários.</span><span class="sxs-lookup"><span data-stu-id="5be3c-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="5be3c-151">Em x. 400, o envelope P1 ou entrega é as informações necessárias para enviar uma mensagem, incluindo propriedades de endereço do destinatário e qualquer sinalizadores de opção controlando a entrega e respostas.</span><span class="sxs-lookup"><span data-stu-id="5be3c-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="5be3c-152">Envelope P2 ou exibição é as informações que geralmente é exibidas para cada destinatário que não seja o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5be3c-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="5be3c-153">Ela normalmente inclui o assunto, importância, prioridade, sensibilidade e hora de envio, bem como os nomes dos destinatários primários e copiados.</span><span class="sxs-lookup"><span data-stu-id="5be3c-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5be3c-154">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5be3c-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5be3c-155">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5be3c-155">Protocol specifications</span></span>

<span data-ttu-id="5be3c-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5be3c-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5be3c-157">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5be3c-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5be3c-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5be3c-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5be3c-159">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="5be3c-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5be3c-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5be3c-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5be3c-161">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="5be3c-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="5be3c-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5be3c-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5be3c-163">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="5be3c-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5be3c-164">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5be3c-164">Header files</span></span>

<span data-ttu-id="5be3c-165">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5be3c-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="5be3c-166">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5be3c-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="5be3c-167">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5be3c-167">Mapitags.h</span></span>
  
> <span data-ttu-id="5be3c-168">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5be3c-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5be3c-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="5be3c-169">See also</span></span>



[<span data-ttu-id="5be3c-170">Propriedade canônica PidTagRecipientStatus</span><span class="sxs-lookup"><span data-stu-id="5be3c-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="5be3c-171">Propriedade canônica PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="5be3c-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="5be3c-172">Propriedade canônica PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="5be3c-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="5be3c-173">Propriedade canônica PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="5be3c-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="5be3c-174">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5be3c-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5be3c-175">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5be3c-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5be3c-176">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5be3c-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5be3c-177">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5be3c-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

