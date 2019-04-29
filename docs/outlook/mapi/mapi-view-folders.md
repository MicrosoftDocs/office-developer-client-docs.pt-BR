---
title: Pastas de exibição MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ca9e5138d3ded13dfe33037f75e43ef1098f3c2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412531"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="92074-103">Pastas de exibição MAPI</span><span class="sxs-lookup"><span data-stu-id="92074-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="92074-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92074-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92074-105">As pastas de exibição são pastas raiz que contêm informações associadas para definir layouts de exibição alternativos para o conteúdo de pastas de mensagens interpessoais (IPM).</span><span class="sxs-lookup"><span data-stu-id="92074-105">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders.</span></span> <span data-ttu-id="92074-106">As pastas de exibição residem na raiz do repositório de mensagens e, portanto, não são visíveis no aplicativo cliente típico.</span><span class="sxs-lookup"><span data-stu-id="92074-106">View folders reside under the root for the message store and, therefore, are not visible in the typical client application.</span></span> <span data-ttu-id="92074-107">Nem todos os repositórios de mensagens incluem pastas de exibição; somente os repositórios de mensagens que estão configurados para funcionar como o repositório de mensagens padrão para a sessão devem incluí-los.</span><span class="sxs-lookup"><span data-stu-id="92074-107">Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="92074-108">O MAPI dá suporte a duas pastas de exibição:</span><span class="sxs-lookup"><span data-stu-id="92074-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="92074-109">Comum — a pasta de modo de exibição comum contém modos de exibição padrão para o repositório de mensagens e pode ser usada por qualquer usuário de um cliente que acessa o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="92074-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="92074-110">O identificador de entrada para a pasta de modo de exibição comum é armazenado na propriedade **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) da loja.</span><span class="sxs-lookup"><span data-stu-id="92074-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="92074-111">Pessoal — a pasta de exibição pessoal contém exibições definidas por um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="92074-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="92074-112">MAPI define a propriedade **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) para conter o identificador de entrada da pasta de exibição pessoal.</span><span class="sxs-lookup"><span data-stu-id="92074-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="92074-113">Usando modos de exibição pessoais, por exemplo, um usuário pode ver um grupo de mensagens classificadas por remetente, listando apenas o assunto da mensagem e a data de recebimento; outro usuário pode ver o mesmo grupo classificado por data, listando o assunto, o remetente e o tamanho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="92074-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92074-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="92074-114">See also</span></span>



[<span data-ttu-id="92074-115">Pastas MAPI</span><span class="sxs-lookup"><span data-stu-id="92074-115">MAPI Folders</span></span>](mapi-folders.md)

