---
title: Sobre o API de armazenamento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 31aff61ec5868b0f1e9ab34d498b2e8175519f0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766123"
---
# <a name="about-the-store-api"></a>Sobre o API de armazenamento

  
  
**Aplica-se a**: Outlook 
  
A API de armazenar fornece uma funcionalidade de diversos repositório para provedores de armazenamento. Ele fornece as seguintes definições, tipos de dados, propriedades e interfaces.
  
Definições:
  
- [Constantes para o repositório de API](mapi-constants.md)
    
Tipos de dados:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Propriedades nomeadas:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Exibir tamanhos de pastas do servidor](display-server-folder-sizes-property.md)**
    
- **[Ocultar a opção de atualização de reunião](hide-meeting-update-option-property.md)**
    
- **[Tornar repositório tipo particular](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Provedores de armazenamento que não exigem qualquer uma das funcionalidades oferecidas dessas propriedades nomeadas podem simplesmente ignorá-las e não implementar suporte na interface do **IMAPIProp** . Porque essas propriedades são fornecidas iniciando no Microsoft Outlook 2003 Service Pack 1, adicioná-los para um repositório em uma versão anterior do Microsoft Outlook não tem efeito. Eles são ignorados se não existirem, ou se seu valor for **false**. 
  
Propriedades:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Interfaces:
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Registrando repositórios para indexação

O manipulador de protocolo MAPI verifica o registro do Windows para repositórios que ele deve indexar para fins de pesquisa. Provedores de armazenamento que devem ser indexados devem ser registrados no registro do Windows. Para obter mais informações sobre como registrar provedores de armazenamento para indexação no Outlook 2013 ou o Outlook 2010, consulte [Sobre registrando repositórios para indexação](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Repositórios de indexação

Provedores de repositório MAPI podem optar por permitir que o manipulador de protocolo para rastrear e indexar mensagens no repositório de MAPI ou enviar notificações para o indexador apenas quando há mensagens a serem indexados. Para obter mais informações sobre a indexação baseada em notificações, consulte [About Notification-Based a indexação de repositório](about-notification-based-store-indexing.md).
  

