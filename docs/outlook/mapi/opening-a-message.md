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
ms.openlocfilehash: e0701e64469576a8241002a6ff11299d1c343556
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582977"
---
# <a name="opening-a-message"></a><span data-ttu-id="c0e87-103">Abrir uma mensagem</span><span class="sxs-lookup"><span data-stu-id="c0e87-103">Opening a message</span></span>
 
<span data-ttu-id="c0e87-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0e87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="c0e87-105">Para abrir uma mensagem</span><span class="sxs-lookup"><span data-stu-id="c0e87-105">To open a message</span></span>
  
1. <span data-ttu-id="c0e87-106">Recupere o identificador de entrada da mensagem de uma das seguintes fontes:</span><span class="sxs-lookup"><span data-stu-id="c0e87-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="c0e87-107">A linha que representa a mensagem na tabela de conteúdo de sua pasta pai.</span><span class="sxs-lookup"><span data-stu-id="c0e87-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="c0e87-108">Para obter mais informações sobre como trabalhar com uma tabela de conteúdo de pasta, consulte [As tabelas de conteúdo](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c0e87-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="c0e87-109">O membro **lpEntryID** da estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) que é enviado com uma notificação de mensagem nova.</span><span class="sxs-lookup"><span data-stu-id="c0e87-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="c0e87-110">Para obter mais informações sobre o recebimento e tratamento de notificações, consulte [Manipulação de notificações](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c0e87-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="c0e87-111">Uma chamada ao método [IMAPIProp::GetProps](imapiprop-getprops.md) da mensagem solicitando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c0e87-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="c0e87-112">Ligue para um dos seguintes métodos para abrir a mensagem, a configuração _lpEntryID_ ao identificador de entrada da mensagem **OpenEntry** :</span><span class="sxs-lookup"><span data-stu-id="c0e87-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="c0e87-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c0e87-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="c0e87-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c0e87-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="c0e87-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c0e87-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="c0e87-116">O método mais rápido pode ser usado apenas para mensagens de entrada e envolve a chamar o método de **IMAPIFolder::OpenEntry** da pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="c0e87-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="c0e87-117">O próximo método mais rápido, chamar o método de **IMsgStore::OpenEntry** do armazenamento de mensagens, é utilizável para todas as mensagens, assim como o método mais lento, chamar **IMAPISession::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="c0e87-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c0e87-118">Pastas e suas tabelas de conteúdo podem ser fechadas a qualquer momento sem afetar de qualquer uma das mensagens que foram abertas a partir do-los.</span><span class="sxs-lookup"><span data-stu-id="c0e87-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="c0e87-119">Para abrir uma mensagem que foi salvo no disco</span><span class="sxs-lookup"><span data-stu-id="c0e87-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="c0e87-120">Chame **StgOpenStorage** para recuperar um ponteiro de interface **IStorage** , passando o nome do arquivo de mensagens para o parâmetro _pwcsName_ .</span><span class="sxs-lookup"><span data-stu-id="c0e87-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="c0e87-121">Chame **OpenIMsgOnIStg** para recuperar um ponteiro de interface **IMessage** para acessar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c0e87-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


