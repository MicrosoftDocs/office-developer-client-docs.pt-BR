---
title: Subárvore IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6fe642d10a50d25874aee170441a07c184b46575
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591090"
---
# <a name="ipm-subtree"></a><span data-ttu-id="39a0a-103">Subárvore IPM</span><span class="sxs-lookup"><span data-stu-id="39a0a-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="39a0a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39a0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39a0a-105">MAPI cria uma árvore de pastas sob a pasta raiz de um armazenamento de mensagens para todos os clientes que enviam mensagens para e recebem mensagens de humana, em vez de computador, os destinatários.</span><span class="sxs-lookup"><span data-stu-id="39a0a-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="39a0a-106">Mensagens trocadas entre os destinatários humanos são conhecidas como interpessoais emails e esta árvore é conhecida como a mensagem interpessoais ou IPM, subárvore.</span><span class="sxs-lookup"><span data-stu-id="39a0a-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="39a0a-107">Uma subárvore IPM para um repositório de entrega consiste em pelo menos as seguintes pastas:</span><span class="sxs-lookup"><span data-stu-id="39a0a-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="39a0a-108">Caixa de Entrada</span><span class="sxs-lookup"><span data-stu-id="39a0a-108">Inbox</span></span>
    
- <span data-ttu-id="39a0a-109">Caixa de saída</span><span class="sxs-lookup"><span data-stu-id="39a0a-109">Outbox</span></span>
    
- <span data-ttu-id="39a0a-110">Itens enviados</span><span class="sxs-lookup"><span data-stu-id="39a0a-110">Sent Items</span></span>
    
- <span data-ttu-id="39a0a-111">Itens excluídos</span><span class="sxs-lookup"><span data-stu-id="39a0a-111">Deleted Items</span></span>
    
<span data-ttu-id="39a0a-112">Estes são os nomes padrão e funções para cada uma dessas pastas; um cliente pode especificar seus próprio nomes se os nomes padrão não forem adequados.</span><span class="sxs-lookup"><span data-stu-id="39a0a-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="39a0a-113">MAPI atribui nomes padrão e associações para essas pastas manter as mensagens de desaparecimento inadvertidamente se um cliente não estabelece pastas de recebimento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="39a0a-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="39a0a-114">Em um contexto do Microsoft Office Outlook, uma subárvore IPM consiste em pastas padrão adicionais para o calendário, contatos, tarefas, anotações e diário.</span><span class="sxs-lookup"><span data-stu-id="39a0a-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="39a0a-115">A caixa de entrada normalmente contém mensagens de entrada e a caixa de saída armazena mensagens de saída (ou seja, mensagens aguardando para serem enviadas).</span><span class="sxs-lookup"><span data-stu-id="39a0a-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="39a0a-116">A pasta Itens enviados contém uma cópia de cada mensagem enviada, se o cliente definiu a propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) como o identificador de entrada dessa pasta.</span><span class="sxs-lookup"><span data-stu-id="39a0a-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="39a0a-117">A pasta Itens excluídos contém mensagens marcadas para remoção.</span><span class="sxs-lookup"><span data-stu-id="39a0a-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39a0a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="39a0a-118">See also</span></span>



[<span data-ttu-id="39a0a-119">Pastas MAPI</span><span class="sxs-lookup"><span data-stu-id="39a0a-119">MAPI Folders</span></span>](mapi-folders.md)

