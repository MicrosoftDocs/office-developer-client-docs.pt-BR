---
title: Abrir um contêiner de catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Última modificação: 08 de novembro de 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436738"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="952dc-103">Abrir um contêiner de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="952dc-103">Opening an address book container</span></span>

<span data-ttu-id="952dc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="952dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="952dc-105">Após abrir o catálogo de endereços integrado MAPI, abra um ou mais contêineres do catálogo de endereços para acessar os destinatários dentro deles.</span><span class="sxs-lookup"><span data-stu-id="952dc-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="952dc-106">Para abrir o contêiner de nível superior do catálogo de endereços, chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md) com um identificador de entrada nulo.</span><span class="sxs-lookup"><span data-stu-id="952dc-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="952dc-107">Os contêineres do catálogo de endereços podem ser implementados com acesso somente leitura ou leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="952dc-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="952dc-108">Contêineres somente leitura são usados apenas para navegação.</span><span class="sxs-lookup"><span data-stu-id="952dc-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="952dc-109">Contêineres de leitura/gravação podem ser modificados, permitindo que os clientes criem novas entradas e excluam e modifiquem entradas existentes.</span><span class="sxs-lookup"><span data-stu-id="952dc-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="952dc-110">Todos os contêineres do catálogo de endereços pessoal (PAB) são implementados como contêineres de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="952dc-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="952dc-111">Para abrir qualquer contêiner de nível inferior, chame **OpenEntry** e especifique o identificador de entrada do contêiner a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="952dc-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="952dc-112">Abra o contêiner designado como o PAB</span><span class="sxs-lookup"><span data-stu-id="952dc-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="952dc-113">Chame [IAddrBook:: GetPAB](iaddrbook-getpab.md) para recuperar o identificador de entrada do PAB.</span><span class="sxs-lookup"><span data-stu-id="952dc-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="952dc-114">Passe este identificador de entrada para [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="952dc-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="952dc-115">Abrir um contêiner que não seja o PAB</span><span class="sxs-lookup"><span data-stu-id="952dc-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="952dc-116">Chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md) com um identificador de entrada nulo para abrir o contêiner raiz do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="952dc-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="952dc-117">Chame o método [IMAPIContainer::](imapicontainer-gethierarchytable.md) GetHierarchyTable do contêiner raiz para recuperar sua tabela de hierarquia — uma lista de todos os contêineres de nível superior no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="952dc-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="952dc-118">Se o contêiner a ser aberto for de um tipo específico:</span><span class="sxs-lookup"><span data-stu-id="952dc-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="952dc-119">Crie uma estrutura **SPropertyRestriction** com **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para a marca de propriedade, o tipo de contêiner para o valor da propriedade e RELOP_EQ para a relação.</span><span class="sxs-lookup"><span data-stu-id="952dc-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="952dc-120">**PR_DISPLAY_TYPE** pode ser definido como muitos valores, entre eles:</span><span class="sxs-lookup"><span data-stu-id="952dc-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="952dc-121">DT_GLOBAL para limitar a tabela de hierarquia a contêineres que pertencem à lista de endereços global.</span><span class="sxs-lookup"><span data-stu-id="952dc-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="952dc-122">DT_LOCAL para limitar a tabela a contêineres pertencentes a um catálogo de endereços local.</span><span class="sxs-lookup"><span data-stu-id="952dc-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="952dc-123">DT_MODIFIABLE para limitar a tabela a contêineres que podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="952dc-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="952dc-124">Criar uma estrutura [SPropTagArray](sproptagarray.md) que inclui o **PR_ENTRYID**, o **PR_DISPLAY_TYPE**e qualquer outra coluna de interesse.</span><span class="sxs-lookup"><span data-stu-id="952dc-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="952dc-125">Chame [HrQueryAllRows](hrqueryallrows.md), passando a restrição de propriedade e a matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="952dc-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="952dc-126">**HrQueryAllRows** retornará zero ou mais linhas, uma linha para cada contêiner que pertence ao tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="952dc-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="952dc-127">Esteja preparado para lidar com o retorno de qualquer número de linhas.</span><span class="sxs-lookup"><span data-stu-id="952dc-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="952dc-128">Chame **IAddrBook:: OpenEntry** com o identificador de entrada da coluna **PR_ENTRYID** da linha que representa o contêiner de interesse.</span><span class="sxs-lookup"><span data-stu-id="952dc-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="952dc-129">Se o contêiner a ser aberto pertencer a um provedor de catálogo de endereços específico:</span><span class="sxs-lookup"><span data-stu-id="952dc-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="952dc-130">Crie uma estrutura [SPropertyRestriction](spropertyrestriction.md) com **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) para a marca de propriedade, um valor específico do provedor para o valor da propriedade e RELOP_EQ para a relação.</span><span class="sxs-lookup"><span data-stu-id="952dc-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="952dc-131">Normalmente, o valor específico do provedor é um identificador global exclusivo ou um GUID.</span><span class="sxs-lookup"><span data-stu-id="952dc-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="952dc-132">Você encontrará esse valor publicado em um dos arquivos de cabeçalho do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="952dc-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="952dc-133">Crie uma estrutura [SPropTagArray](sproptagarray.md) que inclui o **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), o **PR_AB_PROVIDERS**e qualquer outra coluna de interesse.</span><span class="sxs-lookup"><span data-stu-id="952dc-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="952dc-134">Chame [HrQueryAllRows](hrqueryallrows.md), passando a restrição de propriedade e a matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="952dc-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="952dc-135">**HrQueryAllRows** retornará zero linhas se o provedor de catálogo de endereços especificado não estiver no perfil.</span><span class="sxs-lookup"><span data-stu-id="952dc-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="952dc-136">Pode retornar uma ou mais linhas para os contêiners de nível superior do provedor, dependendo de como o provedor é organizado.</span><span class="sxs-lookup"><span data-stu-id="952dc-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="952dc-137">Chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md) com o identificador de entrada da coluna **PR_ENTRYID** da linha que representa o contêiner de interesse.</span><span class="sxs-lookup"><span data-stu-id="952dc-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="952dc-138">Se o contêiner em que você está interessado não for um contêiner de nível superior, encontre o contêiner de nível superior e atravesse a hierarquia.</span><span class="sxs-lookup"><span data-stu-id="952dc-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

