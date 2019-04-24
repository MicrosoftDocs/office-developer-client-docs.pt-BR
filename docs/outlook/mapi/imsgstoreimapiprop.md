---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348717"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso a informações do repositório de mensagens e mensagens e pastas.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Exposto por:  <br/> |Objeto do repositório de mensagens  <br/> |
|Implementado por:  <br/> |Provedores de repositórios de mensagens  <br/> |
|Chamado por:  <br/> |Aplicativos cliente, o spooler MAPI e o MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMsgStore  <br/> |
|Tipo de ponteiro:  <br/> |LPMDB  <br/> |
|Modelo de transação:  <br/> |Não-Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Utilizar](imsgstore-advise.md) <br/> |Registra para receber notificações de eventos específicos que afetam o repositório de mensagens.  <br/> |
|[Cancelar](imsgstore-unadvise.md) <br/> |Cancela o envio de notificações anteriormente configuradas com uma chamada para o método **IMsgStore:: Advise** .  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Compara dois identificadores de entrada para determinar se eles se referem à mesma entrada em um repositório de mensagens.  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |Abre uma pasta ou mensagem e retorna um ponteiro de interface para acesso adicional.  <br/> |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |Estabelece uma pasta como o destino de mensagens de entrada de uma determinada classe de mensagem.  <br/> |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |Obtém a pasta que foi estabelecida como o destino para mensagens de entrada de uma classe de mensagem especificada ou como a pasta de recebimento padrão para o repositório de mensagens.  <br/> |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |Fornece acesso à tabela de pastas de recebimento, uma tabela com informações sobre todas as pastas de recebimento do repositório de mensagens.  <br/> |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |Permite o logoff ordenada do repositório de mensagens.  <br/> |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |Tenta remover uma mensagem da fila de saída.  <br/> |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |Fornece acesso à tabela de fila de saída, uma tabela que tem informações sobre todas as mensagens na fila de saída do repositório de mensagens.  <br/> |
|[SetLockstate](imsgstore-setlockstate.md) <br/> |Bloqueia ou desbloqueia uma mensagem.  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |Permite que o provedor de repositório de mensagens realize o processamento em uma mensagem enviada.  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |Informa ao repositório de mensagens que uma nova mensagem chegou.  <br/> |
   
|**Propriedades necessárias**|**Nível de acesso**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
As propriedades a seguir são para repositórios de mensagens de mensagens interpessoais (IPM):
  
- **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)

