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
# <a name="opening-a-message"></a>Abrir uma mensagem
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>Para abrir uma mensagem
  
1. Recupere o identificador de entrada da mensagem de uma das seguintes fontes:
    
   - A linha que representa a mensagem no índice de conteúdo de sua pasta pai. Para obter mais informações sobre como trabalhar com uma tabela de conteúdo de pasta, consulte [Tabelas de Conteúdo.](contents-tables.md)
    
   - O **membro lpEntryID** da estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) enviada com uma nova notificação por email. Para obter mais informações sobre como receber e manipular notificações, consulte [Manipulando notificações.](handling-notifications.md)
    
   - Uma chamada para o método [IMAPIProp::GetProps](imapiprop-getprops.md) da mensagem que solicita a **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
    
2. Chame um dos seguintes **métodos OpenEntry** para abrir a mensagem, definindo  _lpEntryID_ como o identificador de entrada da mensagem: 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  O método mais rápido só pode ser usado para mensagens de entrada e envolve chamar o método **IMAPIFolder::OpenEntry** da pasta de recebimento. O próximo método mais rápido, chamando o método **IMsgStore::OpenEntry** do repositório de mensagens, pode ser usado para todas as mensagens, como é o método mais lento, chamando **IMAPISession::OpenEntry**.
    
> [!NOTE]
> As pastas e seus índices de conteúdo podem ser fechados a qualquer momento sem afetar negativamente qualquer uma das mensagens que foram abertas dentro delas. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Para abrir uma mensagem que foi salva no disco
  
1. Chame **StgOpenStorage** para recuperar um ponteiro da interface **IStorage,** passando o nome do arquivo de mensagem para o _parâmetro pwcsName._ 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Chame **OpenIMsgOnIStg** para recuperar um ponteiro da interface **IMessage** para acessar a mensagem. 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


