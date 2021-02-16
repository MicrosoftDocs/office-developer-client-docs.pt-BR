---
title: Usar buscas instantâneas para pesquisar uma frase do assunto em todas as pastas e todas as lojas.
TOCTitle: Use instant search to search all folders and all stores for a phrase in the subject
ms:assetid: d3152bfa-6e7d-4b68-8c7e-e2e155a92b49
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424478(v=office.15)
ms:contentKeyID: 55119923
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 07b0ba7a1d488dc1c7e1fcf0e9ae487b04b88755
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335368"
---
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a><span data-ttu-id="85e7d-102">Usar buscas instantâneas para pesquisar uma frase do assunto em todas as pastas e todas as lojas.</span><span class="sxs-lookup"><span data-stu-id="85e7d-102">Use instant search to search all folders and all stores for a phrase in the subject</span></span>

<span data-ttu-id="85e7d-103">Este exemplo usa a pesquisa instantânea para pesquisar uma frase do assunto em todas as pastas e todos os armazenamentos e exibir os itens em uma janela de navegador.</span><span class="sxs-lookup"><span data-stu-id="85e7d-103">This example uses Instant Search to search all folders and all stores for a phrase in the subject, and then displays the items in an explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="85e7d-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="85e7d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="85e7d-105">O exemplo a seguir é um trecho da [programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="85e7d-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="85e7d-106">A pesquisa instantânea é um recurso do Microsoft Outlook que permite pesquisar, emitindo consultas que retornam os resultados com base no conteúdo.</span><span class="sxs-lookup"><span data-stu-id="85e7d-106">Instant Search is a feature of Microsoft Outlook that enables you to search by issuing queries that return results based on the content.</span></span> <span data-ttu-id="85e7d-107">Depois que sua consulta foi processada, os resultados podem ser retornados em uma variedade de objetos, incluindo o objeto[tabela](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), o conjunto de [itens](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) e o objeto [pesquisa](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) objeto.</span><span class="sxs-lookup"><span data-stu-id="85e7d-107">Once your query has been processed, the results can be returned in a variety of objects, including the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection, and the [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="85e7d-108">Você pode escrever o código que usa a pesquisa instantânea com a Sintaxe de Consulta Avançada (AQS) oferecida pela Microsoft Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="85e7d-108">You can write code that uses Instant Search by using the Advanced Query Syntax (AQS) that is offered by Microsoft Windows Desktop Search.</span></span> <span data-ttu-id="85e7d-109">AQS é um dos três idiomas de consulta que o Outlook dá suporte.</span><span class="sxs-lookup"><span data-stu-id="85e7d-109">AQS is one of three query languages that Outlook supports.</span></span> <span data-ttu-id="85e7d-110">É poderosa, mas é limitada à [pesquisa (cadeia de caracteres, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) método do objeto[Explorador](https://msdn.microsoft.com/library/bb623678\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="85e7d-110">It is powerful, but limited to the [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method of the [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object.</span></span> <span data-ttu-id="85e7d-111">É possível usar a AQS para fornecer uma restrição para **tabela** ou para os objetos do **Item**.</span><span class="sxs-lookup"><span data-stu-id="85e7d-111">You cannot use AQS to provide a restriction for **Table** or **Item** objects.</span></span> <span data-ttu-id="85e7d-112">Além disso, os resultados retornados por uma consulta AQS podem ser exibidos apenas na interface de usuário do Outlook.</span><span class="sxs-lookup"><span data-stu-id="85e7d-112">In addition, the results returned by an AQS query can be displayed only in the Outlook user interface.</span></span> <span data-ttu-id="85e7d-113">A tabela a seguir lista os três idiomas de consulta suportados pelo Outlook; No entanto, este tópico irá ilustrar somente o uso de AQS.</span><span class="sxs-lookup"><span data-stu-id="85e7d-113">The following table lists the three query languages that Outlook supports; however, this topic will illustrate the use of only AQS.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85e7d-114">Linguagem de consulta</span><span class="sxs-lookup"><span data-stu-id="85e7d-114">Query language</span></span></p></th>
<th><p><span data-ttu-id="85e7d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="85e7d-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85e7d-116">AQS</span><span class="sxs-lookup"><span data-stu-id="85e7d-116">AQS</span></span></p></td>
<td><p><span data-ttu-id="85e7d-117">A AQS é usada pelo Windows Desktop Search e é a linguagem de consulta para o recurso de pesquisa instantânea do Outlook.</span><span class="sxs-lookup"><span data-stu-id="85e7d-117">AQS is used by Windows Desktop Search and is the query language for the Instant Search feature in Outlook.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e7d-118">DASL</span><span class="sxs-lookup"><span data-stu-id="85e7d-118">DASL</span></span></p></td>
<td><p><span data-ttu-id="85e7d-119">A linguagem de pesquisa DAV para consulta e localização (DASL) se baseia na implementação do Microsoft Exchange DASL no Outlook.</span><span class="sxs-lookup"><span data-stu-id="85e7d-119">DAV Search and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook.</span></span> <span data-ttu-id="85e7d-120">A DASL pode ser usada para retornar resultados no objeto <b>tabela</b>.</span><span class="sxs-lookup"><span data-stu-id="85e7d-120">DASL can be used to return results in the <b>Table</b> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e7d-121">Jet</span><span class="sxs-lookup"><span data-stu-id="85e7d-121">Jet</span></span></p></td>
<td><p><span data-ttu-id="85e7d-122">A linguagem de consulta Jet fornece uma linguagem de consulta simples para Outlook e com base no serviço Microsoft Jet Expression.</span><span class="sxs-lookup"><span data-stu-id="85e7d-122">Jet query language provides a simple query language for Outlook, and is based on the Microsoft Jet Expression Service.</span></span> <span data-ttu-id="85e7d-123">Jet é usado para criar cadeias de caracteres de filtro para os métodos <b>restringir</b>, coleção de<b>itens</b>e o objeto <b>tabela</b>.</span><span class="sxs-lookup"><span data-stu-id="85e7d-123">Jet is used to create filter strings for the <b>Restrict</b> methods of the <b>Items</b> collection and the <b>Table</b> object.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="85e7d-124">No exemplo de código a seguir, o DemoInstantSearch obtém todas as pastas de email de todas as lojas onde a indexação é habilitada usando a propriedade [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) do objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="85e7d-124">In the following code example, DemoInstantSearch gets all mail folders in all stores where indexing is enabled by using the [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) property of the [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object.</span></span> <span data-ttu-id="85e7d-125">Ele usa o método **pesquisa** do objeto **Explorer** para filtrar por todos os itens que contêm a frase exata "Office 2007" no assunto e que foram recebidas no mês passado.</span><span class="sxs-lookup"><span data-stu-id="85e7d-125">It then uses the **Search** method of the **Explorer** object to filter for all items that contain the exact phrase “Office 2007” in the subject and that have been received in the last month.</span></span> <span data-ttu-id="85e7d-126">Por fim, os resultados da pesquisa são exibidos em uma janela separada do Explorer.</span><span class="sxs-lookup"><span data-stu-id="85e7d-126">The results of the search are finally displayed in a separate explorer window.</span></span>

<span data-ttu-id="85e7d-127">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="85e7d-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="85e7d-128">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="85e7d-128">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="85e7d-129">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="85e7d-129">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoInstantSearch()
{
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        Outlook.Explorer explorer = Application.Explorers.Add(
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            as Outlook.Folder,
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        string filter = "subject:" +
            "\"" + "Office 2007" + "\"" +
            " received:(last month)";
        explorer.Search(filter,
            Outlook.OlSearchScope.olSearchScopeAllFolders);
        explorer.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="85e7d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="85e7d-130">See also</span></span>

- [<span data-ttu-id="85e7d-131">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="85e7d-131">Search and filter</span></span>](search-and-filter.md)

