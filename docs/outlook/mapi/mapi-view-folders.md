---
title: Exibir as pastas de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3a89588294f07dca97fb48e56d2cde890c3f80ae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568816"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="f8aed-103">Exibir as pastas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f8aed-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="f8aed-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8aed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8aed-105">Exibir pastas são pastas raiz que contêm informações associadas para definir layouts de exibição alternativo para o conteúdo das pastas de mensagem interpessoais (IPM).</span><span class="sxs-lookup"><span data-stu-id="f8aed-105">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders.</span></span> <span data-ttu-id="f8aed-106">Exibir pastas residem sob a raiz para o armazenamento de mensagens e, portanto, não são visíveis no aplicativo cliente típico.</span><span class="sxs-lookup"><span data-stu-id="f8aed-106">View folders reside under the root for the message store and, therefore, are not visible in the typical client application.</span></span> <span data-ttu-id="f8aed-107">Nem todo armazenamento de mensagens inclui pastas de exibição; somente armazenamentos de mensagens que estão configurados para funcionar como o armazenamento de mensagens padrão para a sessão devem inclui-los.</span><span class="sxs-lookup"><span data-stu-id="f8aed-107">Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="f8aed-108">MAPI suporta duas pastas de exibição:</span><span class="sxs-lookup"><span data-stu-id="f8aed-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="f8aed-109">Comum — A pasta de exibição comuns contém modos de exibição que são padrão para o armazenamento de mensagens e podem ser usados por qualquer usuário de um cliente que acessa o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f8aed-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="f8aed-110">O identificador de entrada para a pasta de exibição comuns é armazenado na propriedade de **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) da loja.</span><span class="sxs-lookup"><span data-stu-id="f8aed-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="f8aed-111">Pessoal — A pasta de exibição pessoal contém modos de exibição que são definidos por um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="f8aed-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="f8aed-112">MAPI define a propriedade **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) para reter o identificador de entrada da pasta de exibição pessoal.</span><span class="sxs-lookup"><span data-stu-id="f8aed-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="f8aed-113">Usando as exibições pessoais, por exemplo, um usuário pode examinar um grupo de mensagens, classificados por remetente, listando apenas a mensagem assunto e recebimento data; outro usuário pode examinar o mesmo grupo classificado por data, listando o assunto, o remetente e o tamanho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f8aed-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8aed-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8aed-114">See also</span></span>



[<span data-ttu-id="f8aed-115">Pastas MAPI</span><span class="sxs-lookup"><span data-stu-id="f8aed-115">MAPI Folders</span></span>](mapi-folders.md)

