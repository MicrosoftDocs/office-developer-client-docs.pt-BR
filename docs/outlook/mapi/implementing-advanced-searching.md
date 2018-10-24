---
title: Implementar a pesquisa avançada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0ba9958588c476ae330b0f4a413361e80d54667a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571966"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="d1b03-103">Implementar a pesquisa avançada</span><span class="sxs-lookup"><span data-stu-id="d1b03-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="d1b03-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1b03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1b03-105">Alguns recipientes do catálogo de endereços oferecem suporte a um recurso de pesquisando avançado que permite aos clientes pesquisar propriedades que não seja **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d1b03-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="d1b03-106">Para suportar pesquisas avançadas, seu provedor deve implementar um contêiner especial que pode ser acessado por meio da propriedade **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) dos seus outros contêineres.</span><span class="sxs-lookup"><span data-stu-id="d1b03-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="d1b03-107">**PR_SEARCH** contém um objeto container que fornece acesso a uma tabela de exibição que descreve a caixa de diálogo usada para inserir e editar os critérios de pesquisa avançada.</span><span class="sxs-lookup"><span data-stu-id="d1b03-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="d1b03-108">**Para oferecer suporte à pesquisa avançada**</span><span class="sxs-lookup"><span data-stu-id="d1b03-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="d1b03-109">Defina uma propriedade para cada um dos seus critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d1b03-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="d1b03-110">Na seção de código no método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do seu contêiner que manipula a propriedade **PR_SEARCH** :</span><span class="sxs-lookup"><span data-stu-id="d1b03-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="d1b03-111">Verifique se o cliente está solicitando a interface **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="d1b03-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="d1b03-112">Se uma interface inadequada é solicitada, falhar e retornar MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="d1b03-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="d1b03-113">Crie um novo objeto de pesquisa que dá suporte à interface **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="d1b03-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="d1b03-114">Neste ponto, vai ser feita uma chamada ao método de **IMAPIProp::OpenProperty** do seu contêiner de pesquisa para recuperar sua propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d1b03-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="d1b03-115">Seu provedor deve fornecer uma exibição de tabela, normalmente por meio de uma chamada para [BuildDisplayTable](builddisplaytable.md), que descreve a caixa de diálogo de pesquisa avançada do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d1b03-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="d1b03-116">MAPI exibe a caixa de diálogo de pesquisa, permitindo que o usuário insira os critérios apropriados.</span><span class="sxs-lookup"><span data-stu-id="d1b03-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="d1b03-117">Quando o usuário tiver terminado, MAPI chama o método de [IMAPIProp::SetProps](imapiprop-setprops.md) do contêiner para armazenar os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d1b03-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="d1b03-118">Será feita uma chamada para solicitar a tabela de conteúdo do seu contêiner de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d1b03-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="d1b03-119">Preenchem a tabela de conteúdo com todas as entradas no contêiner que correspondem aos critérios.</span><span class="sxs-lookup"><span data-stu-id="d1b03-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    

