---
title: Enviar mensagens usando MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438719"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="c55ff-103">Enviar mensagens usando MAPI</span><span class="sxs-lookup"><span data-stu-id="c55ff-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="c55ff-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c55ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c55ff-105">Os aplicativos cliente chamam [o método IMessage::SubmitMessage](imessage-submitmessage.md) para enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="c55ff-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="c55ff-106">**SubmitMessage** chama [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para salvar a mensagem antes de transferir o controle para o spooler MAPI ou diretamente para um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c55ff-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="c55ff-107">O spooler MAPI receberá a mensagem se qualquer uma das seguintes condições ocorrer:</span><span class="sxs-lookup"><span data-stu-id="c55ff-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="c55ff-108">O provedor de armazenamento de mensagens e o provedor de transporte não estão fortemente unidos.</span><span class="sxs-lookup"><span data-stu-id="c55ff-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="c55ff-109">A mensagem requer pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="c55ff-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="c55ff-110">O armazenamento e o transporte de mensagens fortemente a par não podem lidar com todos os destinatários aos quais a mensagem é endereçada.</span><span class="sxs-lookup"><span data-stu-id="c55ff-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="c55ff-111">Um armazenamento de mensagens fortemente a par deve levar em conta o status de uma mensagem antes de apresenta-la ao spooler MAPI a ser baixado para um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c55ff-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="c55ff-112">Há situações em que uma mensagem pode parecer exigir o spooler MAPI, mas o spooler MAPI realmente não deve estar envolvido.</span><span class="sxs-lookup"><span data-stu-id="c55ff-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="c55ff-113">Por exemplo, considere a situação em que um usuário envia uma mensagem da Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="c55ff-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="c55ff-114">O cliente está usando um armazenamento e transporte fortemente próximos.</span><span class="sxs-lookup"><span data-stu-id="c55ff-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="c55ff-115">Se o armazenamento de mensagens fortemente a par usa a localização da mensagem como o único critério para decidir se o spooler MAPI deve ou não manipular a mensagem, o spooler MAPI sempre receberá a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c55ff-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="c55ff-116">Para evitar esse tipo de problema, um armazenamento de mensagens fortemente a par deve verificar o status da mensagem, além do local da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c55ff-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="c55ff-117">Especificamente, o provedor de transporte não deve solicitar que o spooler MAPI baixe qualquer mensagem que seja enviada ativamente.</span><span class="sxs-lookup"><span data-stu-id="c55ff-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="c55ff-118">O processo de transmissão de mensagens envolve o provedor de armazenamento de mensagens, um ou mais provedores de transporte e MAPI.</span><span class="sxs-lookup"><span data-stu-id="c55ff-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="c55ff-119">Os tópicos desta seção fornecem informações detalhadas sobre funções específicas no processo de transmissão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c55ff-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c55ff-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c55ff-120">See also</span></span>



[<span data-ttu-id="c55ff-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c55ff-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="c55ff-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c55ff-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

