---
title: Subárvore IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421218"
---
# <a name="ipm-subtree"></a><span data-ttu-id="d7b35-103">Subárvore IPM</span><span class="sxs-lookup"><span data-stu-id="d7b35-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="d7b35-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7b35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7b35-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span><span class="sxs-lookup"><span data-stu-id="d7b35-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="d7b35-106">As mensagens trocadas entre destinatários humanos são conhecidas como mensagens interpersonalas, e essa árvore é conhecida como a mensagem interpersonal ou subárvore IPM.</span><span class="sxs-lookup"><span data-stu-id="d7b35-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="d7b35-107">Uma subárvore IPM para um armazenamento de entrega consiste em pelo menos as seguintes pastas:</span><span class="sxs-lookup"><span data-stu-id="d7b35-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="d7b35-108">Caixa de Entrada</span><span class="sxs-lookup"><span data-stu-id="d7b35-108">Inbox</span></span>
    
- <span data-ttu-id="d7b35-109">Caixa de saída</span><span class="sxs-lookup"><span data-stu-id="d7b35-109">Outbox</span></span>
    
- <span data-ttu-id="d7b35-110">Itens enviados</span><span class="sxs-lookup"><span data-stu-id="d7b35-110">Sent Items</span></span>
    
- <span data-ttu-id="d7b35-111">Itens excluídos</span><span class="sxs-lookup"><span data-stu-id="d7b35-111">Deleted Items</span></span>
    
<span data-ttu-id="d7b35-112">Estes são os nomes e funções padrão para cada uma dessas pastas; um cliente pode especificar seus próprios nomes se os nomes padrão não são apropriados.</span><span class="sxs-lookup"><span data-stu-id="d7b35-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="d7b35-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client negligencs to establish receiving folders for messages.</span><span class="sxs-lookup"><span data-stu-id="d7b35-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="d7b35-114">Em um contexto do Microsoft Office Outlook, uma subárvore IPM consiste em pastas padrão adicionais para Calendário, Contatos, Tarefas, Anotações e Diário.</span><span class="sxs-lookup"><span data-stu-id="d7b35-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="d7b35-115">A Caixa de Entrada normalmente retém mensagens de entrada, e a Caixa de Saída contém mensagens de saída (ou seja, mensagens aguardando serem enviadas).</span><span class="sxs-lookup"><span data-stu-id="d7b35-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="d7b35-116">A pasta Itens Enviados manterá uma cópia de cada mensagem enviada se o cliente tiver definido a propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) para o identificador de entrada dessa pasta.</span><span class="sxs-lookup"><span data-stu-id="d7b35-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="d7b35-117">A pasta Itens Excluídos contém mensagens marcadas para remoção.</span><span class="sxs-lookup"><span data-stu-id="d7b35-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7b35-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7b35-118">See also</span></span>



[<span data-ttu-id="d7b35-119">Pastas MAPI</span><span class="sxs-lookup"><span data-stu-id="d7b35-119">MAPI Folders</span></span>](mapi-folders.md)

