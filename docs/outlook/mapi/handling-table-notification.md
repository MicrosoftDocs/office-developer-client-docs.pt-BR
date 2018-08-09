---
title: Manipulação de notificação de tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 95ef351e4fe906608319a3e25de8f20a44e23d9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766693"
---
# <a name="handling-table-notification"></a><span data-ttu-id="7f02f-103">Manipulação de notificação de tabela</span><span class="sxs-lookup"><span data-stu-id="7f02f-103">Handling table notification</span></span>

<span data-ttu-id="7f02f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f02f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f02f-105">Como uma alternativa para registrar-se diretamente com um objeto de origem de advise, como uma pasta ou um usuário de mensagens, um cliente pode registrar para notificações sobre um conteúdo ou tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="7f02f-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="7f02f-106">Controle de alterações endereço livro entradas, pastas e mensagens por meio de um conteúdo ou tabela de hierarquia pode ser mais simples e mais simples do que por meio de objetos individuais.</span><span class="sxs-lookup"><span data-stu-id="7f02f-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="7f02f-107">Por exemplo, você pode chamar [IMAPITable::Advise](imapitable-advise.md) na tabela de hierarquia de uma pasta para descobrir quando as alterações ocorrem para uma de suas subpastas.</span><span class="sxs-lookup"><span data-stu-id="7f02f-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="7f02f-108">Caso você ofereça suporte à exibição de mensagens remotas, registre-se com a tabela de status a serem observadas atividade por provedores de transporte e o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="7f02f-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="7f02f-109">No entanto, não é sempre preferível usar notificações de tabela, em vez de notificações de objeto.</span><span class="sxs-lookup"><span data-stu-id="7f02f-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="7f02f-110">Monitoramento das alterações no número de mensagens em uma pasta é um exemplo de quando seu cliente talvez precisem registrar para notificações do objeto em uma pasta, e não em uma tabela implementadas pela pasta.</span><span class="sxs-lookup"><span data-stu-id="7f02f-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

