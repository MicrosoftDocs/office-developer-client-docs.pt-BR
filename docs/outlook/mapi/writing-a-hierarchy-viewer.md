---
title: Criar um visualizador de hierarquia
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325638"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="9e03c-103">Criar um visualizador de hierarquia</span><span class="sxs-lookup"><span data-stu-id="9e03c-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="9e03c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e03c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e03c-105">Um visualizador de hierarquia é um componente de interface de usuário usado para exibir as tabelas de hierarquia de contêiner de pasta e catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="9e03c-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="9e03c-106">Os visualizadores de hierarquia podem exibir membros da hierarquia em diferentes níveis, expandindo e contratando cada nível sob demanda.</span><span class="sxs-lookup"><span data-stu-id="9e03c-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="9e03c-107">A propriedade container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controla o nível no qual um membro de hierarquia é exibido.</span><span class="sxs-lookup"><span data-stu-id="9e03c-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="9e03c-108">As entradas que representam recipientes ou pastas de catálogo de endereços de nível superior têm a propriedade **PR_DEPTH** definida como zero.</span><span class="sxs-lookup"><span data-stu-id="9e03c-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="9e03c-109">O valor dessa propriedade é incrementalmente em sequência para entradas em níveis sequenciais.</span><span class="sxs-lookup"><span data-stu-id="9e03c-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="9e03c-110">Ou seja, quando um usuário seleciona um contêiner de nível superior para expandir, exiba todos os contêineres com **PR_DEPTH** definido como 1.</span><span class="sxs-lookup"><span data-stu-id="9e03c-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="9e03c-111">Quando um usuário expande um desses sub-recipientes, exibe os contêineres com **PR_DEPTH** definido como 2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9e03c-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="9e03c-112">Os visualizadores de hierarquia dão suporte a um intervalo diferente de profundidades.</span><span class="sxs-lookup"><span data-stu-id="9e03c-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="9e03c-113">Você pode limitar o seu visualizador a apenas um ou dois níveis, ou pode dar suporte a vários níveis, se a exibição de uma hierarquia de baixo for uma prioridade.</span><span class="sxs-lookup"><span data-stu-id="9e03c-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="9e03c-114">O catálogo de endereços fornece um visualizador de hierarquia para os recipientes de nível superior no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="9e03c-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="9e03c-115">**Para acessar a tabela de hierarquia de catálogo de endereços**</span><span class="sxs-lookup"><span data-stu-id="9e03c-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="9e03c-116">Chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md), passando um identificador de entrada nulo, para abrir o contêiner raiz do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="9e03c-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="9e03c-117">Chame o método [IMAPIContainer::](imapicontainer-gethierarchytable.md) GetHierarchyTable do contêiner raiz para acessar a tabela de hierarquia do catálogo de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e03c-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="9e03c-118">**Para acessar a tabela de hierarquia do repositório de mensagens padrão**</span><span class="sxs-lookup"><span data-stu-id="9e03c-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="9e03c-119">Chame [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) para acessar a tabela do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9e03c-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="9e03c-120">Crie uma restrição usando a estrutura [SPropertyRestriction](spropertyrestriction.md) para limitar a tabela apenas às linhas que têm uma propriedade **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) definida como true.</span><span class="sxs-lookup"><span data-stu-id="9e03c-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="9e03c-121">Call [IMAPITable:: FindRow](imapitable-findrow.md), passando-o **SPropertyRestriction**para localizar a linha que representa o repositório de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="9e03c-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="9e03c-122">Chame [IMAPISession:: OpenEntry](imapisession-openentry.md), passando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do repositório de mensagens padrão na tabela do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9e03c-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="9e03c-123">Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps do repositório de mensagens para recuperar a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e03c-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="9e03c-124">Chame o método [IMsgStore:: OpenEntry](imsgstore-openentry.md) do repositório de mensagens, passando a propriedade **PR_IPM_SUBTREE_ENTRYID** , para abrir a pasta raiz da sub-árvore IPM do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9e03c-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="9e03c-125">Chame o método [IMAPIContainer::](imapicontainer-gethierarchytable.md) GetHierarchyTable da pasta raiz IPM para acessar sua tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="9e03c-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

