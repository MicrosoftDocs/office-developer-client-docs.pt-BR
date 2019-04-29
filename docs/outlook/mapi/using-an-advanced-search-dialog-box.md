---
title: Usando uma caixa de diálogo de pesquisa avançada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437298"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="004c8-103">Usando uma caixa de diálogo de pesquisa avançada</span><span class="sxs-lookup"><span data-stu-id="004c8-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="004c8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="004c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="004c8-105">Alguns contêineres do catálogo de endereços dão suporte a um recurso de pesquisa avançada que permite que os clientes pesquisem propriedades diferentes de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="004c8-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="004c8-106">Os contêineres do catálogo de endereços que oferecem suporte a pesquisas avançadas têm uma propriedade de objeto de contêiner chamada **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="004c8-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="004c8-107">Este objeto Container fornece acesso a uma tabela de exibição que descreve a caixa de diálogo de pesquisa — uma caixa de diálogo usada para inserir e editar os critérios de pesquisa avançados.</span><span class="sxs-lookup"><span data-stu-id="004c8-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="004c8-108">**Para executar uma pesquisa avançada em um contêiner de catálogo de endereços**</span><span class="sxs-lookup"><span data-stu-id="004c8-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="004c8-109">Chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do contêiner, especificando **PR_SEARCH** para a marca de propriedade e IID_IMAPIContainer para o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="004c8-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="004c8-110">Chame o método **IMAPIProp:: OpenProperty** do objeto de pesquisa, especificando **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) para a marca de propriedade e IID_IMAPITable para o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="004c8-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="004c8-111">Chame o método [IMAPIProp::](imapiprop-setprops.md) SetProps do objeto de pesquisa para estabelecer valores para as propriedades a serem usadas na pesquisa avançada.</span><span class="sxs-lookup"><span data-stu-id="004c8-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="004c8-112">Chame o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) do objeto de pesquisa para salvar os critérios de pesquisa avançados.</span><span class="sxs-lookup"><span data-stu-id="004c8-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="004c8-113">Essa sequência de chamadas resulta na disponibilidade de uma restrição quando um cliente chama o método **GetSearchCriteria** do objeto de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="004c8-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

