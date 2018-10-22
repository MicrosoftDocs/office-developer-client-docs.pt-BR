---
title: Abrir e exibir o conteúdo de um arquivo iCalendar
TOCTitle: Open and display the contents of an iCalendar file
ms:assetid: 2066e404-7aaf-4fd2-bf5c-9604e3fc2681
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644609(v=office.15)
ms:contentKeyID: 55119818
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: dcebc65c651804148969c6260ecac72060bf9ef0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406775"
---
# <a name="open-and-display-the-contents-of-an-icalendar-file"></a><span data-ttu-id="01831-102">Abrir e exibir o conteúdo de um arquivo iCalendar</span><span class="sxs-lookup"><span data-stu-id="01831-102">Open and display the contents of an iCalendar file</span></span>

<span data-ttu-id="01831-103">Este exemplo mostra como abrir e exibir o conteúdo de um arquivo iCalendar, conforme se trate de um arquivo que contém um único compromisso ou um compromisso recorrente ou um arquivo que contém um grupo de compromissos.</span><span class="sxs-lookup"><span data-stu-id="01831-103">This example shows how to open and display the contents of an iCalendar file, depending on whether the file contains a single or recurrent appointment, or the file contains a group of appointments.</span></span>

## <a name="example"></a><span data-ttu-id="01831-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="01831-104">Example</span></span>

<span data-ttu-id="01831-105">Este exemplo de código primeiro tenta usar o método [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para abrir o arquivo iCalendar como um arquivo iCalendar de compromisso único.</span><span class="sxs-lookup"><span data-stu-id="01831-105">This code sample first tries to use the [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to open the iCalendar file as a single-appointment iCalendar file.</span></span> <span data-ttu-id="01831-106">Se tiver êxito, exibirá os detalhes do item de compromisso em uma janela do inspetor.</span><span class="sxs-lookup"><span data-stu-id="01831-106">If it succeeds, it will display the appointment item details in an inspector window.</span></span> <span data-ttu-id="01831-107">No entanto, ele não copiará o item para o armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="01831-107">However, it will not copy the item to the default store.</span></span> <span data-ttu-id="01831-108">Se o exemplo não puder abrir o arquivo como um arquivo iCalendar de compromisso único, ele usará o método [OpenSharedFolder](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) do objeto **NameSpace** para tentar importar o conteúdo como um novo calendário no loja padrão.</span><span class="sxs-lookup"><span data-stu-id="01831-108">If the sample cannot open the file as a single-appointment iCalendar file, then it will use the [OpenSharedFolder](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the **NameSpace** object to attempt to import the contents as a new calendar in the default store.</span></span> <span data-ttu-id="01831-109">Se a importação for realizada, ele exibirá o calendário em uma janela do explorador.</span><span class="sxs-lookup"><span data-stu-id="01831-109">If it succeeds in importing, then it will display the calendar in an explorer window.</span></span>

<span data-ttu-id="01831-110">Este exemplo de código utiliza a classe auxiliar OutlookItem, definida em [Criar uma classe auxiliar para acessar membros comuns de itens do Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), para chamar convenientemente o método **OutlookItem.Display** para exibir o compromisso sem ter que lançar o item primeiro.</span><span class="sxs-lookup"><span data-stu-id="01831-110">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the **OutlookItem.Display** method to display the appointment item without having to first cast the item.</span></span>

<span data-ttu-id="01831-111">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="01831-111">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="01831-112">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="01831-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="01831-113">As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="01831-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub OpenICalendarFile(ByVal fileName As String)
    If String.IsNullOrEmpty(fileName) Then
        Throw New ArgumentException(_
        "Parameter must contain a value.", "exportFileName")
    End If
    If Not File.Exists(fileName) Then
        Throw New FileNotFoundException(fileName)
    End If

    '' First try to open the icalendar file as an appointment 
    '' (not a calendar folder).
    Dim item As Object = Nothing
    Try
         item = Application.Session.OpenSharedItem(fileName)
    Catch
    End Try

    If Not item Is Nothing Then
        '' Display the item
        Dim olItem As OutlookItem = New OutlookItem(item)
        olItem.Display()
        Return
    End If

    '' If unsucessful in opening it as an item, 
    '' try opening it as a folder
    Dim importedFolder As Outlook.Folder = Nothing
    Try
        importedFolder = TryCast( _
            Application.Session.OpenSharedFolder(fileName), _
            Outlook.Folder)
    Catch
    End Try

    '' If sucessful, open the folder in a new explorer window
    If Not importedFolder Is Nothing Then
        Dim explorer As Outlook.Explorer = _
            Application.Explorers.Add( _
            importedFolder, _
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal)
        explorer.Display()
    End If
End Sub
```


```csharp
private void OpenICalendarFile(string fileName)
{
    if (string.IsNullOrEmpty(fileName))
        throw new ArgumentException("exportFileName", 
        "Parameter must contain a value.");
    if (!File.Exists(fileName))
        throw new FileNotFoundException(fileName);

    // First try to open the icalendar file as an appointment 
    // (not a calendar folder).
    object item = null;
    try
    {
        item = Application.Session.OpenSharedItem(fileName);
    }
    catch
    { }

    if (item != null)
    {
         // Display the item
         OutlookItem olItem = new OutlookItem(item);
         olItem.Display();
         return;
    }

    // If unsucessful in opening it as an item, 
    // try opening it as a folder
    Outlook.Folder importedFolder = null;
    try
    {
        importedFolder = Application.Session.OpenSharedFolder(
            fileName, Type.Missing, Type.Missing, Type.Missing) 
            as Outlook.Folder;
    }
    catch
    { }

    // If sucessful, open the folder in a new explorer window
    if (importedFolder != null)
    {
        Outlook.Explorer explorer =
            Application.Explorers.Add(importedFolder, 
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        explorer.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="01831-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="01831-114">See also</span></span>

- [<span data-ttu-id="01831-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="01831-115">Calendar</span></span>](calendar.md)

