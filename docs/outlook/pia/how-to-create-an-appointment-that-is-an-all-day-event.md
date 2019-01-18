---
title: Criar um compromisso que é um evento de dia inteiro
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5065395afe39247f8113bc5223b0e3e403a02fa
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710822"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a><span data-ttu-id="726b5-102">Criar um compromisso que é um evento de dia inteiro</span><span class="sxs-lookup"><span data-stu-id="726b5-102">Create an appointment that is an all-day event</span></span>

<span data-ttu-id="726b5-103">Esse exemplo mostra como usar a propriedade [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) para criar um compromisso que é um evento de dia inteiro.</span><span class="sxs-lookup"><span data-stu-id="726b5-103">This example shows how use the [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) property to create an appointment that is an all-day event.</span></span>

## <a name="example"></a><span data-ttu-id="726b5-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="726b5-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="726b5-105">O exemplo a seguir é um trecho da [programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="726b5-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="726b5-106">Um evento é diferente de um compromisso normal, porque é uma atividade com duração de 24 horas ou mais.</span><span class="sxs-lookup"><span data-stu-id="726b5-106">An event is different from a regular appointment because it is an activity that lasts 24 hours or longer.</span></span> <span data-ttu-id="726b5-107">Feiras de negócios, seminários ou férias são exemplos de eventos.</span><span class="sxs-lookup"><span data-stu-id="726b5-107">Examples of events include trade shows, seminars, or vacations.</span></span> <span data-ttu-id="726b5-108">Eventos e eventos anuais serão exibidos como períodos de tempo bloqueados no calendário do usuário.</span><span class="sxs-lookup"><span data-stu-id="726b5-108">Events and annual events do not appear as occupied blocks of time in the user’s calendar.</span></span> <span data-ttu-id="726b5-109">Em vez disso, eles aparecem como faixas.</span><span class="sxs-lookup"><span data-stu-id="726b5-109">Instead, they appear as banners.</span></span> <span data-ttu-id="726b5-110">Você pode ver faixas na parte superior de uma exibição de dia ou semana do calendário.</span><span class="sxs-lookup"><span data-stu-id="726b5-110">You can see the banners at the top of a calendar day or week view.</span></span> <span data-ttu-id="726b5-111">Para um compromisso de dia inteiro, por padrão, a hora do usuário é exibida como ocupado quando visto por outras pessoas, mas a hora do usuário é exibida como gratuitamente por um evento ou evento.</span><span class="sxs-lookup"><span data-stu-id="726b5-111">For an all-day appointment, by default, the user’s time is displayed as busy when viewed by other people, but the user’s time is displayed as free for an event or annual event.</span></span>

<span data-ttu-id="726b5-112">Para criar um evento de dia inteiro por programação, defina a propriedade[AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) propriedade do objeto[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) como verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="726b5-112">To create an all-day event programmatically, set the [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) property of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object to true.</span></span> <span data-ttu-id="726b5-113">Defina as propriedades [início](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) e [final](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) do AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="726b5-113">Then set the [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) properties of the AppointmentItem.</span></span> <span data-ttu-id="726b5-114">Se você definir a propriedade AllDayEvent como verdadeira e não configurar as propriedades de início e de término, o evento ocorrerá no dia e ele será um compromisso, mostrando o status de ocupado em seu calendário.</span><span class="sxs-lookup"><span data-stu-id="726b5-114">If you set the AllDayEvent property to true and do not set the Start and End properties, the event will occur today, and it will be an appointment, showing a busy status on your calendar.</span></span> <span data-ttu-id="726b5-115">Se quiser que o evento que ocorra em uma data futura, você deve definir as propriedades de início e de término.</span><span class="sxs-lookup"><span data-stu-id="726b5-115">You must set the Start and End properties if you want the event to occur on a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="726b5-116">Para tornar o compromisso de dia inteiro, você deve definir a propriedade de início às 0:00</span><span class="sxs-lookup"><span data-stu-id="726b5-116">To make the appointment an all-day event, you must set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="726b5-117">(meia-noite) do dia em que você deseja que o evento comece e, em seguida, defina a propriedade de final para meia-noite</span><span class="sxs-lookup"><span data-stu-id="726b5-117">(midnight) on the day you want the event to begin, and set End property to 12:00 A.M.</span></span> <span data-ttu-id="726b5-118">do dia depois que você deseja finalizar o evento.</span><span class="sxs-lookup"><span data-stu-id="726b5-118">on the day after you want the event to end.</span></span> <span data-ttu-id="726b5-119">Se você definir a hora de início e término com um valor de data e hora diferente de meia-noite, o compromisso se tornará um compromisso de vários dias em vez de um evento de um dia inteiro.</span><span class="sxs-lookup"><span data-stu-id="726b5-119">If you set the Start or End time to a date and time value other than 12:00 A.M., the appointment will become a multiday appointment instead of an all-day event.</span></span> 
>
> <span data-ttu-id="726b5-120">Por exemplo, se a duração do evento é apenas um dia, defina a propriedade de início como meia-noite</span><span class="sxs-lookup"><span data-stu-id="726b5-120">For example, if your event duration is only one day, set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="726b5-121">do dia em que você deseja que o evento comece e, em seguida, defina a propriedade de final para meia-noite</span><span class="sxs-lookup"><span data-stu-id="726b5-121">on the day you want the event to begin, and set the End property to 12:00 A.M.</span></span> <span data-ttu-id="726b5-122">Nos dia seguinte.</span><span class="sxs-lookup"><span data-stu-id="726b5-122">on the following day.</span></span> <span data-ttu-id="726b5-123">Você sempre deve definir a propriedade de final de meia-noite</span><span class="sxs-lookup"><span data-stu-id="726b5-123">You should always set the End property to 12:00 A.M.</span></span> <span data-ttu-id="726b5-124">em uma data que é mais de um dia depois da data de início.</span><span class="sxs-lookup"><span data-stu-id="726b5-124">on a date that is more than one day after the start date.</span></span>

<span data-ttu-id="726b5-125">O exemplo a seguir, AllDayEventExample cria um evento de dia inteiro que começa em 11 de junho de 2007 e termina em 15 de junho de 2007.</span><span class="sxs-lookup"><span data-stu-id="726b5-125">In the following code example, AllDayEventExample creates an all-day event that begins on June 11, 2007, and ends on June 15, 2007.</span></span> <span data-ttu-id="726b5-126">Observe que a propriedade de término do compromisso é definida como 12:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="726b5-126">Note that the End property for the appointment is set to 12:00 A.M.</span></span> <span data-ttu-id="726b5-127">em 16 de junho de 2007.</span><span class="sxs-lookup"><span data-stu-id="726b5-127">on June 16, 2007.</span></span>

<span data-ttu-id="726b5-128">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="726b5-128">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="726b5-129">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="726b5-129">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="726b5-130">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="726b5-130">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AllDayEventExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Developer's Conference";
    appt.AllDayEvent = true;
    appt.Start = DateTime.Parse("6/11/2007 12:00 AM");
    appt.End = DateTime.Parse("6/16/2007 12:00 AM");
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="726b5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="726b5-131">See also</span></span>

- [<span data-ttu-id="726b5-132">Compromissos</span><span class="sxs-lookup"><span data-stu-id="726b5-132">Appointments</span></span>](appointments.md)

