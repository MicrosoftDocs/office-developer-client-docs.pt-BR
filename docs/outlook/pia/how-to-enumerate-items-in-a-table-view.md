---
title: Enumerar itens em um modo de exibição de tabela
TOCTitle: Enumerate items in a table view
ms:assetid: c7d9a667-cfec-49c1-af7a-4c8063991588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184640(v=office.15)
ms:contentKeyID: 55119900
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: fbb3b6aa9bed2e08eb11cb58090233d271e5fed3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406446"
---
# <a name="enumerate-items-in-a-table-view"></a><span data-ttu-id="dba75-102">Enumerar itens em um modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="dba75-102">Enumerate items in a table view</span></span>

<span data-ttu-id="dba75-103">Este exemplo enumera itens em um modo de exibição de tabela usando o método [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="dba75-103">This example enumerates items in a table view by using the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="dba75-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dba75-104">Example</span></span>

<span data-ttu-id="dba75-105">O exemplo de código a seguir obtém um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) do modo de exibição atual da pasta Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="dba75-105">The following code example obtains a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object from the current view of the Inbox folder.</span></span> <span data-ttu-id="dba75-106">O exemplo de código define a pasta atual do explorador ativo à Caixa de Entrada e, em seguida, verifica se o modo de exibição atual da Caixa de Entrada é um modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="dba75-106">The code sample sets the current folder of the active explorer to the Inbox, and then checks that the current view of the Inbox is a table view.</span></span> <span data-ttu-id="dba75-107">Se o modo de exibição atual for uma tabela, o exemplo de código chamará o método [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) e exibirá cada item representado por cada linha no objeto **Table** retornado.</span><span class="sxs-lookup"><span data-stu-id="dba75-107">If the current view is a table, the code example calls the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method and displays each item represented by each row in the returned **Table**.</span></span>

<span data-ttu-id="dba75-108">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="dba75-108">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="dba75-109">A instrução **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="dba75-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="dba75-110">A seguinte linha de código mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="dba75-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoViewGetTable()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder
    // for View.GetTable to work correctly.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType == 
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view = 
            inbox.CurrentView as Outlook.TableView;
        // No arguments needed for View.GetTable.
        Outlook.Table table = view.GetTable();
        Debug.WriteLine("View Count=" 
            + table.GetRowCount().ToString());
        while (!table.EndOfTable)
        {
            // First row in Table.
            Outlook.Row nextRow = table.GetNextRow();
            Debug.WriteLine(nextRow["Subject"]
                + " Modified: "
                + nextRow["LastModificationTime"]);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="dba75-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="dba75-111">See also</span></span>

- [<span data-ttu-id="dba75-112">Modos de exibição</span><span class="sxs-lookup"><span data-stu-id="dba75-112">Views</span></span>](views.md)

