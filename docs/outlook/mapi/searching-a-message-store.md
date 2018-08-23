---
title: Pesquisando um armazenamento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 74b63719f6d72e3c92cbcef6fdb26ee106d4b9aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571833"
---
# <a name="searching-a-message-store"></a>Pesquisando um armazenamento de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aplicativos cliente podem pesquisar por meio de uma ou mais pastas procurando mensagens que correspondam a critérios de pesquisa. A técnica de pesquisa mais direta envolve a aplicação de uma restrição para definir os critérios e colocar os resultados em uma pasta de resultados de pesquisa, criado explicitamente para esta pesquisa ou para uma pesquisa anterior. Nem todos os repositórios de mensagem suportam essa técnica. 

Para determinar se ou não o armazenamento de mensagens você está usando suporta o uso de pastas de resultados da pesquisa, chamar o método [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar o **PR\_STORE_SUPPORT_MASK** propriedade ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Se o sinalizador STORE_SEARCH_OK estiver definido, a pesquisa é suportada. Se não estiver definida, você precisará de uma abordagem alternativa como inspecionando manualmente as pastas de destino.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Para pesquisar uma ou mais pastas em um armazenamento de mensagens
  
1. Se você tiver uma pasta de resultados de pesquisa a partir de uma pesquisa anterior, pule para a etapa 2. Caso contrário, para criar uma pasta de resultados de pesquisa:
    
    1. Recupere o identificador de entrada para a pasta raiz de resultados de pesquisa chamando o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens e solicitando **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).
        
    2. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir a pasta representada por PR_FINDER_ENTRYID. 
        
    3. Chame o método de [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) da pasta para criar uma pasta de resultados de pesquisa com o sinalizador FOLDER_SEARCH definido. 
    
2. Construa uma restrição para armazenar seus critérios de pesquisa. 
    
3. Crie uma matriz de identificadores de entrada que representam as pastas a serem pesquisadas. Essa etapa será necessária se a pasta de resultados de pesquisa tiver sido usada antes e você quiser as mesmas pastas de pesquisa.
    
4. Chame o método de [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) da pasta resultados de pesquisa, apontando _lpContainerList_ para a matriz de identificador de entrada e _lpRestriction_ para a restrição. 
    
5. Se você registrou para notificações de pesquisa completa com o armazenamento de mensagens, aguarde a notificação chegar.
    
6. Exiba os resultados da pesquisa chamando os resultados da pesquisa do método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da pasta para acessar sua tabela de conteúdo. 
    
7. Chame o conteúdo [IMAPITable:: QueryRows](imapitable-queryrows.md) método tabela para recuperar as mensagens que satisfazem os critérios de pesquisa. 
    

