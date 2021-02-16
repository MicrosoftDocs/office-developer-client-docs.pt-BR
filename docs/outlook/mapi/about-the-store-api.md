---
title: Sobre a API de Armazenamento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405552"
---
# <a name="about-the-store-api"></a>Sobre a API de Armazenamento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A API da Loja fornece diversas funcionalidades de armazenamento para armazenar provedores. Ele fornece as seguintes definições, tipos de dados, propriedades e interfaces.
  
Definições:
  
- [Constantes para a API da Loja](mapi-constants.md)
    
Tipos de dados:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Propriedades nomeadas:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Exibir tamanhos de pasta do servidor](display-server-folder-sizes-property.md)**
    
- **[Ocultar Opção de Atualização de Reunião](hide-meeting-update-option-property.md)**
    
- **[Tornar Tipo de Loja Particular](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Os provedores da Loja que não exigem nenhuma das funcionalidades oferecidas por essas propriedades nomeadas podem simplesmente ignorá-las e não implementar o suporte na interface **IMAPIProp.** Como essas propriedades são fornecidas a partir do Microsoft Outlook 2003 Service Pack 1, adiá-las a um armazenamento em uma versão anterior do Microsoft Outlook não tem efeito. Eles serão ignorados se não existirem ou se o valor for **falso.** 
  
Propriedades:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Interfaces:
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Registrando lojas para indexação

O Manipulador de Protocolo MAPI verifica o Registro do Windows em busca de armazenamentos que ele deve indexar para fins de pesquisa. Os provedores da Loja que querem ser indexados devem ser registrados no Registro do Windows. For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Indexando lojas

Os provedores de armazenamento MAPI podem optar por permitir que o Manipulador de Protocolo MAPI rastrear e indexar mensagens no armazenamento ou enviar notificações ao indexador somente quando houver mensagens a serem indexadas. Para obter mais informações sobre indexação baseada em notificações, consulte [Sobre Notification-Based Indexação da Loja.](about-notification-based-store-indexing.md)
  

