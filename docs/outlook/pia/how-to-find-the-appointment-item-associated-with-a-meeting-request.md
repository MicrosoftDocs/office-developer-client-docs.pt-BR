---
title: Localizar o item de compromisso associado a uma solicitação de reunião
TOCTitle: Find the appointment item associated with a meeting request
ms:assetid: ff356fcf-0980-4567-8570-4bbcb14381e7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184658(v=office.15)
ms:contentKeyID: 55119875
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43bc64dbbed14dae2e185ea89d15b6061858de42
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703283"
---
# <a name="find-the-appointment-item-associated-with-a-meeting-request"></a><span data-ttu-id="2a89d-102">Localizar o item de compromisso associado a uma solicitação de reunião</span><span class="sxs-lookup"><span data-stu-id="2a89d-102">Find the appointment item associated with a meeting request</span></span>

<span data-ttu-id="2a89d-103">Este exemplo mostra como usar o método [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) para localizar o compromisso associado a uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="2a89d-103">This example shows how to use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to find the appointment that is associated with a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="2a89d-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2a89d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="2a89d-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="2a89d-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="2a89d-106">Um objeto [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) não representa um compromisso, mas uma mensagem que contém uma solicitação para adicionar um compromisso ao calendário do destinatário.</span><span class="sxs-lookup"><span data-stu-id="2a89d-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object does not represent an appointment, but a message that contains a request to add an appointment to the recipient’s calendar.</span></span> <span data-ttu-id="2a89d-107">No exemplo de código a seguir, MeetingRequestExample usa o método [GetAssociatedAppointment (Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) do objeto **MeetingItem** em cada **MeetingItem** recuperado da Caixa de Entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="2a89d-107">In the following code example, MeetingRequestExample uses the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method of the **MeetingItem** object on each **MeetingItem** retrieved from the user’s Inbox.</span></span> <span data-ttu-id="2a89d-108">O objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) retornado é então usado para escrever o assunto do compromisso para os ouvintes de rastreamento da coleção [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="2a89d-108">The returned [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object is then used to write the subject of the appointment to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="2a89d-109">Observe que o argumento **GetAssociatedAppointment** está definido como **false** para que o compromisso não seja adicionado ao calendário do usuário.</span><span class="sxs-lookup"><span data-stu-id="2a89d-109">Note that **GetAssociatedAppointment** argument is set to **false** so that the appointment is not added to the user’s calendar.</span></span>

<span data-ttu-id="2a89d-110">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="2a89d-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="2a89d-111">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="2a89d-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="2a89d-112">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="2a89d-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void MeetingRequestsExample()
{
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(false);
        if (appt != null)
        {
            Debug.WriteLine(appt.Subject);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="2a89d-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a89d-113">See also</span></span>

- [<span data-ttu-id="2a89d-114">Solicitações de reunião</span><span class="sxs-lookup"><span data-stu-id="2a89d-114">Meeting requests</span></span>](meeting-requests.md)

