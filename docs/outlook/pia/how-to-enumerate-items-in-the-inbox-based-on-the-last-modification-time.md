---
title: Enumerar itens na Caixa de Entrada baseada na hora da última modificação
TOCTitle: Enumerate items in the Inbox based on the last modification time
ms:assetid: 93a25143-def6-4832-bac2-3744558c2736
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184626(v=office.15)
ms:contentKeyID: 55119920
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: ecc4ed8f2fb207b8952fef41481738dd8be0ee02
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406040"
---
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a><span data-ttu-id="72f01-102">Enumerar itens na Caixa de Entrada baseada na hora da última modificação</span><span class="sxs-lookup"><span data-stu-id="72f01-102">Enumerate items in the Inbox based on the last modification time</span></span>

<span data-ttu-id="72f01-103">Este exemplo mostra como enumerar itens na pasta Caixa de Entrada com base na hora da última modificação.</span><span class="sxs-lookup"><span data-stu-id="72f01-103">This example shows how to enumerate items in the Inbox folder based on the last modification time.</span></span>

## <a name="example"></a><span data-ttu-id="72f01-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="72f01-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="72f01-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="72f01-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="72f01-106">O objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa um conjunto de itens de um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="72f01-106">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of items from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="72f01-107">Para obter uma **Table**, chame o método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) em um objeto **Folder** ou **Search**.</span><span class="sxs-lookup"><span data-stu-id="72f01-107">To obtain a **Table**, call the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on a **Folder** or **Search** object.</span></span> <span data-ttu-id="72f01-108">Cada item na **Table** retornada contém apenas um subconjunto padrão das propriedades do item.</span><span class="sxs-lookup"><span data-stu-id="72f01-108">By default, each item in the returned **Table** contains only a default subset of its properties.</span></span> <span data-ttu-id="72f01-109">Cada objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) pode ser considerado como um item na pasta, e cada objeto [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) como uma propriedade de um item.</span><span class="sxs-lookup"><span data-stu-id="72f01-109">Each [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object can be regarded as an item in the folder, and each [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object as a property of an item.</span></span> <span data-ttu-id="72f01-110">Não há suporte para remover, adicionar ou alterar linhas em **Table**.</span><span class="sxs-lookup"><span data-stu-id="72f01-110">Removing, adding, or changing rows is not supported in the **Table**.</span></span> <span data-ttu-id="72f01-111">Para enumerar itens em uma **Table**, use a propriedade [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) para ver se sua posição atual está no fim da tabela.</span><span class="sxs-lookup"><span data-stu-id="72f01-111">To enumerate items in a **Table**, first use the [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) property to see whether your current position is at the end of the table.</span></span> <span data-ttu-id="72f01-112">Se **EndOfTable** retornar **false**, use o método [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) para retornar uma **Row**, que contém um número padrão de objetos **Column**.</span><span class="sxs-lookup"><span data-stu-id="72f01-112">If **EndOfTable** returns **false**, use the [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) method to return a **Row**, which contains a default number of **Column** objects.</span></span> <span data-ttu-id="72f01-113">Continue a iteração de forma ininterrupta por meio de \*\*Table \*\* chamando **GetNextRow** até **EndOfTable** retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="72f01-113">You continue iterating in a forward manner through the **Table** by calling **GetNextRow** until **EndOfTable** returns **true**.</span></span>

<span data-ttu-id="72f01-114">No exemplo de código a seguir, DemoTableForInbox obtém um objeto **Table** para a pasta Caixa de Entrada, classifica o objeto **Table** usando a propriedade **LastModificationTime** e o método [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)), iterando a tabela para escrever o assunto de cada item para o rastreamento de assunto de cada item para os ouvintes de rastreamento do conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="72f01-114">In the following code example, DemoTableForInbox obtains a **Table** object for the Inbox folder, sorts the **Table** object by using the **LastModificationTime** property and [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)) method, and iterates through the table to write the subject of each item to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="72f01-115">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="72f01-115">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="72f01-116">O \*\* que usa a instrução\*\* não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="72f01-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="72f01-117">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="72f01-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTableForInbox()
{
    //Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    //Obtain Table using defaults
    Outlook.Table table =
        folder.GetTable(Type.Missing, Type.Missing);
    table.Sort("LastModificationTime",
        Outlook.OlSortOrder.olDescending);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="72f01-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="72f01-118">See also</span></span>

- [<span data-ttu-id="72f01-119">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="72f01-119">Search and Filter</span></span>](search-and-filter.md)

