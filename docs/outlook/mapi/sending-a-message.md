---
title: Enviar uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6845c3d86fb3d34119a296ebbae76a7322d7d8c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590908"
---
# <a name="sending-a-message"></a><span data-ttu-id="b52ad-103">Enviar uma mensagem</span><span class="sxs-lookup"><span data-stu-id="b52ad-103">Sending a Message</span></span>

  
  
<span data-ttu-id="b52ad-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b52ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b52ad-105">Quando você estiver pronto para enviar uma mensagem, chame seu método de [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="b52ad-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="b52ad-106">**SubmitMessage** coloca a mensagem na fila de saída e define o sinalizador MSGFLAG_SUBMIT na propriedade de **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b52ad-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="b52ad-107">O provedor de armazenamento de mensagem, se fortemente acoplada a um provedor de transporte, dará a mensagem diretamente para o transporte que entrega para o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b52ad-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="b52ad-108">Se não estreitamente acoplado, o provedor de armazenamento de mensagem informa o spooler MAPI que a fila de saída foi alterada e o MAPI spooler transfere a mensagem para um provedor de transporte adequado.</span><span class="sxs-lookup"><span data-stu-id="b52ad-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="b52ad-109">Se você permitir aos usuários cancelar uma operação de envio, chame [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para implementar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="b52ad-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="b52ad-110">**AbortSubmit** remove a mensagem da fila de saída.</span><span class="sxs-lookup"><span data-stu-id="b52ad-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="b52ad-111">Os usuários podem ter permissão para interromper um envio aconteça até que a mensagem é fornecida para o sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="b52ad-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="b52ad-112">Se **SubmitMessage** retornar MAPI_E_CORRUPT_DATA, suponha que os dados que estão sendo enviados são agora perdido.</span><span class="sxs-lookup"><span data-stu-id="b52ad-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="b52ad-113">Antes de tentar enviar uma segunda vez, gravar novamente a mensagem chamando [IMAPIProp::SetProps](imapiprop-setprops.md) e [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="b52ad-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="b52ad-114">Exiba um erro ao usuário se essas chamadas **IMAPIProp** falharem ou se **SubmitMessage** falhar uma segunda vez.</span><span class="sxs-lookup"><span data-stu-id="b52ad-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="b52ad-115">Depois de uma chamada bem sucedida a **SubmitMessage**, liberar qualquer memória que foi alocada para a lista de destinatários e liberar a mensagem e seus respectivos anexos.</span><span class="sxs-lookup"><span data-stu-id="b52ad-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="b52ad-116">Depois que uma mensagem foi enviada, MAPI não permite que quaisquer operações mais sobre os ponteiros para esses objetos.</span><span class="sxs-lookup"><span data-stu-id="b52ad-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="b52ad-117">A única exceção é chamando **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="b52ad-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="b52ad-118">Nenhuma outra chamada é permitida porque muitos provedores de armazenamento de mensagem invalidar identificadores de entrada para mensagens que foram enviados.</span><span class="sxs-lookup"><span data-stu-id="b52ad-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

