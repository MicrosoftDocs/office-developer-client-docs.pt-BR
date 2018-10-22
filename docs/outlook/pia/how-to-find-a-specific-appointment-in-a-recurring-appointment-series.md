---
title: Localizar um compromisso específico em uma série de compromissos recorrentes
TOCTitle: Find a specific appointment in a recurring appointment series
ms:assetid: 01f55f04-7245-4325-a354-50a6eb270a31
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184586(v=office.15)
ms:contentKeyID: 55119812
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: ab245fc0ff9b60862cebe57fbb2d996735442b89
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405865"
---
# <a name="find-a-specific-appointment-in-a-recurring-appointment-series"></a>Localizar um compromisso específico em uma série de compromissos recorrentes

Este exemplo mostra como retornar um objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa um compromisso específico em uma série de compromissos recorrentes.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Para localizar uma instância de um compromisso recorrente que ocorre em uma data e hora especificadas, use o método [GetOccurrence (DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) do objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) para retornar um objeto **AppointmentItem**.

Ao trabalhar com itens de compromisso recorrente, você deve liberar referências anteriores, obter novas referências para o item de compromisso recorrente antes de acessar ou modificar o item e liberar essas referências assim que tiver terminado e salvado as alterações. Essa prática aplica o objeto **AppointmentItem** recorrente e a qualquer objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Para liberar uma referência no Visual Basic, defina esse objeto existente como Nothing. Em C\#, libere explicitamente a memória para esse objeto.

Observe que mesmo após liberar sua referência e tentar obter uma nova referência, se ainda houver uma referência ativa (mantida por outro suplemento ou pelo Outlook) para um dos objetos acima, sua nova referência continuará a apontar para uma cópia desatualizada do objeto. Portanto, é importante liberar suas referências assim que seu compromisso recorrente terminar.

No exemplo de código a seguir, CheckOccurrenceExample usa o compromisso recorrente criado no exemplo de código em [Criar um compromisso recorrente com um padrão semanal](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md). Em seguida, chama o método GetOccurrence para determinar se o compromisso recorrente é iniciado na data e hora especificadas. Para garantir que o procedimento continuará mesmo se as informações fornecidas não corresponderem à data e hora de início de uma instância do compromisso recorrente, o exemplo usará um bloco try… catch. Depois de chamar o método GetOccurrence em cada compromisso na série de compromissos recorrentes, CheckOccurrenceExample testa a variável singleAppt para determinar se ela está definida como uma referência nula, indicando que o método falhou e não retornou um objeto **AppointmentItem**.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CheckOccurrenceExample()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find(
        "[Subject]='Recurring Appointment DaysOfWeekMask Example'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        try
        {
            Outlook.RecurrencePattern pattern =
                appt.GetRecurrencePattern();
            Outlook.AppointmentItem singleAppt =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (singleAppt != null)
            {
                Debug.WriteLine("7/21/2006 2:00 PM occurrence found.");
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Compromissos](appointments.md)

