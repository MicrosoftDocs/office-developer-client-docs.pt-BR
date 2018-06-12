---
title: Usando uma caixa de diálogo de pesquisa avançada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3c27b859f6d056d3b9a98bd4d71db8e500dff696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770693"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="17ebf-103">Usando uma caixa de diálogo de pesquisa avançada</span><span class="sxs-lookup"><span data-stu-id="17ebf-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="17ebf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="17ebf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="17ebf-105">Alguns recipientes do catálogo de endereços oferecem suporte a um recurso de pesquisando avançado que permite aos clientes pesquisar propriedades que não seja **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="17ebf-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="17ebf-106">Contêineres de catálogo de endereços que oferecem suporte a pesquisas avançadas possuem uma propriedade de objeto de contêiner chamada **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="17ebf-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="17ebf-107">Este objeto de contêiner fornece acesso a uma tabela de exibição que descreve a caixa de diálogo de pesquisa — uma caixa de diálogo usada para inserir e editar os critérios de pesquisa avançada.</span><span class="sxs-lookup"><span data-stu-id="17ebf-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="17ebf-108">**Para realizar uma pesquisa avançada em um contêiner de catálogo de endereços**</span><span class="sxs-lookup"><span data-stu-id="17ebf-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="17ebf-109">Chame o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner, especificando **PR_SEARCH** para a marca de propriedade e IID_IMAPIContainer para o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="17ebf-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="17ebf-110">Chame o método de **IMAPIProp::OpenProperty** do objeto de pesquisa, especificando **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) para a marca de propriedade e IID_IMAPITable para o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="17ebf-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="17ebf-111">Chame o método de [IMAPIProp::SetProps](imapiprop-setprops.md) do objeto de pesquisa para estabelecer valores para as propriedades a ser usado na página Pesquisa avançada.</span><span class="sxs-lookup"><span data-stu-id="17ebf-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="17ebf-112">Chame o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) do objeto de pesquisa para salvar os critérios de pesquisa avançada.</span><span class="sxs-lookup"><span data-stu-id="17ebf-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="17ebf-113">Esta sequência de chamadas resulta em uma restrição fique disponível quando um cliente chama o método de **obter GetSearchCriteria** do objeto search.</span><span class="sxs-lookup"><span data-stu-id="17ebf-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

