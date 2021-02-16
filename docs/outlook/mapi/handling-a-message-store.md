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
ms.openlocfilehash: 933dbd95a4b2f82d78e6e8035936eb2be4ba09ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407540"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="36141-103">Manipular um repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="36141-103">Handling a message store</span></span>
  
<span data-ttu-id="36141-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36141-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36141-105">Lidar com um armazenamento de mensagens é uma parte importante do conjunto de tarefas de qualquer cliente.</span><span class="sxs-lookup"><span data-stu-id="36141-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="36141-106">Essas tarefas incluem abrir, copiar, mover, adicionar e excluir pastas e mensagens, exibir várias tabelas, definir propriedades e controlar níveis de acesso.</span><span class="sxs-lookup"><span data-stu-id="36141-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="36141-107">[Abrir um Armazenamento de Mensagens:](opening-a-message-store.md)descreve como abrir um ou mais armazenamentos de mensagens durante uma sessão.</span><span class="sxs-lookup"><span data-stu-id="36141-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="36141-108">[Abrir o Armazenamento de Mensagens Padrão:](opening-the-default-message-store.md)descreve como abrir o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="36141-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="36141-109">[Validando e inicializando um armazenamento de mensagens:](validating-and-initializing-a-message-store.md)descreve como inicializar e validar um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="36141-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="36141-110">[Pesquisar um Armazenamento de Mensagens:](searching-a-message-store.md)descreve como procurar uma ou mais pastas em busca de mensagens que corresponderem aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="36141-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="36141-111">[Selecionando uma Pasta de](selecting-a-receive-folder.md)Recebimento: descreve as etapas para criar uma pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="36141-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="36141-112">[Abrir uma pasta do armazenamento](opening-a-message-store-folder.md)de mensagens: descreve como abrir uma pasta.</span><span class="sxs-lookup"><span data-stu-id="36141-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="36141-113">[Exibindo uma tabela de conteúdo de pasta:](displaying-a-folder-contents-table.md)descreve como exibir a tabela de conteúdo da pasta que contém informações resumidas sobre todas as suas mensagens.</span><span class="sxs-lookup"><span data-stu-id="36141-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="36141-114">[Percorrendo a pasta Caixa de](traversing-the-inbox-folder.md)Entrada: descreve como percorrer todas as mensagens na Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="36141-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="36141-115">[Copiar ou mover uma mensagem ou uma pasta:](copying-or-moving-a-message-or-a-folder.md)descreve como copiar ou mover uma ou mais mensagens.</span><span class="sxs-lookup"><span data-stu-id="36141-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="36141-116">[Abrir uma mensagem:](opening-a-message.md)descreve como abrir uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="36141-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="36141-117">[Localizar o ícone de uma mensagem:](finding-the-icon-for-a-message.md)descreve como encontrar um ícone associado a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="36141-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="36141-118">[Abrir um Descritor de Exibição:](opening-a-view-descriptor.md)descreve como abrir um descritor de exibição.</span><span class="sxs-lookup"><span data-stu-id="36141-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="36141-119">[Excluindo uma mensagem:](deleting-a-message.md)descreve como excluir uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="36141-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="36141-120">[Salvar uma mensagem na Caixa de](saving-a-message-in-the-inbox.md)Entrada: descreve como armazenar uma mensagem na Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="36141-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="36141-121">[Localizando mensagens enviadas ou salvas:](finding-sent-or-saved-messages.md)descreve como localizar todas as mensagens de saída que foram salvas ou enviadas.</span><span class="sxs-lookup"><span data-stu-id="36141-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="36141-122">[Acompanhar conversas:](tracking-conversations.md)descreve como acompanhar conversas.</span><span class="sxs-lookup"><span data-stu-id="36141-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

