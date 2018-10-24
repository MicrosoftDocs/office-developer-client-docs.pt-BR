---
title: Configurar opções de Catálogo de Endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0d93fde7d654f0ee56dcda9f2fb69ad622e476dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593617"
---
# <a name="setting-address-book-options"></a><span data-ttu-id="1ae4f-103">Configurar opções de Catálogo de Endereços</span><span class="sxs-lookup"><span data-stu-id="1ae4f-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="1ae4f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ae4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ae4f-105">Você pode definir três propriedades que descrevem as opções para usar o catálogo de endereços:</span><span class="sxs-lookup"><span data-stu-id="1ae4f-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="1ae4f-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1ae4f-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="1ae4f-107">A propriedade **PR_AB_SEARCH_PATH** é usada pelo [IAddrBook::ResolveName](iaddrbook-resolvename.md) para determinar os contêineres estar envolvidos na resolução de nome e a ordem que devem ser envolvidos.</span><span class="sxs-lookup"><span data-stu-id="1ae4f-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="1ae4f-108">Para cada contêiner no **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** chama seu método de [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) .</span><span class="sxs-lookup"><span data-stu-id="1ae4f-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="1ae4f-109">Contêineres no início do **PR_AB_SEARCH_PATH** são pesquisados antes de contêineres no final da **PR_AB_SEARCH_PATH**.</span><span class="sxs-lookup"><span data-stu-id="1ae4f-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="1ae4f-110">A ordem de pesquisa no **PR_AB_SEARCH_PATH** é especificada usando uma estrutura [SRowSet](srowset.md) , a mesma estrutura que é usada para representar as linhas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="1ae4f-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="1ae4f-111">Você pode exibir o caminho de pesquisa atual chamando o método [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) e alterá-lo chamando o método [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) .</span><span class="sxs-lookup"><span data-stu-id="1ae4f-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="1ae4f-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1ae4f-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="1ae4f-113">A propriedade **PR_AB_DEFAULT_DIR** é o identificador de entrada do contêiner de catálogo de endereços a ser exibido inicialmente quando o catálogo de endereços é exibido.</span><span class="sxs-lookup"><span data-stu-id="1ae4f-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="1ae4f-114">A configuração padrão do diretório permanece em vigor até você alterá-lo chamando o método [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) .</span><span class="sxs-lookup"><span data-stu-id="1ae4f-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="1ae4f-115">Você pode exibir o diretório padrão chamando o método [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) .</span><span class="sxs-lookup"><span data-stu-id="1ae4f-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="1ae4f-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1ae4f-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="1ae4f-117">Essas três propriedades são especiais porque você não pode trabalhar com eles com os métodos **IMAPIProp** padrão.</span><span class="sxs-lookup"><span data-stu-id="1ae4f-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="1ae4f-118">Em vez disso, você deve usar os métodos **IAddrBook** .</span><span class="sxs-lookup"><span data-stu-id="1ae4f-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="1ae4f-119">Porque nenhuma dessas propriedades pode ser alterada com **IMAPIProp::SetProps**, não é necessário chamar **IMAPIProp::SaveChanges** para fazer alterações permanentes.</span><span class="sxs-lookup"><span data-stu-id="1ae4f-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="1ae4f-120">As modificações feitas por meio dos métodos **IAddrBook** entrarão em vigor imediatamente.</span><span class="sxs-lookup"><span data-stu-id="1ae4f-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ae4f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ae4f-121">See also</span></span>



[<span data-ttu-id="1ae4f-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1ae4f-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

