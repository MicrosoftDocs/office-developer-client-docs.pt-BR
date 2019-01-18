---
title: Localizar um compromisso específico em uma série de compromissos recorrentes
TOCTitle: Find a specific appointment in a recurring appointment series
ms:assetid: 01f55f04-7245-4325-a354-50a6eb270a31
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184586(v=office.15)
ms:contentKeyID: 55119812
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 19502895996d4777f2d1a6887aa80883a5398a09
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722974"
---
# <a name="find-a-specific-appointment-in-a-recurring-appointment-series"></a><span data-ttu-id="01820-102">Localizar um compromisso específico em uma série de compromissos recorrentes</span><span class="sxs-lookup"><span data-stu-id="01820-102">Find a specific appointment in a recurring appointment series</span></span>

<span data-ttu-id="01820-103">Este exemplo mostra como retornar um objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa um compromisso específico em uma série de compromissos recorrentes.</span><span class="sxs-lookup"><span data-stu-id="01820-103">This example shows how to return an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a specific appointment in a recurring appointment series.</span></span>

## <a name="example"></a><span data-ttu-id="01820-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="01820-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="01820-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="01820-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="01820-106">Para localizar uma instância de um compromisso recorrente que ocorre em uma data e hora especificadas, use o método [GetOccurrence (DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) do objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) para retornar um objeto **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="01820-106">To find an instance of a recurring appointment that occurs at a specified date and time, use the [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) method of the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object to return an **AppointmentItem** object.</span></span>

<span data-ttu-id="01820-107">Ao trabalhar com itens de compromisso recorrente, você deve liberar referências anteriores, obter novas referências para o item de compromisso recorrente antes de acessar ou modificar o item e liberar essas referências assim que tiver terminado e salvado as alterações.</span><span class="sxs-lookup"><span data-stu-id="01820-107">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="01820-108">Essa prática aplica o objeto **AppointmentItem** recorrente e a qualquer objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="01820-108">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="01820-109">Para liberar uma referência no Visual Basic, defina esse objeto existente como Nothing.</span><span class="sxs-lookup"><span data-stu-id="01820-109">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="01820-110">Em C\#, libere explicitamente a memória para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="01820-110">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="01820-p102">Observe que mesmo após liberar sua referência e tentar obter uma nova referência, se ainda houver uma referência ativa (mantida por outro suplemento ou pelo Outlook) para um dos objetos acima, sua nova referência continuará a apontar para uma cópia desatualizada do objeto. Portanto, é importante liberar suas referências assim que seu compromisso recorrente terminar.</span><span class="sxs-lookup"><span data-stu-id="01820-p102">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="01820-113">No exemplo de código a seguir, CheckOccurrenceExample usa o compromisso recorrente criado no exemplo de código em [Criar um compromisso recorrente com um padrão semanal](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="01820-113">In the following code example, CheckOccurrenceExample uses the recurring appointment that was created in the code example in [Create a Recurring Appointment That Has a Weekly Pattern](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md).</span></span> <span data-ttu-id="01820-114">Em seguida, chama o método GetOccurrence para determinar se o compromisso recorrente é iniciado na data e hora especificadas.</span><span class="sxs-lookup"><span data-stu-id="01820-114">It then calls the GetOccurrence method to determine whether the recurring appointment starts on the specified date and time.</span></span> <span data-ttu-id="01820-115">Para garantir que o procedimento continuará mesmo se as informações fornecidas não corresponderem à data e hora de início de uma instância do compromisso recorrente, o exemplo usará um bloco try… catch.</span><span class="sxs-lookup"><span data-stu-id="01820-115">To ensure that the procedure will continue even if the provided information does not match the start date and time of an instance of the recurring appointment, the example uses a try…catch block.</span></span> <span data-ttu-id="01820-116">Depois de chamar o método GetOccurrence em cada compromisso na série de compromissos recorrentes, CheckOccurrenceExample testa a variável singleAppt para determinar se ela está definida como uma referência nula, indicando que o método falhou e não retornou um objeto **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="01820-116">After calling the GetOccurrence method on every appointment in the recurring appointment series, CheckOccurrenceExample tests the singleAppt variable to determine whether it is set to a null reference, indicating that the method failed and did not return an **AppointmentItem** object.</span></span>

<span data-ttu-id="01820-117">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="01820-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="01820-118">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="01820-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="01820-119">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="01820-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CheckOccurrenceExample()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find(
        "[Subject]='Recurring Appointment DaysOfWeekMask Example'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        try
        {
            Outlook.RecurrencePattern pattern =
                appt.GetRecurrencePattern();
            Outlook.AppointmentItem singleAppt =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (singleAppt != null)
            {
                Debug.WriteLine("7/21/2006 2:00 PM occurrence found.");
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="01820-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="01820-120">See also</span></span>

- [<span data-ttu-id="01820-121">Compromissos</span><span class="sxs-lookup"><span data-stu-id="01820-121">Appointments</span></span>](appointments.md)

