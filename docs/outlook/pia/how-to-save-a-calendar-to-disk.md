---
title: Salvar um calendário no disco
TOCTitle: Save a calendar to disk
ms:assetid: f1b57bd0-c972-4b86-8870-f26290f28050
ms:mtpsurl: https://msdn.microsoft.com/library/Bb647583(v=office.15)
ms:contentKeyID: 55119827
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b07df7458f80b751077358ac3c53ad41032d1080
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361044"
---
# <a name="save-a-calendar-to-disk"></a><span data-ttu-id="804dd-102">Salvar um calendário no disco</span><span class="sxs-lookup"><span data-stu-id="804dd-102">Save a calendar to disk</span></span>

<span data-ttu-id="804dd-103">Este exemplo mostra como salvar um calendário inteiro no disco no formato de arquivo iCalendar (ICS).</span><span class="sxs-lookup"><span data-stu-id="804dd-103">This example shows how to save an entire calendar to disk in the iCalendar (.ics) file format.</span></span>

## <a name="example"></a><span data-ttu-id="804dd-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="804dd-104">Example</span></span>

<span data-ttu-id="804dd-105">Este exemplo de código usa o objeto [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) que é compatível com o salvamento de um calendário inteiro ou um intervalo de compromissos do calendário para o disco.</span><span class="sxs-lookup"><span data-stu-id="804dd-105">This code sample uses the [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object that supports saving a whole calendar or a range of appointments from the calendar to disk.</span></span> <span data-ttu-id="804dd-106">O Outlook otimiza automaticamente um arquivo .ics para que os compromissos recorrentes não sejam salvos como compromissos individuais no arquivo .ics.</span><span class="sxs-lookup"><span data-stu-id="804dd-106">Outlook automatically optimizes an .ics file so that recurring appointments are not saved as individual appointments in the .ics file.</span></span> <span data-ttu-id="804dd-107">Dependendo do tamanho do calendário que está sendo salvo, salvar um calendário em disco pode levar um tempo significativo.</span><span class="sxs-lookup"><span data-stu-id="804dd-107">Depending on the size of the calendar being saved, saving a calendar to disk can take a significant amount of time.</span></span> <span data-ttu-id="804dd-108">Ao salvar o calendário, a janela do Outlook parece não responder ao usuário.</span><span class="sxs-lookup"><span data-stu-id="804dd-108">While saving the calendar, the Outlook window appears unresponsive to the user.</span></span>

<span data-ttu-id="804dd-109">O exemplo de código primeiro chama [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) na pasta Calendário padrão para receber um objeto **CalendarSharing**.</span><span class="sxs-lookup"><span data-stu-id="804dd-109">The code sample first calls [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) on the default Calendar folder to obtain a **CalendarSharing** object.</span></span> <span data-ttu-id="804dd-110">Em seguida, ele define propriedades do objeto **CalendarSharing** para especificar critérios para a exportação, como se deve salvar o calendário todo e se deseja incluir detalhes dos compromissos marcados como "particulares".</span><span class="sxs-lookup"><span data-stu-id="804dd-110">Then it sets properties of the **CalendarSharing** object to specify criteria for the export, such as whether to save the entire calendar and include details of appointments that are marked "private".</span></span>

<span data-ttu-id="804dd-111">Para salvar as informações do calendário no formato de arquivo .ics, o exemplo de código chama o método [ForwardAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) do objeto **CalendarSharing**.</span><span class="sxs-lookup"><span data-stu-id="804dd-111">To save the calendar information in .ics file format, the code sample calls the [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) method of the **CalendarSharing** object.</span></span>

<span data-ttu-id="804dd-112">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="804dd-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="804dd-113">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="804dd-113">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="804dd-114">As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="804dd-114">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SaveCalendarToDisk(ByVal calendarFileName As String)
    If String.IsNullOrEmpty(calendarFileName) Then
        Throw New ArgumentException( _
        "Parameter must contain a value.", "calendarFileName")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder(_
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = _
        calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = True
    exporter.RestrictToWorkingHours = False
    exporter.IncludeWholeCalendar = True

    '' Save the calendar to disk
    exporter.SaveAsICal(calendarFileName)
End Sub
```


```csharp
private void SaveCalendarToDisk(string calendarFileName)
{
    if (string.IsNullOrEmpty(calendarFileName))
        throw new ArgumentException("calendarFileName", 
        "Parameter must contain a value.");

    Outlook.Folder calendar = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar) as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = true;
    exporter.RestrictToWorkingHours = false;
    exporter.IncludeWholeCalendar = true;

    // Save the calendar to disk
    exporter.SaveAsICal(calendarFileName);
}
```

## <a name="see-also"></a><span data-ttu-id="804dd-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="804dd-115">See also</span></span>

- [<span data-ttu-id="804dd-116">Calendar</span><span class="sxs-lookup"><span data-stu-id="804dd-116">Calendar</span></span>](calendar.md)

