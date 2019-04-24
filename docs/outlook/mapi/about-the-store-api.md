---
title: Sobre a API de Armazenamento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321746"
---
# <a name="about-the-store-api"></a>Sobre a API de Armazenamento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A API do repositório fornece funcionalidade de repositório diversos para armazenar provedores. Ele fornece os seguintes defintions, tipos de dados, propriedades e interfaces.
  
Definições:
  
- [Constantes para a API de repositório](mapi-constants.md)
    
Tipos de dados:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Propriedades nomeadas:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Exibir tamanhos de pasta do servidor](display-server-folder-sizes-property.md)**
    
- **[Ocultar opção de atualização de reunião](hide-meeting-update-option-property.md)**
    
- **[Tornar o tipo de repositório privado](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Os provedores de repositórios que não exigem nenhuma das funcionalidades oferecidas por essas propriedades nomeadas podem simplesmente ignorá-los e não implementar o suporte na interface **IMAPIProp** . Como essas propriedades são fornecidas a partir do Microsoft Outlook 2003 Service Pack 1, adicioná-las a um repositório em uma versão anterior do Microsoft Outlook não tem efeito. Eles serão ignorados se não existirem ou se o valor for **false**. 
  
Propriedades:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Interfaces:
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Registrar repositórios para indexação

O manipulador de protocolo MAPI verifica o registro do Windows em busca de armazenamentos que ele deve indexar para fins de pesquisa. Os provedores de repositórios que desejam ser indexados devem ser registrados no registro do Windows. Para obter mais informações sobre como registrar provedores de repositório para indexação no Outlook 2013 ou no Outlook 2010, consulte [sobre o registro de repositórios para indexação](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Indexação de repositórios

Os provedores de repositório MAPI podem optar por permitir que o manipulador de protocolo MAPI rastreie e indexe mensagens no repositório ou envie notificações ao indexador somente quando houver mensagens a serem indexadas. Para obter mais informações sobre indexação baseada em notificações, consulte [about Notification-based Store Indexing](about-notification-based-store-indexing.md).
  

