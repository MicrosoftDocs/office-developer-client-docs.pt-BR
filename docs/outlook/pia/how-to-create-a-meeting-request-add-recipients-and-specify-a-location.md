---
title: Criar uma solicitação de reunião, adicionar destinatários e especificar um local
TOCTitle: Create a meeting request, add recipients, and specify a location
ms:assetid: 3053c27e-34d9-440e-9b66-06de940c2813
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644964(v=office.15)
ms:contentKeyID: 55119873
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 0f637d3d21f79ec538d10cf509fb09f5abf0b0ac
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723086"
---
# <a name="create-a-meeting-request-add-recipients-and-specify-a-location"></a>Criar uma solicitação de reunião, adicionar destinatários e especificar um local

Este exemplo cria um item de compromisso como uma solicitação de reunião, especifica a hora, os destinatários e local da reunião e exibe o compromisso em um inspetor.

## <a name="example"></a>Exemplo

No Outlook, uma solicitação de reunião é um [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Para definir um item de compromisso como uma solicitação de reunião, defina a propriedade [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) para **olMeeting**. Use a propriedade [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) do objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) para especificar se o participante da reunião é opcional ou se um destinatário é, na verdade, um recurso da reunião em vez de um participante.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SetRecipientTypeForAppt()
    Dim appt As Outlook.AppointmentItem = _
        CType(Application.CreateItem( _
        Outlook.OlItemType.olAppointmentItem), Outlook.AppointmentItem)
    appt.Subject = "Customer Review"
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting
    appt.Location = "36/2021"
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM")
    appt.End = DateTime.Parse("10/20/2006 11:00 AM")
    Dim recipRequired As Outlook.Recipient = _
        appt.Recipients.Add("Ryan Gregg")
    recipRequired.Type = _
        Outlook.OlMeetingRecipientType.olRequired
    Dim recipOptional As Outlook.Recipient = _
        appt.Recipients.Add("Peter Allenspach")
    recipOptional.Type = _
        Outlook.OlMeetingRecipientType.olOptional
    Dim recipConf As Outlook.Recipient = _
        appt.Recipients.Add("Conf Room 36/2021 (14) AV")
    recipConf.Type = _
        Outlook.OlMeetingRecipientType.olResource
    appt.Recipients.ResolveAll()
    appt.Display(False)
End Sub
```


```csharp
private void SetRecipientTypeForAppt()
{
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Customer Review";
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Location = "36/2021";
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM");
    appt.End = DateTime.Parse("10/20/2006 11:00 AM");
    Outlook.Recipient recipRequired =
        appt.Recipients.Add("Ryan Gregg");
    recipRequired.Type =
        (int)Outlook.OlMeetingRecipientType.olRequired;
    Outlook.Recipient recipOptional =
        appt.Recipients.Add("Peter Allenspach");
    recipOptional.Type =
        (int)Outlook.OlMeetingRecipientType.olOptional;
    Outlook.Recipient recipConf =
       appt.Recipients.Add("Conf Room 36/2021 (14) AV");
    recipConf.Type =
        (int)Outlook.OlMeetingRecipientType.olResource;
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a>Confira também

- [Solicitações de reunião](meeting-requests.md)

