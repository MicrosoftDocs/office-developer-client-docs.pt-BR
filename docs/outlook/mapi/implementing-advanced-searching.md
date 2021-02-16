---
title: Implementando a Pesquisa Avançada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407386"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="d3cb2-103">Implementando a Pesquisa Avançada</span><span class="sxs-lookup"><span data-stu-id="d3cb2-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="d3cb2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3cb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3cb2-105">Alguns contêineres de livro de endereços suportam um recurso de pesquisa avançada que permite que os clientes pesquisem em propriedades diferentes de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d3cb2-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="d3cb2-106">Para dar suporte a pesquisas avançadas, seu provedor deve implementar um contêiner especial que seja acessível por meio da propriedade **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de seus outros contêineres.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="d3cb2-107">**PR_SEARCH** contém um objeto container que fornece acesso a uma tabela de exibição que descreve a caixa de diálogo usada para inserir e editar os critérios de pesquisa avançados.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="d3cb2-108">**Para dar suporte à pesquisa avançada**</span><span class="sxs-lookup"><span data-stu-id="d3cb2-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="d3cb2-109">Defina uma propriedade para cada um dos seus critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="d3cb2-110">Na seção do código no método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner que lida com PR_SEARCH **propriedade:**</span><span class="sxs-lookup"><span data-stu-id="d3cb2-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="d3cb2-111">Verifique se o cliente está solicitando a interface **IMAPIContainer.**</span><span class="sxs-lookup"><span data-stu-id="d3cb2-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="d3cb2-112">Se uma interface inadequada estiver sendo solicitada, falhará e retornará MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="d3cb2-113">Crie um novo objeto de pesquisa que suporte a interface **IMAPIContainer.**</span><span class="sxs-lookup"><span data-stu-id="d3cb2-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="d3cb2-114">Neste ponto, será feita uma chamada ao método **IMAPIProp::OpenProperty** do contêiner de pesquisa para recuperar sua **propriedade PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d3cb2-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="d3cb2-115">Seu provedor deve fornecer uma tabela de exibição, normalmente por meio de uma chamada para [BuildDisplayTable](builddisplaytable.md), que descreve a caixa de diálogo de pesquisa avançada do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="d3cb2-116">O MAPI exibe a caixa de diálogo de pesquisa, permitindo que o usuário insira os critérios apropriados.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="d3cb2-117">Quando o usuário tiver terminado, o MAPI chamará o método [IMAPIProp::SetProps](imapiprop-setprops.md) do contêiner para armazenar os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="d3cb2-118">Uma chamada será feita para solicitar a tabela de conteúdo do contêiner de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="d3cb2-119">Preencha a tabela de conteúdo com todas as entradas no contêiner que corresponderem aos critérios.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    

