---
title: Criar uma lista de distribuição
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f37338209ea468d0143dfd1063c3c57216bc13ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359651"
---
# <a name="create-a-distribution-list"></a><span data-ttu-id="3e0a8-102">Criar uma lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="3e0a8-102">Create a distribution list</span></span>

<span data-ttu-id="3e0a8-103">Este exemplo mostra como criar uma lista de distribuição e exibi-la ao usuário.</span><span class="sxs-lookup"><span data-stu-id="3e0a8-103">This example shows how to create a distribution list and display it to the user.</span></span>

## <a name="example"></a><span data-ttu-id="3e0a8-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3e0a8-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="3e0a8-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="3e0a8-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="3e0a8-106">No exemplo de código a seguir, CreateDistributionList cria uma lista de distribuição chamando o método [CreateItem (OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) para criar um objeto [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3e0a8-106">In the following code example, CreateDistributionList creates a distribution list by calling the [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) method to create a [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)) object.</span></span> <span data-ttu-id="3e0a8-107">Em seguida, ele cria um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) e chama o método [GetTable (Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) para localizar todos os contatos na pasta Contatos padrão para os quais o valor da propriedade [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) é "Top Customer" e o valor da propriedade [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) não está vazio.</span><span class="sxs-lookup"><span data-stu-id="3e0a8-107">Next it creates a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, and calls the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) method to find all contacts in the default Contacts folder for which the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property value is “Top Customer” and the [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) property value is not empty.</span></span> <span data-ttu-id="3e0a8-108">Depois que todos os contatos são identificados, o nome **Email1Address** é adicionado como uma coluna à **Table**.</span><span class="sxs-lookup"><span data-stu-id="3e0a8-108">Once all contacts are identified, the **Email1Address** name is added as a column to the **Table**.</span></span> <span data-ttu-id="3e0a8-109">CreateDistributionList cria um objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) usando o método [CreateRecipient (String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3e0a8-109">CreateDistributionList then creates a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object by using the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) method from the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="3e0a8-110">CreateDistributionList finalmente exibe a lista de distribuição "Top Customers" para o usuário.</span><span class="sxs-lookup"><span data-stu-id="3e0a8-110">CreateDistributionList finally displays the “Top Customers” distribution list to the user.</span></span>

> [!NOTE] 
> <span data-ttu-id="3e0a8-111">Você deve passar um objeto **Recipient** resolvido como um parâmetro para o método [AddMember (Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) do objeto [DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15)).</span><span class="sxs-lookup"><span data-stu-id="3e0a8-111">You must pass a resolved **Recipient** object as a parameter to the [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) method of the [DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15)) object.</span></span> <span data-ttu-id="3e0a8-112">Para resolver um objeto **Recipient**, use o método [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)).</span><span class="sxs-lookup"><span data-stu-id="3e0a8-112">To resolve a **Recipient** object, use the [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)) method.</span></span>

<span data-ttu-id="3e0a8-113">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="3e0a8-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3e0a8-114">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="3e0a8-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3e0a8-115">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="3e0a8-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateDistributionList()
{
    Outlook.DistListItem distList = Application.CreateItem(
        Outlook.OlItemType.olDistributionListItem)
        as Outlook.DistListItem;
    distList.Subject = "Top Customers";
    //Find top customer category in Contacts folder
    string filter = "[Categories] = 'Top Customer'"
        + " AND [Email1Address] <> ''";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderContacts).
        GetTable(filter, Outlook.OlTableContents.olUserItems);
    table.Columns.Add("Email1Address");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Outlook.Recipient recip =
            Application.Session.CreateRecipient(
            nextRow["Email1Address"].ToString());
        //Resolve the Recipient before calling AddMember
        recip.Resolve();
        distList.AddMember(recip);
    }
    distList.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="3e0a8-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e0a8-116">See also</span></span>

- [<span data-ttu-id="3e0a8-117">Usuários do Exchange</span><span class="sxs-lookup"><span data-stu-id="3e0a8-117">Exchange users</span></span>](exchange-users.md)

