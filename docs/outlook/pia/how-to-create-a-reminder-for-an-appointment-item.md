---
title: Criar um lembrete para um item de compromisso
TOCTitle: Create a reminder for an appointment item
ms:assetid: 85e772f0-65ac-4abc-8286-9099882a2400
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184623(v=office.15)
ms:contentKeyID: 55119814
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 164e744e03ab0984265736673c71d2d0bf57bf45
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405970"
---
# <a name="create-a-reminder-for-an-appointment-item"></a>Criar um lembrete para um item de compromisso

Este exemplo usa a propriedade [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) para criar um lembrete para um item do compromisso.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


O Outlook fornece uma maneira de definir um lembrete para um compromisso usando a propriedade [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) do objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Esta propriedade indica se um lembrete foi criado para o compromisso. Definir a propriedade ReminderSet como true cria um lembrete e defini-la como false remove o lembrete.

No exemplo de código a seguir, ReminderExample cria um lembrete em um compromisso particular para degustação de vinhos em Napa, Califórnia, e define o lembrete para ocorrer duas horas antes do início do compromisso. Primeiro, ReminderExample cria um objeto **AppointmentItem** do Outlook. Em seguida, define a propriedade [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) do item para [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)). Isso indica que o compromisso é um compromisso particular. Depois de definir outras propriedades do compromisso, como os horários de [Início](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) e [Fim](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), o ReminderExample define a propriedade [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) para indicar o número de minutos em que o lembrete aparecerá antes do início do compromisso. Nesse caso, ReminderMinutesBeforeStart é definida para 120 minutos (duas horas).

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void ReminderExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Wine Tasting";
    appt.Location = "Napa CA";
    appt.Sensitivity = Outlook.OlSensitivity.olPrivate;
    appt.Start = DateTime.Parse("10/21/2006 10:00 AM");
    appt.End = DateTime.Parse("10/21/2006 3:00 PM");
    appt.ReminderSet = true;
    appt.ReminderMinutesBeforeStart = 120;
    appt.Save();
}
```

## <a name="see-also"></a>Confira também

- [Compromissos](appointments.md)

