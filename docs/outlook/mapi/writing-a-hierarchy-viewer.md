---
title: Escrevendo um Visualizador de Hierarquias
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421127"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="2c2a3-103">Escrevendo um Visualizador de Hierarquias</span><span class="sxs-lookup"><span data-stu-id="2c2a3-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="2c2a3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c2a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c2a3-105">Um visualizador de hierarquias é um componente de interface do usuário usado para exibir tabelas de hierarquia de contêineres de pasta e de livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="2c2a3-106">Os visualizadores de hierarquia podem exibir membros da hierarquia em níveis diferentes, expandindo e contratando cada nível sob demanda.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="2c2a3-107">A propriedade de contêiner, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controla o nível no qual um membro da hierarquia é exibido.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="2c2a3-108">As entradas que representam contêineres ou pastas de lista de endereços de nível superior têm sua **PR_DEPTH** definida como zero.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="2c2a3-109">O valor dessa propriedade é incrementado sequencialmente para entradas em níveis sequenciais.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="2c2a3-110">Ou seja, quando um usuário seleciona um contêiner de nível superior para expandir, exibe todos os contêineres com PR_DEPTH **definido** como 1.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="2c2a3-111">Quando um usuário expande um desses subcontainers,  exibe os contêineres com PR_DEPTH definido como 2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="2c2a3-112">Visualizadores de hierarquia suportam uma variedade diferente de profundidades.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="2c2a3-113">Você pode limitar o visualizador a apenas um ou dois níveis ou pode dar suporte a vários níveis, se a exibição de uma hierarquia expansiva for uma prioridade.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="2c2a3-114">O livro de endereços fornece um visualizador de hierarquias para os contêineres de nível superior no livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="2c2a3-115">**Para acessar a tabela de hierarquia do livro de endereços**</span><span class="sxs-lookup"><span data-stu-id="2c2a3-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="2c2a3-116">Chame [IAddrBook::OpenEntry](iaddrbook-openentry.md), passando um identificador de entrada nulo, para abrir o contêiner raiz do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="2c2a3-117">Chame o método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) do contêiner raiz para acessar a tabela de hierarquia do livro de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="2c2a3-118">**Para acessar a tabela de hierarquia do armazenamento de mensagens padrão**</span><span class="sxs-lookup"><span data-stu-id="2c2a3-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="2c2a3-119">Chame [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para acessar a tabela do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="2c2a3-120">Crie uma **restrição** usando a estrutura [SPropertyRestriction](spropertyrestriction.md) para limitar a tabela apenas às linhas que tenham uma propriedade PR_DEFAULT_STORE ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) definida como TRUE.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="2c2a3-121">Chame [IMAPITable::FindRow](imapitable-findrow.md), passando o **SPropertyRestriction** para localizar a linha que representa o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="2c2a3-122">Chame [IMAPISession::OpenEntry](imapisession-openentry.md), passando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do armazenamento de mensagens padrão na tabela do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="2c2a3-123">Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="2c2a3-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="2c2a3-124">Chame o método [IMsgStore::OpenEntry](imsgstore-openentry.md) do repositório de mensagens, passando a propriedade **PR_IPM_SUBTREE_ENTRYID,** para abrir a pasta raiz da subárvore IPM do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="2c2a3-125">Chame o método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) da pasta raiz do IPM para acessar sua tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="2c2a3-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

