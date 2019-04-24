---
title: Enviar uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339743"
---
# <a name="sending-a-message"></a><span data-ttu-id="eae8a-103">Enviar uma mensagem</span><span class="sxs-lookup"><span data-stu-id="eae8a-103">Sending a Message</span></span>

  
  
<span data-ttu-id="eae8a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eae8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eae8a-105">Quando estiver pronto para enviar uma mensagem, chame o método [IMessage:: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="eae8a-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="eae8a-106">**SubmitMessage** coloca a mensagem na fila de saída e define o sinalizador MSGFLAG_SUBMIT na propriedade **PR_MESSAGE_FLAGS** da mensagem ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eae8a-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="eae8a-107">O provedor de repositório de mensagens, se rigidamente acoplado a um provedor de transporte, fornece a mensagem diretamente ao transporte que a entrega ao sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="eae8a-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="eae8a-108">Se não estiver rigidamente acoplado, o provedor de armazenamento de mensagens informa ao spooler MAPI que a fila de saída foi alterada e o spooler MAPI transfere a mensagem para um provedor de transporte apropriado.</span><span class="sxs-lookup"><span data-stu-id="eae8a-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="eae8a-109">Se você permitir que os usuários cancelem uma operação de envio, chame [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para implementar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="eae8a-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="eae8a-110">**AbortSubmit** remove a mensagem da fila de saída.</span><span class="sxs-lookup"><span data-stu-id="eae8a-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="eae8a-111">Os usuários podem ter permissão para interromper um envio de acontecer até que a mensagem seja dada ao sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="eae8a-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="eae8a-112">Se **SubmitMessage** retornar MAPI_E_CORRUPT_DATA, presuma que os dados que estão sendo enviados serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="eae8a-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="eae8a-113">Antes de tentar enviar uma segunda vez, reescreva a mensagem chamando [IMAPIProp::](imapiprop-setprops.md) SetProps e [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="eae8a-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="eae8a-114">Exibe um erro para o usuário se essas **IMAPIProp** chamadas falharem ou se o **SubmitMessage** falhar uma segunda vez.</span><span class="sxs-lookup"><span data-stu-id="eae8a-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="eae8a-115">Após uma chamada bem-sucedida para o **SubmitMessage**, libere qualquer memória que tenha sido alocada para a lista de destinatários e libere a mensagem e seus anexos.</span><span class="sxs-lookup"><span data-stu-id="eae8a-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="eae8a-116">Depois que uma mensagem for enviada, o MAPI não permitirá nenhuma operação adicional nos ponteiros desses objetos.</span><span class="sxs-lookup"><span data-stu-id="eae8a-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="eae8a-117">A única exceção é chamar **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="eae8a-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="eae8a-118">Nenhuma outra chamada é permitida porque muitos provedores de repositórios de mensagens invalidam identificadores de entrada para mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="eae8a-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

