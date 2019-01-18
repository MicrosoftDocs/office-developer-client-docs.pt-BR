---
title: Usar SetColumns para enumerar itens de forma eficiente em uma pasta
TOCTitle: Use SetColumns to efficiently enumerate items in a folder
ms:assetid: cd7c7758-8a9c-4f1c-a49c-9305d75be341
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184641(v=office.15)
ms:contentKeyID: 55119921
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bdfccc6432d35b6f39564e4c87404cc57b6ea27e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708085"
---
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="fae49-102">Usar SetColumns para enumerar itens de forma eficiente em uma pasta</span><span class="sxs-lookup"><span data-stu-id="fae49-102">Use SetColumns to efficiently enumerate items in a folder</span></span>

<span data-ttu-id="fae49-103">Este exemplo mostra como melhorar o desempenho da enumeração do conjunto [Itens](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) usando o método [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) para armazenar em cache determinadas propriedades de cada item no conjunto.</span><span class="sxs-lookup"><span data-stu-id="fae49-103">This example shows how to improve the performance of enumerating the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection by using the [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) method to cache certain properties of each item in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="fae49-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fae49-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fae49-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="fae49-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="fae49-106">Para enumerar itens em uma coleção, use o método **SetColumns** para armazenar em cache as propriedades na coleção **Items**.</span><span class="sxs-lookup"><span data-stu-id="fae49-106">To enumerate items in a collection, use the **SetColumns** method to cache properties on the **Items** collection.</span></span> <span data-ttu-id="fae49-107">**SetColumns** recebe um argumento que é uma cadeia de caracteres delimitada por vírgula que representa os nomes das propriedades.</span><span class="sxs-lookup"><span data-stu-id="fae49-107">**SetColumns** takes an argument that is a comma-delimited string that represents property names.</span></span> <span data-ttu-id="fae49-108">Depois que todos os itens da coleção tiverem sido enumerados, chame o método [ResetColumns ()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) para limpar o cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="fae49-108">Once all items in the collection have been enumerated, call the [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) method to clear the property cache.</span></span>

<span data-ttu-id="fae49-109">No exemplo de código a seguir, EnumerateContactsWithSetColumns usa o método **SetColumns** para armazenar em cache as propriedades [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) e [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) dos itens na pasta Contatos.</span><span class="sxs-lookup"><span data-stu-id="fae49-109">In the following code example, EnumerateContactsWithSetColumns uses the **SetColumns** method to cache the [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), and [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) properties of items in the Contacts folder.</span></span> <span data-ttu-id="fae49-110">Observe que você deve fazer testes em busca de cadeias de caracteres vazias ou uma referência nula na restrição.</span><span class="sxs-lookup"><span data-stu-id="fae49-110">Note that you must test for empty strings or a null reference in the restriction.</span></span>

<span data-ttu-id="fae49-111">Observe que uma pasta do Outlook pode conter itens de tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="fae49-111">Note that an Outlook folder can possibly contain items of different types.</span></span> <span data-ttu-id="fae49-112">Esta amostra de código faz uso da classe auxiliar OutlookItem, definida em [Criar uma classe auxiliar para acessar membros comuns de itens do Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), para chamar convenientemente a propriedade OutlookItem.Class para verificar a classe de mensagem de cada item no subconjunto filtrado de itens na pasta, antes de definir o item como um item de contato.</span><span class="sxs-lookup"><span data-stu-id="fae49-112">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.Class property to verify the message class of each item in the filtered subset of items in the folder, before assuming the item is a contact item.</span></span>

<span data-ttu-id="fae49-113">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="fae49-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="fae49-114">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="fae49-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="fae49-115">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="fae49-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateContactsWithSetColumns()
{
    // Obtain Contacts folder
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    string filter = "Not([CompanyName] Is Null)" +
        " AND Not([JobTitle] Is Null)";
    Outlook.Items items = folder.Items.Restrict(filter);
    items.SetColumns("FileAs, CompanyName, JobTitle");
    for (int i = 1; i <= items.Count; i++)
    {
        // Create an instance of OutlookItem
        OutlookItem myItem = new OutlookItem(items[i]);
        if (myItem.Class == Outlook.OlObjectClass.olContact)
        {
            // Use InnerObject to return ContactItem
            Outlook.ContactItem contact =
                myItem.InnerObject as Outlook.ContactItem;
            StringBuilder sb = new StringBuilder();
            sb.AppendLine(contact.FileAs);
            sb.AppendLine(contact.CompanyName);
            sb.AppendLine(contact.JobTitle);
            sb.AppendLine();
            Debug.WriteLine(sb.ToString());
        }
    }
    items.ResetColumns();
}
```

## <a name="see-also"></a><span data-ttu-id="fae49-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="fae49-116">See also</span></span>

- [<span data-ttu-id="fae49-117">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="fae49-117">Search and filter</span></span>](search-and-filter.md)

