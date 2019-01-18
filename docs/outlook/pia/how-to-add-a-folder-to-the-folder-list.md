---
title: Adicionar uma pasta à lista de pastas
TOCTitle: Add a folder to the folder list
ms:assetid: f636a190-d966-4421-9977-0ead2bff5eee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184655(v=office.15)
ms:contentKeyID: 55119850
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 27a9efb76fdbb1c6ac6b0b57e874ca59d002b928
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710304"
---
# <a name="add-a-folder-to-the-folder-list"></a><span data-ttu-id="9357f-102">Adicionar uma pasta à lista de pastas</span><span class="sxs-lookup"><span data-stu-id="9357f-102">Add a folder to the folder list</span></span>

<span data-ttu-id="9357f-103">Este exemplo mostra como usar o método [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) para adicionar uma pasta à lista de pastas do Outlook.</span><span class="sxs-lookup"><span data-stu-id="9357f-103">This example shows how to use the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add a folder to the Outlook folder list.</span></span>

## <a name="example"></a><span data-ttu-id="9357f-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9357f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="9357f-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="9357f-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="9357f-106">No seguinte exemplo de código, **AddMyNewFolder** chama o método **Add** da coleção [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) para adicionar um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) que representa uma pasta chamada "Minha Nova Pasta" à lista de pastas **Inbox** do Outlook.</span><span class="sxs-lookup"><span data-stu-id="9357f-106">In the following code example, **AddMyNewFolder** calls the **Add** method of the [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) collection to add a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that represents a folder called “My New Folder” to the **Inbox** in the Outlook folder list.</span></span> <span data-ttu-id="9357f-107">"Minha Nova Pasta" é exibida.</span><span class="sxs-lookup"><span data-stu-id="9357f-107">“My New Folder” is then displayed.</span></span>

<span data-ttu-id="9357f-108">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="9357f-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="9357f-109">A instrução **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="9357f-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="9357f-110">A seguinte linha de código mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="9357f-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddMyNewFolder()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Folders folders = folder.Folders;
    try
    {
        Outlook.Folder newFolder = folders.Add(
            "My New Folder", Type.Missing)
            as Outlook.Folder;
        newFolder.Display();
    }
    catch
    {
        MessageBox.Show(
            "Could not add 'My New Folder'",
            "Add Folder",
            MessageBoxButtons.OK,
            MessageBoxIcon.Error);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="9357f-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="9357f-111">See also</span></span>

- [<span data-ttu-id="9357f-112">Pastas</span><span class="sxs-lookup"><span data-stu-id="9357f-112">Folders</span></span>](folders.md)

