---
title: Solicitar que um usuário responda a uma solicitação de reunião
TOCTitle: Prompt a user to respond to a meeting request
ms:assetid: a0d69f82-8659-457d-9418-1a897a10882f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184630(v=office.15)
ms:contentKeyID: 55119877
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26e59cca7431e9f11f3fea5fa058548b9a5903a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722610"
---
# <a name="prompt-a-user-to-respond-to-a-meeting-request"></a><span data-ttu-id="10330-102">Solicitar que um usuário responda a uma solicitação de reunião</span><span class="sxs-lookup"><span data-stu-id="10330-102">Prompt a user to respond to a meeting request</span></span>

<span data-ttu-id="10330-103">Este exemplo mostra como solicitar ao usuário uma resposta à solicitação de reunião e permitir que ele edite a resposta antes de enviá-la.</span><span class="sxs-lookup"><span data-stu-id="10330-103">This example shows how to prompt the user for a response to a meeting request, and to enable the user to edit the response before sending it.</span></span>

## <a name="example"></a><span data-ttu-id="10330-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="10330-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="10330-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="10330-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="10330-106">O método [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) do objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) é usado para notificar o organizador da reunião sobre se ela foi aceita, recusada ou provisoriamente adicionada ao calendário do destinatário.</span><span class="sxs-lookup"><span data-stu-id="10330-106">The [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object is used to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient’s calendar.</span></span> <span data-ttu-id="10330-107">Ao usar o método **Respond**, você pode indicar se deseja enviar a notificação automaticamente ou se deseja permitir que o usuário edite a resposta antes de enviá-la.</span><span class="sxs-lookup"><span data-stu-id="10330-107">By using the **Respond** method, you can indicate whether you want to send the notification automatically, or whether you want to allow the user to edit the response before sending it.</span></span> <span data-ttu-id="10330-108">O método **Respond** aceita três parâmetros.</span><span class="sxs-lookup"><span data-stu-id="10330-108">The **Respond** method accepts three parameters.</span></span> <span data-ttu-id="10330-109">O parâmetro *Response* indica se a resposta é aceitar, recusar, ou provisório.</span><span class="sxs-lookup"><span data-stu-id="10330-109">The *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="10330-110">Os parâmetros *fNoUI* e *fAdditionalTextDialog* são valores **bool** que indicam se a resposta será enviada para o organizador ou não e determinam se o usuário pode ou não editar o corpo da resposta antes de enviá-la, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="10330-110">The *fNoUI* and *fAdditionalTextDialog* parameters are **bool** values that indicate whether the response will be sent to the organizer, and whether the user can edit the body of the response before sending it, respectively.</span></span> 

<span data-ttu-id="10330-111">No exemplo código a seguir, PromptUserMeetingRequest enumera por meio de objetos [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) para que obter os objetos **AppointmentItem** associados, e chama o método **Respond** com o parâmetro *fNoUI* definido como **false** e o parâmetro *fAdditionalTextDialog* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="10330-111">In the following code example, PromptUserMeetingRequest enumerates through the [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) objects to get the associated **AppointmentItem** objects, and then calls the **Respond** method with the *fNoUI* parameter set to **false** and the *fAdditionalTextDialog* parameter set to **true**.</span></span> <span data-ttu-id="10330-112">Isso permite ao usuário escolher se deseja enviar uma resposta e se deseja editar o corpo da resposta antes de enviá-la.</span><span class="sxs-lookup"><span data-stu-id="10330-112">This allows the user to choose whether to send a response, and whether to edit the body of the response before sending it.</span></span>

<span data-ttu-id="10330-113">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="10330-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="10330-114">O \*\* que usa a instrução\*\* não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="10330-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="10330-115">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="10330-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void PromptUserMeetingRequest()
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
                false, true);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="10330-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="10330-116">See also</span></span>

- [<span data-ttu-id="10330-117">Solicitações de reunião</span><span class="sxs-lookup"><span data-stu-id="10330-117">Meeting requests</span></span>](meeting-requests.md)

