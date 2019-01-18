---
title: Pesquisar e obter itens em um modo de exibição agregado
TOCTitle: Search and obtain items in an aggregated view
ms:assetid: 1a875dc8-dd52-4e9c-b292-5f6ba3d7a940
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184592(v=office.15)
ms:contentKeyID: 55119925
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92f99069dae2976a00ac075f605754fe8704ae60
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704384"
---
# <a name="search-and-obtain-items-in-an-aggregated-view"></a><span data-ttu-id="4c82b-102">Pesquisar e obter itens em um modo de exibição agregado</span><span class="sxs-lookup"><span data-stu-id="4c82b-102">Search and obtain items in an aggregated view</span></span>

<span data-ttu-id="4c82b-103">Este exemplo mostra como pesquisar itens em várias pastas e lojas e retornar os itens em um modo de exibição de tabela agregado.</span><span class="sxs-lookup"><span data-stu-id="4c82b-103">This example shows how to search for items in multiple folders and stores and to return those items in an aggregated table view.</span></span>

## <a name="example"></a><span data-ttu-id="4c82b-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4c82b-104">Example</span></span>

<span data-ttu-id="4c82b-105">O método [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) do objeto [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) pode retornar, em uma exibição agregada, um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) que contém itens de uma ou mais pastas na mesma loja ou que distribuídos em várias lojas.</span><span class="sxs-lookup"><span data-stu-id="4c82b-105">The [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method of the [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) object can return, in an aggregated view, a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object that contains items from one or more folders in the same store or spanning over multiple stores.</span></span> <span data-ttu-id="4c82b-106">Isso é particularmente útil quando você quer acessar itens retornados de uma pesquisa (por exemplo, uma pesquisa em todos os itens de email de uma loja).</span><span class="sxs-lookup"><span data-stu-id="4c82b-106">This is particularly useful when you want to access items returned from a search (for example, a search on all mail items in a store).</span></span> <span data-ttu-id="4c82b-107">Este tópico mostra um exemplo de como usar a **Pesquisa Instantânea** para pesquisar todos os itens recebidos do gerente do usuário atual marcados como importantes, e depois exibir o assunto da cada resultado da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4c82b-107">This topic shows an example of how to use **Instant Search** to search for all items received from the manager of the current user that are marked important, and then display the subject of each search result.</span></span>

<span data-ttu-id="4c82b-108">No exemplo de código a seguir, o método **GetItemsInView** verifica se a conta principal da loja de entrega do usuário atual é uma conta Exchange, se o usuário atual tem um gerente e se a **Pesquisa Instantânea** está operando na loja padrão da sessão.</span><span class="sxs-lookup"><span data-stu-id="4c82b-108">In the following code example, the **GetItemsInView** method checks whether the current user’s primary delivery store account is an Exchange account, whether the current user has a manager, and whether **Instant Search** is operational in the default store of the session.</span></span> <span data-ttu-id="4c82b-109">Como a pesquisa depende do método de [Pesquisa](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) do objeto do [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)), e o resultado da pesquisa é obtido pelo uso do método **GetTable**, o **GetItemsInView** criar um objeto do **Explorer**, exibe a Caixa de Entrada neste objeto e o utiliza para configurar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4c82b-109">Because the search relies on the [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method of the [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object, and the search result is obtained by using the **GetTable** method, **GetItemsInView** creates an **Explorer** object, displays the Inbox in this object, and uses it to set up the search.</span></span> 

<span data-ttu-id="4c82b-110">**GetItemsInView** pesquisa todas as pastas do tipo [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) do gerente do usuário atual marcadas como importantes.</span><span class="sxs-lookup"><span data-stu-id="4c82b-110">**GetItemsInView** searches all folders of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) type for items from the current user's manager that are marked as important.</span></span> <span data-ttu-id="4c82b-111">Depois de **GetItemsInView** chamar método de [Pesquisa](https://msdn.microsoft.com/library/bb610561\(v=office.15\)), todos os resultados de pesquisa que houver serão exibidos no Explorer, incluindo os itens de outras pastas e lojas que se encaixam nos critérios da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4c82b-111">After **GetItemsInView** calls the [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method, any search results are displayed in the Explorer, including items from other folders and stores that meet the search criteria.</span></span> <span data-ttu-id="4c82b-112">**GetItemsInView** obtém um objeto\*\* TableView\*\* que contém este modo de exibição do Explorer dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4c82b-112">**GetItemsInView** gets a **TableView** object that contains this explorer view of the search results.</span></span> <span data-ttu-id="4c82b-113">Usando o método **GetTable** deste objeto **TableView**, **GetItemsInView** obtém um objeto **Table** que contém os itens agregados retornados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4c82b-113">By using the **GetTable** method of this **TableView** object, **GetItemsInView** then gets a **Table** object that contains the aggregated items returned from the search.</span></span> <span data-ttu-id="4c82b-114">Por fim **GetItemsInView** exibe a coluna de assunto de cada linha do objeto **Table** que representa um item nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4c82b-114">Finally **GetItemsInView** displays the subject column of each row of the **Table** object that represents an item in the search results.</span></span>

<span data-ttu-id="4c82b-115">Se usar o Visual Studio para testar este exemplo de código, você precisa primeiro adicionar uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especificar a variável do Outlook quando você importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="4c82b-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="4c82b-116">O \*\* que usa a instrução\*\* não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="4c82b-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="4c82b-117">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="4c82b-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetItemsInView()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;

    // Check whether the current user uses the Exchange Server.
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();

        // Check whether the current user has a manager.
        if (manager != null)
        {
            string managerName = manager.Name;

            // Check whether Instant Search is enabled and 
            // operational in the default store.
            if (Application.Session.DefaultStore.IsInstantSearchEnabled)
            {
                Outlook.Folder inbox =
                    Application.Session.GetDefaultFolder(
                    Outlook.OlDefaultFolders.olFolderInbox);

                // Create a new explorer to display the Inbox as
                // the current folder.
                Outlook.Explorer explorer =
                    Application.Explorers.Add(inbox,
                    Outlook.OlFolderDisplayMode.olFolderDisplayNormal);

                // Make the new explorer visible.
                explorer.Display;

                // Search for items from the manager marked important, 
                // from all folders of the same item type as the current folder, 
                // which is the MailItem item type.
                string searchFor =
                    "from:" + "\"" + managerName 
                    + "\"" + " importance:high";
                explorer.Search(searchFor,
                    Outlook.OlSearchScope.olSearchScopeAllFolders);

                // Any search results are displayed in that new explorer
                // in an aggregated table view.
                Outlook.TableView tableView = 
                    explorer.CurrentView as Outlook.TableView;

                // Use GetTable of that table view to obtain items in that
                // aggregated view in a Table object.
                Outlook.Table table = tableView.GetTable();
                while (!table.EndOfTable)
                {
                    // Then display each row in the Table object
                    // that represents an item in the search results.
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="4c82b-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c82b-118">See also</span></span>

- [<span data-ttu-id="4c82b-119">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="4c82b-119">Search and filter</span></span>](search-and-filter.md)

