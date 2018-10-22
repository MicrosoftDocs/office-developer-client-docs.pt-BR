---
title: Criar um compromisso recorrente que usa o padrão de recorrência padrão
TOCTitle: Create a recurring appointment by using the default recurrence pattern
ms:assetid: 157bf1ae-2efe-4783-99ea-606722dde204
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184589(v=office.15)
ms:contentKeyID: 55119809
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: be6c024012c02d31af7ce37af6010ba6b40419ce
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406705"
---
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a>Criar um compromisso recorrente que usa o padrão de recorrência padrão

Este exemplo mostra como criar um compromisso recorrente usando o padrão de recorrência padrão.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Ao criar um compromisso no Outlook, você está criando um objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Seu compromisso será um compromisso recorrente se a propriedade [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) do AppointmentItem estiver definida como true. IsRecurring não pode ser definido diretamente. 

No entanto, é possível criar um compromisso recorrente usando o objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Para criar um compromisso recorrente programaticamente, crie um objeto **AppointmentItem**, chame o método [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) do objeto **AppointmentItem** e, em seguida, salve o objeto **AppointmentItem**. Isso cria um compromisso que usa o padrão de recorrência padrão que ocorre semanalmente no dia da semana para o qual o compromisso foi criado e não tem data de término. O objeto RecurrencePattern permite a criação de compromissos recorrentes em intervalos especificados: diário, semanal, mensal ou anual. Se você não especificar intervalos para o objeto RecurrencePattern, o Outlook usará o padrão de recorrência padrão.

Ao trabalhar com itens de compromisso recorrente, você deve liberar referências anteriores, obter novas referências para o item de compromisso recorrente antes de acessar ou modificar o item e liberar essas referências assim que tiver terminado e salvado as alterações. Essa prática aplica o objeto **AppointmentItem** recorrente e a qualquer objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Para liberar uma referência no Visual Basic, defina esse objeto existente como Nothing. Em C\#, libere explicitamente a memória para esse objeto.

Observe que mesmo após liberar sua referência e tentar obter uma nova referência, se ainda houver uma referência ativa (mantida por outro suplemento ou pelo Outlook) para um dos objetos acima, sua nova referência continuará a apontar para uma cópia desatualizada do objeto. Portanto, é importante liberar suas referências assim que seu compromisso recorrente terminar.

No exemplo a seguir CreateRecurringAppointment cria um objeto **AppointmentItem**. Em seguida, ele chama GetRecurrencePattern. GetRecurrencePattern retorna um objeto RecurrencePattern e AppointmentItem é salvo. Isso cria um compromisso recorrente que usa o padrão de recorrência padrão.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateRecurringAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Weekly Extensibility Team Meeting";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    appt.Save();
}
```

## <a name="see-also"></a>Confira também

- [Compromissos](appointments.md)

