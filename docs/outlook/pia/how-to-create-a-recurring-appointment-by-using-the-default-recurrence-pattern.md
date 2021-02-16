---
title: Criar um compromisso recorrente que usa o padrão de recorrência padrão
TOCTitle: Create a recurring appointment by using the default recurrence pattern
ms:assetid: 157bf1ae-2efe-4783-99ea-606722dde204
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184589(v=office.15)
ms:contentKeyID: 55119809
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: de58523e663349c43cc358f5b76896987a0f23b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332113"
---
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a><span data-ttu-id="c4436-102">Criar um compromisso recorrente que usa o padrão de recorrência padrão</span><span class="sxs-lookup"><span data-stu-id="c4436-102">Create a recurring appointment by using the default recurrence pattern</span></span>

<span data-ttu-id="c4436-103">Este exemplo mostra como criar um compromisso recorrente usando o padrão de recorrência padrão.</span><span class="sxs-lookup"><span data-stu-id="c4436-103">This example shows how to create a recurring appointment by using the default recurrence pattern.</span></span>

## <a name="example"></a><span data-ttu-id="c4436-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c4436-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c4436-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="c4436-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="c4436-106">Ao criar um compromisso no Outlook, você está criando um objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c4436-106">When you create an appointment in Outlook, you are creating an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="c4436-107">Seu compromisso será um compromisso recorrente se a propriedade [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) do AppointmentItem estiver definida como true.</span><span class="sxs-lookup"><span data-stu-id="c4436-107">Your appointment is a recurring appointment if the [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) property of the AppointmentItem is set to true.</span></span> <span data-ttu-id="c4436-108">IsRecurring não pode ser definido diretamente.</span><span class="sxs-lookup"><span data-stu-id="c4436-108">IsRecurring cannot be set directly.</span></span> 

<span data-ttu-id="c4436-109">No entanto, é possível criar um compromisso recorrente usando o objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c4436-109">However, you can create a recurring appointment by using the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="c4436-110">Para criar um compromisso recorrente programaticamente, crie um objeto **AppointmentItem**, chame o método [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) do objeto **AppointmentItem** e, em seguida, salve o objeto **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="c4436-110">To create a recurring appointment programmatically, create an **AppointmentItem** object, call the [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) method of the **AppointmentItem** object, and then save the **AppointmentItem** object.</span></span> <span data-ttu-id="c4436-111">Isso cria um compromisso que usa o padrão de recorrência padrão que ocorre semanalmente no dia da semana para o qual o compromisso foi criado e não tem data de término.</span><span class="sxs-lookup"><span data-stu-id="c4436-111">This creates an appointment that uses the default recurrence pattern, which occurs weekly on the day of the week for which the appointment was created, and has no end date.</span></span> <span data-ttu-id="c4436-112">O objeto RecurrencePattern permite a criação de compromissos recorrentes em intervalos especificados: diário, semanal, mensal ou anual.</span><span class="sxs-lookup"><span data-stu-id="c4436-112">The RecurrencePattern object allows you to create recurring appointments at specified intervals—daily, weekly, monthly, or yearly.</span></span> <span data-ttu-id="c4436-113">Se você não especificar intervalos para o objeto RecurrencePattern, o Outlook usará o padrão de recorrência padrão.</span><span class="sxs-lookup"><span data-stu-id="c4436-113">If you do not specify intervals for the RecurrencePattern object, Outlook will use the default recurrence pattern.</span></span>

<span data-ttu-id="c4436-114">Ao trabalhar com itens de compromisso recorrente, você deve liberar referências anteriores, obter novas referências para o item de compromisso recorrente antes de acessar ou modificar o item e liberar essas referências assim que tiver terminado e salvado as alterações.</span><span class="sxs-lookup"><span data-stu-id="c4436-114">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="c4436-115">Essa prática aplica o objeto **AppointmentItem** recorrente e a qualquer objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c4436-115">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="c4436-116">Para liberar uma referência no Visual Basic, defina esse objeto existente como Nothing.</span><span class="sxs-lookup"><span data-stu-id="c4436-116">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="c4436-117">Em C\#, libere explicitamente a memória para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="c4436-117">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="c4436-p104">Observe que mesmo após liberar sua referência e tentar obter uma nova referência, se ainda houver uma referência ativa (mantida por outro suplemento ou pelo Outlook) para um dos objetos acima, sua nova referência continuará a apontar para uma cópia desatualizada do objeto. Portanto, é importante liberar suas referências assim que seu compromisso recorrente terminar.</span><span class="sxs-lookup"><span data-stu-id="c4436-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="c4436-120">No exemplo a seguir CreateRecurringAppointment cria um objeto **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="c4436-120">In the following example, CreateRecurringAppointment creates an **AppointmentItem** object.</span></span> <span data-ttu-id="c4436-121">Em seguida, ele chama GetRecurrencePattern.</span><span class="sxs-lookup"><span data-stu-id="c4436-121">It then calls GetRecurrencePattern.</span></span> <span data-ttu-id="c4436-122">GetRecurrencePattern retorna um objeto RecurrencePattern e AppointmentItem é salvo.</span><span class="sxs-lookup"><span data-stu-id="c4436-122">GetRecurrencePattern returns a RecurrencePattern object, and the AppointmentItem is saved.</span></span> <span data-ttu-id="c4436-123">Isso cria um compromisso recorrente que usa o padrão de recorrência padrão.</span><span class="sxs-lookup"><span data-stu-id="c4436-123">This creates a recurring appointment that uses the default recurrence pattern.</span></span>

<span data-ttu-id="c4436-124">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c4436-124">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c4436-125">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="c4436-125">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c4436-126">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="c4436-126">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateRecurringAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Weekly Extensibility Team Meeting";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    appt.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="c4436-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4436-127">See also</span></span>

- [<span data-ttu-id="c4436-128">Compromissos</span><span class="sxs-lookup"><span data-stu-id="c4436-128">Appointments</span></span>](appointments.md)

