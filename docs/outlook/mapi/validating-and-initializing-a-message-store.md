---
title: Validando e inicializando um repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433686"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="ff187-103">Validando e inicializando um repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="ff187-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="ff187-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff187-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff187-105">Quando você abre um repositório de mensagens por meio do método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) sem definir o sinalizador MDB_NO_MAIL, o MAPI cria várias pastas e atribui nomes e funções padrão.</span><span class="sxs-lookup"><span data-stu-id="ff187-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="ff187-106">O MAPI é responsável por criar essas pastas para evitar incompatibilidades que, inevitavelmente, ocorreria se os clientes ou provedores de repositórios de mensagens fossem responsáveis pela criação.</span><span class="sxs-lookup"><span data-stu-id="ff187-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="ff187-107">Às vezes, é necessário verificar se as pastas apropriadas foram criadas e se elas são válidas.</span><span class="sxs-lookup"><span data-stu-id="ff187-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="ff187-108">A função [HrValidateIPMSubtree](hrvalidateipmsubtree.md) está disponível para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="ff187-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="ff187-109">Se você estiver validando o repositório de mensagens padrão, passe o sinalizador MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="ff187-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="ff187-110">Um grupo de pastas mais abrangente é criado para o repositório de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="ff187-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="ff187-111">Quando o **HrValidateIPMSubtree** recebe o sinalizador MAPI_FULL_IPM_TREE, ele verifica as seguintes pastas:</span><span class="sxs-lookup"><span data-stu-id="ff187-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="ff187-112">Pasta raiz da sub-árvore IPM</span><span class="sxs-lookup"><span data-stu-id="ff187-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="ff187-113">Pasta itens excluídos na pasta raiz IPM</span><span class="sxs-lookup"><span data-stu-id="ff187-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="ff187-114">Pasta caixa de entrada na pasta raiz IPM</span><span class="sxs-lookup"><span data-stu-id="ff187-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="ff187-115">Pasta de saída na pasta raiz IPM</span><span class="sxs-lookup"><span data-stu-id="ff187-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="ff187-116">Pasta Itens enviados na pasta raiz IPM</span><span class="sxs-lookup"><span data-stu-id="ff187-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="ff187-117">Modos de exibição de pasta na pasta raiz do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="ff187-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="ff187-118">Modos de exibição comuns na pasta raiz do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="ff187-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="ff187-119">Pasta de pesquisa na pasta raiz do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="ff187-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="ff187-120">Se o repositório de mensagens não for o padrão, você poderá definir ou não o sinalizador MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="ff187-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="ff187-121">Quando esse sinalizador não é definido, o **HrValidateIPMSubtree** verifica apenas a pasta raiz da subárvore, a pasta itens excluídos e a pasta raiz dos resultados da pesquisa do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ff187-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="ff187-122">Para inicializar um repositório de mensagens, armazene as seguintes propriedades na memória para que estejam prontamente disponíveis:</span><span class="sxs-lookup"><span data-stu-id="ff187-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="ff187-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ff187-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="ff187-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ff187-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="ff187-125">Essas propriedades são bitmasks que descrevem os recursos do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ff187-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="ff187-126">O **PR_VALID_FOLDER_MASK** tem um conjunto de bits para cada pasta especial que existe no repositório de mensagens e tem um identificador de entrada atribuído válido.</span><span class="sxs-lookup"><span data-stu-id="ff187-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="ff187-127">Para obter mais informações sobre como acessar essas pastas e seus identificadores de entrada, consulte [abrir uma pasta de armazenamento de mensagens](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="ff187-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="ff187-128">O **PR_STORE_SUPPORT_MASK** tem um conjunto de bits para cada recurso suportado no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ff187-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="ff187-129">Por exemplo, se um repositório de mensagens suportar a notificação e o texto formatado, seus **PR_STORE_SUPPORT_MASK** terão os bits STORE_NOTIFY_OK e STORE_RTF_OK definidos.</span><span class="sxs-lookup"><span data-stu-id="ff187-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="ff187-130">Outras propriedades que devem ser armazenadas localmente incluem os identificadores de entrada para as pastas que a propriedade **PR_VALID_FOLDER_MASK** descreve como válida.</span><span class="sxs-lookup"><span data-stu-id="ff187-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="ff187-131">Cada uma dessas pastas especiais, exceto a pasta caixa de entrada, tem uma propriedade de identificador de entrada associada a ela.</span><span class="sxs-lookup"><span data-stu-id="ff187-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="ff187-132">Por exemplo, o identificador de entrada da pasta de saída é sua propriedade **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ff187-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="ff187-133">Como essas pastas são as pastas que serão abertas com frequência, é uma boa ideia ter seus identificadores de entrada prontamente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ff187-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

