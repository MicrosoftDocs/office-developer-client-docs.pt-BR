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
# <a name="about-the-store-api"></a><span data-ttu-id="45dfc-103">Sobre a API de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="45dfc-103">About the Store API</span></span>

  
  
<span data-ttu-id="45dfc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45dfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45dfc-105">A API do repositório fornece funcionalidade de repositório diversos para armazenar provedores.</span><span class="sxs-lookup"><span data-stu-id="45dfc-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="45dfc-106">Ele fornece os seguintes defintions, tipos de dados, propriedades e interfaces.</span><span class="sxs-lookup"><span data-stu-id="45dfc-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="45dfc-107">Definições:</span><span class="sxs-lookup"><span data-stu-id="45dfc-107">Definitions:</span></span>
  
- [<span data-ttu-id="45dfc-108">Constantes para a API de repositório</span><span class="sxs-lookup"><span data-stu-id="45dfc-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="45dfc-109">Tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="45dfc-109">Data types:</span></span>
  
- <span data-ttu-id="45dfc-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="45dfc-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="45dfc-112">Propriedades nomeadas:</span><span class="sxs-lookup"><span data-stu-id="45dfc-112">Named Properties:</span></span>
  
- <span data-ttu-id="45dfc-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="45dfc-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="45dfc-115">**[Exibir tamanhos de pasta do servidor](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="45dfc-116">**[Ocultar opção de atualização de reunião](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="45dfc-117">**[Tornar o tipo de repositório privado](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="45dfc-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="45dfc-119">Os provedores de repositórios que não exigem nenhuma das funcionalidades oferecidas por essas propriedades nomeadas podem simplesmente ignorá-los e não implementar o suporte na interface **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="45dfc-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="45dfc-120">Como essas propriedades são fornecidas a partir do Microsoft Outlook 2003 Service Pack 1, adicioná-las a um repositório em uma versão anterior do Microsoft Outlook não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="45dfc-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="45dfc-121">Eles serão ignorados se não existirem ou se o valor for **false**.</span><span class="sxs-lookup"><span data-stu-id="45dfc-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="45dfc-122">Propriedades:</span><span class="sxs-lookup"><span data-stu-id="45dfc-122">Properties:</span></span>
  
- <span data-ttu-id="45dfc-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="45dfc-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="45dfc-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="45dfc-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="45dfc-127">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="45dfc-127">Interfaces:</span></span>
  
- <span data-ttu-id="45dfc-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="45dfc-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="45dfc-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="45dfc-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="45dfc-131">Registrar repositórios para indexação</span><span class="sxs-lookup"><span data-stu-id="45dfc-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="45dfc-132">O manipulador de protocolo MAPI verifica o registro do Windows em busca de armazenamentos que ele deve indexar para fins de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="45dfc-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="45dfc-133">Os provedores de repositórios que desejam ser indexados devem ser registrados no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="45dfc-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="45dfc-134">Para obter mais informações sobre como registrar provedores de repositório para indexação no Outlook 2013 ou no Outlook 2010, consulte [sobre o registro de repositórios para indexação](about-registering-stores-for-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="45dfc-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="45dfc-135">Indexação de repositórios</span><span class="sxs-lookup"><span data-stu-id="45dfc-135">Indexing Stores</span></span>

<span data-ttu-id="45dfc-136">Os provedores de repositório MAPI podem optar por permitir que o manipulador de protocolo MAPI rastreie e indexe mensagens no repositório ou envie notificações ao indexador somente quando houver mensagens a serem indexadas.</span><span class="sxs-lookup"><span data-stu-id="45dfc-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="45dfc-137">Para obter mais informações sobre indexação baseada em notificações, consulte [about Notification-based Store Indexing](about-notification-based-store-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="45dfc-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

