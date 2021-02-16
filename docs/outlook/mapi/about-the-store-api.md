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
# <a name="about-the-store-api"></a><span data-ttu-id="1db4b-103">Sobre a API de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="1db4b-103">About the Store API</span></span>

  
  
<span data-ttu-id="1db4b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1db4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1db4b-105">A API da Loja fornece diversas funcionalidades de armazenamento para armazenar provedores.</span><span class="sxs-lookup"><span data-stu-id="1db4b-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="1db4b-106">Ele fornece as seguintes definições, tipos de dados, propriedades e interfaces.</span><span class="sxs-lookup"><span data-stu-id="1db4b-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="1db4b-107">Definições:</span><span class="sxs-lookup"><span data-stu-id="1db4b-107">Definitions:</span></span>
  
- [<span data-ttu-id="1db4b-108">Constantes para a API da Loja</span><span class="sxs-lookup"><span data-stu-id="1db4b-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="1db4b-109">Tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="1db4b-109">Data types:</span></span>
  
- <span data-ttu-id="1db4b-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="1db4b-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="1db4b-112">Propriedades nomeadas:</span><span class="sxs-lookup"><span data-stu-id="1db4b-112">Named Properties:</span></span>
  
- <span data-ttu-id="1db4b-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="1db4b-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="1db4b-115">**[Exibir tamanhos de pasta do servidor](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="1db4b-116">**[Ocultar Opção de Atualização de Reunião](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="1db4b-117">**[Tornar Tipo de Loja Particular](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="1db4b-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="1db4b-119">Os provedores da Loja que não exigem nenhuma das funcionalidades oferecidas por essas propriedades nomeadas podem simplesmente ignorá-las e não implementar o suporte na interface **IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="1db4b-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="1db4b-120">Como essas propriedades são fornecidas a partir do Microsoft Outlook 2003 Service Pack 1, adiá-las a um armazenamento em uma versão anterior do Microsoft Outlook não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="1db4b-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="1db4b-121">Eles serão ignorados se não existirem ou se o valor for **falso.**</span><span class="sxs-lookup"><span data-stu-id="1db4b-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="1db4b-122">Propriedades:</span><span class="sxs-lookup"><span data-stu-id="1db4b-122">Properties:</span></span>
  
- <span data-ttu-id="1db4b-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="1db4b-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="1db4b-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="1db4b-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="1db4b-127">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="1db4b-127">Interfaces:</span></span>
  
- <span data-ttu-id="1db4b-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="1db4b-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="1db4b-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="1db4b-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="1db4b-131">Registrando lojas para indexação</span><span class="sxs-lookup"><span data-stu-id="1db4b-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="1db4b-132">O Manipulador de Protocolo MAPI verifica o Registro do Windows em busca de armazenamentos que ele deve indexar para fins de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="1db4b-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="1db4b-133">Os provedores da Loja que querem ser indexados devem ser registrados no Registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="1db4b-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="1db4b-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="1db4b-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="1db4b-135">Indexando lojas</span><span class="sxs-lookup"><span data-stu-id="1db4b-135">Indexing Stores</span></span>

<span data-ttu-id="1db4b-136">Os provedores de armazenamento MAPI podem optar por permitir que o Manipulador de Protocolo MAPI rastrear e indexar mensagens no armazenamento ou enviar notificações ao indexador somente quando houver mensagens a serem indexadas.</span><span class="sxs-lookup"><span data-stu-id="1db4b-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="1db4b-137">Para obter mais informações sobre indexação baseada em notificações, consulte [Sobre Notification-Based Indexação da Loja.](about-notification-based-store-indexing.md)</span><span class="sxs-lookup"><span data-stu-id="1db4b-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

