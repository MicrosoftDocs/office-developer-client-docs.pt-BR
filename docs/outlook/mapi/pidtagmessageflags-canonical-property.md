---
title: Propriedade canônica PidTagMessageFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageFlags
api_type:
- HeaderDef
ms.assetid: 7561112b-ca72-4c49-a8a0-cc1879a4e151
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f2e565dc8137edee441643a5d02a154f78737099
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769482"
---
# <a name="pidtagmessageflags-canonical-property"></a><span data-ttu-id="784f2-103">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="784f2-103">PidTagMessageFlags Canonical Property</span></span>

  
  
<span data-ttu-id="784f2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="784f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="784f2-105">Contém uma bitmask dos sinalizadores que indicam a origem e o estado atual de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="784f2-105">Contains a bitmask of flags that indicate the origin and current state of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="784f2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="784f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="784f2-107">PR_MESSAGE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="784f2-107">PR_MESSAGE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="784f2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="784f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="784f2-109">0x0E07</span><span class="sxs-lookup"><span data-stu-id="784f2-109">0x0E07</span></span>  <br/> |
|<span data-ttu-id="784f2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="784f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="784f2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="784f2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="784f2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="784f2-112">Area:</span></span>  <br/> |<span data-ttu-id="784f2-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="784f2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="784f2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="784f2-114">Remarks</span></span>

<span data-ttu-id="784f2-115">Essa propriedade é uma propriedade de mensagem nontransmittable exposta no nível o envio e recebimento extremidades de uma transmissão, com valores diferentes dependendo do aplicativo ou repositório provedor do cliente envolvido.</span><span class="sxs-lookup"><span data-stu-id="784f2-115">This property is a nontransmittable message property exposed at both the sending and receiving ends of a transmission, with different values depending upon the client application or store provider involved.</span></span> <span data-ttu-id="784f2-116">Essa propriedade é inicializada, o provedor de armazenamento de cliente ou de mensagem quando uma mensagem é criada e salvo pela primeira vez e, em seguida, atualizada periodicamente o provedor de armazenamento de mensagem, um provedor de transporte e o MAPI spooler conforme a mensagem é processada e seu estado alterações.</span><span class="sxs-lookup"><span data-stu-id="784f2-116">This property is initialized by the client or message store provider when a message is created and saved for the first time and then updated periodically by the message store provider, a transport provider, and the MAPI spooler as the message is processed and its state changes.</span></span> 
  
<span data-ttu-id="784f2-117">Essa propriedade existe em uma mensagem antes e após o envio e todas as cópias da mensagem recebida.</span><span class="sxs-lookup"><span data-stu-id="784f2-117">This property exists on a message both before and after submission, and on all copies of the received message.</span></span> <span data-ttu-id="784f2-118">Embora não seja uma propriedade de destinatário, ele é exposto forma diferente para cada destinatário de acordo com se ele tiver sido lidos ou modificado por que o destinatário.</span><span class="sxs-lookup"><span data-stu-id="784f2-118">Although it is not a recipient property, it is exposed differently to each recipient according to whether it has been read or modified by that recipient.</span></span> 
  
<span data-ttu-id="784f2-119">Um ou mais dos seguintes sinalizadores podem ser definido para essa propriedade:</span><span class="sxs-lookup"><span data-stu-id="784f2-119">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="784f2-120">MSGFLAG_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="784f2-120">MSGFLAG_ASSOCIATED</span></span> 
  
> <span data-ttu-id="784f2-121">A mensagem é uma mensagem associada de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="784f2-121">The message is an associated message of a folder.</span></span> <span data-ttu-id="784f2-122">O cliente ou o provedor tem acesso somente leitura para esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="784f2-122">The client or provider has read-only access to this flag.</span></span> <span data-ttu-id="784f2-123">O sinalizador MSGFLAG_READ é ignorado para mensagens associadas, o qual não mantém um estado lido /.</span><span class="sxs-lookup"><span data-stu-id="784f2-123">The MSGFLAG_READ flag is ignored for associated messages, which do not retain a read/unread state.</span></span> 
    
<span data-ttu-id="784f2-124">MSGFLAG_FROMME</span><span class="sxs-lookup"><span data-stu-id="784f2-124">MSGFLAG_FROMME</span></span> 
  
