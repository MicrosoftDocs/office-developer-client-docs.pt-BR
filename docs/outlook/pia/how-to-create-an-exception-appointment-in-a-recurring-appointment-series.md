---
title: Criar um compromisso de exceção em uma série de compromissos recorrentes
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70e491069fd3f178371e9e8e3e6bcd8dc08e729e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356431"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a><span data-ttu-id="4dbb2-102">Criar um compromisso de exceção em uma série de compromissos recorrentes</span><span class="sxs-lookup"><span data-stu-id="4dbb2-102">Create an exception appointment in a recurring appointment series</span></span>

<span data-ttu-id="4dbb2-103">Este exemplo usa um objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) para criar uma exceção para um padrão de recorrência padrão para um compromisso.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-103">This example uses an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object to create an exception to a standard recurrence pattern for an appointment.</span></span>

## <a name="example"></a><span data-ttu-id="4dbb2-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4dbb2-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="4dbb2-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="4dbb2-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="4dbb2-106">Depois de excluir ou alterar uma ocorrência de compromisso de um compromisso recorrente, o Outlook cria um objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="4dbb2-106">Once you delete or change one appointment instance of a recurring appointment, Outlook creates an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object.</span></span> <span data-ttu-id="4dbb2-107">O objeto Exception permite que você crie uma exceção para um padrão de recorrência padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-107">The Exception object allows you to create an exception to a standard recurrence pattern.</span></span> <span data-ttu-id="4dbb2-108">As propriedades do objeto contêm as alterações feitas à instância do compromisso.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-108">The object’s properties contain the changes that were made to the appointment instance.</span></span> <span data-ttu-id="4dbb2-109">O conjunto [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) contém todos os objetos de Exception para um compromisso recorrente, e é associado o objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) do compromisso.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-109">The [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) collection contains all of the Exception objects for a recurring appointment, and is associated with the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span>

<span data-ttu-id="4dbb2-110">Para obter o objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa a exceção ao padrão de recorrência original do compromisso recorrente, use a propriedade [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) da Exception.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-110">To get the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents the exception to the original recurrence pattern of the recurring appointment, use the [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) property of the Exception.</span></span> <span data-ttu-id="4dbb2-111">Usando os métodos e propriedades do AppointmentItem retornado, você pode definir as propriedades da exceção de compromisso.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-111">By using the methods and properties of the returned AppointmentItem, you can set the properties of the appointment exception.</span></span>

<span data-ttu-id="4dbb2-112">Ao trabalhar com itens de compromisso recorrente, você deve liberar referências anteriores, obter novas referências para o item de compromisso recorrente antes de acessar ou modificar o item e liberar essas referências assim que tiver terminado e salvado as alterações.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-112">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="4dbb2-113">Essa prática aplica o objeto **AppointmentItem** recorrente e a qualquer objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="4dbb2-113">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="4dbb2-114">Para liberar uma referência no Visual Basic, defina esse objeto existente como Nothing.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-114">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="4dbb2-115">No C\#, libere explicitamente a memória para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-115">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="4dbb2-p104">Observe que, mesmo depois que você liberar a sua referência e tenta obter uma referência de nova, se ainda houver uma referência ativa, conduzida por outro suplemento ou no Outlook, como um dos objetos acima, sua nova referência continuarão a apontar para uma cópia desatualizada do objeto. Portanto, é importante que você libera seus referências tão logo terminar com um compromisso recorrente.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference, held by another add-in or Outlook, to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="4dbb2-118">No exemplo código a seguir, CreateExceptionExample altera o assunto do compromisso recorrente que foi criado no tópico [Encontrar um compromisso específico em uma série de compromissos recorrentes](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md) e, em seguida, usa a propriedade AppointmentItem do objeto Exception resultante para recuperar o AppointmentItem que corresponde à exceção do compromisso.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-118">In the following code example, CreateExceptionExample changes the subject of the recurring appointment that was created in the topic [Find a Specific Appointment in a Recurring Appointment Series](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md), and then uses the AppointmentItem property of the resulting Exception object to retrieve the AppointmentItem that corresponds to the appointment exception.</span></span> <span data-ttu-id="4dbb2-119">CreateExceptionExample em seguida altera as horas de início e término da exceção do compromisso.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-119">CreateExceptionExample then changes the start and end times of the appointment exception.</span></span>

<span data-ttu-id="4dbb2-120">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="4dbb2-121">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="4dbb2-122">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="4dbb2-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateExceptionExample()
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
            Outlook.AppointmentItem myInstance =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (myInstance != null)
            {
                myInstance.Subject = "My Exception";
                myInstance.Save();
                Outlook.RecurrencePattern newPattern =
                    appt.GetRecurrencePattern();
                Outlook.Exception myException =
                    newPattern.Exceptions[1];
                if (myException != null)
                {
                    Outlook.AppointmentItem myNewInstance =
                        myException.AppointmentItem;
                    myNewInstance.Start =
                        DateTime.Parse("7/21/2006 1:00 PM");
                    myNewInstance.End =
                        DateTime.Parse("7/21/2006 2:00 PM");
                    myNewInstance.Save();
                }
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="4dbb2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4dbb2-123">See also</span></span>

- [<span data-ttu-id="4dbb2-124">Compromissos</span><span class="sxs-lookup"><span data-stu-id="4dbb2-124">Appointments</span></span>](appointments.md)

