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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357670"
---
# <a name="mapi-search-folders"></a><span data-ttu-id="06c5a-103">Pastas de pesquisa MAPI</span><span class="sxs-lookup"><span data-stu-id="06c5a-103">MAPI Search Folders</span></span>

  
  
<span data-ttu-id="06c5a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06c5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06c5a-105">Uma pasta de resultados de pesquisa contém links para mensagens em pastas genéricas, em vez de mensagens reais.</span><span class="sxs-lookup"><span data-stu-id="06c5a-105">A search-results folder holds links to messages in generic folders rather than the actual messages.</span></span> <span data-ttu-id="06c5a-106">Os clientes criam uma pasta de resultados de pesquisa chamando o método [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) com FOLDER_SEARCH como o parâmetro _ulFolderType_ .</span><span class="sxs-lookup"><span data-stu-id="06c5a-106">Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter.</span></span> <span data-ttu-id="06c5a-107">Os clientes preenchem uma pasta de resultados de pesquisa Configurando e aplicando critérios de pesquisa — regras que filtram mensagens com características específicas.</span><span class="sxs-lookup"><span data-stu-id="06c5a-107">Clients fill a search-results folder by setting up and applying search criteria — rules that filter out messages with particular characteristics.</span></span> <span data-ttu-id="06c5a-108">Os critérios de pesquisa são configurados com o método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="06c5a-108">Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> <span data-ttu-id="06c5a-109">Os clientes criam uma ou mais estruturas [SRestriction](srestriction.md) para representar os critérios de pesquisa a serem aplicados e passá-los para o **SetSearchCriteria**.</span><span class="sxs-lookup"><span data-stu-id="06c5a-109">Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**.</span></span> <span data-ttu-id="06c5a-110">**SetSearchCriteria** também especifica uma lista de pastas que indicam o domínio de pesquisa e um conjunto de sinalizadores que controlam como a pesquisa é realizada.</span><span class="sxs-lookup"><span data-stu-id="06c5a-110">**SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed.</span></span> 
  
 <span data-ttu-id="06c5a-111">**SetSearchCriteria** identifica as mensagens que correspondem à restrição especificada.</span><span class="sxs-lookup"><span data-stu-id="06c5a-111">**SetSearchCriteria** identifies the messages that match the specified restriction.</span></span> <span data-ttu-id="06c5a-112">As mensagens selecionadas (as que satisfazem os critérios) são exibidas como links na pasta Search-Results.</span><span class="sxs-lookup"><span data-stu-id="06c5a-112">The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder.</span></span> <span data-ttu-id="06c5a-113">Quando o cliente chama o método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable para acessar a tabela de conteúdo da pasta de resultados de pesquisa, as mensagens selecionadas são exibidas na tabela.</span><span class="sxs-lookup"><span data-stu-id="06c5a-113">When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table.</span></span> <span data-ttu-id="06c5a-114">As tabelas de conteúdo das pastas de resultados de pesquisa contêm as mesmas colunas que as tabelas de conteúdo para pastas genéricas.</span><span class="sxs-lookup"><span data-stu-id="06c5a-114">Contents tables for search-results folders contain the same columns as contents tables for generic folders.</span></span> <span data-ttu-id="06c5a-115">No enTanto, para pastas de resultados de pesquisa, a propriedade **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) especifica o identificador de entrada da pasta onde a mensagem vinculada reside.</span><span class="sxs-lookup"><span data-stu-id="06c5a-115">However, for search-results folders, the **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property specifies the entry identifier of the folder where the linked message resides.</span></span> <span data-ttu-id="06c5a-116">As pastas de resultados de pesquisa não são consideradas pastas pai.</span><span class="sxs-lookup"><span data-stu-id="06c5a-116">Search-results folders are not considered parent folders.</span></span>
  
<span data-ttu-id="06c5a-117">As pastas de resultados de pesquisa têm os seguintes limites:</span><span class="sxs-lookup"><span data-stu-id="06c5a-117">Search-results folders have the following limits:</span></span>
  
- <span data-ttu-id="06c5a-118">A única maneira de que o conteúdo de uma pasta de resultados de pesquisa pode ser modificado é por meio de uma chamada a **SetSearchCriteria**.</span><span class="sxs-lookup"><span data-stu-id="06c5a-118">The only way that the contents of a search-results folder can be modified is through a call to **SetSearchCriteria**.</span></span> <span data-ttu-id="06c5a-119">Para obter mais informações sobre a implementação do **SetSearchCriteria**, consulte o artigo 260322 da base de dados de conhecimento [: como pesquisar pastas com o método SetSearchCriteria](https://go.microsoft.com/fwlink/?LinkId=123603).</span><span class="sxs-lookup"><span data-stu-id="06c5a-119">For more information about the implementation of **SetSearchCriteria**, see Knowledge Base article [260322: How To Search Folders with the SetSearchCriteria Method](https://go.microsoft.com/fwlink/?LinkId=123603).</span></span>
    
- <span data-ttu-id="06c5a-120">As mensagens não podem ser movidas ou copiadas para pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="06c5a-120">Messages cannot be moved or copied into search-results folders.</span></span>
    
- <span data-ttu-id="06c5a-121">Search-Result Folders não podem conter subpastas.</span><span class="sxs-lookup"><span data-stu-id="06c5a-121">Search-results folders cannot contain subfolders.</span></span> 
    
- <span data-ttu-id="06c5a-122">Os clientes não podem criar uma pasta de resultados de pesquisa o assunto de uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="06c5a-122">Clients cannot make a search-results folder the subject of a search.</span></span>
    
<span data-ttu-id="06c5a-123">No entanto, é possível modificar as propriedades de uma pasta de resultados de pesquisa e usá-la para excluir uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="06c5a-123">It is possible, however, to modify the properties of a search-results folder and use it to delete a message.</span></span> <span data-ttu-id="06c5a-124">Quando uma mensagem é excluída de uma pasta de resultados de pesquisa, ela é realmente excluída da pasta real.</span><span class="sxs-lookup"><span data-stu-id="06c5a-124">When a message is deleted from a search-results folder, it is actually deleted from the real folder.</span></span> <span data-ttu-id="06c5a-125">No enTanto, excluir a pasta de resultados de pesquisa em si não tem impacto nas mensagens de dentro; Eles permanecem em suas pastas genéricas.</span><span class="sxs-lookup"><span data-stu-id="06c5a-125">However, deleting the search-results folder itself has no impact on the messages inside; they remain in their generic folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06c5a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="06c5a-126">See also</span></span>



[<span data-ttu-id="06c5a-127">Pastas MAPI</span><span class="sxs-lookup"><span data-stu-id="06c5a-127">MAPI Folders</span></span>](mapi-folders.md)

