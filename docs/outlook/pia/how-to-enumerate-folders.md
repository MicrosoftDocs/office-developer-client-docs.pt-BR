---
title: Enumerar pastas
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 91165754ccd86ebff07ec99e60f0ad1a167dea05
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406250"
---
# <a name="enumerate-folders"></a><span data-ttu-id="65209-102">Enumerar pastas</span><span class="sxs-lookup"><span data-stu-id="65209-102">Enumerate folders</span></span>

<span data-ttu-id="65209-103">Este exemplo mostra como enumerar pastas por iteração por meio de um conjunto de pastas.</span><span class="sxs-lookup"><span data-stu-id="65209-103">This example shows how to enumerate folders by iterating through a collection of folders.</span></span>

## <a name="example"></a><span data-ttu-id="65209-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="65209-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="65209-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="65209-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="65209-106">No exemplo código a seguir, o método EnumerateFoldersInDefaultStore primeiro obtém a pasta raiz do armazenamento padrão usando o método [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="65209-106">In the following code example, the EnumerateFoldersInDefaultStore method first obtains the root folder for the default store by using the [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) method.</span></span> <span data-ttu-id="65209-107">Ele chama o método EnumerateFolders na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="65209-107">It then calls the EnumerateFolders method on the root folder.</span></span> <span data-ttu-id="65209-108">EnumerateFolders assume uma pasta raiz e percorre as pastas do armazenamento padrão que representa a pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="65209-108">EnumerateFolders takes in a root folder and walks through the folders of the default store that the root folder represents.</span></span> <span data-ttu-id="65209-109">EnumerateFolders primeiro usa a propriedade [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) para ter as subpastas do objeto raiz [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="65209-109">EnumerateFolders first uses the [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) property to obtain the subfolders of the root [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span> <span data-ttu-id="65209-110">EnumerateFolders é então chamado recursivamente para enumerar todas as pastas em uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="65209-110">EnumerateFolders is then called recursively to enumerate all the folders in a hierarchy.</span></span> <span data-ttu-id="65209-111">Por fim, EnumerateFolders grava a propriedade [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) de cada **Folder** para os ouvintes de rastreamento no conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="65209-111">Finally, EnumerateFolders writes the [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) property of each **Folder** to the trace listeners in the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="65209-112">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="65209-112">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="65209-113">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="65209-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="65209-114">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="65209-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateFoldersInDefaultStore()
{
    Outlook.Folder root =
        Application.Session.
        DefaultStore.GetRootFolder() as Outlook.Folder;
    EnumerateFolders(root);
}

// Uses recursion to enumerate Outlook subfolders.
private void EnumerateFolders(Outlook.Folder folder)
{
    Outlook.Folders childFolders =
        folder.Folders;
    if (childFolders.Count > 0)
    {
        foreach (Outlook.Folder childFolder in childFolders)
        {
            // Write the folder path.
            Debug.WriteLine(childFolder.FolderPath);
            // Call EnumerateFolders using childFolder.
            EnumerateFolders(childFolder);
        }
    }
}               
```

## <a name="see-also"></a><span data-ttu-id="65209-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="65209-115">See also</span></span>

- [<span data-ttu-id="65209-116">Pastas</span><span class="sxs-lookup"><span data-stu-id="65209-116">Folders</span></span>](folders.md)

