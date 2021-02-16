---
title: Adicionar ou remover um repositório
TOCTitle: Add or remove a store
ms:assetid: db2930ec-ef99-4e31-86c5-820e8368e05f
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612380(v=office.15)
ms:contentKeyID: 55119895
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4346f3bf1b7bba1f26a34e1562997b4d043c8d49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359742"
---
# <a name="add-or-remove-a-store"></a><span data-ttu-id="3da10-102">Adicionar ou remover um repositório</span><span class="sxs-lookup"><span data-stu-id="3da10-102">Add or remove a store</span></span>

<span data-ttu-id="3da10-103">Este exemplo mostra como adicionar e remover um repositório em determinado perfil.</span><span class="sxs-lookup"><span data-stu-id="3da10-103">This example shows how to add and remove a store in a given profile.</span></span>

## <a name="example"></a><span data-ttu-id="3da10-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3da10-104">Example</span></span>

<span data-ttu-id="3da10-105">Este exemplo de código mostra como adicionar e remover um armazenamento em um perfil especificado, chamando o método [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) e o método [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)), respectivamente, no objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3da10-105">This code sample shows how to add and remove a store in a specified profile, by calling the [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) method and the [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)) method respectively on the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span>

<span data-ttu-id="3da10-106">No Outlook, você pode adicionar ou remover um repositório PST somente por meio de programação.</span><span class="sxs-lookup"><span data-stu-id="3da10-106">In Outlook, you can add or remove a PST store only programmatically.</span></span> <span data-ttu-id="3da10-107">O exemplo de código a seguir adiciona um armazenamento Unicode e coloca o arquivo .pst no local padrão dos arquivos .pst do usuário: Documents and Settings\\\<UserName\>\\Local Settings\\Application Data\\Microsoft\\Outlook.</span><span class="sxs-lookup"><span data-stu-id="3da10-107">The following code sample adds a Unicode store and places the .pst file in the default location for user .pst files: Documents and Settings\\\<UserName\>\\Local Settings\\Application Data\\Microsoft\\Outlook.</span></span> <span data-ttu-id="3da10-108">O exemplo de código usa Environment.SpecialFolder.LocalApplicationData para recuperar o caminho para a pasta Application Data na pasta Local Settings.</span><span class="sxs-lookup"><span data-stu-id="3da10-108">The code sample uses Environment.SpecialFolder.LocalApplicationData to retrieve the path to the Application Data folder under the Local Settings folder.</span></span> <span data-ttu-id="3da10-109">Depois que o repositório foi adicionado, o exemplo de código remove o repositório.</span><span class="sxs-lookup"><span data-stu-id="3da10-109">Once the store has been added, the code sample removes the store.</span></span> <span data-ttu-id="3da10-110">Como o método **RemoveStore** requer um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) para remover o objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)), ele enumera a coleção [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) para localizar o objeto **Store** que acaba de ser adicionado com base na propriedade [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) do objeto **Store**.</span><span class="sxs-lookup"><span data-stu-id="3da10-110">Because the **RemoveStore** method requires a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object to remove the [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, it enumerates the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to find the **Store** object that has just been added based on the [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) property of the **Store** object.</span></span>

<span data-ttu-id="3da10-111">**RemoveStore** remove apenas o repositório do perfil atual.</span><span class="sxs-lookup"><span data-stu-id="3da10-111">**RemoveStore** only removes the store from the current profile.</span></span> <span data-ttu-id="3da10-112">Não exclui o arquivo .pst do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3da10-112">It does not delete the .pst file from the file system.</span></span>

<span data-ttu-id="3da10-113">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="3da10-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3da10-114">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="3da10-114">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3da10-115">As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="3da10-115">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateUnicodePST()
    Dim path As String = Environment.GetFolderPath( _
        Environment.SpecialFolder.LocalApplicationData) _
        & "\Microsoft\Outlook\MyUnicodeStore.pst"
    Try
        Application.Session.AddStoreEx( _
            path, Outlook.OlStoreType.olStoreUnicode)
        Dim stores As Outlook.Stores = Application.Session.Stores
        For Each store As Outlook.Store In stores
            If store.FilePath = path Then
                Dim folder As Outlook.Folder = _
                    CType(store.GetRootFolder(), Outlook.Folder)
                ' Remove the store
                Application.Session.RemoveStore(folder)
            End If
        Next
    Catch ex As Exception
        Debug.WriteLine(ex.Message)
    End Try
End Sub
```


```csharp
private void CreateUnicodePST()
{
    string path = Environment.GetFolderPath(
        Environment.SpecialFolder.LocalApplicationData)
        + @"\Microsoft\Outlook\MyUnicodeStore.pst";
    try
    {
        Application.Session.AddStoreEx(
            path, Outlook.OlStoreType.olStoreUnicode);
        Outlook.Stores stores = Application.Session.Stores;
        foreach (Outlook.Store store in stores)
        {
            if (store.FilePath == path)
            {
               Outlook.Folder folder =
                    store.GetRootFolder() as Outlook.Folder;
               // Remove the store
               Application.Session.RemoveStore(folder);
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3da10-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="3da10-116">See also</span></span>

- [<span data-ttu-id="3da10-117">Repositórios</span><span class="sxs-lookup"><span data-stu-id="3da10-117">Stores</span></span>](stores.md)

