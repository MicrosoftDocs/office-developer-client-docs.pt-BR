---
title: Obter uma pasta padrão e enumerar as subpastas dela
TOCTitle: Get a default folder and enumerate its subfolders
ms:assetid: 587e8392-cb03-442c-9058-1282f36dabdb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184610(v=office.15)
ms:contentKeyID: 55119857
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 934b5f823127fde9fbbd3a49f41cedb791277e7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407398"
---
# <a name="get-a-default-folder-and-enumerate-its-subfolders"></a><span data-ttu-id="bec4a-102">Obter uma pasta padrão e enumerar as subpastas dela</span><span class="sxs-lookup"><span data-stu-id="bec4a-102">Get a default folder and enumerate its subfolders</span></span>

<span data-ttu-id="bec4a-103">Este exemplo mostra como obter uma pasta padrão no repositório padrão do usuário e enumerar as subpastas dela.</span><span class="sxs-lookup"><span data-stu-id="bec4a-103">This example shows how to obtain a default folder in the user’s default store and enumerate its subfolders.</span></span>

## <a name="example"></a><span data-ttu-id="bec4a-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bec4a-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="bec4a-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="bec4a-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="bec4a-106">No exemplo de código a seguir, GetRSSFeeds usa o método [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para obter a pasta raiz RSS Feeds.</span><span class="sxs-lookup"><span data-stu-id="bec4a-106">In the following code example, GetRSSFeeds uses the [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to obtain the user’s RSS Feeds root folder.</span></span> <span data-ttu-id="bec4a-107">GetRSSFeeds exibe uma caixa de mensagem que contém os nomes de pasta de todos os RSS feeds da pasta RSS Feeds.</span><span class="sxs-lookup"><span data-stu-id="bec4a-107">GetRSSFeeds then displays a message box that contains the folder names for all RSS feeds in the RSS Feeds folder.</span></span>

<span data-ttu-id="bec4a-108">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="bec4a-108">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="bec4a-109">A instrução **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="bec4a-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="bec4a-110">A seguinte linha de código mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="bec4a-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetRSSFeeds()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderRssFeeds)
        as Outlook.Folder;
    if (folder != null)
    {
        if (folder.Folders.Count > 0)
        {
            StringBuilder sb = new StringBuilder();
            foreach (Outlook.Folder subfolder
                in folder.Folders)
            {
                sb.AppendLine(subfolder.Name);
            }
            MessageBox.Show(sb.ToString(),
                "RSS Feeds",
                MessageBoxButtons.OK,
                MessageBoxIcon.Information);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="bec4a-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="bec4a-111">See also</span></span>

- [<span data-ttu-id="bec4a-112">Pastas</span><span class="sxs-lookup"><span data-stu-id="bec4a-112">Folders</span></span>](folders.md)

