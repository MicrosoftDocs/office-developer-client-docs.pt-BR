---
title: Abrindo uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4ea75f723a2fcb242d8b9a516498855aa20cfdd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768172"
---
# <a name="opening-a-message"></a>Abrindo uma mensagem
 
**Aplica-se a**: Outlook 
  
### <a name="to-open-a-message"></a>Para abrir uma mensagem
  
1. Recupere o identificador de entrada da mensagem de uma das seguintes fontes:
    
   - A linha que representa a mensagem na tabela de conteúdo de sua pasta pai. Para obter mais informações sobre como trabalhar com uma tabela de conteúdo de pasta, consulte [As tabelas de conteúdo](contents-tables.md).
    
   - O membro **lpEntryID** da estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) que é enviado com uma notificação de mensagem nova. Para obter mais informações sobre o recebimento e tratamento de notificações, consulte [Manipulação de notificações](handling-notifications.md).
    
   - Uma chamada ao método [IMAPIProp::GetProps](imapiprop-getprops.md) da mensagem solicitando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
    
2. Ligue para um dos seguintes métodos para abrir a mensagem, a configuração _lpEntryID_ ao identificador de entrada da mensagem **OpenEntry** : 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  O método mais rápido pode ser usado apenas para mensagens de entrada e envolve a chamar o método de **IMAPIFolder::OpenEntry** da pasta de recebimento. O próximo método mais rápido, chamar o método de **IMsgStore::OpenEntry** do armazenamento de mensagens, é utilizável para todas as mensagens, assim como o método mais lento, chamar **IMAPISession::OpenEntry**.
    
> [!NOTE]
> Pastas e suas tabelas de conteúdo podem ser fechadas a qualquer momento sem afetar de qualquer uma das mensagens que foram abertas a partir do-los. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Para abrir uma mensagem que foi salvo no disco
  
1. Chame **StgOpenStorage** para recuperar um ponteiro de interface **IStorage** , passando o nome do arquivo de mensagens para o parâmetro _pwcsName_ . 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Chame **OpenIMsgOnIStg** para recuperar um ponteiro de interface **IMessage** para acessar a mensagem. 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


