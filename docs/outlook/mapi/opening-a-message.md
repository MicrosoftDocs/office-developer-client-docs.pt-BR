---
title: Abrir uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bf633a971f7e3077ce2f418021ef183a36db8cc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411089"
---
# <a name="opening-a-message"></a><span data-ttu-id="db64b-103">Abrir uma mensagem</span><span class="sxs-lookup"><span data-stu-id="db64b-103">Opening a message</span></span>
 
<span data-ttu-id="db64b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db64b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="db64b-105">Para abrir uma mensagem</span><span class="sxs-lookup"><span data-stu-id="db64b-105">To open a message</span></span>
  
1. <span data-ttu-id="db64b-106">Recupere o identificador de entrada da mensagem de uma das seguintes fontes:</span><span class="sxs-lookup"><span data-stu-id="db64b-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="db64b-107">A linha que representa a mensagem no índice de conteúdo de sua pasta pai.</span><span class="sxs-lookup"><span data-stu-id="db64b-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="db64b-108">Para obter mais informações sobre como trabalhar com uma tabela de conteúdo de pasta, consulte [Tabelas de Conteúdo.](contents-tables.md)</span><span class="sxs-lookup"><span data-stu-id="db64b-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="db64b-109">O **membro lpEntryID** da estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) enviada com uma nova notificação por email.</span><span class="sxs-lookup"><span data-stu-id="db64b-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="db64b-110">Para obter mais informações sobre como receber e manipular notificações, consulte [Manipulando notificações.](handling-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="db64b-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="db64b-111">Uma chamada para o método [IMAPIProp::GetProps](imapiprop-getprops.md) da mensagem que solicita a **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="db64b-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="db64b-112">Chame um dos seguintes **métodos OpenEntry** para abrir a mensagem, definindo  _lpEntryID_ como o identificador de entrada da mensagem:</span><span class="sxs-lookup"><span data-stu-id="db64b-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="db64b-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="db64b-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="db64b-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="db64b-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="db64b-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="db64b-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="db64b-116">O método mais rápido só pode ser usado para mensagens de entrada e envolve chamar o método **IMAPIFolder::OpenEntry** da pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="db64b-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="db64b-117">O próximo método mais rápido, chamando o método **IMsgStore::OpenEntry** do repositório de mensagens, pode ser usado para todas as mensagens, como é o método mais lento, chamando **IMAPISession::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="db64b-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="db64b-118">As pastas e seus índices de conteúdo podem ser fechados a qualquer momento sem afetar negativamente qualquer uma das mensagens que foram abertas dentro delas.</span><span class="sxs-lookup"><span data-stu-id="db64b-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="db64b-119">Para abrir uma mensagem que foi salva no disco</span><span class="sxs-lookup"><span data-stu-id="db64b-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="db64b-120">Chame **StgOpenStorage** para recuperar um ponteiro da interface **IStorage,** passando o nome do arquivo de mensagem para o _parâmetro pwcsName._</span><span class="sxs-lookup"><span data-stu-id="db64b-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="db64b-121">Chame **OpenIMsgOnIStg** para recuperar um ponteiro da interface **IMessage** para acessar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="db64b-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


