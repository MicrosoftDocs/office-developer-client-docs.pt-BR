---
title: SubÁrvore IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317105"
---
# <a name="ipm-subtree"></a><span data-ttu-id="5ff74-103">SubÁrvore IPM</span><span class="sxs-lookup"><span data-stu-id="5ff74-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="5ff74-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ff74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ff74-105">O MAPI cria uma árvore de pastas abaixo da pasta raiz de um repositório de mensagens para todos os clientes que enviam e recebem mensagens de pessoas humanas, e não de computador.</span><span class="sxs-lookup"><span data-stu-id="5ff74-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="5ff74-106">As mensagens trocadas entre destinatários humanos são conhecidas como mensagens interpessoais e esta árvore é conhecida como mensagem interpessoal, ou IPM, subárvore.</span><span class="sxs-lookup"><span data-stu-id="5ff74-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="5ff74-107">Uma sub-árvore IPM para um repositório de entrega consiste em pelo menos as seguintes pastas:</span><span class="sxs-lookup"><span data-stu-id="5ff74-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="5ff74-108">Caixa de Entrada</span><span class="sxs-lookup"><span data-stu-id="5ff74-108">Inbox</span></span>
    
- <span data-ttu-id="5ff74-109">Enviada</span><span class="sxs-lookup"><span data-stu-id="5ff74-109">Outbox</span></span>
    
- <span data-ttu-id="5ff74-110">Itens enviados</span><span class="sxs-lookup"><span data-stu-id="5ff74-110">Sent Items</span></span>
    
- <span data-ttu-id="5ff74-111">Itens excluídos</span><span class="sxs-lookup"><span data-stu-id="5ff74-111">Deleted Items</span></span>
    
<span data-ttu-id="5ff74-112">Estes são os nomes e funções padrão de cada uma dessas pastas; um cliente pode especificar seus próprios nomes se os nomes padrão não forem apropriados.</span><span class="sxs-lookup"><span data-stu-id="5ff74-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="5ff74-113">MAPI atribui nomes e associações padrão para essas pastas para manter as mensagens de desaparecer inadvertidamente se um cliente não consegue estabelecer pastas de recebimento para mensagens.</span><span class="sxs-lookup"><span data-stu-id="5ff74-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="5ff74-114">Em um contexto do Microsoft Office Outlook, uma subárvore IPM consiste em pastas padrão adicionais para calendário, contatos, tarefas, anotações e diário.</span><span class="sxs-lookup"><span data-stu-id="5ff74-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="5ff74-115">A caixa de entrada normalmente contém mensagens de entrada, e a caixa de saída mantém mensagens de saída (ou seja, mensagens que aguardam para serem enviadas).</span><span class="sxs-lookup"><span data-stu-id="5ff74-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="5ff74-116">A pasta Itens enviados mantém uma cópia de cada mensagem enviada se o cliente tiver definido a propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) para o identificador de entrada dessa pasta.</span><span class="sxs-lookup"><span data-stu-id="5ff74-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="5ff74-117">A pasta itens excluídos contém mensagens marcadas para remoção.</span><span class="sxs-lookup"><span data-stu-id="5ff74-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ff74-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ff74-118">See also</span></span>



[<span data-ttu-id="5ff74-119">Pastas MAPI</span><span class="sxs-lookup"><span data-stu-id="5ff74-119">MAPI Folders</span></span>](mapi-folders.md)

