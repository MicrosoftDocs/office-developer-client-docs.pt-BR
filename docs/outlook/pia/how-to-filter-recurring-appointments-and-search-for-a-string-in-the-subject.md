---
title: Filtrar compromissos recorrentes e pesquisar por uma cadeia de caracteres no assunto
TOCTitle: Filter recurring appointments and search for a string in the subject
ms:assetid: 997186aa-5264-4b19-bed6-51c38831c03d
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611267(v=office.15)
ms:contentKeyID: 55119891
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1815cc4e1314a848229f6187925377809e7200cf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406299"
---
# <a name="filter-recurring-appointments-and-search-for-a-string-in-the-subject"></a><span data-ttu-id="11b68-102">Filtrar compromissos recorrentes e pesquisar por uma cadeia de caracteres no assunto</span><span class="sxs-lookup"><span data-stu-id="11b68-102">Filter recurring appointments and search for a string in the subject</span></span>

<span data-ttu-id="11b68-103">Este exemplo filtra compromissos recorrentes que se encontram em um intervalo de datas específico em uma pasta de Calendário, e pesquisa de duas maneiras pela cadeia de caracteres "office" no assunto.</span><span class="sxs-lookup"><span data-stu-id="11b68-103">This example filters recurring appointments that fall within a date range in a Calendar folder, and then searches in two ways for the string "office" in the subject.</span></span>

## <a name="example"></a><span data-ttu-id="11b68-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="11b68-104">Example</span></span>