> <span data-ttu-id="784f2-125">O usuário enviando mensagens era o usuário mensagens recebendo a mensagem.</span><span class="sxs-lookup"><span data-stu-id="784f2-125">The messaging user sending was the messaging user receiving the message.</span></span> <span data-ttu-id="784f2-126">O cliente ou o provedor tem acesso de leitura/gravação para esse sinalizador até a primeira chamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e somente leitura depois disso.</span><span class="sxs-lookup"><span data-stu-id="784f2-126">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> <span data-ttu-id="784f2-127">Esse sinalizador é destinado a ser definido pelo provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="784f2-127">This flag is meant to be set by the transport provider.</span></span> 
    
<span data-ttu-id="784f2-128">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="784f2-128">MSGFLAG_HASATTACH</span></span> 
  
> <span data-ttu-id="784f2-129">A mensagem possui pelo menos um anexo.</span><span class="sxs-lookup"><span data-stu-id="784f2-129">The message has at least one attachment.</span></span> <span data-ttu-id="784f2-130">Esse sinalizador corresponde à propriedade de **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="784f2-130">This flag corresponds to the message's **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) property.</span></span> <span data-ttu-id="784f2-131">O cliente tem acesso somente leitura para esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="784f2-131">The client has read-only access to this flag.</span></span> 
    
<span data-ttu-id="784f2-132">MSGFLAG_NRN_PENDING</span><span class="sxs-lookup"><span data-stu-id="784f2-132">MSGFLAG_NRN_PENDING</span></span> 
  
> <span data-ttu-id="784f2-133">Um relatório nonread precisa ser enviada para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="784f2-133">A nonread report needs to be sent for the message.</span></span> <span data-ttu-id="784f2-134">O cliente ou o provedor tem acesso somente leitura para esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="784f2-134">The client or provider has read-only access to this flag.</span></span> 
    
<span data-ttu-id="784f2-135">MSGFLAG_ORIGIN_INTERNET</span><span class="sxs-lookup"><span data-stu-id="784f2-135">MSGFLAG_ORIGIN_INTERNET</span></span> 
  
> <span data-ttu-id="784f2-136">A mensagem de entrada foi recebida pela Internet.</span><span class="sxs-lookup"><span data-stu-id="784f2-136">The incoming message arrived over the Internet.</span></span> <span data-ttu-id="784f2-137">Ela se originou fora da organização ou de uma fonte que o gateway não pode considerar confiáveis.</span><span class="sxs-lookup"><span data-stu-id="784f2-137">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="784f2-138">O cliente deve exibir uma mensagem apropriada para o usuário.</span><span class="sxs-lookup"><span data-stu-id="784f2-138">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="784f2-139">Provedores de transporte definir esse sinalizador; o cliente tem acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="784f2-139">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="784f2-140">MSGFLAG_ORIGIN_MISC_EXT</span><span class="sxs-lookup"><span data-stu-id="784f2-140">MSGFLAG_ORIGIN_MISC_EXT</span></span> 
  
> <span data-ttu-id="784f2-141">A mensagem de entrada chegado por um link externo que não seja x. 400 ou a Internet.</span><span class="sxs-lookup"><span data-stu-id="784f2-141">The incoming message arrived over an external link other than X.400 or the Internet.</span></span> <span data-ttu-id="784f2-142">Ela se originou fora da organização ou de uma fonte que o gateway não pode considerar confiáveis.</span><span class="sxs-lookup"><span data-stu-id="784f2-142">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="784f2-143">O cliente deve exibir uma mensagem apropriada para o usuário.</span><span class="sxs-lookup"><span data-stu-id="784f2-143">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="784f2-144">Provedores de transporte definir esse sinalizador; o cliente tem acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="784f2-144">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="784f2-145">MSGFLAG_ORIGIN_X400</span><span class="sxs-lookup"><span data-stu-id="784f2-145">MSGFLAG_ORIGIN_X400</span></span> 
  
