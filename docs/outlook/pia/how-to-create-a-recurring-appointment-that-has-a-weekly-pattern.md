---
title: Criar um compromisso recorrente com um padrão semanal
TOCTitle: Create a recurring appointment that has a weekly pattern
ms:assetid: 20b46b26-e278-451b-9e35-36683205d164
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184595(v=office.15)
ms:contentKeyID: 55119810
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b326ad23f8cbe47e5141775eacdd2bc9302db3cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359168"
---
# <a name="create-a-recurring-appointment-that-has-a-weekly-pattern"></a><span data-ttu-id="2427f-102">Criar um compromisso recorrente com um padrão semanal</span><span class="sxs-lookup"><span data-stu-id="2427f-102">Create a recurring appointment that has a weekly pattern</span></span>

<span data-ttu-id="2427f-103">Este exemplo mostra como criar um compromisso recorrente com um padrão semanal (por exemplo, um compromisso que ocorre a cada segunda-feira, quarta-feira e sexta-feira).</span><span class="sxs-lookup"><span data-stu-id="2427f-103">This example shows how to create a recurring appointment that has a weekly pattern (for example, an appointment that occurs every Monday, Wednesday, and Friday).</span></span>

## <a name="example"></a><span data-ttu-id="2427f-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2427f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="2427f-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="2427f-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="2427f-106">Quando você cria um novo compromisso recorrente, o padrão de recorrência se baseia no período de tempo especificado quando você cria o compromisso.</span><span class="sxs-lookup"><span data-stu-id="2427f-106">When you create a new recurring appointment, the recurrence pattern is based on the time you specify when you create the appointment.</span></span> <span data-ttu-id="2427f-107">Por exemplo, se você criar um compromisso que ocorre diariamente às 13:00, o compromisso será repetido apenas às 13:00 diariamente.</span><span class="sxs-lookup"><span data-stu-id="2427f-107">For example, if you create an appointment that recurs daily at 1:00 PM, the appointment will recur only at 1:00 PM on a daily basis.</span></span> <span data-ttu-id="2427f-108">Para alterar o padrão de recorrência de um compromisso, defina as propriedades do objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) do compromisso.</span><span class="sxs-lookup"><span data-stu-id="2427f-108">To change the recurrence pattern of an appointment, set the properties of the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="2427f-109">Definir a propriedade [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) do objeto RecurrencePattern antes de definir outras propriedades RecurrencePattern.</span><span class="sxs-lookup"><span data-stu-id="2427f-109">Set the [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) property of the RecurrencePattern object before setting other RecurrencePattern properties.</span></span> <span data-ttu-id="2427f-110">A tabela a seguir mostra propriedades válidas de RecurrencePattern para um determinado RecurrenceType (especificado pela enumeração [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="2427f-110">The following table shows valid RecurrencePattern properties for a given RecurrenceType (specified by the [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\)) enumeration).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2427f-111">Valor de OlRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="2427f-111">OlRecurrenceType value</span></span></p></th>
<th><p><span data-ttu-id="2427f-112">Propriedades RecurrencePattern válidas</span><span class="sxs-lookup"><span data-stu-id="2427f-112">Valid RecurrencePattern properties</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2427f-113">olRecursDaily</span><span class="sxs-lookup"><span data-stu-id="2427f-113">olRecursDaily</span></span></p></td>
<td><p><span data-ttu-id="2427f-114"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></span><span class="sxs-lookup"><span data-stu-id="2427f-114"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2427f-115">olRecursWeekly</span><span class="sxs-lookup"><span data-stu-id="2427f-115">olRecursWeekly</span></span></p></td>
<td><p><span data-ttu-id="2427f-116"><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="2427f-116"><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2427f-117">olRecursMonthly</span><span class="sxs-lookup"><span data-stu-id="2427f-117">olRecursMonthly</span></span></p></td>
<td><p><span data-ttu-id="2427f-118"><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="2427f-118"><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2427f-119">olRecursMonthNth</span><span class="sxs-lookup"><span data-stu-id="2427f-119">olRecursMonthNth</span></span></p></td>
<td><p><span data-ttu-id="2427f-120">DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="2427f-120">DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2427f-121">olRecursYearly</span><span class="sxs-lookup"><span data-stu-id="2427f-121">olRecursYearly</span></span></p></td>
<td><p><span data-ttu-id="2427f-122">DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="2427f-122">DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2427f-123">olRecursYearNth</span><span class="sxs-lookup"><span data-stu-id="2427f-123">olRecursYearNth</span></span></p></td>
<td><p><span data-ttu-id="2427f-124">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="2427f-124">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2427f-125">Ao trabalhar com itens de compromisso recorrente, você deve liberar referências anteriores, obter novas referências para o item de compromisso recorrente antes de acessar ou modificar o item e liberar essas referências assim que tiver terminado e salvado as alterações.</span><span class="sxs-lookup"><span data-stu-id="2427f-125">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="2427f-126">Essa prática aplica o objeto **AppointmentItem** recorrente e a qualquer objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="2427f-126">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="2427f-127">Para liberar uma referência no Visual Basic, defina esse objeto existente como Nothing.</span><span class="sxs-lookup"><span data-stu-id="2427f-127">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="2427f-128">Em C\#, libere explicitamente a memória para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="2427f-128">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="2427f-p103">Observe que mesmo após liberar sua referência e tentar obter uma nova referência, se ainda houver uma referência ativa (mantida por outro suplemento ou pelo Outlook) para um dos objetos acima, sua nova referência continuará a apontar para uma cópia desatualizada do objeto. Portanto, é importante liberar suas referências assim que seu compromisso recorrente terminar.</span><span class="sxs-lookup"><span data-stu-id="2427f-p103">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="2427f-131">No exemplo de código a seguir, RecurringAppointmentEveryMondayWednesdayFriday cria um objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) e chama [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) para obter o objeto RecurrencePattern recém-criado do compromisso.</span><span class="sxs-lookup"><span data-stu-id="2427f-131">In the following code example, RecurringAppointmentEveryMondayWednesdayFriday creates an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, and then calls [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) to get the newly created appointment’s RecurrencePattern object.</span></span> <span data-ttu-id="2427f-132">RecurringAppointmentEveryMondayWednesdayFriday então define as propriedades RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime e Subject, salva o compromisso e, por fim, exibe o compromisso com o padrão "Ocorre todas as segundas, quartas e sextas-feira desde 10/7/2006 até 25/8/2006, de 14:00 a 15:00."</span><span class="sxs-lookup"><span data-stu-id="2427f-132">RecurringAppointmentEveryMondayWednesdayFriday then sets the RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime, and Subject properties, saves the appointment, and finally displays the appointment with the pattern "Occurs every Monday, Wednesday, and Friday effective 7/10/2006 until 8/25/2006 from 2:00 PM to 3:00 PM."</span></span>

<span data-ttu-id="2427f-133">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="2427f-133">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="2427f-134">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="2427f-134">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="2427f-135">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="2427f-135">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringAppointmentEveryMondayWednesdayFriday()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring Appointment DaysOfWeekMask Example";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursWeekly;
    // Logical OR for DayOfWeekMask creates pattern
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday |
        Outlook.OlDaysOfWeek.olWednesday |
        Outlook.OlDaysOfWeek.olFriday;
    pattern.PatternStartDate = DateTime.Parse("7/10/2006");
    pattern.PatternEndDate = DateTime.Parse("8/25/2006");
    pattern.Duration = 60;
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("3:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="2427f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="2427f-136">See also</span></span>

- [<span data-ttu-id="2427f-137">Compromissos</span><span class="sxs-lookup"><span data-stu-id="2427f-137">Appointments</span></span>](appointments.md)

