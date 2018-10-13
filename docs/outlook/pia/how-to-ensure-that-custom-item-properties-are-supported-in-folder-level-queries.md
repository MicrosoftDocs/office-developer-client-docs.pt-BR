---
title: Certifique-se de que as propriedades de item personalizado têm suporte em consultas ao nível de pasta
TOCTitle: Ensure that custom item properties are supported in folder-level queries
ms:assetid: 02cf14c6-ee1b-4e04-a865-32adaac13f9b
ms:mtpsurl: https://msdn.microsoft.com/library/Bb608929(v=office.15)
ms:contentKeyID: 55119863
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 659919de8eeb17e675ed67f3b777f67b04f13b54
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406936"
---
# <a name="ensure-that-custom-item-properties-are-supported-in-folder-level-queries"></a><span data-ttu-id="cd01a-102">Certifique-se de que as propriedades de item personalizado têm suporte em consultas ao nível de pasta</span><span class="sxs-lookup"><span data-stu-id="cd01a-102">Ensure that custom item properties are supported in folder-level queries</span></span>

<span data-ttu-id="cd01a-103">Este exemplo mostra como garantir que, ao adicionar uma propriedade personalizada a um tipo de item, você também adiciona a propriedade à pasta, para que possa consultar essa propriedade personalizada no nível da pasta.</span><span class="sxs-lookup"><span data-stu-id="cd01a-103">This example shows how to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

## <a name="example"></a><span data-ttu-id="cd01a-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="cd01a-104">Example</span></span>

<span data-ttu-id="cd01a-105">Este exemplo de código mostra como usar o objeto [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) e o objeto [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) para garantir que quando você adiciona uma propriedade personalizada a um tipo de item, também adiciona a propriedade à pasta, para que possa consultar essa propriedade personalizada no nível da pasta.</span><span class="sxs-lookup"><span data-stu-id="cd01a-105">This code sample shows how to use the [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) object and the [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) object to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

<span data-ttu-id="cd01a-106">Quando você usa o método [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) no conjunto [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) para adicionar uma propriedade personalizada a um item, você pode especificar o parâmetro *AddToFolderFields* como **true** para adicionar a propriedade à pasta.</span><span class="sxs-lookup"><span data-stu-id="cd01a-106">When you use the [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) method on the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection to add a custom property to an item, you can specify the *AddToFolderFields* parameter as **true** to add the property to the folder.</span></span> <span data-ttu-id="cd01a-107">No entanto, a propriedade personalizada pode não ser adicionada à pasta desejada devido a um erro do desenvolvedor ou uma ação do usuário, como remover a propriedade personalizada por meio do Seletor de Campos do Outlook ou mover o item para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="cd01a-107">However, the custom property might not get added to the desired folderbecause of developer error or a user action, such as removing the custom property through the Outlook Field Chooser or moving the item to another folder.</span></span> <span data-ttu-id="cd01a-108">Consequentemente, o método [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) e o método [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) do objeto [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) que usa essa propriedade personalizada falhará.</span><span class="sxs-lookup"><span data-stu-id="cd01a-108">Consequently, the [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) method and the [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method of the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) object that uses that custom property will fail.</span></span> <span data-ttu-id="cd01a-109">Usando o objeto **UserDefinedProperties**, você pode verificar se suas propriedades personalizadas existem na pasta e adicionar as propriedades personalizadas se não existirem ou tiverem sido removidas.</span><span class="sxs-lookup"><span data-stu-id="cd01a-109">By using the **UserDefinedProperties** object, you can test whether your custom properties exist in the folder, and add the custom properties if they do not exist or if they have been removed.</span></span>

