---
title: Sobre a API de armazenamento
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
# <a name="about-the-store-api"></a><span data-ttu-id="a472f-103">Sobre a API de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a472f-103">About the Store API</span></span>

  
  
<span data-ttu-id="a472f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a472f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a472f-105">A API de armazenar fornece uma funcionalidade de diversos repositório para provedores de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a472f-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="a472f-106">Ele fornece as seguintes definições, tipos de dados, propriedades e interfaces.</span><span class="sxs-lookup"><span data-stu-id="a472f-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="a472f-107">Definições:</span><span class="sxs-lookup"><span data-stu-id="a472f-107">Definitions:</span></span>
  
- [<span data-ttu-id="a472f-108">Constantes para o repositório de API</span><span class="sxs-lookup"><span data-stu-id="a472f-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="a472f-109">Tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="a472f-109">Data types:</span></span>
  
- <span data-ttu-id="a472f-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="a472f-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="a472f-112">Propriedades nomeadas:</span><span class="sxs-lookup"><span data-stu-id="a472f-112">Named Properties:</span></span>
  
- <span data-ttu-id="a472f-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="a472f-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="a472f-115">**[Exibir tamanhos de pastas do servidor](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="a472f-116">**[Ocultar a opção de atualização de reunião](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="a472f-117">**[Tornar repositório tipo particular](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="a472f-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="a472f-119">Provedores de armazenamento que não exigem qualquer uma das funcionalidades oferecidas dessas propriedades nomeadas podem simplesmente ignorá-las e não implementar suporte na interface do **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="a472f-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="a472f-120">Porque essas propriedades são fornecidas iniciando no Microsoft Outlook 2003 Service Pack 1, adicioná-los para um repositório em uma versão anterior do Microsoft Outlook não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="a472f-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="a472f-121">Eles são ignorados se não existirem, ou se seu valor for **false**.</span><span class="sxs-lookup"><span data-stu-id="a472f-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="a472f-122">Propriedades:</span><span class="sxs-lookup"><span data-stu-id="a472f-122">Properties:</span></span>
  
- <span data-ttu-id="a472f-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="a472f-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="a472f-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="a472f-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="a472f-127">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="a472f-127">Interfaces:</span></span>
  
- <span data-ttu-id="a472f-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="a472f-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="a472f-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="a472f-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="a472f-131">Registrando repositórios para indexação</span><span class="sxs-lookup"><span data-stu-id="a472f-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="a472f-132">O manipulador de protocolo MAPI verifica o registro do Windows para repositórios que ele deve indexar para fins de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a472f-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="a472f-133">Provedores de armazenamento que devem ser indexados devem ser registrados no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="a472f-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="a472f-134">Para obter mais informações sobre como registrar provedores de armazenamento para indexação no Outlook 2013 ou o Outlook 2010, consulte [Sobre registrando repositórios para indexação](about-registering-stores-for-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="a472f-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="a472f-135">Repositórios de indexação</span><span class="sxs-lookup"><span data-stu-id="a472f-135">Indexing Stores</span></span>

<span data-ttu-id="a472f-136">Provedores de repositório MAPI podem optar por permitir que o manipulador de protocolo para rastrear e indexar mensagens no repositório de MAPI ou enviar notificações para o indexador apenas quando há mensagens a serem indexados.</span><span class="sxs-lookup"><span data-stu-id="a472f-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="a472f-137">Para obter mais informações sobre a indexação baseada em notificações, consulte [About Notification-Based a indexação de repositório](about-notification-based-store-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="a472f-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

