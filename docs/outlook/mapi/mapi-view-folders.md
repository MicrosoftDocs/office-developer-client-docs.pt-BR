---
title: Exibir as pastas de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cb26771e9968175ab67366e35cf019ce23d51b8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767975"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="1795f-103">Exibir as pastas de MAPI</span><span class="sxs-lookup"><span data-stu-id="1795f-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="1795f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1795f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1795f-105">Exibir pastas são pastas raiz que contêm informações associadas para definir layouts de exibição alternativo para o conteúdo das pastas de mensagem interpessoais (IPM).</span><span class="sxs-lookup"><span data-stu-id="1795f-105">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders.</span></span> <span data-ttu-id="1795f-106">Exibir pastas residem sob a raiz para o armazenamento de mensagens e, portanto, não são visíveis no aplicativo cliente típico.</span><span class="sxs-lookup"><span data-stu-id="1795f-106">View folders reside under the root for the message store and, therefore, are not visible in the typical client application.</span></span> <span data-ttu-id="1795f-107">Nem todo armazenamento de mensagens inclui pastas de exibição; somente armazenamentos de mensagens que estão configurados para funcionar como o armazenamento de mensagens padrão para a sessão devem inclui-los.</span><span class="sxs-lookup"><span data-stu-id="1795f-107">Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="1795f-108">MAPI suporta duas pastas de exibição:</span><span class="sxs-lookup"><span data-stu-id="1795f-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="1795f-109">Comum — A pasta de exibição comuns contém modos de exibição que são padrão para o armazenamento de mensagens e podem ser usados por qualquer usuário de um cliente que acessa o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1795f-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="1795f-110">O identificador de entrada para a pasta de exibição comuns é armazenado na propriedade de **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) da loja.</span><span class="sxs-lookup"><span data-stu-id="1795f-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="1795f-111">Pessoal — A pasta de exibição pessoal contém modos de exibição que são definidos por um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="1795f-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="1795f-112">MAPI define a propriedade **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) para reter o identificador de entrada da pasta de exibição pessoal.</span><span class="sxs-lookup"><span data-stu-id="1795f-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="1795f-113">Usando as exibições pessoais, por exemplo, um usuário pode examinar um grupo de mensagens, classificados por remetente, listando apenas a mensagem assunto e recebimento data; outro usuário pode examinar o mesmo grupo classificado por data, listando o assunto, o remetente e o tamanho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1795f-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1795f-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="1795f-114">See also</span></span>



[<span data-ttu-id="1795f-115">Pastas MAPI</span><span class="sxs-lookup"><span data-stu-id="1795f-115">MAPI Folders</span></span>](mapi-folders.md)

