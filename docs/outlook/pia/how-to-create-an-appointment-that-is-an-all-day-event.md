---
title: Criar um compromisso que é um evento de dia inteiro
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 79bffb9185db43395df7254bc353ac24b65d717a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405935"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a>Criar um compromisso que é um evento de dia inteiro

Esse exemplo mostra como usar a propriedade [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) para criar um compromisso que é um evento de dia inteiro.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo a seguir é um trecho da [programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Um evento é diferente de um compromisso normal, porque é uma atividade com duração de 24 horas ou mais. Feiras de negócios, seminários ou férias são exemplos de eventos. Eventos e eventos anuais serão exibidos como períodos de tempo bloqueados no calendário do usuário. Em vez disso, eles aparecem como faixas. Você pode ver faixas na parte superior de uma exibição de dia ou semana do calendário. Para um compromisso de dia inteiro, por padrão, a hora do usuário é exibida como ocupado quando visto por outras pessoas, mas a hora do usuário é exibida como gratuitamente por um evento ou evento.

Para criar um evento de dia inteiro por programação, defina a propriedade[AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) propriedade do objeto[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) como verdadeiro. Defina as propriedades [início](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) e [final](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) do AppointmentItem. Se você definir a propriedade AllDayEvent como verdadeira e não configurar as propriedades de início e de término, o evento ocorrerá no dia e ele será um compromisso, mostrando o status de ocupado em seu calendário. Se quiser que o evento que ocorra em uma data futura, você deve definir as propriedades de início e de término.

> [!NOTE]
> Para tornar o compromisso de dia inteiro, você deve definir a propriedade de início às 0:00 (meia-noite) do dia em que você deseja que o evento comece e, em seguida, defina a propriedade de final para meia-noite do dia depois que você deseja finalizar o evento. Se você definir a hora de início e término com um valor de data e hora diferente de meia-noite, o compromisso se tornará um compromisso de vários dias em vez de um evento de um dia inteiro. 
>
> Por exemplo, se a duração do evento é apenas um dia, defina a propriedade de início como meia-noite do dia em que você deseja que o evento comece e, em seguida, defina a propriedade de final para meia-noite Nos dia seguinte. Você sempre deve definir a propriedade de final de meia-noite em uma data que é mais de um dia depois da data de início.

O exemplo a seguir, AllDayEventExample cria um evento de dia inteiro que começa em 11 de junho de 2007 e termina em 15 de junho de 2007. Observe que a propriedade de término do compromisso é definida como 12:00 A.M. em 16 de junho de 2007.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AllDayEventExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Developer's Conference";
    appt.AllDayEvent = true;
    appt.Start = DateTime.Parse("6/11/2007 12:00 AM");
    appt.End = DateTime.Parse("6/16/2007 12:00 AM");
    appt.Display(false);
}
```

## <a name="see-also"></a>Confira também

- [Compromissos](appointments.md)

