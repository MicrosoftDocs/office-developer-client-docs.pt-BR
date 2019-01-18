---
title: Especificar tipos diferentes de destinatários para um item de compromisso
TOCTitle: Specify different recipient types for an appointment item
ms:assetid: 83aedc8f-adc0-453d-8e71-1bb9aacc7993
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184622(v=office.15)
ms:contentKeyID: 55119807
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: beb29c46d590938d1650dac0c862dd5f898333fc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709177"
---
# <a name="specify-different-recipient-types-for-an-appointment-item"></a>Especificar tipos diferentes de destinatários para um item de compromisso

Este exemplo mostra como usar a enumeração [OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) para especificar tipos diferentes de destinatário para um item de compromisso.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Para adicionar destinatários a um objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa uma solicitação de reunião, use a enumeração OlMeetingRecipientType para especificar se o destinatário da mensagem é um participante obrigatório ou opcional ou um recurso (como uma sala ou equipamento).

No exemplo a seguir, SetRecipientTypeForAppt cria um objeto **AppointmentItem**, define propriedades do objeto e adiciona participantes obrigatórios e opcionais. Ele também adiciona uma sala de conferências para a reunião. Observe que a propriedade [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) está definida como [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)), indicando que o compromisso é uma solicitação de reunião.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
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

- [Compromissos](appointments.md)

