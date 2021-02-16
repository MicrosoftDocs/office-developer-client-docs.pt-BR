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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342757"
---
# <a name="search-and-obtain-items-in-an-aggregated-view"></a>Pesquisar e obter itens em um modo de exibição agregado

Este exemplo mostra como pesquisar itens em várias pastas e lojas e retornar os itens em um modo de exibição de tabela agregado.

## <a name="example"></a>Exemplo

O método [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) do objeto [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) pode retornar, em uma exibição agregada, um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) que contém itens de uma ou mais pastas na mesma loja ou que distribuídos em várias lojas. Isso é particularmente útil quando você quer acessar itens retornados de uma pesquisa (por exemplo, uma pesquisa em todos os itens de email de uma loja). Este tópico mostra um exemplo de como usar a **Pesquisa Instantânea** para pesquisar todos os itens recebidos do gerente do usuário atual marcados como importantes, e depois exibir o assunto da cada resultado da pesquisa.

No exemplo de código a seguir, o método **GetItemsInView** verifica se a conta principal da loja de entrega do usuário atual é uma conta Exchange, se o usuário atual tem um gerente e se a **Pesquisa Instantânea** está operando na loja padrão da sessão. Como a pesquisa depende do método de [Pesquisa](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) do objeto do [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)), e o resultado da pesquisa é obtido pelo uso do método **GetTable**, o **GetItemsInView** criar um objeto do **Explorer**, exibe a Caixa de Entrada neste objeto e o utiliza para configurar a pesquisa. 

**GetItemsInView** pesquisa todas as pastas do tipo [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) do gerente do usuário atual marcadas como importantes. Depois de **GetItemsInView** chamar método de [Pesquisa](https://msdn.microsoft.com/library/bb610561\(v=office.15\)), todos os resultados de pesquisa que houver serão exibidos no Explorer, incluindo os itens de outras pastas e lojas que se encaixam nos critérios da pesquisa. **GetItemsInView** obtém um objeto **TableView** que contém este modo de exibição do Explorer dos resultados da pesquisa. Usando o método **GetTable** deste objeto **TableView**, **GetItemsInView** obtém um objeto **Table** que contém os itens agregados retornados da pesquisa. Por fim **GetItemsInView** exibe a coluna de assunto de cada linha do objeto **Table** que representa um item nos resultados da pesquisa.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Pesquisar e filtrar](search-and-filter.md)

