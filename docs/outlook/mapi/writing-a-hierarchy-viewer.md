---
title: Gravar um visualizador de hierarquia
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6ff394c95dfa3166d39dcba4b0c577dcfac7b8d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581591"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="d89d5-103">Gravar um visualizador de hierarquia</span><span class="sxs-lookup"><span data-stu-id="d89d5-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="d89d5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d89d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d89d5-105">Um visualizador de hierarquia é um componente de interface do usuário que é usado para exibir a pasta e o endereço de tabelas de hierarquias de contêiner de catálogo.</span><span class="sxs-lookup"><span data-stu-id="d89d5-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="d89d5-106">Visualizadores de hierarquia podem exibir os membros da hierarquia em níveis diferentes, expandindo e firmando contrato cada nível sob demanda.</span><span class="sxs-lookup"><span data-stu-id="d89d5-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="d89d5-107">A propriedade container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controla o nível no qual um membro de hierarquia é exibido.</span><span class="sxs-lookup"><span data-stu-id="d89d5-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="d89d5-108">Entradas que representam os contêineres do catálogo de endereços de nível superior ou pastas têm sua propriedade **PR_DEPTH** definida como zero.</span><span class="sxs-lookup"><span data-stu-id="d89d5-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="d89d5-109">O valor dessa propriedade é incrementado sequencialmente para entradas nos níveis sequenciais.</span><span class="sxs-lookup"><span data-stu-id="d89d5-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="d89d5-110">Ou seja, quando o usuário seleciona um contêiner de nível superior para expandir e exibir todos os contêineres com **PR_DEPTH** é definida como 1.</span><span class="sxs-lookup"><span data-stu-id="d89d5-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="d89d5-111">Quando um usuário expande um desses subcontêineres, exibir os contêineres com **PR_DEPTH** definido como 2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d89d5-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="d89d5-112">Visualizadores de hierarquia oferecem suporte a um intervalo diferente de Profundidades.</span><span class="sxs-lookup"><span data-stu-id="d89d5-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="d89d5-113">Você pode limitar o visualizador a apenas um ou dois níveis, ou você pode oferecer suporte a vários níveis, se a exibição de uma hierarquia expansiva é uma prioridade.</span><span class="sxs-lookup"><span data-stu-id="d89d5-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="d89d5-114">O catálogo de endereços fornece um visualizador de hierarquia para os recipientes de nível superior no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="d89d5-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="d89d5-115">**Para acessar a tabela de hierarquia de catálogo de endereços**</span><span class="sxs-lookup"><span data-stu-id="d89d5-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="d89d5-116">Chame [IAddrBook::OpenEntry](iaddrbook-openentry.md), passando um identificador de entrada nulo, para abrir o contêiner de raiz do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="d89d5-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="d89d5-117">Chame o método de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) do contêiner raiz para acessar a tabela de hierarquia do catálogo de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="d89d5-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="d89d5-118">**Para acessar a tabela de hierarquia do armazenamento de mensagens padrão**</span><span class="sxs-lookup"><span data-stu-id="d89d5-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="d89d5-119">Chame [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para acessar a tabela de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d89d5-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="d89d5-120">Construa uma restrição usando a estrutura de [SPropertyRestriction](spropertyrestriction.md) para limitar a tabela de somente as linhas que possuem uma propriedade de **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) definida como TRUE.</span><span class="sxs-lookup"><span data-stu-id="d89d5-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="d89d5-121">Chame [IMAPITable:: FindRow](imapitable-findrow.md), passando-lhe o **SPropertyRestriction**, para localizar a linha que representa o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="d89d5-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="d89d5-122">Chame [IMAPISession::OpenEntry](imapisession-openentry.md), passando na propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do armazenamento de mensagens padrão da tabela de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d89d5-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="d89d5-123">Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d89d5-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="d89d5-124">Chame o método de [IMsgStore::OpenEntry](imsgstore-openentry.md) do armazenamento de mensagens, passando a propriedade **PR_IPM_SUBTREE_ENTRYID** , para abrir a pasta raiz do subárvore IPM do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d89d5-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="d89d5-125">Chame o método de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) da pasta raiz IPM para acessar sua tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="d89d5-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

