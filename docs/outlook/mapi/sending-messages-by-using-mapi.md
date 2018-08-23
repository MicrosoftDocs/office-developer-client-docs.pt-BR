---
title: Enviar mensagens usando MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6a3172dcd962c04d72aacd14d2e42990fb0f78c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593449"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="0753e-103">Enviar mensagens usando MAPI</span><span class="sxs-lookup"><span data-stu-id="0753e-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="0753e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0753e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0753e-105">Aplicativos cliente chamam o método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="0753e-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="0753e-106">**SubmitMessage** chama [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para salvar a mensagem antes de transferir o controle para o spooler MAPI ou diretamente a um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="0753e-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="0753e-107">O MAPI spooler recebe a mensagem se qualquer um destes procedimentos ocorrer:</span><span class="sxs-lookup"><span data-stu-id="0753e-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="0753e-108">O provedor de armazenamento de mensagem e o provedor de transporte não estão intimamente ligadas.</span><span class="sxs-lookup"><span data-stu-id="0753e-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="0753e-109">A mensagem requer pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="0753e-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="0753e-110">O repositório de ligação estreita de mensagem e transporte não podem lidar com todos os destinatários para quem a mensagem é endereçada.</span><span class="sxs-lookup"><span data-stu-id="0753e-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="0753e-111">Um armazenamento de mensagens de ligação estreita deve levar em conta o status de uma mensagem antes que ele apresenta-as para o MAPI spooler sejam baixados para um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="0753e-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="0753e-112">Existem situações em que uma mensagem é exibida exigir que o spooler MAPI, mas o MAPI spooler realmente não deveriam estar envolvido.</span><span class="sxs-lookup"><span data-stu-id="0753e-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="0753e-113">Por exemplo, considere a situação em que um usuário envia uma mensagem da caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="0753e-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="0753e-114">O cliente está usando um repositório de ligação estreita e o transporte.</span><span class="sxs-lookup"><span data-stu-id="0753e-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="0753e-115">Se o armazenamento de mensagens de ligação estreita usa do local da mensagem como o único critério para decidir sobre se devem ou não permitir que o spooler MAPI lidar com a mensagem, o MAPI spooler sempre receberá a mensagem.</span><span class="sxs-lookup"><span data-stu-id="0753e-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="0753e-116">Para evitar esse tipo de problema, um armazenamento de mensagens de ligação estreita deve verificar o status de mensagem além do local da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0753e-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="0753e-117">Especificamente, o provedor de transporte não deve solicitar que o MAPI spooler baixar qualquer mensagem que será enviada ativamente.</span><span class="sxs-lookup"><span data-stu-id="0753e-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="0753e-118">O processo de transmissão de mensagem envolve o provedor de armazenamento de mensagem, um ou mais provedores de transporte e MAPI.</span><span class="sxs-lookup"><span data-stu-id="0753e-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="0753e-119">Os tópicos desta seção fornecem informações detalhadas sobre funções específicas no processo de transmissão de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0753e-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0753e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0753e-120">See also</span></span>



[<span data-ttu-id="0753e-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="0753e-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="0753e-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="0753e-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

