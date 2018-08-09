---
title: Pesquisar o catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6673e1d51a7c030a35a7c5c3cbc955341afba299
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770348"
---
# <a name="searching-the-address-book"></a><span data-ttu-id="5ee24-103">Pesquisar o catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="5ee24-103">Searching the address book</span></span>

<span data-ttu-id="5ee24-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5ee24-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5ee24-105">MAPI permite que os provedores de catálogo de endereços implementar dois níveis de funcionalidade de pesquisa:</span><span class="sxs-lookup"><span data-stu-id="5ee24-105">MAPI enables address book providers to implement two levels of search functionality:</span></span>
  
- <span data-ttu-id="5ee24-106">Um nível básico que corresponda a um nome especificado com a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) das entradas do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="5ee24-106">A basic level that matches a specified name with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of address book entries.</span></span> <span data-ttu-id="5ee24-107">Este nível permite que os usuários, por exemplo, para exibir listas de distribuição com nomes começando com Noroeste ou localizar usuários individuais de mensagens cujo sobrenome seja marrom.</span><span class="sxs-lookup"><span data-stu-id="5ee24-107">This level allows users, for example, to view distribution lists with names beginning with Northwest or locate individual messaging users whose last name is Brown.</span></span>
    
- <span data-ttu-id="5ee24-108">Um nível avançado que corresponda a propriedades que não seja **PR_DISPLAY_NAME**.</span><span class="sxs-lookup"><span data-stu-id="5ee24-108">An advanced level that matches on properties other than **PR_DISPLAY_NAME**.</span></span> <span data-ttu-id="5ee24-109">Este nível permite que os usuários, por exemplo, para reduzir ainda mais suas pesquisas e localizar mensagens chamados Brown com um tipo de endereço específico de usuários.</span><span class="sxs-lookup"><span data-stu-id="5ee24-109">This level allows users, for example, to further narrow their searches and find messaging users named Brown with a particular address type.</span></span>
    
