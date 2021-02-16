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
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435891"
---
# <a name="handling-table-notification"></a><span data-ttu-id="5a8f9-103">Manipular notificações de tabela</span><span class="sxs-lookup"><span data-stu-id="5a8f9-103">Handling table notification</span></span>

<span data-ttu-id="5a8f9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a8f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a8f9-105">Como alternativa ao registro direto com um objeto de origem de aviso, como uma pasta ou um usuário de mensagens, um cliente pode se registrar para notificações em um conteúdo ou tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="5a8f9-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="5a8f9-106">O rastreamento de alterações em entradas, pastas e mensagens de um conteúdo ou de uma tabela de hierarquia pode ser mais simples e simples do que por meio de objetos individuais.</span><span class="sxs-lookup"><span data-stu-id="5a8f9-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="5a8f9-107">Por exemplo, você pode chamar [IMAPITable::Advise](imapitable-advise.md) na tabela de hierarquia de uma pasta para descobrir quando ocorrem alterações em uma de suas subpastas.</span><span class="sxs-lookup"><span data-stu-id="5a8f9-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="5a8f9-108">Se você suportar a exibição de mensagens remotas, registre-se na tabela de status para observar a atividade dos provedores de transporte e do spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="5a8f9-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="5a8f9-109">No entanto, nem sempre é preferível usar notificações de tabela em vez de notificações de objeto.</span><span class="sxs-lookup"><span data-stu-id="5a8f9-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="5a8f9-110">O monitoramento de alterações no número de mensagens em uma pasta é um exemplo de quando seu cliente pode precisar se registrar para notificações de objeto em uma pasta, em vez de em uma tabela implementada pela pasta.</span><span class="sxs-lookup"><span data-stu-id="5a8f9-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