<span data-ttu-id="cd01a-110">Para manter uma propriedade personalizada representada por um objeto **UserDefinedProperty** em uma pasta, você deve salvar a propriedade personalizada com o mesmo nome no item.</span><span class="sxs-lookup"><span data-stu-id="cd01a-110">To persist a custom property represented by a **UserDefinedProperty** object in a folder, you must save the custom property with the same name in the item.</span></span> <span data-ttu-id="cd01a-111">Armazenar um valor no objeto **UserDefinedProperty** da pasta não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="cd01a-111">Storing a value in the **UserDefinedProperty** object for the folder has no effect.</span></span> <span data-ttu-id="cd01a-112">Você deve definir o conjunto **UserProperties** do item para acessar o objeto [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) que você deseja definir, e definir o valor no objeto **UserProperty**.</span><span class="sxs-lookup"><span data-stu-id="cd01a-112">You must se the item's **UserProperties** collection to access the [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) object that you want to set, and then set the value on the **UserProperty** object.</span></span> <span data-ttu-id="cd01a-113">Certifique-se de chamar o método **Save** no item para manter suas alterações.</span><span class="sxs-lookup"><span data-stu-id="cd01a-113">Be sure to call the **Save** method on the item to persist your changes.</span></span>

<span data-ttu-id="cd01a-114">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="cd01a-114">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="cd01a-115">A instrução **Imports** ou **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionada antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="cd01a-115">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="cd01a-116">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="cd01a-116">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoUserDefinedProperty()
    Dim folder As Outlook.Folder = _
        CType(Application.ActiveExplorer().CurrentFolder(), _
        Outlook.Folder)
    Dim post As Outlook.PostItem = CType( _
        folder.Items.Add("IPM.Post"), Outlook.PostItem)
    ' Add UserProperty to PostItem
    post.UserProperties.Add("ColorID", _
        Outlook.OlUserPropertyType.olText, False)
    post.UserProperties("ColorID").Value = "Green"
    post.Subject = "UserProperty Example"
    post.Save()
    Dim findPost As Outlook.PostItem
    Try
        ' Items.Find will fail unless custom property
        ' is defined in the folder
        findPost = _
            CType(folder.Items.Find("[ColorID] = 'Green'"), _
            Outlook.PostItem)
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
        ' Add ColorID field to the folder
        folder.UserDefinedProperties.Add("ColorID", _
            Outlook.OlUserPropertyType.olText)
        ' Now the find works ok
        Dim findPostOK As Outlook.PostItem
        Try
            findPostOK = _
                CType(folder.Items.Find("[ColorID] = 'Green'"), _
                Outlook.PostItem)
            If Not (findPostOK Is Nothing) Then
                Debug.WriteLine("Found PostItem")
            End If
            ' Cleanup by deleting PostItem and ColorID
            findPostOK.Delete()
            Dim userProperty As Outlook.UserDefinedProperty = _
                folder.UserDefinedProperties("ColorID")
            userProperty.Delete()
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
End Sub
```


```csharp
private void DemoUserDefinedProperty()
{
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.PostItem post = folder.Items.Add("IPM.Post")
        as Outlook.PostItem;
    // Add UserProperty to PostItem
    post.UserProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        false, Type.Missing);
    post.UserProperties["ColorID"].Value = "Green";
    post.Subject = "UserProperty Example";
    post.Save();
    Outlook.PostItem findPost;
    try
    {
        // Items.Find will fail unless custom property
        // is defined in the folder
        findPost =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
     // Add ColorID field to the folder
    folder.UserDefinedProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        Type.Missing, Type.Missing);
    // Now the find works ok
    Outlook.PostItem findPostOK;
    try
    {
        findPostOK =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
        if (findPostOK != null)
        {
            Debug.WriteLine("Found PostItem");
        }
        // Cleanup by deleting PostItem and ColorID
        findPostOK.Delete();
        Outlook.UserDefinedProperty userProperty =
            folder.UserDefinedProperties["ColorID"];
        userProperty.Delete();
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="cd01a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd01a-117">See also</span></span>

- [<span data-ttu-id="cd01a-118">Pastas</span><span class="sxs-lookup"><span data-stu-id="cd01a-118">Folders</span></span>](folders.md)

