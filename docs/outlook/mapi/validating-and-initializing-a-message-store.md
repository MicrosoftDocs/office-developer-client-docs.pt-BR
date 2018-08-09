---
title: Validar e inicializar um repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 48883ec33db9ffd6b3e7cc6e16ae9c2487a31607
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770716"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="d4121-103">Validar e inicializar um repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="d4121-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="d4121-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4121-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4121-105">Quando você abre um armazenamento de mensagens por meio do método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) sem definir o sinalizador MDB_NO_MAIL, MAPI cria várias pastas e os atribui funções e os nomes padrão.</span><span class="sxs-lookup"><span data-stu-id="d4121-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="d4121-106">MAPI é responsável por criar essas pastas para evitar incompatibilidades que ocorreriam inevitavelmente fossem clientes ou provedores de armazenamento de mensagem responsáveis pela criação.</span><span class="sxs-lookup"><span data-stu-id="d4121-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="d4121-107">Em alguns casos, é necessário verificar se as pastas apropriadas foram criadas e que são válidos.</span><span class="sxs-lookup"><span data-stu-id="d4121-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="d4121-108">A função [HrValidateIPMSubtree](hrvalidateipmsubtree.md) está disponível para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="d4121-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="d4121-109">Se você estiver validando o armazenamento de mensagens padrão, passe o sinalizador MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="d4121-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="d4121-110">Um grupo mais abrangente de pastas é criado para o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="d4121-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="d4121-111">Quando **HrValidateIPMSubtree** recebe o sinalizador MAPI_FULL_IPM_TREE, ele verifica as seguintes pastas:</span><span class="sxs-lookup"><span data-stu-id="d4121-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="d4121-112">Pasta raiz para a subárvore IPM</span><span class="sxs-lookup"><span data-stu-id="d4121-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="d4121-113">Pasta de itens excluídos na pasta raiz IPM</span><span class="sxs-lookup"><span data-stu-id="d4121-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d4121-114">Pasta de caixa de entrada na pasta raiz IPM</span><span class="sxs-lookup"><span data-stu-id="d4121-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d4121-115">Pasta na pasta raiz IPM caixa de saída</span><span class="sxs-lookup"><span data-stu-id="d4121-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d4121-116">Pasta Itens enviados na pasta raiz IPM</span><span class="sxs-lookup"><span data-stu-id="d4121-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d4121-117">Modos de exibição de pasta na pasta raiz do repositório de mensagem</span><span class="sxs-lookup"><span data-stu-id="d4121-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="d4121-118">Modos de exibição comuns na pasta raiz do repositório de mensagem</span><span class="sxs-lookup"><span data-stu-id="d4121-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="d4121-119">Pasta de pesquisa na pasta raiz do repositório de mensagem</span><span class="sxs-lookup"><span data-stu-id="d4121-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="d4121-120">Se o armazenamento de mensagens não é o padrão, você pode definir ou não definir o sinalizador MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="d4121-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="d4121-121">Quando esse sinalizador não estiver definida, **HrValidateIPMSubtree** procura somente a pasta raiz para a subárvore, a pasta Itens excluídos e a pasta raiz de mensagem armazenam os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d4121-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="d4121-122">Para inicializar um armazenamento de mensagens, armazene as seguintes propriedades na memória, para que sejam prontamente disponíveis:</span><span class="sxs-lookup"><span data-stu-id="d4121-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="d4121-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d4121-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="d4121-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d4121-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="d4121-125">Essas propriedades são máscaras de bits que descrevem os recursos de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d4121-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="d4121-126">**PR_VALID_FOLDER_MASK** tem um bit definido para cada pasta especial que existe no armazenamento de mensagens e tem um identificador de entrada atribuídas que é válido.</span><span class="sxs-lookup"><span data-stu-id="d4121-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="d4121-127">Para obter mais informações sobre o acesso a essas pastas e seus identificadores de entrada, consulte [abrindo uma pasta de repositório de mensagem](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="d4121-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="d4121-128">**PR_STORE_SUPPORT_MASK** tem um bit definido para cada recurso compatíveis com o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d4121-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="d4121-129">Por exemplo, se um armazenamento de mensagens oferece suporte a notificação e texto formatado, seu **PR_STORE_SUPPORT_MASK** terá o conjunto de bits STORE_NOTIFY_OK e STORE_RTF_OK.</span><span class="sxs-lookup"><span data-stu-id="d4121-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="d4121-130">Outras propriedades que devem ser armazenadas localmente incluem os identificadores de entrada para as pastas que a propriedade **PR_VALID_FOLDER_MASK** descreve como válido.</span><span class="sxs-lookup"><span data-stu-id="d4121-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="d4121-131">Cada uma dessas pastas especiais, exceto para a pasta de caixa de entrada, tem uma propriedade de identificador de entrada associada a ela.</span><span class="sxs-lookup"><span data-stu-id="d4121-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="d4121-132">Por exemplo, o identificador de entrada para a pasta caixa de saída é sua propriedade **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d4121-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="d4121-133">Como essas pastas são as pastas que serão abertas com frequência, é uma boa ideia ter seus identificadores de entrada prontamente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d4121-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

