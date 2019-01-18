---
title: Criar um lembrete para um item de compromisso
TOCTitle: Create a reminder for an appointment item
ms:assetid: 85e772f0-65ac-4abc-8286-9099882a2400
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184623(v=office.15)
ms:contentKeyID: 55119814
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1f5f31c480f31b01e53fec9651c8154765b581a3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722778"
---
# <a name="create-a-reminder-for-an-appointment-item"></a><span data-ttu-id="55cd7-102">Criar um lembrete para um item de compromisso</span><span class="sxs-lookup"><span data-stu-id="55cd7-102">Create a reminder for an appointment item</span></span>

<span data-ttu-id="55cd7-103">Este exemplo usa a propriedade [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) para criar um lembrete para um item do compromisso.</span><span class="sxs-lookup"><span data-stu-id="55cd7-103">This example shows how to use the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property to create a reminder for an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="55cd7-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="55cd7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="55cd7-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="55cd7-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="55cd7-106">O Outlook fornece uma maneira de definir um lembrete para um compromisso usando a propriedade [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) do objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="55cd7-106">Outlook provides a way to set a reminder for an appointment by using the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="55cd7-107">Esta propriedade indica se um lembrete foi criado para o compromisso.</span><span class="sxs-lookup"><span data-stu-id="55cd7-107">This property indicates whether a reminder has been created for the appointment.</span></span> <span data-ttu-id="55cd7-108">Definir a propriedade ReminderSet como true cria um lembrete e defini-la como false remove o lembrete.</span><span class="sxs-lookup"><span data-stu-id="55cd7-108">Setting the ReminderSet property to true creates a reminder, and setting it to false removes the reminder.</span></span>

<span data-ttu-id="55cd7-109">No exemplo de código a seguir, ReminderExample cria um lembrete em um compromisso particular para degustação de vinhos em Napa, Califórnia, e define o lembrete para ocorrer duas horas antes do início do compromisso.</span><span class="sxs-lookup"><span data-stu-id="55cd7-109">In the following code example, ReminderExample creates a reminder on a private appointment for wine tasting in Napa, California, and sets the reminder to occur two hours before the appointment starts.</span></span> <span data-ttu-id="55cd7-110">Primeiro, ReminderExample cria um objeto **AppointmentItem** do Outlook.</span><span class="sxs-lookup"><span data-stu-id="55cd7-110">First, ReminderExample creates an Outlook **AppointmentItem** object.</span></span> <span data-ttu-id="55cd7-111">Em seguida, define a propriedade [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) do item para [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="55cd7-111">It then sets the [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) property for the item to [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)).</span></span> <span data-ttu-id="55cd7-112">Isso indica que o compromisso é um compromisso particular.</span><span class="sxs-lookup"><span data-stu-id="55cd7-112">This indicates that the appointment is a private appointment.</span></span> <span data-ttu-id="55cd7-113">Depois de definir outras propriedades do compromisso, como os horários de [Início](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) e [Fim](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), o ReminderExample define a propriedade [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) para indicar o número de minutos em que o lembrete aparecerá antes do início do compromisso.</span><span class="sxs-lookup"><span data-stu-id="55cd7-113">After setting other properties of the appointment, such as [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) times, ReminderExample sets the [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) property to indicate the number of minutes that the reminder will appear before the start of the appointment.</span></span> <span data-ttu-id="55cd7-114">Nesse caso, ReminderMinutesBeforeStart é definida para 120 minutos (duas horas).</span><span class="sxs-lookup"><span data-stu-id="55cd7-114">In this case, ReminderMinutesBeforeStart is set to 120 minutes (two hours).</span></span>

<span data-ttu-id="55cd7-115">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="55cd7-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="55cd7-116">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="55cd7-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="55cd7-117">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="55cd7-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void ReminderExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Wine Tasting";
    appt.Location = "Napa CA";
    appt.Sensitivity = Outlook.OlSensitivity.olPrivate;
    appt.Start = DateTime.Parse("10/21/2006 10:00 AM");
    appt.End = DateTime.Parse("10/21/2006 3:00 PM");
    appt.ReminderSet = true;
    appt.ReminderMinutesBeforeStart = 120;
    appt.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="55cd7-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="55cd7-118">See also</span></span>

- [<span data-ttu-id="55cd7-119">Compromissos</span><span class="sxs-lookup"><span data-stu-id="55cd7-119">Appointments</span></span>](appointments.md)

