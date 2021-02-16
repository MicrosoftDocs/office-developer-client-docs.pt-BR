---
title: Validando e inicializando um armazenamento de mensagens
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
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="d374c-103">Validando e inicializando um armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="d374c-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="d374c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d374c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d374c-105">Quando você abre um repositório de mensagens por meio do método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) sem definir o sinalizador MDB_NO_MAIL, o MAPI cria várias pastas e atribui a elas nomes e funções padrão.</span><span class="sxs-lookup"><span data-stu-id="d374c-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="d374c-106">A MAPI é responsável por criar essas pastas para evitar as incompatibilidades que inevitavelmente ocorreriam se clientes ou provedores de armazenamento de mensagens fossem responsáveis pela criação.</span><span class="sxs-lookup"><span data-stu-id="d374c-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="d374c-107">Às vezes, é necessário verificar se as pastas apropriadas foram criadas e se são válidas.</span><span class="sxs-lookup"><span data-stu-id="d374c-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="d374c-108">A [função HrValidateIPMSubtree](hrvalidateipmsubtree.md) está disponível para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="d374c-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="d374c-109">Se você estiver validando o armazenamento de mensagens padrão, passe o sinalizador MAPI_FULL_IPM_TREE mensagem.</span><span class="sxs-lookup"><span data-stu-id="d374c-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="d374c-110">Um grupo mais extenso de pastas é criado para o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="d374c-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="d374c-111">Quando **HrValidateIPMSubtree** recebe o sinalizador MAPI_FULL_IPM_TREE, ele verifica as seguintes pastas:</span><span class="sxs-lookup"><span data-stu-id="d374c-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="d374c-112">Pasta raiz da subárvore do IPM</span><span class="sxs-lookup"><span data-stu-id="d374c-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="d374c-113">Pasta Itens Excluídos na pasta raiz do IPM</span><span class="sxs-lookup"><span data-stu-id="d374c-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d374c-114">Pasta caixa de entrada na pasta raiz do IPM</span><span class="sxs-lookup"><span data-stu-id="d374c-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d374c-115">Pasta caixa de saída na pasta raiz do IPM</span><span class="sxs-lookup"><span data-stu-id="d374c-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d374c-116">Pasta Itens Enviados na pasta raiz do IPM</span><span class="sxs-lookup"><span data-stu-id="d374c-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d374c-117">Exibições de pasta na pasta raiz do armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="d374c-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="d374c-118">Exibições comuns na pasta raiz do armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="d374c-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="d374c-119">Pasta de pesquisa na pasta raiz do armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="d374c-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="d374c-120">Se o armazenamento de mensagens não for o padrão, você poderá definir ou não o sinalizador MAPI_FULL_IPM_TREE mensagem.</span><span class="sxs-lookup"><span data-stu-id="d374c-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="d374c-121">Quando esse sinalizador não está definido, **HrValidateIPMSubtree** verifica somente a pasta raiz da subárvore, a pasta Itens Excluídos e a pasta raiz dos resultados de pesquisa do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d374c-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="d374c-122">Para inicializar um armazenamento de mensagens, armazene as seguintes propriedades na memória para que elas sejam prontamente disponíveis:</span><span class="sxs-lookup"><span data-stu-id="d374c-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="d374c-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d374c-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="d374c-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d374c-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="d374c-125">Essas propriedades são bitmasks que descrevem os recursos do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d374c-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="d374c-126">**PR_VALID_FOLDER_MASK** tem um bit definido para cada pasta especial que existe no armazenamento de mensagens e tem um identificador de entrada atribuído que é válido.</span><span class="sxs-lookup"><span data-stu-id="d374c-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="d374c-127">Para obter mais informações sobre como acessar essas pastas e seus identificadores de entrada, consulte [Abrindo uma pasta do armazenamento de mensagens.](opening-a-message-store-folder.md)</span><span class="sxs-lookup"><span data-stu-id="d374c-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="d374c-128">**PR_STORE_SUPPORT_MASK** tem um bit definido para cada recurso com suporte no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d374c-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="d374c-129">Por exemplo, se um armazenamento de mensagens  suportar a notificação e o texto formatado, sua PR_STORE_SUPPORT_MASK terá os bits STORE_NOTIFY_OK e STORE_RTF_OK bits definidos.</span><span class="sxs-lookup"><span data-stu-id="d374c-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="d374c-130">Outras propriedades que devem ser armazenadas localmente incluem os identificadores de entrada para as pastas que a PR_VALID_FOLDER_MASK **propriedade** descreve como válida.</span><span class="sxs-lookup"><span data-stu-id="d374c-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="d374c-131">Cada uma dessas pastas especiais, exceto a pasta Caixa de Entrada, tem uma propriedade de identificador de entrada associada a ela.</span><span class="sxs-lookup"><span data-stu-id="d374c-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="d374c-132">Por exemplo, o identificador de entrada para a pasta Caixa de Saída é sua **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="d374c-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="d374c-133">Como essas pastas são as que serão abertas com frequência, é uma boa ideia ter seus identificadores de entrada prontamente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d374c-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

