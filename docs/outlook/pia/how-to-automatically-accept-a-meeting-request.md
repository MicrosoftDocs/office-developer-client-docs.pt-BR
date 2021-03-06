---
title: Aceitar automaticamente uma solicitação de reunião
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f546b4e2de2a77034fdfeca4d685d7b7f909f40a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359700"
---
# <a name="automatically-accept-a-meeting-request"></a>Aceitar automaticamente uma solicitação de reunião

Este exemplo mostra como usar o método [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) para automaticamente aceitar uma solicitação de reunião.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Um objeto [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) representa uma solicitação para adicionar um compromisso, representado por um objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), ao calendário de um destinatário. Para responder a uma solicitação de reunião, use o método [GetAssociatedAppointment (Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) para obter o **AppointmentItem** associado à solicitação de reunião. Em seguida, use o método [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) do objeto **AppointmentItem** para notificar o organizador da reunião sobre se ela foi aceita, recusada ou provisoriamente adicionada ao calendário do destinatário. O método **Respond** aceita três parâmetros. 

O parâmetro *Response* indica se a resposta é aceitar, recusar ou provisório. Os parâmetros fNoUI e fAdditionalTextDialog são valores **bool** que indicam se a resposta será enviada e se o usuário pode ou não editar a resposta, respectivamente. No exemplo de código a seguir, AutoAcceptMeetingRequests enumera todos os objetos **MeetingItem** para obter o **AppointmentItem** associado. Em seguida, AutoAcceptMeetingRequests usa o método **Respond** com o parâmetro *fNoUI* definido como **true** para indicar que uma resposta será enviada automaticamente para aceitar a solicitação de reunião.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Solicitações de reunião](meeting-requests.md)

