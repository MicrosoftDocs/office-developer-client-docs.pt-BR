---
title: Obter uma pasta com base em seu caminho da pasta
TOCTitle: Get a folder based on its folder path
ms:assetid: 613f2209-667c-48f0-82cf-86e3c9a24cb4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184612(v=office.15)
ms:contentKeyID: 55119858
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fed1e7eb39f31ddd4340fc82a16e31ec67523a9d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320283"
---
# <a name="get-a-folder-based-on-its-folder-path"></a><span data-ttu-id="e9c22-102">Obter uma pasta com base em seu caminho da pasta</span><span class="sxs-lookup"><span data-stu-id="e9c22-102">Get a folder based on its folder path</span></span>

<span data-ttu-id="e9c22-103">Este exemplo usa um caminho da pasta e obtém a pasta associada.</span><span class="sxs-lookup"><span data-stu-id="e9c22-103">This example takes a folder path and obtains the associated folder.</span></span>

## <a name="example"></a><span data-ttu-id="e9c22-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e9c22-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e9c22-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="e9c22-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="e9c22-106">No exemplo de código a seguir, o método GetKeyContacts usa a propriedade [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) para obter o caminho da pasta Contatos Principais dos Contatos\\.</span><span class="sxs-lookup"><span data-stu-id="e9c22-106">In the following code example, the GetKeyContacts method uses the [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) property to obtain the folder path of the Contacts\\Key Contacts folder.</span></span> <span data-ttu-id="e9c22-107">O método GetFolder é então chamado usando a propriedade [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) como argumento.</span><span class="sxs-lookup"><span data-stu-id="e9c22-107">The GetFolder method is then called by using the [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) property as the argument.</span></span> <span data-ttu-id="e9c22-108">Se GetFolder retornar uma pasta, aparecerá uma mensagem dizendo que os contatos principais foram encontrados.</span><span class="sxs-lookup"><span data-stu-id="e9c22-108">If GetFolder returns a folder, a message will appear saying the Key Contacts are found.</span></span> <span data-ttu-id="e9c22-109">O método GetFolder utiliza um caminho para uma pasta e retorna o objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) correto.</span><span class="sxs-lookup"><span data-stu-id="e9c22-109">The GetFolder method takes in a path to a folder and returns the correct [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span> <span data-ttu-id="e9c22-110">Isso é feito primeiro dividindo a propriedade **FolderPath** em uma matriz de cadeia de caracteres e depois usando a matriz para localizar a **Folder** correta a partir da parte superior da propriedade **FolderPath**.</span><span class="sxs-lookup"><span data-stu-id="e9c22-110">This is done by first splitting the **FolderPath** property into a string array and then using the array to find the correct **Folder** object starting from the top of the **FolderPath** property.</span></span> <span data-ttu-id="e9c22-111">Se a pasta especificada não for encontrada, GetFolder retornará uma referência nula.</span><span class="sxs-lookup"><span data-stu-id="e9c22-111">If the specified folder is not found, GetFolder returns a null reference.</span></span>

<span data-ttu-id="e9c22-112">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e9c22-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e9c22-113">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="e9c22-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e9c22-114">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="e9c22-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetKeyContacts()
{
    string folderPath =
        Application.Session.
        DefaultStore.GetRootFolder().FolderPath
        + @"\Contacts\Key Contacts";
    Outlook.Folder folder = GetFolder(folderPath);
    if (folder != null)
    {
        //Work with folder here
        Debug.WriteLine("Found Key Contacts");
    }
}

// Returns Folder object based on folder path
private Outlook.Folder GetFolder(string folderPath)
{
    Outlook.Folder folder;
    string backslash = @"\";
    try
    {
        if (folderPath.StartsWith(@"\\"))
        {
            folderPath = folderPath.Remove(0, 2);
        }
        String[] folders =
            folderPath.Split(backslash.ToCharArray());
        folder =
            Application.Session.Folders[folders[0]]
            as Outlook.Folder;
        if (folder != null)
        {
            for (int i = 1; i <= folders.GetUpperBound(0); i++)
            {
                Outlook.Folders subFolders = folder.Folders;
                folder = subFolders[folders[i]]
                    as Outlook.Folder;
                if (folder == null)
                {
                    return null;
                }
            }
        }
        return folder;
    }
    catch { return null; }
}        
```

## <a name="see-also"></a><span data-ttu-id="e9c22-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9c22-115">See also</span></span>

- [<span data-ttu-id="e9c22-116">Pastas</span><span class="sxs-lookup"><span data-stu-id="e9c22-116">Folders</span></span>](folders.md)