<span data-ttu-id="11b68-105">Para filtrar compromissos recorrentes, este exemplo de código usa o conjunto [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) em vez do objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), porque o objeto **Table** retorna apenas compromissos da série mestre e não inclui itens recorrentes na pasta.</span><span class="sxs-lookup"><span data-stu-id="11b68-105">To filter recurring appointments, this code sample uses the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection instead of the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, because the **Table** object returns only the master series appointments and does not include recurring items in the folder.</span></span> <span data-ttu-id="11b68-106">Para incluir compromissos recorrentes ao chamar o método [Find(String)](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) ou [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)), o exemplo de código define a propriedade [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) do conjunto **Items** e classifica compromissos na pasta por sua propriedade [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="11b68-106">To include recurring appointments when calling the [Find(String)](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) or [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method, the code sample sets the [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) property of the **Items** collection, and then sorts appointments in the folder by their [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) property.</span></span> <span data-ttu-id="11b68-107">Em seguida, usa uma consulta Jet para especificar as datas de início e término para as recorrências.</span><span class="sxs-lookup"><span data-stu-id="11b68-107">It then uses a Jet query to specify start and end dates for the recurrences.</span></span>

<span data-ttu-id="11b68-108">Depois de obter um conjunto **Items** de itens de compromisso recorrentes que ocorrem dentro do intervalo de datas especificado, o exemplo de código executa mais duas pesquisas usando consultas DAV de Pesquisa e Localização (DASL).</span><span class="sxs-lookup"><span data-stu-id="11b68-108">After obtaining an **Items** collection of recurring appointment items that fall within the specified range of dates, the code sample carries out two more searches using DAV Searching and Locating (DASL) queries.</span></span> <span data-ttu-id="11b68-109">A primeira pesquisa usa **Items.Find**, [FindNext](https://msdn.microsoft.com/library/bb623799\(v=office.15\)) e a palavra-chave **like** para procurar itens que tenham "office" como uma subcadeia de caracteres no assunto.</span><span class="sxs-lookup"><span data-stu-id="11b68-109">The first search uses **Items.Find**, [FindNext](https://msdn.microsoft.com/library/bb623799\(v=office.15\)), and the **like** keyword to search for items that have "office" as a substring in the subject.</span></span> <span data-ttu-id="11b68-110">A segunda pesquisa usa o método **Items.Restrict** e a palavra-chave **ci\_startswith** para procurar os itens que tenham assuntos que começam com "office".</span><span class="sxs-lookup"><span data-stu-id="11b68-110">The second search uses the **Items.Restrict** method and the **ci\_startswith** keyword to search for items that have subjects beginning with "office."</span></span>

<span data-ttu-id="11b68-111">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="11b68-111">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="11b68-112">A instrução **Imports** ou **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionada antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="11b68-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="11b68-113">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="11b68-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SearchRecurringAppointments()
    Dim appt As Outlook.AppointmentItem = Nothing
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar), _
        Outlook.Folder)
    ' Set start value
    Dim startTime As DateTime = New DateTime(2006, 8, 9, 0, 0, 0)
    ' Set end value
    Dim endTime As DateTime = New DateTime(2006, 12, 14, 0, 0, 0)
    ' Initial restriction is Jet query for date range
    Dim filter1 As String = "[Start] >= '" & startTime.ToString("g") _
        & "' AND [End] <= '" & endTime.ToString("g") & "'"
    Dim calendarItems As Outlook.Items = folder.Items.Restrict(filter1)
    calendarItems.IncludeRecurrences = True
    calendarItems.Sort("[Start]")
    ' Must use 'like' comparison for Find/FindNext
    Dim filter2 As String
    filter2 = "@SQL=" & _
        Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & _
        " like '%Office%'"
    ' Create DASL query for additional Restrict method
    Dim filter3 As String
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter3 = "@SQL=" & _
            Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & " _
            ci_startswith 'Office'"
    Else
        filter3 = "@SQL=" & _
            Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & " _
            like '%Office%'"
    End If
    ' Use Find and FindNext methods
    appt = CType(calendarItems.Find(filter2), Outlook.AppointmentItem)
    While Not (appt Is Nothing)
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(appt.Subject)
        sb.AppendLine("Start: " & appt.Start)
        sb.AppendLine("End: " & appt.End)
        Debug.WriteLine(sb.ToString())
        ' Find the next appointment
        appt = CType(calendarItems.FindNext(), Outlook.AppointmentItem)
    End While
    ' Restrict calendarItems with DASL query
    Dim restrictedItems As Outlook.Items = _
        calendarItems.Restrict(filter3)
    For Each apptItem As Outlook.AppointmentItem In restrictedItems
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(apptItem.Subject)
        sb.AppendLine("Start: " & apptItem.Start)
        sb.AppendLine("End: " & apptItem.End)
        sb.AppendLine()
        Debug.WriteLine(sb.ToString())
    Next
End Sub
```


```csharp
private void SearchRecurringAppointments()
{
    Outlook.AppointmentItem appt = null;
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    // Set start value
    DateTime start =
        new DateTime(2006, 8, 9, 0, 0, 0);
    // Set end value
    DateTime end =
        new DateTime(2006, 12, 14, 0, 0, 0);
    // Initial restriction is Jet query for date range
    string filter1 = "[Start] >= '" +
        start.ToString("g")
        + "' AND [End] <= '" +
        end.ToString("g") + "'";
    Outlook.Items calendarItems = folder.Items.Restrict(filter1);
    calendarItems.IncludeRecurrences = true;
    calendarItems.Sort("[Start]", Type.Missing);
    // Must use 'like' comparison for Find/FindNext
    string filter2;
    filter2 = "@SQL="
        + "\"" + "urn:schemas:httpmail:subject" + "\""
        + " like '%Office%'";
    // Create DASL query for additional Restrict method
    string filter3;
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter3 = "@SQL="
            + "\"" + "urn:schemas:httpmail:subject" + "\""
            + " ci_startswith 'Office'";
    }
    else
    {
        filter3 = "@SQL="
            + "\"" + "urn:schemas:httpmail:subject" + "\""
            + " like '%Office%'";
    }
    // Use Find and FindNext methods
    appt = calendarItems.Find(filter2)
        as Outlook.AppointmentItem;
    while (appt != null)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(appt.Subject);
        sb.AppendLine("Start: " + appt.Start);
        sb.AppendLine("End: " + appt.End);
        Debug.WriteLine(sb.ToString());
        // Find the next appointment
        appt = calendarItems.FindNext()
            as Outlook.AppointmentItem;
    }
    // Restrict calendarItems with DASL query
    Outlook.Items restrictedItems =
        calendarItems.Restrict(filter3);
    foreach (Outlook.AppointmentItem apptItem in restrictedItems)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(apptItem.Subject);
        sb.AppendLine("Start: " + apptItem.Start);
        sb.AppendLine("End: " + apptItem.End);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="11b68-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="11b68-114">See also</span></span>

- [<span data-ttu-id="11b68-115">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="11b68-115">Search and Filter</span></span>](search-and-filter.md)

