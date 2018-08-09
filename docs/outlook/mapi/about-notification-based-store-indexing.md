---
title: Sobre a indexação de repositórios baseados em notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 338ae3c3c8d8b4037ab0c7b46916e45cf5a8ded2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766093"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="f799f-103">Sobre a indexação de repositórios baseados em notificação</span><span class="sxs-lookup"><span data-stu-id="f799f-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="f799f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f799f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f799f-105">Um provedor de repositório MAPI pode especificar se o manipulador de protocolo MAPI rastreamentos e índices de mensagens no repositório ou se o repositório envia notificações para o indexador quando há mensagens a serem indexados.</span><span class="sxs-lookup"><span data-stu-id="f799f-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="f799f-106">O último é conhecido como indexação baseada em notificação e um repositório que ofereça suporte a indexação baseada em notificação é um conhecido como um repositório pusher.</span><span class="sxs-lookup"><span data-stu-id="f799f-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="f799f-107">Um provedor de armazenamento que ofereça suporte a conjuntos de indexação baseados em notificação o sinalizador **STORE_PUSHER_OK** na propriedade **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="f799f-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="f799f-108">O manipulador de protocolo MAPI ou um cliente pode obter a propriedade **PR_STORE_SUPPORT_MASK** para determinar as características do repositório.</span><span class="sxs-lookup"><span data-stu-id="f799f-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="f799f-109">Sempre que houver um anexo, pasta ou uma mensagem a ser indexado, o provedor de armazenamento gera um MAPI URL Uniform Resource Locator () que identifica o objeto a ser indexado e enviá-la para o indexador.</span><span class="sxs-lookup"><span data-stu-id="f799f-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="f799f-110">Essa URL MAPI é codificado em Unicode e deve identificar exclusivamente o objeto para o manipulador de protocolo de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f799f-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="f799f-111">Para obter mais informações sobre URLs de MAPI, consulte [Sobre URLs de MAPI para indexação com base em notificação](about-mapi-urls-for-notification-based-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="f799f-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="f799f-112">Porque um indexador sempre não pode indexar tudo antes da ocorrência de um desligamento em um repositório pusher, o repositório de pusher deve persistir o que precisa ser enviada.</span><span class="sxs-lookup"><span data-stu-id="f799f-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="f799f-113">Quando um provedor de armazenamento envia uma notificação sobre um objeto que precisa ser indexado, ele especifica o tipo de notificação **fnevIndexing** no membro **ulEventType** da estrutura de **[notificação](notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="f799f-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="f799f-114">O membro **info** da estrutura de **notificação** contém uma estrutura **[EXTENDED_NOTIFICATION](extended_notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="f799f-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="f799f-115">O provedor de armazenamento identifica o processo na propriedade **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="f799f-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="f799f-116">Ele também identifica o processo na estrutura de [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) e passa essas informações como parte do membro **pbEventParameters** da estrutura **EXTENDED_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="f799f-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="f799f-117">Se o processo for desligado ou falha, o manipulador de protocolo MAPI poderão detectar que imediatamente e interromper a indexação o repositório pusher.</span><span class="sxs-lookup"><span data-stu-id="f799f-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f799f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f799f-118">See also</span></span>



[<span data-ttu-id="f799f-119">Sobre a API de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f799f-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="f799f-120">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f799f-120">MAPI Constants</span></span>](mapi-constants.md)

