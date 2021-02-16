---
title: Sobre Notification-Based Store Indexação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409171"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="e64d1-103">Sobre Notification-Based Store Indexação</span><span class="sxs-lookup"><span data-stu-id="e64d1-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="e64d1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e64d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e64d1-105">Um provedor de armazenamento MAPI pode especificar se o Manipulador de Protocolo MAPI rastreará e indexa mensagens no armazenamento ou se o armazenamento enviará notificações ao indexador quando houver mensagens a serem indexadas.</span><span class="sxs-lookup"><span data-stu-id="e64d1-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="e64d1-106">O último é conhecido como indexação baseada em notificação, e um armazenamento que oferece suporte à indexação baseada em notificação é conhecido como um armazenamento por push.</span><span class="sxs-lookup"><span data-stu-id="e64d1-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="e64d1-107">Um provedor de armazenamento que oferece suporte à indexação baseada em notificação define **o STORE_PUSHER_OK** de dados na **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** propriedade.</span><span class="sxs-lookup"><span data-stu-id="e64d1-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="e64d1-108">O Manipulador de Protocolo MAPI ou um cliente pode obter a **PR_STORE_SUPPORT_MASK** para determinar as características do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e64d1-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="e64d1-109">Sempre que houver um anexo, pasta ou mensagem a ser indexada, o provedor de armazenamento gera uma URL (Uniform Resource Locator) MAPI que identifica o objeto a ser indexado e o envia ao indexador.</span><span class="sxs-lookup"><span data-stu-id="e64d1-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="e64d1-110">Essa URL MAPI é codificada em Unicode e deve identificar exclusivamente o objeto para o Manipulador de Protocolo MAPI.</span><span class="sxs-lookup"><span data-stu-id="e64d1-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="e64d1-111">Para obter mais informações sobre URLs MAPI, consulte [Sobre URLs MAPI para Notification-Based indexação.](about-mapi-urls-for-notification-based-indexing.md)</span><span class="sxs-lookup"><span data-stu-id="e64d1-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="e64d1-112">Como um indexador não pode sempre indexar tudo antes que um desligamento ocorra em um armazenamento por push, o armazenamento do pusher deve manter o que precisa ser pressionado.</span><span class="sxs-lookup"><span data-stu-id="e64d1-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="e64d1-113">Quando um provedor de armazenamento envia uma notificação sobre um objeto que precisa ser indexado, ele especifica o tipo de notificação **fnevIndexing** no **membro ulEventType** da estrutura **[NOTIFICATION.](notification.md)**</span><span class="sxs-lookup"><span data-stu-id="e64d1-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="e64d1-114">A **estrutura** do membro de informações da **estrutura de** NOTIFICAÇÃO contém **[uma estrutura de](extended_notification.md)** EXTENDED_NOTIFICATION.</span><span class="sxs-lookup"><span data-stu-id="e64d1-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="e64d1-115">O provedor do armazenamento identifica o processo **[na](pidtagsearchownerid-canonical-property.md)** PR_SEARCH_OWNER_ID propriedade.</span><span class="sxs-lookup"><span data-stu-id="e64d1-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="e64d1-116">Ele também identifica o processo na estrutura [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) e passa essas informações como parte do membro **pbEventParameters** da estrutura **EXTENDED_NOTIFICATION** estrutura.</span><span class="sxs-lookup"><span data-stu-id="e64d1-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="e64d1-117">Se o processo for encerrado ou falhar, o Manipulador de Protocolo MAPI poderá detectar imediatamente isso e parar de indexar o armazenamento do pusher.</span><span class="sxs-lookup"><span data-stu-id="e64d1-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e64d1-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e64d1-118">See also</span></span>



[<span data-ttu-id="e64d1-119">Sobre a API de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="e64d1-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="e64d1-120">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="e64d1-120">MAPI Constants</span></span>](mapi-constants.md)

