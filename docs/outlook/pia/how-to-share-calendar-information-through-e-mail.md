---
title: Compartilhar informações de calendário por email
TOCTitle: Share calendar information through email
ms:assetid: 3382010c-0a16-4dca-a99e-669e9178354e
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609881(v=office.15)
ms:contentKeyID: 55119817
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48b299ad4d3afe5c0c9aaa05f5d8af3b92bf655d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332072"
---
# <a name="share-calendar-information-through-email"></a><span data-ttu-id="c7224-102">Compartilhar informações de calendário por email</span><span class="sxs-lookup"><span data-stu-id="c7224-102">Share calendar information through email</span></span>

<span data-ttu-id="c7224-103">Este exemplo mostra como compartilhar informações de um calendário por email no formato iCalendar.</span><span class="sxs-lookup"><span data-stu-id="c7224-103">This example shows how to share information from a calendar by email in the iCalendar format.</span></span>

## <a name="example"></a><span data-ttu-id="c7224-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c7224-104">Example</span></span>

<span data-ttu-id="c7224-105">O formato iCalendar permite enviar itens para outros clientes do Outlook, ou que não sejam do Outlook por meio de formatos e protocolos padrão de correio da Internet.</span><span class="sxs-lookup"><span data-stu-id="c7224-105">The iCalendar format allows you to send items to other Outlook or non-Outlook clients via standard Internet mail formats and protocols.</span></span> <span data-ttu-id="c7224-106">O exemplo de código usa o objeto [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) que oferece suporte à exportação de informações de uma pasta de calendário para o formato iCalendar.</span><span class="sxs-lookup"><span data-stu-id="c7224-106">The code sample uses the [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object that supports exporting information from a calendar folder to the iCalendar format.</span></span>

<span data-ttu-id="c7224-107">O exemplo de código primeiro chama [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) na pasta Calendário padrão para receber um objeto **CalendarSharing**.</span><span class="sxs-lookup"><span data-stu-id="c7224-107">The code sample first calls [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) on the default Calendar folder to obtain a **CalendarSharing** object.</span></span> <span data-ttu-id="c7224-108">Em seguida, ele define propriedades do objeto **CalendarSharing** para especificar critérios para a exportação, como o intervalo de datas das informações do calendário, se deseja incluir anexos e detalhes dos compromissos marcados como "particulares".</span><span class="sxs-lookup"><span data-stu-id="c7224-108">Then it sets properties of the **CalendarSharing** object to specify criteria for the export, such as the date range of calendar information, whether to include attachments, and details of appointments that are marked "private."</span></span>

<span data-ttu-id="c7224-109">Para enviar as informações de calendário por email, o exemplo de código chama o método [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) do objeto **CalendarSharing**.</span><span class="sxs-lookup"><span data-stu-id="c7224-109">To send the calendar information by email, the code sample calls the [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) method of the **CalendarSharing** object.</span></span>

<span data-ttu-id="c7224-110">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c7224-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c7224-111">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="c7224-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c7224-112">As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="c7224-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub SendNextWeekToAddress(ByVal sendToAddresses As String)
    If String.IsNullOrEmpty(sendToAddresses) Then
        Throw New ArgumentException( _
            "Parameter must contain a value.", "sendToAddress")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = False
    exporter.RestrictToWorkingHours = False
    exporter.StartDate = DateTime.Today.Date
    exporter.EndDate = DateTime.Today.Date.AddDays(7)

    '' Create a new mail item
    Dim calendarMail As Outlook.MailItem = exporter.ForwardAsICal _
        (Outlook.OlCalendarMailFormat. _
        olCalendarMailFormatDailySchedule)
    calendarMail.To = sendToAddresses
    calendarMail.Send()
    calendarMail.Display()
End Sub
```

```csharp
private void SendNextWeekToAddress(string sendToAddresses)
{
    if (string.IsNullOrEmpty(sendToAddresses))
        throw new ArgumentException(
        "sendToAddress","Parameter must contain a value.");
    Outlook.Folder calendar = 
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = false;
    exporter.RestrictToWorkingHours = false;
    exporter.StartDate = DateTime.Today.Date;
    exporter.EndDate = DateTime.Today.Date.AddDays(7);

    // Create a new mail item
    Outlook.MailItem calendarMail = 
        exporter.ForwardAsICal(Outlook.OlCalendarMailFormat.
        olCalendarMailFormatDailySchedule);
    calendarMail.To = sendToAddresses;
    ((Outlook.MailItemClass)calendarMail).Send();
    ((Outlook.MailItemClass)calendarMail).Display(Type.Missing);
}
```

## <a name="see-also"></a><span data-ttu-id="c7224-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7224-113">See also</span></span>

- [<span data-ttu-id="c7224-114">Calendar</span><span class="sxs-lookup"><span data-stu-id="c7224-114">Calendar</span></span>](calendar.md)

