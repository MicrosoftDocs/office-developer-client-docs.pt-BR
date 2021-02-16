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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426034"
---
# <a name="searching-a-message-store"></a>Pesquisar um repositório de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente podem pesquisar por uma ou mais pastas em busca de mensagens que corresponderem aos critérios de pesquisa. A técnica de pesquisa mais simples envolve a aplicação de uma restrição para definir critérios e colocar os resultados em uma pasta de resultados de pesquisa, criada explicitamente para essa pesquisa ou para uma pesquisa anterior. Nem todos os armazenamentos de mensagens suportam essa técnica. 

Para determinar se o repositório de mensagens que você está usando suporta usando pastas de resultados de pesquisa, chame seu método [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar a propriedade **PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Se o STORE_SEARCH_OK sinalizador estiver definido, a pesquisa será suportada. Se não estiver definido, você precisará de uma abordagem alternativa, como inspecionar manualmente as pastas de destino.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Para pesquisar uma ou mais pastas em um armazenamento de mensagens
  
1. Se você tiver uma pasta de resultados de pesquisa de uma pesquisa anterior, pule para a etapa 2. Caso contrário, para criar uma pasta de resultados de pesquisa:
    
    1. Recupere o identificador de entrada para **a** pasta raiz de resultados de pesquisa chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens e solicitando PR_FINDER_ENTRYID ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).
        
    2. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir a pasta representada por PR_FINDER_ENTRYID. 
        
    3. Chame o método [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) da pasta para criar uma pasta de resultados de pesquisa com o FOLDER_SEARCH sinalizador definido. 
    
2. Crie uma restrição para manter seus critérios de pesquisa. 
    
3. Crie uma matriz de identificadores de entrada que representem as pastas a pesquisar. Esta etapa será desnecessária se a pasta de resultados de pesquisa tiver sido usada antes e você quiser pesquisar as mesmas pastas.
    
4. Chame o método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) da pasta de resultados de pesquisa, apontando  _lpContainerList_ para a matriz de identificador de entrada e  _lpRestriction_ para a restrição. 
    
5. Se você se registrou para notificações de pesquisa completas com o armazenamento de mensagens, aguarde a notificação chegar.
    
6. Veja os resultados da pesquisa chamando o método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da pasta de resultados de pesquisa para acessar sua tabela de conteúdo. 
    
7. Chame o método [IMAPITable::QueryRows](imapitable-queryrows.md) da tabela de conteúdo para recuperar as mensagens que satisfazem os critérios de pesquisa. 
    

