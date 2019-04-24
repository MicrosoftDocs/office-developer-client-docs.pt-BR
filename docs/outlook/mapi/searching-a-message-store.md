---
title: Pesquisar um repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7240f49a15fdaea4d1f30dae578d25c3f2c1c0f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338798"
---
# <a name="searching-a-message-store"></a>Pesquisar um repositório de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente podem pesquisar em uma ou mais pastas procurando mensagens que correspondam aos critérios de pesquisa. A técnica de pesquisa mais direta envolve a aplicação de uma restrição para definir critérios e colocar os resultados em uma pasta de resultados de pesquisa, criada explicitamente para esta pesquisa ou para uma pesquisa anterior. Nem todos os repositórios de mensagens dão suporte a essa técnica. 

Para determinar se o repositório de mensagens que você está usando oferece suporte usando pastas de resultados de pesquisa, chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps para recuperar a propriedade **\_PR STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Se o sinalizador STORE_SEARCH_OK estiver definido, haverá suporte para pesquisa. Se ele não estiver definido, você precisará de uma abordagem alternativa, como inspecionar manualmente as pastas de destino.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Para pesquisar uma ou mais pastas em um repositório de mensagens
  
1. Se você tiver uma pasta de resultados de pesquisa de uma pesquisa anterior, pule para a etapa 2. Caso contrário, para criar uma pasta de resultados de pesquisa:
    
    1. Recupere o identificador de entrada da pasta raiz de resultados de pesquisa chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps do repositório de mensagens e solicitando o **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).
        
    2. Chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir a pasta representada por PR_FINDER_ENTRYID. 
        
    3. Chame o método [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) da pasta para criar uma pasta de resultados de pesquisa com o sinalizador FOLDER_SEARCH definido. 
    
2. Criar uma restrição para manter seus critérios de pesquisa. 
    
3. Criar uma matriz de identificadores de entrada que representam as pastas a serem pesquisadas. Esta etapa será desnecessária se a pasta de resultados de pesquisa tiver sido usada antes e você quiser pesquisar as mesmas pastas.
    
4. Chame o método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) da pasta de resultados de pesquisa, apontando _lpContainerList_ para a matriz de identificador de entrada e _lpRestriction_ para a restrição. 
    
5. Se você tiver registrado para notificações de pesquisa concluída com o repositório de mensagens, aguarde até que a notificação chegue.
    
6. Visualize os resultados da pesquisa chamando o método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable da pasta de resultados de pesquisa para acessar sua tabela de conteúdo. 
    
7. Chame o método imApitable [:: QueryRows](imapitable-queryrows.md) da tabela de conteúdo para recuperar as mensagens que atendem aos critérios de pesquisa. 
    

