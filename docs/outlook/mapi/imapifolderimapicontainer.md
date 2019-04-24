---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329488"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Realiza operações nas mensagens e subpastas em uma pasta.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Exposto por:  <br/> |Objetos Folder  <br/> |
|Implementado por:  <br/> |Provedores de repositórios de mensagens  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFolder  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFOLDER  <br/> |
|Modelo de transação:  <br/> |Não-Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |Cria uma nova mensagem.  <br/> |
|[CopyMessages](imapifolder-copymessages.md) <br/> |Copia ou move uma ou mais mensagens.  <br/> |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |Exclui uma ou mais mensagens.  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Cria uma nova subpasta.  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Copia ou move uma subpasta.  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Exclui uma subpasta.  <br/> |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |Define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma ou mais das mensagens da pasta e gerencia o envio de relatórios de leitura.  <br/> |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |Obtém o status associado a uma mensagem em uma pasta específica.  <br/> |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |Define o status associado a uma mensagem.  <br/> |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |Define a ordem de classificação padrão para a tabela de conteúdo de uma pasta.  <br/> |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |Exclui todas as mensagens e subpastas de uma pasta sem excluir a própria pasta.  <br/> |
   
|**Propriedades necessárias**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

