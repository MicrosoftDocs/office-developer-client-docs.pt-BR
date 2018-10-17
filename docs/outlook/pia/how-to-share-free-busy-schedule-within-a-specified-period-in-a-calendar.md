---
title: Compartilhar cronograma de disponibilidade em um período específico de um calendário
TOCTitle: Share Free/Busy schedule within a specified period in a calendar
ms:assetid: 1d038f56-80dd-42fd-809b-f5b3a47cd5ee
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609503(v=office.15)
ms:contentKeyID: 55119824
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 359b328002b711930eab6c029474b3b39cbc184e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406187"
---
# <a name="share-freebusy-schedule-within-a-specified-period-in-a-calendar"></a><span data-ttu-id="eaf18-102">Compartilhar cronograma de disponibilidade em um período específico de um calendário</span><span class="sxs-lookup"><span data-stu-id="eaf18-102">Share Free/Busy schedule within a specified period in a calendar</span></span>

<span data-ttu-id="eaf18-103">Este exemplo obtém o cronograma de disponibilidade de determinada semana e exibe os detalhes de disponibilidade e assunto para o usuário.</span><span class="sxs-lookup"><span data-stu-id="eaf18-103">This example obtains the Free/Busy schedule within a specified week from a calendar and displays the free, busy, and subject details to the user.</span></span>

## <a name="example"></a><span data-ttu-id="eaf18-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="eaf18-104">Example</span></span>

<span data-ttu-id="eaf18-105">Este exemplo de código usa o método [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) do objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) para obter um objeto [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) para a pasta padrão Calendário em um período específico de uma semana.</span><span class="sxs-lookup"><span data-stu-id="eaf18-105">This code sample uses the [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) method of the [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object to obtain a [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object for the default Calendar folder for a specific one-week period.</span></span> <span data-ttu-id="eaf18-106">Em seguida, chama o método [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) no objeto **CalendarSharing** e exibe a mensagem com uma carga iCalendar.</span><span class="sxs-lookup"><span data-stu-id="eaf18-106">It then calls the [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) method on the **CalendarSharing** object and displays the message with an iCalendar payload.</span></span>

<span data-ttu-id="eaf18-107">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="eaf18-107">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="eaf18-108">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="eaf18-108">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="eaf18-109">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="eaf18-109">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub DemoCalendarSharing()
    ' Get instance of CalendarSharing object
    Dim calShare As Outlook.CalendarSharing = _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar). _
        GetCalendarExporter()
    ' Free busy and subject details
    calShare.CalendarDetail = _
        Outlook.OlCalendarDetail.olFreeBusyAndSubject
    ' Set start and end dates
    calShare.StartDate = DateTime.Today
    calShare.EndDate = calShare.StartDate.AddDays(1)
    ' Call ForwardAsICal method
    Dim mail As Outlook.MailItem = _
        calShare.ForwardAsICal( _
        Outlook.OlCalendarMailFormat.olCalendarMailFormatDailySchedule)
    ' Add recipient
    mail.Recipients.Add("someone@example.com")
    mail.Recipients.ResolveAll()
    ' Set subject
    Dim CalName As String = _
    Application.Session.GetDefaultFolder( _
    Outlook.OlDefaultFolders.olFolderCalendar).Name
    mail.Subject = _
        Application.Session.CurrentUser.Name & _
        CalName.PadLeft(CalName.Length + 1)
    ' Display calendar sharing item
    mail.Display(False)
End Sub
```

```csharp
private void DemoCalendarSharing()
{
    // Get instance of CalendarSharing object
    Outlook.CalendarSharing calShare =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderCalendar).
        GetCalendarExporter();
    // Free busy and subject details
    calShare.CalendarDetail =
        Outlook.OlCalendarDetail.olFreeBusyAndSubject;
    // Set start and end dates
    calShare.StartDate = DateTime.Today;
    calShare.EndDate = calShare.StartDate.AddDays(1);
    // Call ForwardAsICal method
    Outlook.MailItem mail =
        calShare.ForwardAsICal(Outlook.OlCalendarMailFormat
        .olCalendarMailFormatDailySchedule);
    // Add recipient
    mail.Recipients.Add("someone@example.com");
    mail.Recipients.ResolveAll();
    // Set subject
    string CalName =
        Application.Session.GetDefaultFolder
    (Outlook.OlDefaultFolders.olFolderCalendar).Name;
    mail.Subject =
        Application.Session.CurrentUser.Name +
        CalName.PadLeft(CalName.Length + 1);
    // Display calendar sharing item
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="eaf18-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="eaf18-110">See also</span></span>

- [<span data-ttu-id="eaf18-111">Calendário</span><span class="sxs-lookup"><span data-stu-id="eaf18-111">Calendar</span></span>](calendar.md)

