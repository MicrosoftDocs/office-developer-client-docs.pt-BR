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
# <a name="searching-a-message-store"></a><span data-ttu-id="d393d-103">Pesquisar um repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="d393d-103">Searching a message store</span></span>

<span data-ttu-id="d393d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d393d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d393d-105">Os aplicativos cliente podem pesquisar em uma ou mais pastas procurando mensagens que correspondam aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d393d-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="d393d-106">A técnica de pesquisa mais direta envolve a aplicação de uma restrição para definir critérios e colocar os resultados em uma pasta de resultados de pesquisa, criada explicitamente para esta pesquisa ou para uma pesquisa anterior.</span><span class="sxs-lookup"><span data-stu-id="d393d-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="d393d-107">Nem todos os repositórios de mensagens dão suporte a essa técnica.</span><span class="sxs-lookup"><span data-stu-id="d393d-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="d393d-108">Para determinar se o repositório de mensagens que você está usando oferece suporte usando pastas de resultados de pesquisa, chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps para recuperar a propriedade **\_PR STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d393d-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="d393d-109">Se o sinalizador STORE_SEARCH_OK estiver definido, haverá suporte para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d393d-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="d393d-110">Se ele não estiver definido, você precisará de uma abordagem alternativa, como inspecionar manualmente as pastas de destino.</span><span class="sxs-lookup"><span data-stu-id="d393d-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="d393d-111">Para pesquisar uma ou mais pastas em um repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="d393d-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="d393d-112">Se você tiver uma pasta de resultados de pesquisa de uma pesquisa anterior, pule para a etapa 2.</span><span class="sxs-lookup"><span data-stu-id="d393d-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="d393d-113">Caso contrário, para criar uma pasta de resultados de pesquisa:</span><span class="sxs-lookup"><span data-stu-id="d393d-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="d393d-114">Recupere o identificador de entrada da pasta raiz de resultados de pesquisa chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps do repositório de mensagens e solicitando o **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d393d-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="d393d-115">Chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir a pasta representada por PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="d393d-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="d393d-116">Chame o método [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) da pasta para criar uma pasta de resultados de pesquisa com o sinalizador FOLDER_SEARCH definido.</span><span class="sxs-lookup"><span data-stu-id="d393d-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="d393d-117">Criar uma restrição para manter seus critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d393d-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="d393d-118">Criar uma matriz de identificadores de entrada que representam as pastas a serem pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="d393d-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="d393d-119">Esta etapa será desnecessária se a pasta de resultados de pesquisa tiver sido usada antes e você quiser pesquisar as mesmas pastas.</span><span class="sxs-lookup"><span data-stu-id="d393d-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="d393d-120">Chame o método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) da pasta de resultados de pesquisa, apontando _lpContainerList_ para a matriz de identificador de entrada e _lpRestriction_ para a restrição.</span><span class="sxs-lookup"><span data-stu-id="d393d-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="d393d-121">Se você tiver registrado para notificações de pesquisa concluída com o repositório de mensagens, aguarde até que a notificação chegue.</span><span class="sxs-lookup"><span data-stu-id="d393d-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="d393d-122">Visualize os resultados da pesquisa chamando o método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable da pasta de resultados de pesquisa para acessar sua tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d393d-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="d393d-123">Chame o método imApitable [:: QueryRows](imapitable-queryrows.md) da tabela de conteúdo para recuperar as mensagens que atendem aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d393d-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

