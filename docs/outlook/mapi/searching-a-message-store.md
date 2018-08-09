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
ms.openlocfilehash: 90ed7da43d7f9e5e8b5f3024f1eee99a2d7a2b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770340"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="84e3b-103">Pesquisando um armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="84e3b-103">Searching a message store</span></span>

<span data-ttu-id="84e3b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84e3b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84e3b-105">Aplicativos cliente podem pesquisar por meio de uma ou mais pastas procurando mensagens que correspondam a critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="84e3b-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="84e3b-106">A técnica de pesquisa mais direta envolve a aplicação de uma restrição para definir os critérios e colocar os resultados em uma pasta de resultados de pesquisa, criado explicitamente para esta pesquisa ou para uma pesquisa anterior.</span><span class="sxs-lookup"><span data-stu-id="84e3b-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="84e3b-107">Nem todos os repositórios de mensagem suportam essa técnica.</span><span class="sxs-lookup"><span data-stu-id="84e3b-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="84e3b-108">Para determinar se ou não o armazenamento de mensagens você está usando suporta o uso de pastas de resultados da pesquisa, chamar o método [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar o **PR\_STORE_SUPPORT_MASK** propriedade ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="84e3b-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="84e3b-109">Se o sinalizador STORE_SEARCH_OK estiver definido, a pesquisa é suportada.</span><span class="sxs-lookup"><span data-stu-id="84e3b-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="84e3b-110">Se não estiver definida, você precisará de uma abordagem alternativa como inspecionando manualmente as pastas de destino.</span><span class="sxs-lookup"><span data-stu-id="84e3b-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="84e3b-111">Para pesquisar uma ou mais pastas em um armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="84e3b-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="84e3b-112">Se você tiver uma pasta de resultados de pesquisa a partir de uma pesquisa anterior, pule para a etapa 2.</span><span class="sxs-lookup"><span data-stu-id="84e3b-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="84e3b-113">Caso contrário, para criar uma pasta de resultados de pesquisa:</span><span class="sxs-lookup"><span data-stu-id="84e3b-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="84e3b-114">Recupere o identificador de entrada para a pasta raiz de resultados de pesquisa chamando o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens e solicitando **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="84e3b-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="84e3b-115">Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir a pasta representada por PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="84e3b-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="84e3b-116">Chame o método de [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) da pasta para criar uma pasta de resultados de pesquisa com o sinalizador FOLDER_SEARCH definido.</span><span class="sxs-lookup"><span data-stu-id="84e3b-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="84e3b-117">Construa uma restrição para armazenar seus critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="84e3b-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="84e3b-118">Crie uma matriz de identificadores de entrada que representam as pastas a serem pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="84e3b-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="84e3b-119">Essa etapa será necessária se a pasta de resultados de pesquisa tiver sido usada antes e você quiser as mesmas pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="84e3b-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="84e3b-120">Chame o método de [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) da pasta resultados de pesquisa, apontando _lpContainerList_ para a matriz de identificador de entrada e _lpRestriction_ para a restrição.</span><span class="sxs-lookup"><span data-stu-id="84e3b-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="84e3b-121">Se você registrou para notificações de pesquisa completa com o armazenamento de mensagens, aguarde a notificação chegar.</span><span class="sxs-lookup"><span data-stu-id="84e3b-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="84e3b-122">Exiba os resultados da pesquisa chamando os resultados da pesquisa do método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da pasta para acessar sua tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="84e3b-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="84e3b-123">Chame o conteúdo [IMAPITable:: QueryRows](imapitable-queryrows.md) método tabela para recuperar as mensagens que satisfazem os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="84e3b-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

