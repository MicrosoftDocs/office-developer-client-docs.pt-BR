---
title: Aceitar automaticamente uma solicitação de reunião
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d49044d87cd14c150527d518108f740b9eb319da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405732"
---
# <a name="automatically-accept-a-meeting-request"></a><span data-ttu-id="882ea-102">Aceitar automaticamente uma solicitação de reunião</span><span class="sxs-lookup"><span data-stu-id="882ea-102">Automatically accept a meeting request</span></span>

<span data-ttu-id="882ea-103">Este exemplo mostra como usar o método [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) para automaticamente aceitar uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="882ea-103">This example shows how to use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method to automatically accept a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="882ea-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="882ea-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="882ea-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="882ea-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="882ea-106">Um objeto [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) representa uma solicitação para adicionar um compromisso, representado por um objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), ao calendário de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="882ea-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object represents a request to add an appointment, represented by an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, to a recipient’s calendar.</span></span> <span data-ttu-id="882ea-107">Para responder a uma solicitação de reunião, use o método [GetAssociatedAppointment (Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) para obter o **AppointmentItem** associado à solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="882ea-107">To respond to a meeting request, use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to obtain the **AppointmentItem** associated with the meeting request.</span></span> <span data-ttu-id="882ea-108">Em seguida, use o método [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) do objeto **AppointmentItem** para notificar o organizador da reunião sobre se ela foi aceita, recusada ou provisoriamente adicionada ao calendário do destinatário.</span><span class="sxs-lookup"><span data-stu-id="882ea-108">Then use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the **AppointmentItem** to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient’s calendar.</span></span> <span data-ttu-id="882ea-109">O método **Respond** aceita três parâmetros.</span><span class="sxs-lookup"><span data-stu-id="882ea-109">The **Respond** method accepts three parameters.</span></span> 

<span data-ttu-id="882ea-110">O parâmetro *Response* indica se a resposta é aceitar, recusar ou provisório.</span><span class="sxs-lookup"><span data-stu-id="882ea-110">The *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="882ea-111">Os parâmetros fNoUI e fAdditionalTextDialog são valores **bool** que indicam se a resposta será enviada e se o usuário pode ou não editar a resposta, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="882ea-111">The fNoUI and fAdditionalTextDialog parameters are **bool** values that determine whether a response will be sent, and whether the user may or may not edit the response, respectively.</span></span> <span data-ttu-id="882ea-112">No exemplo de código a seguir, AutoAcceptMeetingRequests enumera todos os objetos **MeetingItem** para obter o **AppointmentItem** associado.</span><span class="sxs-lookup"><span data-stu-id="882ea-112">In the following code example, AutoAcceptMeetingRequests enumerates through every **MeetingItem** object to get the associated **AppointmentItem**.</span></span> <span data-ttu-id="882ea-113">Em seguida, AutoAcceptMeetingRequests usa o método **Respond** com o parâmetro *fNoUI* definido como **true** para indicar que uma resposta será enviada automaticamente para aceitar a solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="882ea-113">AutoAcceptMeetingRequests then uses the **Respond** method with the *fNoUI* parameter set to **true** to indicate that a response will be sent automatically to accept the meeting request.</span></span>

<span data-ttu-id="882ea-114">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="882ea-114">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="882ea-115">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="882ea-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="882ea-116">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="882ea-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AutoAcceptMeetingRequests()
{
    Outlook.MeetingItem mtgResponse;
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(true);
        if (appt != null)
        {
            mtgResponse = appt.Respond(
                Outlook.OlMeetingResponse.olMeetingAccepted,
                true, Type.Missing);
            mtgResponse.Send();
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="882ea-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="882ea-117">See also</span></span>

- [<span data-ttu-id="882ea-118">Solicitações de reunião</span><span class="sxs-lookup"><span data-stu-id="882ea-118">Meeting requests</span></span>](meeting-requests.md)

