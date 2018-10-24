---
title: Manipular notificações de tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b36e4697bfd4360f4ea6ea47c70eaaae434696d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595129"
---
# <a name="handling-table-notification"></a><span data-ttu-id="2dec0-103">Manipular notificações de tabela</span><span class="sxs-lookup"><span data-stu-id="2dec0-103">Handling table notification</span></span>

<span data-ttu-id="2dec0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dec0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dec0-105">Como uma alternativa para registrar-se diretamente com um objeto de origem de advise, como uma pasta ou um usuário de mensagens, um cliente pode registrar para notificações sobre um conteúdo ou tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="2dec0-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="2dec0-106">Controle de alterações endereço livro entradas, pastas e mensagens por meio de um conteúdo ou tabela de hierarquia pode ser mais simples e mais simples do que por meio de objetos individuais.</span><span class="sxs-lookup"><span data-stu-id="2dec0-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="2dec0-107">Por exemplo, você pode chamar [IMAPITable::Advise](imapitable-advise.md) na tabela de hierarquia de uma pasta para descobrir quando as alterações ocorrem para uma de suas subpastas.</span><span class="sxs-lookup"><span data-stu-id="2dec0-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="2dec0-108">Caso você ofereça suporte à exibição de mensagens remotas, registre-se com a tabela de status a serem observadas atividade por provedores de transporte e o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="2dec0-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="2dec0-109">No entanto, não é sempre preferível usar notificações de tabela, em vez de notificações de objeto.</span><span class="sxs-lookup"><span data-stu-id="2dec0-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="2dec0-110">Monitoramento das alterações no número de mensagens em uma pasta é um exemplo de quando seu cliente talvez precisem registrar para notificações do objeto em uma pasta, e não em uma tabela implementadas pela pasta.</span><span class="sxs-lookup"><span data-stu-id="2dec0-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

