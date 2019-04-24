---
title: Atribuir categorias a um item
TOCTitle: Assign categories to an item
ms:assetid: 4070801b-994a-46df-91fe-4efca834886e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424469(v=office.15)
ms:contentKeyID: 55119828
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8b94d03a1aea447c4dba859659f044d8ec11994
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359728"
---
# <a name="assign-categories-to-an-item"></a><span data-ttu-id="08586-102">Atribuir categorias a um item</span><span class="sxs-lookup"><span data-stu-id="08586-102">Assign categories to an item</span></span>

<span data-ttu-id="08586-103">Este exemplo mostra como atribuir categorias a um item usando a propriedade **Categories**.</span><span class="sxs-lookup"><span data-stu-id="08586-103">This example shows how to assign categories to an item by using its **Categories** property.</span></span>

## <a name="example"></a><span data-ttu-id="08586-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="08586-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="08586-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="08586-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="08586-106">Para atribuir categorias a um item, use a propriedade **Categories**.</span><span class="sxs-lookup"><span data-stu-id="08586-106">To assign categories to an item, use the particular item's **Categories** property.</span></span> <span data-ttu-id="08586-107">Esta amostra de código utiliza a classe auxiliar OutlookItem, definida em [Criar uma classe auxiliar para acessar membros comuns de itens do Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), para chamar convenientemente a propriedade OutlookItem.**Categories** sem ter que lançar o item primeiro.</span><span class="sxs-lookup"><span data-stu-id="08586-107">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.**Categories** property without having to first cast the item.</span></span> <span data-ttu-id="08586-108">A propriedade **Categories** obtém ou define categorias representadas por uma cadeia delimitada por vírgula que pode conter no máximo 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="08586-108">The **Categories** property gets or sets categories that are represented by a comma-delimited string that can contain a maximum of 255 characters.</span></span> <span data-ttu-id="08586-109">Vírgulas e espaços são usados para separar os valores da categoria.</span><span class="sxs-lookup"><span data-stu-id="08586-109">The commas and spaces are used to separate the category values.</span></span> <span data-ttu-id="08586-110">Atribuir uma categoria que não esteja no conjunto [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) fará com que a categoria não exiba uma cor.</span><span class="sxs-lookup"><span data-stu-id="08586-110">Assigning a category that is not in the [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) collection of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object will result in the category not displaying a color.</span></span>

<span data-ttu-id="08586-111">No exemplo de código a seguir, AssignCategories cria uma restrição para itens que contêm “ISV” no assunto, primeiro usando uma consulta DAV Searching and Locating (DASL) para filtrar itens na Caixa de Entrada que contenham “ISV” no assunto.</span><span class="sxs-lookup"><span data-stu-id="08586-111">In the following code example, AssignCategories creates a restriction for items that contain “ISV” in the subject by first using a DAV Searching and Locating (DASL) query to filter items in the Inbox that contain “ISV” in the subject.</span></span> <span data-ttu-id="08586-112">Em seguida, AssignCategories percorre os itens filtrados usando a classe **OutlookItem** e, se a cadeia de caracteres retornada por **item.Categories** não for uma referência nula ou já tiver sido atribuída à ISV, a categoria ISV será atribuída ao item.</span><span class="sxs-lookup"><span data-stu-id="08586-112">AssignCategories then iterates through the filtered items by using the **OutlookItem** class and, if the string returned by **item.Categories** is not a null reference or was already assigned to the ISV, the ISV category is assigned to the item.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AssignCategories()
{
    string filter = "@SQL=" + "\"" + "urn:schemas:httpmail:subject"
        + "\"" + " ci_phrasematch 'ISV'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Restrict(filter);
    for (int i = 1; i <= items.Count; i++)
    {
        OutlookItem item = new OutlookItem(items[i]);
        string existingCategories = item.Categories;
        if (String.IsNullOrEmpty(existingCategories))
        {
            item.Categories = "ISV";
        }
        else
        {
            if (item.Categories.Contains("ISV") == false)
            {
                item.Categories = existingCategories + ", ISV";
            }
        }
        item.Save();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="08586-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="08586-113">See also</span></span>

- [<span data-ttu-id="08586-114">Categorias de cor</span><span class="sxs-lookup"><span data-stu-id="08586-114">Color categories</span></span>](color-categories.md)

