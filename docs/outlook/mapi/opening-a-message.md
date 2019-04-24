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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348605"
---
# <a name="opening-a-message"></a>Abrir uma mensagem
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>Para abrir uma mensagem
  
1. Recupere o identificador de entrada da mensagem de uma das seguintes fontes:
    
   - A linha que representa a mensagem na tabela de conteúdo de sua pasta pai. Para obter mais informações sobre como trabalhar com uma tabela de conteúdo da pasta, consulte [tabelas de conteúdo](contents-tables.md).
    
   - O membro **lpEntryID** da estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) que é enviado com uma nova notificação de email. Para obter mais informações sobre o recebimento e o tratamento de notificações, consulte [Handling Notifications](handling-notifications.md).
    
   - Uma chamada para o método [IMAPIProp::](imapiprop-getprops.md) GetProps da mensagem solicitando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
    
2. Chame um dos seguintes métodos **OpenEntry** para abrir a mensagem, configurando _lpEntryID_ para o identificador de entrada da mensagem: 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  O método mais rápido é utilizável somente para mensagens de entrada e envolve chamar o método **IMAPIFolder:: OpenEntry** da pasta de recebimento. O próximo método mais rápido, chamar o método **IMsgStore:: OpenEntry** do repositório de mensagens, pode ser usado para todas as mensagens, como é o método mais lento, chamando **IMAPISession:: OpenEntry**.
    
> [!NOTE]
> Pastas e suas tabelas de conteúdo podem ser fechadas a qualquer momento sem afetar adversamente qualquer uma das mensagens que foram abertas dentro delas. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Para abrir uma mensagem que foi salva no disco
  
1. Chame **StgOpenStorage** para recuperar um ponteiro de interface **IStorage** , passando o nome do arquivo de mensagem para o parâmetro _pwcsName_ . 
    
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


