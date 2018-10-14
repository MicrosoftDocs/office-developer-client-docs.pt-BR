---
title: Criar um compromisso recorrente anual que usa um padrão YearNth
TOCTitle: Create an annual recurring appointment that uses a YearNth pattern
ms:assetid: 5fb2ad0b-248c-417d-8868-52e0550d970f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184611(v=office.15)
ms:contentKeyID: 55119811
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 9aa18f0e2f875e86acf6cacbf222577e0f9c93e2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407076"
---
# <a name="create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern"></a>Criar um compromisso recorrente anual que usa um padrão YearNth

Este exemplo mostra como criar um compromisso para o qual o padrão de recorrência anual é um dia específico, como a primeira segunda-feira de junho.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Se você quiser criar um compromisso anual com recorrência em um determinado dia da semana durante um mês específico (por exemplo, a primeira segunda-feira em junho), você deve usar recorrências YearNth. Para definir uma recorrência YearNth, primeiro você deve definir a propriedade [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) do objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) como olRecursYearNth. Depois, defina a propriedade [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)) para especificar em que dia da semana o compromisso deve se repetir, e o a propriedade [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)) para especificar a n-ésima ocorrência do dia da semana especificado (por exemplo, a terceira terça-feira) durante um mês especificado para o padrão anual.

Ao trabalhar com itens de compromisso recorrente, você deve liberar referências anteriores, obter novas referências para o item de compromisso recorrente antes de acessar ou modificar o item e liberar essas referências assim que tiver terminado e salvado as alterações. Essa prática aplica o objeto **AppointmentItem** recorrente, além de qualquer objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Para liberar uma referência no Visual Basic, defina esse objeto existente como Nothing. Em C\#, libere explicitamente a memória para esse objeto.

Observe que mesmo após liberar sua referência e tentar obter uma nova referência, se ainda houver uma referência ativa (mantida por outro suplemento ou pelo Outlook) para um dos objetos acima, sua nova referência continuará a apontar para uma cópia desatualizada do objeto. Portanto, é importante liberar suas referências assim que seu compromisso recorrente terminar.

No exemplo de código a seguir, RecurringYearNthAppointment cria um compromisso com um padrão de recorrência de YearNth. RecurringYearNthAppointment primeiro cria um compromisso recorrente criando um objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Em seguida, ele recebe o padrão de recorrência do compromisso usando o método [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)). Em seguida, ele define as seguintes propriedades RecurrencePattern: RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)) e [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)). A propriedade MonthOfYear pode levar um valor numérico de 1 a 12, onde cada número representa o mês correspondente. Quando as propriedades estão definidas, RecurringYearNthAppointment salva o compromisso e o exibe com o padrão "Ocorre na primeira segunda-feira de junho de 1/6/2007 até 6/6/2016 de 14:00 a 17:00."

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. O ** que usa a instrução** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringYearNthAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring YearNth Appointment";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearNth;
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday;
    pattern.MonthOfYear = 6;
    pattern.Instance = 1;
    pattern.Occurrences = 10;
    pattern.Duration = 180;
    pattern.PatternStartDate = DateTime.Parse("6/1/2007");
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("5:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a>Confira também

- [Compromissos](appointments.md)

