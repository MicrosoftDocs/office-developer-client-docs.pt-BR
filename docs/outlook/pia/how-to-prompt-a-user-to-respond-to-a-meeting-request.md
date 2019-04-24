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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320045"
---
# <a name="prompt-a-user-to-respond-to-a-meeting-request"></a>Solicitar que um usuário responda a uma solicitação de reunião

Este exemplo mostra como solicitar ao usuário uma resposta à solicitação de reunião e permitir que ele edite a resposta antes de enviá-la.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

O método [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) do objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) é usado para notificar o organizador da reunião sobre se ela foi aceita, recusada ou provisoriamente adicionada ao calendário do destinatário. Ao usar o método **Respond**, você pode indicar se deseja enviar a notificação automaticamente ou se deseja permitir que o usuário edite a resposta antes de enviá-la. O método **Respond** aceita três parâmetros. O parâmetro *Response* indica se a resposta é aceitar, recusar, ou provisório. Os parâmetros *fNoUI* e *fAdditionalTextDialog* são valores **bool** que indicam se a resposta será enviada para o organizador ou não e determinam se o usuário pode ou não editar o corpo da resposta antes de enviá-la, respectivamente. 

No exemplo código a seguir, PromptUserMeetingRequest enumera por meio de objetos [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) para que obter os objetos **AppointmentItem** associados, e chama o método **Respond** com o parâmetro *fNoUI* definido como **false** e o parâmetro *fAdditionalTextDialog* definido como **true**. Isso permite ao usuário escolher se deseja enviar uma resposta e se deseja editar o corpo da resposta antes de enviá-la.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Solicitações de reunião](meeting-requests.md)

