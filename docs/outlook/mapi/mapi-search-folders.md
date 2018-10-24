---
title: Pastas de pesquisa MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 36c14d91-77f7-43a3-8d87-d50bcc21fad7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c1d7f67458852319587d98831d031b2c3a131871
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400898"
---
# <a name="mapi-search-folders"></a><span data-ttu-id="277fa-103">Pastas de pesquisa MAPI</span><span class="sxs-lookup"><span data-stu-id="277fa-103">MAPI Search Folders</span></span>

  
  
<span data-ttu-id="277fa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="277fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="277fa-105">Uma pasta de resultados de pesquisa contém links para as mensagens nas pastas genéricas em vez das mensagens reais.</span><span class="sxs-lookup"><span data-stu-id="277fa-105">A search-results folder holds links to messages in generic folders rather than the actual messages.</span></span> <span data-ttu-id="277fa-106">Clientes crie uma pasta de resultados de pesquisa chamando o método [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) com FOLDER_SEARCH como o parâmetro _ulFolderType_ .</span><span class="sxs-lookup"><span data-stu-id="277fa-106">Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter.</span></span> <span data-ttu-id="277fa-107">Clientes preencher uma pasta de resultados de pesquisa, configurando e a aplicação de critérios de pesquisa — regras que filtram mensagens com características específicas.</span><span class="sxs-lookup"><span data-stu-id="277fa-107">Clients fill a search-results folder by setting up and applying search criteria — rules that filter out messages with particular characteristics.</span></span> <span data-ttu-id="277fa-108">Critérios de pesquisa são configurados com o método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="277fa-108">Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> <span data-ttu-id="277fa-109">Clientes construa uma ou mais estruturas [SRestriction](srestriction.md) para representar os critérios de pesquisa será aplicado e passá-las para **definir SetSearchCriteria**.</span><span class="sxs-lookup"><span data-stu-id="277fa-109">Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**.</span></span> <span data-ttu-id="277fa-110">**Definir SetSearchCriteria** também especifica uma lista de pastas que indicam o domínio de pesquisa e um conjunto de sinalizadores que controlam como a pesquisa é realizada.</span><span class="sxs-lookup"><span data-stu-id="277fa-110">**SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed.</span></span> 
  
 <span data-ttu-id="277fa-111">**Definir SetSearchCriteria** identifica as mensagens que correspondem a restrição especificada.</span><span class="sxs-lookup"><span data-stu-id="277fa-111">**SetSearchCriteria** identifies the messages that match the specified restriction.</span></span> <span data-ttu-id="277fa-112">As mensagens selecionadas (aqueles que satisfazem os critérios) são exibidas como links na pasta resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="277fa-112">The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder.</span></span> <span data-ttu-id="277fa-113">Quando o cliente chama o método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para acessar a tabela de conteúdo da pasta resultados de pesquisa, as mensagens selecionadas são exibidas na tabela.</span><span class="sxs-lookup"><span data-stu-id="277fa-113">When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table.</span></span> <span data-ttu-id="277fa-114">Tabelas de conteúdo para pastas de resultados de pesquisa contêm as mesmas colunas como tabelas de conteúdo para pastas genéricas.</span><span class="sxs-lookup"><span data-stu-id="277fa-114">Contents tables for search-results folders contain the same columns as contents tables for generic folders.</span></span> <span data-ttu-id="277fa-115">No entanto, para pastas de resultados da pesquisa, a propriedade **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) Especifica o identificador de entrada da pasta em que a mensagem vinculada reside.</span><span class="sxs-lookup"><span data-stu-id="277fa-115">However, for search-results folders, the **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property specifies the entry identifier of the folder where the linked message resides.</span></span> <span data-ttu-id="277fa-116">Pastas de resultados de pesquisa não são consideradas pastas pai.</span><span class="sxs-lookup"><span data-stu-id="277fa-116">Search-results folders are not considered parent folders.</span></span>
  
<span data-ttu-id="277fa-117">Pastas de resultados de pesquisa tem os seguintes limites:</span><span class="sxs-lookup"><span data-stu-id="277fa-117">Search-results folders have the following limits:</span></span>
  
- <span data-ttu-id="277fa-118">A única maneira que o conteúdo de uma pasta de resultados de pesquisa pode ser modificado é por meio de uma chamada para **definir SetSearchCriteria**.</span><span class="sxs-lookup"><span data-stu-id="277fa-118">The only way that the contents of a search-results folder can be modified is through a call to **SetSearchCriteria**.</span></span> <span data-ttu-id="277fa-119">Para obter mais informações sobre a implementação do **definir SetSearchCriteria**, consulte o artigo [260322: como para pastas de pesquisa com o método definir SetSearchCriteria](https://go.microsoft.com/fwlink/?LinkId=123603).</span><span class="sxs-lookup"><span data-stu-id="277fa-119">For more information about the implementation of **SetSearchCriteria**, see Knowledge Base article [260322: How To Search Folders with the SetSearchCriteria Method](https://go.microsoft.com/fwlink/?LinkId=123603).</span></span>
    
- <span data-ttu-id="277fa-120">As mensagens não podem ser movidas ou copiadas em pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="277fa-120">Messages cannot be moved or copied into search-results folders.</span></span>
    
- <span data-ttu-id="277fa-121">Pastas de resultados de pesquisa não podem conter subpastas.</span><span class="sxs-lookup"><span data-stu-id="277fa-121">Search-results folders cannot contain subfolders.</span></span> 
    
- <span data-ttu-id="277fa-122">Os clientes não podem fazer uma pasta de resultados de pesquisa o assunto de uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="277fa-122">Clients cannot make a search-results folder the subject of a search.</span></span>
    
<span data-ttu-id="277fa-123">No entanto, é possível, para modificar as propriedades de uma pasta de resultados de pesquisa e usá-lo para excluir uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="277fa-123">It is possible, however, to modify the properties of a search-results folder and use it to delete a message.</span></span> <span data-ttu-id="277fa-124">Quando uma mensagem é excluída de uma pasta de resultados de pesquisa, ser realmente excluído da pasta real.</span><span class="sxs-lookup"><span data-stu-id="277fa-124">When a message is deleted from a search-results folder, it is actually deleted from the real folder.</span></span> <span data-ttu-id="277fa-125">No entanto, excluindo a própria pasta de resultados de pesquisa tem nenhum impacto sobre as mensagens dentro; eles permanecem em suas pastas genéricas.</span><span class="sxs-lookup"><span data-stu-id="277fa-125">However, deleting the search-results folder itself has no impact on the messages inside; they remain in their generic folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="277fa-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="277fa-126">See also</span></span>



[<span data-ttu-id="277fa-127">Pastas MAPI</span><span class="sxs-lookup"><span data-stu-id="277fa-127">MAPI Folders</span></span>](mapi-folders.md)