> <span data-ttu-id="784f2-146">A mensagem de entrada foi recebida em um vínculo de x. 400.</span><span class="sxs-lookup"><span data-stu-id="784f2-146">The incoming message arrived over an X.400 link.</span></span> <span data-ttu-id="784f2-147">Ela se originou fora da organização ou de uma fonte que o gateway não pode considerar confiáveis.</span><span class="sxs-lookup"><span data-stu-id="784f2-147">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="784f2-148">O cliente deve exibir uma mensagem apropriada para o usuário.</span><span class="sxs-lookup"><span data-stu-id="784f2-148">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="784f2-149">Provedores de transporte definir esse sinalizador; o cliente tem acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="784f2-149">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="784f2-150">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="784f2-150">MSGFLAG_READ</span></span> 
  
> <span data-ttu-id="784f2-151">A mensagem é marcada como tendo sido lidas.</span><span class="sxs-lookup"><span data-stu-id="784f2-151">The message is marked as having been read.</span></span> <span data-ttu-id="784f2-152">Isso pode ocorrer como resultado de uma chamada a qualquer momento para [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="784f2-152">This can occur as the result of a call at any time to [IMessage::SetReadFlag](imessage-setreadflag.md) or [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span> <span data-ttu-id="784f2-153">Os clientes também podem definir esse sinalizador chamando o método de **IMAPIProp::SetProps** da mensagem antes que a mensagem foi salvo pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="784f2-153">Clients can also set this flag by calling a message's **IMAPIProp::SetProps** method before the message has been saved for the first time.</span></span> <span data-ttu-id="784f2-154">Esse sinalizador é ignorada se o sinalizador **MSGFLAG_ASSOCIATED** está definido.</span><span class="sxs-lookup"><span data-stu-id="784f2-154">This flag is ignored if the **MSGFLAG_ASSOCIATED** flag is set.</span></span> 
    
<span data-ttu-id="784f2-155">MSGFLAG_RESEND</span><span class="sxs-lookup"><span data-stu-id="784f2-155">MSGFLAG_RESEND</span></span> 
  
> <span data-ttu-id="784f2-156">A mensagem inclui uma solicitação para uma operação de reenvio com um relatório de não entrega.</span><span class="sxs-lookup"><span data-stu-id="784f2-156">The message includes a request for a resend operation with a nondelivery report.</span></span> <span data-ttu-id="784f2-157">O cliente ou o provedor tem acesso de leitura/gravação para esse sinalizador até a primeira chamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e somente leitura depois disso.</span><span class="sxs-lookup"><span data-stu-id="784f2-157">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> 
    
<span data-ttu-id="784f2-158">MSGFLAG_RN_PENDING</span><span class="sxs-lookup"><span data-stu-id="784f2-158">MSGFLAG_RN_PENDING</span></span> 
  
> <span data-ttu-id="784f2-159">Um relatório de leitura precisa ser enviada para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="784f2-159">A read report needs to be sent for the message.</span></span> <span data-ttu-id="784f2-160">O cliente ou o provedor tem acesso somente leitura para esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="784f2-160">The client or provider has read-only access to this flag.</span></span> 
    
<span data-ttu-id="784f2-161">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="784f2-161">MSGFLAG_SUBMIT</span></span> 
  
> <span data-ttu-id="784f2-162">A mensagem é marcada para enviar como resultado de uma chamada para [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="784f2-162">The message is marked for sending as a result of a call to [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> <span data-ttu-id="784f2-163">Provedores de armazenamento de mensagem definir esse sinalizador; o cliente tem acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="784f2-163">Message store providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="784f2-164">MSGFLAG_UNMODIFIED</span><span class="sxs-lookup"><span data-stu-id="784f2-164">MSGFLAG_UNMODIFIED</span></span> 
  
> <span data-ttu-id="784f2-165">A mensagem de saída não foi modificada desde na primeira vez que ela foi salva; a mensagem de entrada não foi modificada desde que ela foi entregue.</span><span class="sxs-lookup"><span data-stu-id="784f2-165">The outgoing message has not been modified since the first time that it was saved; the incoming message has not been modified since it was delivered.</span></span> 
    
<span data-ttu-id="784f2-166">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="784f2-166">MSGFLAG_UNSENT</span></span> 
  
> <span data-ttu-id="784f2-167">A mensagem ainda está sendo composta.</span><span class="sxs-lookup"><span data-stu-id="784f2-167">The message is still being composed.</span></span> <span data-ttu-id="784f2-168">Ele é salvo, mas não foi enviado.</span><span class="sxs-lookup"><span data-stu-id="784f2-168">It is saved, but has not been sent.</span></span> <span data-ttu-id="784f2-169">O cliente ou o provedor tem acesso de leitura/gravação para esse sinalizador até a primeira chamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e somente leitura depois disso.</span><span class="sxs-lookup"><span data-stu-id="784f2-169">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> <span data-ttu-id="784f2-170">Se um cliente não definir esse sinalizador no momento em que a mensagem é enviada, o provedor de armazenamento de mensagens a define quando **IMessage::SubmitMessage** é chamado.</span><span class="sxs-lookup"><span data-stu-id="784f2-170">If a client doesn't set this flag by the time the message is sent, the message store provider sets it when **IMessage::SubmitMessage** is called.</span></span> <span data-ttu-id="784f2-171">Normalmente, esse sinalizador é limpa depois que a mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="784f2-171">Typically, this flag is cleared after the message is sent.</span></span> 
    
<span data-ttu-id="784f2-172">Um provedor de armazenamento do cliente ou mensagem pode verificar o estado atual da mensagem a qualquer momento chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) para ler os valores de sinalizador.</span><span class="sxs-lookup"><span data-stu-id="784f2-172">A client or message store provider can check the current state of the message at any time by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method to read the flag values.</span></span> <span data-ttu-id="784f2-173">O cliente ou o provedor também pode chamar o método [IMAPIProp::SetProps](imapiprop-setprops.md) para alterar qualquer sinalizadores que atualmente têm acesso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="784f2-173">The client or provider can also call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to change any flags that currently have read/write access.</span></span> 
  
<span data-ttu-id="784f2-174">Vários dos sinalizadores são sempre somente leitura.</span><span class="sxs-lookup"><span data-stu-id="784f2-174">Several of the flags are always read-only.</span></span> <span data-ttu-id="784f2-175">Alguns são leitura/gravação até que a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e depois disso serão somente leitura que diz respeito **IMAPIProp::SetProps** .</span><span class="sxs-lookup"><span data-stu-id="784f2-175">Some are read/write until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and thereafter become read-only as far as **IMAPIProp::SetProps** is concerned.</span></span> <span data-ttu-id="784f2-176">Um dos seguintes procedimentos, MSGFLAG_READ, pode ser alterado posteriormente através de [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="784f2-176">One of these, MSGFLAG_READ, can be changed later through [IMessage::SetReadFlag](imessage-setreadflag.md) or [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span> 
  
<span data-ttu-id="784f2-177">Os valores iniciais para essa propriedade normalmente são MSGFLAG_UNSENT e MSGFLAG_UNMODIFIED para indicar uma mensagem que ainda não foram enviada ou alterada.</span><span class="sxs-lookup"><span data-stu-id="784f2-177">The initial values for this property are typically MSGFLAG_UNSENT and MSGFLAG_UNMODIFIED to indicate a message that has not yet been sent or changed.</span></span> <span data-ttu-id="784f2-178">Quando uma mensagem é salva para a segunda vez, o provedor de armazenamento de mensagem limpa o sinalizador MSGFLAG_UNMODIFIED.</span><span class="sxs-lookup"><span data-stu-id="784f2-178">When a message is saved for the second time, the message store provider clears the MSGFLAG_UNMODIFIED flag.</span></span> <span data-ttu-id="784f2-179">Outro valor que um provedor de armazenamento de mensagem pode ser definidas quando uma mensagem é salvo é o sinalizador MSGFLAG_HASATTACH, indicando que a mensagem tem um ou mais anexos.</span><span class="sxs-lookup"><span data-stu-id="784f2-179">Another value that a message store provider can set when a message is saved is the MSGFLAG_HASATTACH flag, indicating that the message has one or more attachments.</span></span> <span data-ttu-id="784f2-180">A propriedade **PR_HASATTACH** é computada a partir dessa definição.</span><span class="sxs-lookup"><span data-stu-id="784f2-180">The **PR_HASATTACH** property is computed from this setting.</span></span> 
  
<span data-ttu-id="784f2-181">Quando um cliente chama o método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar a mensagem, o provedor de armazenamento de mensagem faz uma cópia dele para o spooler MAPI e atualiza essa propriedade, definindo o sinalizador MSGFLAG_SUBMIT.</span><span class="sxs-lookup"><span data-stu-id="784f2-181">When a client calls the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message, the message store provider makes a copy of it for the MAPI spooler and updates this property by setting the MSGFLAG_SUBMIT flag.</span></span> <span data-ttu-id="784f2-182">O provedor de armazenamento de mensagem também define MSGFLAG_UNSENT se ainda não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="784f2-182">The message store provider also sets MSGFLAG_UNSENT if it is not yet set.</span></span> <span data-ttu-id="784f2-183">MSGFLAG_SUBMIT indica que **SubmitMessage** tiver sido chamado, iniciar o processo de envio, e que a mensagem agora é somente leitura para o cliente.</span><span class="sxs-lookup"><span data-stu-id="784f2-183">MSGFLAG_SUBMIT indicates that **SubmitMessage** has been called, beginning the send process, and that the message is now read-only to the client.</span></span> <span data-ttu-id="784f2-184">MSGFLAG_UNSENT indica que o spooler MAPI está tratando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="784f2-184">MSGFLAG_UNSENT indicates that the MAPI spooler is handling the message.</span></span> <span data-ttu-id="784f2-185">Se o processo de envio for cancelado, o provedor de armazenamento de mensagem redefine esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="784f2-185">If the send process is canceled, the message store provider resets this flag.</span></span> 
  
<span data-ttu-id="784f2-186">Quando a mensagem é determinada a um provedor de transporte para entrega, o provedor de transporte define o sinalizador MSGFLAG_FROMME se o remetente tinha a mesma conta no servidor de mensagens, como a mensagem foi recebida em.</span><span class="sxs-lookup"><span data-stu-id="784f2-186">When the message is given to a transport provider for delivery, the transport provider sets the MSGFLAG_FROMME flag if the sender had the same account on the messaging server as the message was received on.</span></span> <span data-ttu-id="784f2-187">Provedores de transporte definir MSGFLAG_FROMME para uma mensagem de entrada que foi enviada pelo usuário conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="784f2-187">Transport providers set MSGFLAG_FROMME for an incoming message that was sent by the currently logged on user.</span></span> <span data-ttu-id="784f2-188">Um cliente pode usar esse valor para determinar o que é mais apropriado mostrar os nomes dos destinatários na tabela de conteúdo da pasta Itens enviados do que os nomes de remetente.</span><span class="sxs-lookup"><span data-stu-id="784f2-188">A client can use this value to determine that it is more appropriate to show recipient names in the contents table of the Sent Items folder than sender names.</span></span> <span data-ttu-id="784f2-189">Mensagens que foram salvas durante o processo de composição e ainda não enviadas também devem ser exibidas com os nomes dos destinatários em vez de nomes de remetente.</span><span class="sxs-lookup"><span data-stu-id="784f2-189">Messages that have been saved during the composition process and not yet sent should also be displayed with recipient names rather than sender names.</span></span> 
  
<span data-ttu-id="784f2-190">Uma mensagem de entrada, um provedor de armazenamento de mensagem limpa o sinalizador MSGFLAG_READ para redefinir o seu status de leitura.</span><span class="sxs-lookup"><span data-stu-id="784f2-190">For an incoming message, a message store provider clears the MSGFLAG_READ flag to reset its read status.</span></span> <span data-ttu-id="784f2-191">Um cliente pode definir ou limpar o sinalizador MSGFLAG_READ quando for necessário alterar o status de leitura e controlar o envio de relatórios de leitura e nonread, chamando o método de [IMessage::SetReadFlag](imessage-setreadflag.md) da mensagem ou sua pasta [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) método.</span><span class="sxs-lookup"><span data-stu-id="784f2-191">A client can set or clear the MSGFLAG_READ flag when it is necessary to change the read status and control the sending of read and nonread reports, by calling either the message's [IMessage::SetReadFlag](imessage-setreadflag.md) method or its folder's [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) method.</span></span> <span data-ttu-id="784f2-192">A principal diferença entre esses métodos, que não seja o objeto implementá-las, é que o método da pasta pode afetar uma, várias ou todas as mensagens na pasta.</span><span class="sxs-lookup"><span data-stu-id="784f2-192">The main difference between these methods, other than the object implementing them, is that the folder method can affect one, several, or all of the messages in the folder.</span></span> <span data-ttu-id="784f2-193">O método de mensagem afeta a uma única mensagem.</span><span class="sxs-lookup"><span data-stu-id="784f2-193">The message method affects a single message.</span></span> 
  
<span data-ttu-id="784f2-194">Um cliente também deve testar uma mensagem de entrada para os sinalizadores MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET e MSGFLAG_ORIGIN_MISC_EXT.</span><span class="sxs-lookup"><span data-stu-id="784f2-194">A client should also test an incoming message for the MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET, and MSGFLAG_ORIGIN_MISC_EXT flags.</span></span> <span data-ttu-id="784f2-195">Esses sinalizadores estão definidos pelo provedor de transporte de entrada e indicam que a mensagem foi recebida de uma fonte que o gateway não pode ser considerados confiáveis.</span><span class="sxs-lookup"><span data-stu-id="784f2-195">These flags are set by the inbound transport provider and indicate that the message arrived from a source that the gateway cannot consider trusted.</span></span> <span data-ttu-id="784f2-196">Isso significa que a mensagem se originou seja fora da organização, ou internamente mas a partir de uma estação de trabalho não conhecido para o gateway.</span><span class="sxs-lookup"><span data-stu-id="784f2-196">This means the message originated either outside the organization, or internally but from a workstation not known to the gateway.</span></span> <span data-ttu-id="784f2-197">Em qualquer caso, a identidade do remetente não pode ser confirmada e há um risco de introduzir um vírus na organização.</span><span class="sxs-lookup"><span data-stu-id="784f2-197">In any case, the identity of the sender may not be confirmed, and there is a risk of introducing a computer virus into the organization.</span></span> <span data-ttu-id="784f2-198">O cliente deve exibir uma mensagem de aviso ao usuário e oferecem uma opção de excluir a mensagem sem abri-lo.</span><span class="sxs-lookup"><span data-stu-id="784f2-198">The client should display a warning message to the user and offer an option of deleting the message without opening it.</span></span> 
  
<span data-ttu-id="784f2-199">Provedores de armazenamento de mensagem defina o sinalizador MSGFLAG_UNMODIFIED para mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="784f2-199">Message store providers set the MSGFLAG_UNMODIFIED flag for incoming messages.</span></span> <span data-ttu-id="784f2-200">MSGFLAG_UNMODIFIED indica que uma mensagem não foi alterada desde a entrega.</span><span class="sxs-lookup"><span data-stu-id="784f2-200">MSGFLAG_UNMODIFIED indicates that a message has not been changed since delivery.</span></span> <span data-ttu-id="784f2-201">Um cliente não pode desmarcar esse valor depois que ele tiver sido definido por um provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="784f2-201">A client cannot clear this value after it has been set by a message store provider.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="784f2-202">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="784f2-202">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="784f2-203">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="784f2-203">Protocol specifications</span></span>

<span data-ttu-id="784f2-204">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="784f2-204">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="784f2-205">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="784f2-205">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="784f2-206">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="784f2-206">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="784f2-207">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="784f2-207">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="784f2-208">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="784f2-208">Header files</span></span>

<span data-ttu-id="784f2-209">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="784f2-209">Mapidefs.h</span></span>
  
> <span data-ttu-id="784f2-210">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="784f2-210">Provides data type definitions.</span></span>
    
<span data-ttu-id="784f2-211">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="784f2-211">Mapitags.h</span></span>
  
> <span data-ttu-id="784f2-212">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="784f2-212">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="784f2-213">Confira também</span><span class="sxs-lookup"><span data-stu-id="784f2-213">See also</span></span>



[<span data-ttu-id="784f2-214">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="784f2-214">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)


[<span data-ttu-id="784f2-215">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="784f2-215">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="784f2-216">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="784f2-216">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="784f2-217">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="784f2-217">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="784f2-218">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="784f2-218">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
