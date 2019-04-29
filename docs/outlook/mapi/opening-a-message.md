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
# <a name="opening-a-message"></a><span data-ttu-id="7fdec-103">Abrir uma mensagem</span><span class="sxs-lookup"><span data-stu-id="7fdec-103">Opening a message</span></span>
 
<span data-ttu-id="7fdec-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fdec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="7fdec-105">Para abrir uma mensagem</span><span class="sxs-lookup"><span data-stu-id="7fdec-105">To open a message</span></span>
  
1. <span data-ttu-id="7fdec-106">Recupere o identificador de entrada da mensagem de uma das seguintes fontes:</span><span class="sxs-lookup"><span data-stu-id="7fdec-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="7fdec-107">A linha que representa a mensagem na tabela de conteúdo de sua pasta pai.</span><span class="sxs-lookup"><span data-stu-id="7fdec-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="7fdec-108">Para obter mais informações sobre como trabalhar com uma tabela de conteúdo da pasta, consulte [tabelas de conteúdo](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7fdec-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="7fdec-109">O membro **lpEntryID** da estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) que é enviado com uma nova notificação de email.</span><span class="sxs-lookup"><span data-stu-id="7fdec-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="7fdec-110">Para obter mais informações sobre o recebimento e o tratamento de notificações, consulte [Handling Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7fdec-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="7fdec-111">Uma chamada para o método [IMAPIProp::](imapiprop-getprops.md) GetProps da mensagem solicitando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7fdec-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="7fdec-112">Chame um dos seguintes métodos **OpenEntry** para abrir a mensagem, configurando _lpEntryID_ para o identificador de entrada da mensagem:</span><span class="sxs-lookup"><span data-stu-id="7fdec-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="7fdec-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7fdec-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="7fdec-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7fdec-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="7fdec-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7fdec-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="7fdec-116">O método mais rápido é utilizável somente para mensagens de entrada e envolve chamar o método **IMAPIFolder:: OpenEntry** da pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="7fdec-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="7fdec-117">O próximo método mais rápido, chamar o método **IMsgStore:: OpenEntry** do repositório de mensagens, pode ser usado para todas as mensagens, como é o método mais lento, chamando **IMAPISession:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="7fdec-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7fdec-118">Pastas e suas tabelas de conteúdo podem ser fechadas a qualquer momento sem afetar adversamente qualquer uma das mensagens que foram abertas dentro delas.</span><span class="sxs-lookup"><span data-stu-id="7fdec-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="7fdec-119">Para abrir uma mensagem que foi salva no disco</span><span class="sxs-lookup"><span data-stu-id="7fdec-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="7fdec-120">Chame **StgOpenStorage** para recuperar um ponteiro de interface **IStorage** , passando o nome do arquivo de mensagem para o parâmetro _pwcsName_ .</span><span class="sxs-lookup"><span data-stu-id="7fdec-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="7fdec-121">Chame **OpenIMsgOnIStg** para recuperar um ponteiro de interface **IMessage** para acessar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="7fdec-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


