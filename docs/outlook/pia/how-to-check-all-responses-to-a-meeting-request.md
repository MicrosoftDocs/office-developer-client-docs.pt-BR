---
title: Verificar todas as respostas à solicitação de reunião
TOCTitle: Check all responses to a meeting request
ms:assetid: ebe10e5a-7f04-447a-bfc1-aa8a726cb0b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184650(v=office.15)
ms:contentKeyID: 55119881
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 89f3aa7037659bb29346bb70338d535cbbc200b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359714"
---
# <a name="check-all-responses-to-a-meeting-request"></a>Verificar todas as respostas à solicitação de reunião

Este exemplo mostra como verificar o status da resposta de cada destinatário para uma solicitação de reunião.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

No exemplo de código a seguir, CheckAttendeeStatus enumera a coleção [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) para o objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), que representa uma solicitação de reunião e examina a propriedade [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) de cada objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)). Cada objeto **Recipient** representa um destinatário da solicitação de reunião. O valor da propriedade **MeetingResponseStatus** pode ser um dos seguintes valores de enumeração de [OlResponseStatus](https://msdn.microsoft.com/library/bb644655\(v=office.15\)):

- [olResponseAccepted](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseDeclined](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseNone](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseNotResponded](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseOrganized](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseTentative](https://msdn.microsoft.com/library/bb644655\(v=office.15\))

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CheckAttendeeStatus()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find("[Subject]='Sales Strategy FY2007'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            switch (recip.MeetingResponseStatus)
            {
                case Outlook.OlResponseStatus.olResponseAccepted:
                    Debug.WriteLine("Accepted: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseTentative:
                    Debug.WriteLine("Tentative: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseDeclined:
                    Debug.WriteLine("Declined: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseOrganized:
                    Debug.WriteLine("Organizer: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNone:
                    Debug.WriteLine("None: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNotResponded:
                    Debug.WriteLine("Not responded: " + recip.Name);
                    break;
            }
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Solicitações de reunião](meeting-requests.md)