<span data-ttu-id="5ee24-110">Porque oferece suporte a procurando por cada um dos seus contêineres no nível básico, em ambos os níveis, ou optar por não suportá-las em todos os provedores de catálogo de endereços, não espera pesquisando para ser implementado como um recurso padrão.</span><span class="sxs-lookup"><span data-stu-id="5ee24-110">Because address book providers can support searching for each of their containers at the basic level, at both levels, or choose not to support it at all, do not expect searching to be implemented as a standard feature.</span></span> <span data-ttu-id="5ee24-111">Para determinar se um determinado recipiente suporta pesquisas, tente estabelecer critérios de pesquisa em uma chamada para seu método de [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="5ee24-111">To determine if a particular container supports searches, attempt to establish search criteria in a call to its [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> <span data-ttu-id="5ee24-112">Se **definir SetSearchCriteria** retornar MAPI_E_NO_SUPPORT, o contêiner não oferece suporte a pesquisas.</span><span class="sxs-lookup"><span data-stu-id="5ee24-112">If **SetSearchCriteria** returns MAPI_E_NO_SUPPORT, the container does not support searches.</span></span> 
  
<span data-ttu-id="5ee24-113">Em um contêiner que suporta pesquisas, recupere critérios estabelecidos chamando [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md).</span><span class="sxs-lookup"><span data-stu-id="5ee24-113">In a container that supports searches, retrieve established criteria by calling [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md).</span></span> <span data-ttu-id="5ee24-114">Você também pode solicitar que o usuário solicitado para os critérios de pesquisa antes de tabela de conteúdo de um contêiner é exibida.</span><span class="sxs-lookup"><span data-stu-id="5ee24-114">You can also request that the user be prompted for search criteria before a container's contents table is displayed.</span></span> <span data-ttu-id="5ee24-115">Para escolher essa opção, defina o sinalizador AB_FIND_ON_OPEN da propriedade de **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) do contêiner.</span><span class="sxs-lookup"><span data-stu-id="5ee24-115">To choose this option, set the AB_FIND_ON_OPEN flag of the container's **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property.</span></span> <span data-ttu-id="5ee24-116">Depois que o usuário insere os critérios, é armazenada como uma restrição e passada para o método **definir SetSearchCriteria** .</span><span class="sxs-lookup"><span data-stu-id="5ee24-116">After the user enters the criteria, it is stored as a restriction and passed to the **SetSearchCriteria** method.</span></span> <span data-ttu-id="5ee24-117">Definindo AB_FIND_ON_OPEN é particularmente útil se você estiver usando um serviço online ou qualquer provedor de catálogo de endereços que tem um vínculo lento para seus dados.</span><span class="sxs-lookup"><span data-stu-id="5ee24-117">Setting AB_FIND_ON_OPEN is particularly useful if you are using an online service or any address book provider that has a slow link to its data.</span></span> 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a><span data-ttu-id="5ee24-118">Para executar uma pesquisa básica em um contêiner de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="5ee24-118">To perform a basic search in an address book container</span></span>
  
1. <span data-ttu-id="5ee24-119">Chame o método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) do contêiner para abrir a tabela de seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5ee24-119">Call the container's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
2. <span data-ttu-id="5ee24-120">Escolha uma técnica de pesquisa que atenda às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="5ee24-120">Choose a search technique that meets your needs.</span></span> <span data-ttu-id="5ee24-121">As opções incluem:</span><span class="sxs-lookup"><span data-stu-id="5ee24-121">The choices include:</span></span>
    
   - <span data-ttu-id="5ee24-122">[IMAPITable:: FindRow](imapitable-findrow.md) para localizar uma linha específica na tabela.</span><span class="sxs-lookup"><span data-stu-id="5ee24-122">[IMAPITable::FindRow](imapitable-findrow.md) to locate a specific row in the table.</span></span> 
    
   - <span data-ttu-id="5ee24-123">[IMAPITable:: SortTable](imapitable-sorttable.md) às linhas de pedido na tabela.</span><span class="sxs-lookup"><span data-stu-id="5ee24-123">[IMAPITable::SortTable](imapitable-sorttable.md) to order rows in the table.</span></span> 
    
   - <span data-ttu-id="5ee24-124">[IMAPITable:: Restrict](imapitable-restrict.md) para limitar o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="5ee24-124">[IMAPITable::Restrict](imapitable-restrict.md) to limit the table view.</span></span> 
    
   - <span data-ttu-id="5ee24-125">Restrição de propriedade usando a propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para resolver nomes ambíguos.</span><span class="sxs-lookup"><span data-stu-id="5ee24-125">Property restriction using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property for resolving ambiguous names.</span></span> <span data-ttu-id="5ee24-126">Chame **IMAPITable:: Restrict** para impor essa restrição.</span><span class="sxs-lookup"><span data-stu-id="5ee24-126">Call **IMAPITable::Restrict** to impose this restriction.</span></span> 
    
   - <span data-ttu-id="5ee24-127">[IABContainer:: ResolveNames](iabcontainer-resolvenames.md) para resolver nomes de ambíguos.</span><span class="sxs-lookup"><span data-stu-id="5ee24-127">[IABContainer::ResolveNames](iabcontainer-resolvenames.md) to resolve ambiguous names.</span></span> 
    
3. <span data-ttu-id="5ee24-128">Chame [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas as linhas que atendem aos critérios de pesquisa aplicados.</span><span class="sxs-lookup"><span data-stu-id="5ee24-128">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve any rows that meet your applied search criteria.</span></span> <span data-ttu-id="5ee24-129">**QueryRows** pode retornar zero ou mais linhas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="5ee24-129">**QueryRows** can return zero or more matching rows.</span></span> 
    
<span data-ttu-id="5ee24-130">Os métodos **FindRow**, **SortTable**e **Restrict** são tabela que estão disponíveis para qualquer tabela que pode ser criada por um cliente ou um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="5ee24-130">The **FindRow**, **SortTable**, and **Restrict** methods are table methods that are available for any table that can be created, either by a client or a service provider.</span></span> <span data-ttu-id="5ee24-131">O **PR\_ANR** método **IABContainer:: ResolveNames** e restrição de propriedade são específicos para provedores de catálogo de endereços e são usados para resolver nomes ambíguos.</span><span class="sxs-lookup"><span data-stu-id="5ee24-131">The **PR\_ANR** property restriction and **IABContainer::ResolveNames** method are specific to address book providers and are used for resolving ambiguous names.</span></span> <span data-ttu-id="5ee24-132">Nomes ambíguos são entradas em uma lista de destinatários que não possuem uma propriedade **PR_ENTRYID** associada a eles.</span><span class="sxs-lookup"><span data-stu-id="5ee24-132">Ambiguous names are entries in a recipient list that do not have a **PR_ENTRYID** property associated with them.</span></span> 
  
<span data-ttu-id="5ee24-133">O **PR\_ANR** restrição invoca um algoritmo que separa uma cadeia de caracteres em palavras e faz a correspondência dessas palavras com informações no catálogo de endereços usando a correspondência de prefixo.</span><span class="sxs-lookup"><span data-stu-id="5ee24-133">The **PR\_ANR** restriction invokes an algorithm that separates a character string into words and matches those words with information in the address book using prefix-matching.</span></span> <span data-ttu-id="5ee24-134">As informações utilizadas para a correspondência dependem do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="5ee24-134">The information used for the matching depends on the address book provider.</span></span> <span data-ttu-id="5ee24-135">Todos os provedores de catálogo de endereços são necessárias para dar suporte a restrição de **PR_ANR** para seus contêineres do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="5ee24-135">All address book providers are required to support the **PR_ANR** restriction for their address book containers.</span></span> <span data-ttu-id="5ee24-136">Para obter mais informações, consulte [Implementando a resolução de nome](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="5ee24-136">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="5ee24-137">**IABContainer:: ResolveNames** realiza a restrição de **PR_ANR** de processamento em vários nomes sem a necessidade de tabela de conteúdo do contêiner para ser aberto.</span><span class="sxs-lookup"><span data-stu-id="5ee24-137">**IABContainer::ResolveNames** performs **PR_ANR** restriction processing on multiple names without requiring the container's contents table to be open.</span></span> <span data-ttu-id="5ee24-138">Chamar **ResolveNames** uma vez para resolver nomes de vários pode ser muito mais rápido do que chamar uma **PR\_ANR** restrição várias vezes.</span><span class="sxs-lookup"><span data-stu-id="5ee24-138">Calling **ResolveNames** once to resolve multiple names can be much faster than invoking a **PR\_ANR** restriction multiple times.</span></span> <span data-ttu-id="5ee24-139">No entanto, provedores de catálogo de endereços não são necessárias para dar suporte a **ResolveNames**.</span><span class="sxs-lookup"><span data-stu-id="5ee24-139">However, address book providers are not required to support **ResolveNames**.</span></span>
  
