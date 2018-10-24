---
title: Manipular um repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7eca0e1f-a855-4ef7-b892-0bddee59de5e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0712407a7882c449c065cb6816694b4a1611036f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568466"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="34cd3-103">Manipular um repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="34cd3-103">Handling a message store</span></span>
  
<span data-ttu-id="34cd3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34cd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34cd3-105">Manipulação de um armazenamento de mensagens é uma parte importante do conjunto de qualquer cliente de tarefas.</span><span class="sxs-lookup"><span data-stu-id="34cd3-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="34cd3-106">Essas tarefas incluem a abertura, copiar, mover, adicionando e excluindo pastas e mensagens, exibindo várias tabelas, definindo propriedades e controlar níveis de acesso.</span><span class="sxs-lookup"><span data-stu-id="34cd3-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="34cd3-107">[Abrindo um armazenamento de mensagens](opening-a-message-store.md): descreve como abrir um ou mais armazenamentos de mensagem durante uma sessão.</span><span class="sxs-lookup"><span data-stu-id="34cd3-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="34cd3-108">[Abrindo o armazenamento de mensagens padrão](opening-the-default-message-store.md): descreve como abrir o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="34cd3-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="34cd3-109">[Validando e inicializar um armazenamento de mensagens](validating-and-initializing-a-message-store.md): descreve como inicializar e validar um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="34cd3-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="34cd3-110">[Pesquisando um armazenamento de mensagens](searching-a-message-store.md): descreve como pesquisar por meio de uma ou mais pastas procurando mensagens que correspondam a critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="34cd3-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="34cd3-111">[Selecionando uma pasta de recebimento](selecting-a-receive-folder.md): descreve as etapas para a criação de uma pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="34cd3-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="34cd3-112">[Abrir uma pasta de repositório de mensagens](opening-a-message-store-folder.md): descreve como abrir uma pasta.</span><span class="sxs-lookup"><span data-stu-id="34cd3-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="34cd3-113">[Exibindo uma tabela de conteúdo de pasta](displaying-a-folder-contents-table.md): descreve como exibir a tabela de conteúdo de pasta que contém informações de resumo sobre todas as suas mensagens.</span><span class="sxs-lookup"><span data-stu-id="34cd3-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="34cd3-114">[Atravessando a pasta caixa de entrada](traversing-the-inbox-folder.md): descreve como percorrer todas as mensagens na caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="34cd3-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="34cd3-115">[Copiar ou mover uma mensagem ou uma pasta](copying-or-moving-a-message-or-a-folder.md): descreve como copiar ou mover uma ou mais mensagens.</span><span class="sxs-lookup"><span data-stu-id="34cd3-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="34cd3-116">[Abrindo uma mensagem](opening-a-message.md): descreve como abrir uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="34cd3-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="34cd3-117">[Localizando o ícone de uma mensagem](finding-the-icon-for-a-message.md): descreve como localizar um ícone que é associado a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="34cd3-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="34cd3-118">[Abrindo um descritor de modo de exibição](opening-a-view-descriptor.md): descreve como abrir um descritor de modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="34cd3-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="34cd3-119">[Exclusão de uma mensagem](deleting-a-message.md): descreve como excluir uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="34cd3-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="34cd3-120">[Salvando uma mensagem na caixa de entrada](saving-a-message-in-the-inbox.md): descreve como armazenar uma mensagem na caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="34cd3-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="34cd3-121">[Localizando enviadas ou mensagens salvas](finding-sent-or-saved-messages.md): descreve como localizar todas as mensagens de saída que foram salvas ou enviadas.</span><span class="sxs-lookup"><span data-stu-id="34cd3-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="34cd3-122">[Acompanhamento de conversas](tracking-conversations.md): descreve como controlar as conversas.</span><span class="sxs-lookup"><span data-stu-id="34cd3-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

