---
title: Enumerar itens ocultos em uma pasta
TOCTitle: Enumerate hidden items in a folder
ms:assetid: dafad1fb-94ce-4584-b5d1-2de5fad2f72a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184645(v=office.15)
ms:contentKeyID: 55119888
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6508ea955ad74b49b5fef73352b4a1706d8e338c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357404"
---
# <a name="enumerate-hidden-items-in-a-folder"></a><span data-ttu-id="2ea88-102">Enumerar itens ocultos em uma pasta</span><span class="sxs-lookup"><span data-stu-id="2ea88-102">Enumerate hidden items in a folder</span></span>

<span data-ttu-id="2ea88-103">Este exemplo mostra como localizar e enumerar itens ocultos em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="2ea88-103">This example shows how to find and enumerate hidden items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="2ea88-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2ea88-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="2ea88-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="2ea88-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="2ea88-106">Um recurso do objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), que representa um conjunto de itens em uma pasta, é que ele pode ter itens ocultos.</span><span class="sxs-lookup"><span data-stu-id="2ea88-106">One feature of the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, which represents a set of items in a folder, is that it may have hidden items.</span></span> <span data-ttu-id="2ea88-107">Para retornar itens ocultos em uma pasta, defina o parâmetro *TableContents* no método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) do objeto [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) para [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="2ea88-107">To return hidden items in a folder, set the *TableContents* parameter in the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object to [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)).</span></span> <span data-ttu-id="2ea88-108">No exemplo de código a seguir, TableForInboxHiddenItems obtém os itens ocultos de uma pasta Caixa de Entrada e grava os valores das propriedades [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) e [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\)) de cada item oculto nos ouvintes de rastreamento da coleção [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="2ea88-108">In the following code example, TableForInboxHiddenItems obtains the hidden items of an Inbox folder, and writes the values of the [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) and [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\)) properties for each hidden item to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="2ea88-109">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="2ea88-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="2ea88-110">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="2ea88-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="2ea88-111">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="2ea88-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableForInboxHiddenItems()
{
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with OlTableContents.olHiddenItems
    Outlook.Table table =
        folder.GetTable("",
        Outlook.OlTableContents.olHiddenItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        // Test for null subject
        if (nextRow["Subject"] == null)
        {
            Debug.WriteLine(nextRow["MessageClass"]);
        }
        else
        {
            Debug.WriteLine(nextRow["Subject"] + " "
                + nextRow["MessageClass"]);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="2ea88-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ea88-112">See also</span></span>

<span data-ttu-id="2ea88-113">-[Pesquisar e filtrar](search-and-filter.md)</span><span class="sxs-lookup"><span data-stu-id="2ea88-113">-[Search and filter](search-and-filter.md)</span></span>

