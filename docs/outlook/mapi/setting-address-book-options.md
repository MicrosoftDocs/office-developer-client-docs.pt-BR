---
title: Definindo opções do address book
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417340"
---
# <a name="setting-address-book-options"></a><span data-ttu-id="5d8fe-103">Definindo opções do address book</span><span class="sxs-lookup"><span data-stu-id="5d8fe-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="5d8fe-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d8fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d8fe-105">Você pode definir três propriedades que descrevem opções para usar o address book:</span><span class="sxs-lookup"><span data-stu-id="5d8fe-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="5d8fe-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d8fe-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="5d8fe-107">A **PR_AB_SEARCH_PATH** propriedade é usada por [IAddrBook::ResolveName](iaddrbook-resolvename.md) para determinar os contêineres a serem envolvidos na resolução de nomes e na ordem em que eles devem estar envolvidos.</span><span class="sxs-lookup"><span data-stu-id="5d8fe-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="5d8fe-108">Para cada contêiner em **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** chama seu [método IABContainer::ResolveNames.](iabcontainer-resolvenames.md)</span><span class="sxs-lookup"><span data-stu-id="5d8fe-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="5d8fe-109">Contêineres no início do **PR_AB_SEARCH_PATH** são pesquisados antes de contêineres no final do **PR_AB_SEARCH_PATH**.</span><span class="sxs-lookup"><span data-stu-id="5d8fe-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="5d8fe-110">A ordem de pesquisa **PR_AB_SEARCH_PATH** é especificada usando uma estrutura [SRowSet,](srowset.md) a mesma estrutura usada para representar linhas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="5d8fe-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="5d8fe-111">Você pode exibir o caminho de pesquisa atual chamando o método [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) e alterá-lo chamando o método [IAddrBook::SetSearchPath.](iaddrbook-setsearchpath.md)</span><span class="sxs-lookup"><span data-stu-id="5d8fe-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="5d8fe-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d8fe-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="5d8fe-113">A **PR_AB_DEFAULT_DIR** é o identificador de entrada do contêiner do livro de endereços a ser exibido inicialmente quando o livro de endereços é exibido.</span><span class="sxs-lookup"><span data-stu-id="5d8fe-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="5d8fe-114">A configuração de diretório padrão permanece em vigor até você alterá-la chamando o [método IAddrBook::SetDefaultDir.](iaddrbook-setdefaultdir.md)</span><span class="sxs-lookup"><span data-stu-id="5d8fe-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="5d8fe-115">Você pode exibir o diretório padrão chamando o [método IAddrBook::GetDefaultDir.](iaddrbook-getdefaultdir.md)</span><span class="sxs-lookup"><span data-stu-id="5d8fe-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="5d8fe-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d8fe-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="5d8fe-117">Essas três propriedades são especiais porque você não pode trabalhar com elas usando os métodos **IMAPIProp** padrão.</span><span class="sxs-lookup"><span data-stu-id="5d8fe-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="5d8fe-118">Em vez disso, você deve usar **os métodos IAddrBook.**</span><span class="sxs-lookup"><span data-stu-id="5d8fe-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="5d8fe-119">Como nenhuma dessas propriedades pode ser alterada com **IMAPIProp::SetProps,** não há necessidade de chamar **IMAPIProp::SaveChanges** para tornar as alterações permanentes.</span><span class="sxs-lookup"><span data-stu-id="5d8fe-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="5d8fe-120">As modificações feitas por meio **dos métodos IAddrBook** tem efeito imediato.</span><span class="sxs-lookup"><span data-stu-id="5d8fe-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d8fe-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d8fe-121">See also</span></span>



[<span data-ttu-id="5d8fe-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5d8fe-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

