---
title: Pesquisar e obter compromissos em um intervalo de tempo
TOCTitle: Search and obtain appointments in a time range
ms:assetid: ce5205ad-6967-4f21-8a9d-503b731dbd40
ms:mtpsurl: https://msdn.microsoft.com/library/Gg619398(v=office.15)
ms:contentKeyID: 55119927
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9088da5f2deb4b3d4ccb1c2bc5409e0ff280ed24
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723002"
---
# <a name="search-and-obtain-appointments-in-a-time-range"></a>Pesquisar e obter compromissos em um intervalo de tempo

Este exemplo mostra compromissos em um intervalo de tempo específico no calendário padrão do Microsoft Outlook.

## <a name="example"></a>Exemplo

Este exemplo de código contém dois métodos: DemoAppointmentsInRange e GetAppointmentsInRange. DemoAppointmentsInRange obtém o calendário padrão para o perfil do Outlook conectado no momento, com um intervalo de datas de cinco dias a partir da meia-noite Hoje, o GetAppointmentsInRange é chamado para obter compromissos que estão nesse intervalo de tempo e exibe o assunto e o início de cada um dos compromissos retornados.

O GetAppointmentsInRange aceita uma pasta do Outlook e os valores de início e término **DateTime** do intervalo de tempo como parâmetros de entrada. Este método emprega o método [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) e uma cadeia de caracteres filtrada no formato Jet que apresenta compromisso que começam e terminam em um período de tempo específico. Presumindo que \[Início\] e \[Final\] são as horas de início e hora de término de um compromisso e que, a hora de início e hora de término são o tempo de início e fim em um intervalo de tempo especificado, o GetAppointmentsInRange configura um filtro que procura  compromissos`[Start]>=startTime`, e `[End]<=endTime`. O código a seguir mostra o filtro Jet em C\#.

```csharp
string filter = "[Start] >= '"
    + startTime.ToString("g")
    + "' AND [End] <= '"
    + endTime.ToString("g") + "'";
```

Antes de chamar o método **Items.Restrict**Procurar compromissos, o GetAppointmentsInRange faz duas outras coisas para incluir compromissos recorrentes no intervalo de tempo especificado:

- Defina a propriedade [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) do conjunto de[itens](https://msdn.microsoft.com/library/bb645287\(v=office.15\)).

- Tipos de itens de compromisso na pasta Calendário determinados pela propriedade [iniciar](https://msdn.microsoft.com/library/bb647263\(v=office.15\)).

Como alternativa, se você também estiver interessado em compromissos que se sobreponham parcialmente ou completamente ao intervalo de tempo especificado, você deve especificar um filtro diferente para retornar tipos adicionais de compromissos (como mostrado na Figura 1):

- Compromissos que iniciam e terminam dentro do intervalo de tempo especificado (por exemplo, compromisso A):<br/><br/>`[Start]>=startTime and [End]<=endTime`

- Compromissos começam antes do intervalo de tempo especificado, mas terminam dentro do intervalo de tempo (por exemplo, compromisso B):<br/><br/>`[Start]<startTime and [End]<=endTime`

- Compromissos que iniciam dentro do intervalo de tempo especificado, mas terminam após o intervalo de tempo (por exemplo, compromisso C):<br/><br/>`[Start]>=startTime and [End]>endTime`

- Compromissos que começam antes do intervalo de tempo especificado e terminam após o intervalo de tempo (por exemplo, compromisso D):<br/><br/>`[Start]<startTime and [End]>endTime`

**Figura 1. Tipos de compromissos que ocorrem em um intervalo de tempo ou se sobrepõem a esse intervalo de tempo**

![Tipos de compromissos que ocorrem em um intervalo de tempo ou se sobrepõem a esse intervalo de tempo](media/pia-appointment-starttime-endtime.gif)
 

Como em qualquer intervalo de tempo `startTime<=endTime`, um filtro com `[Start]<=endTime` e `[End]>=startTime` captura os tipos de compromissos no intervalo de tempo anteriores.

Em C\#, você pode expressar o filtro Jet da seguinte maneira.

```csharp
string filter = "[Start] <= '"
    + endTime.ToString("g")
    + "' AND [End] >= '"
    + startTime.ToString("g") + "'";
```

O código a seguir mostra o exemplo completo. Se você usar o Visual Studio para testar este exemplo de código, primeiro você deve adicionar uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especificar a variável Outlook quando você importa a namespace **Microsoft.Office.Interop.Outlook**. As declarações **importar** ou **usando**não devem se situar antes de funções no exemplo de código, mas devem ser adicionadas antes da declaração classe pública. As linhas seguintes do código mostram como fazer a importação e a tarefa no Visual Basic e C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoAppointmentsInRange()
{
    Outlook.Folder calFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    DateTime start = DateTime.Now;
    DateTime end = start.AddDays(5);
    Outlook.Items rangeAppts = GetAppointmentsInRange(calFolder, start, end);
    if (rangeAppts != null)
    {
        foreach (Outlook.AppointmentItem appt in rangeAppts)
        {
            Debug.WriteLine("Subject: " + appt.Subject 
                + " Start: " + appt.Start.ToString("g"));
        }
    }
}

/// <summary>
/// Get recurring appointments in date range.
/// </summary>
/// <param name="folder"></param>
/// <param name="startTime"></param>
/// <param name="endTime"></param>
/// <returns>Outlook.Items</returns>
private Outlook.Items GetAppointmentsInRange(
    Outlook.Folder folder, DateTime startTime, DateTime endTime)
{
    string filter = "[Start] >= '"
        + startTime.ToString("g")
        + "' AND [End] <= '"
        + endTime.ToString("g") + "'";
    Debug.WriteLine(filter);
    try
    {
        Outlook.Items calItems = folder.Items;
        calItems.IncludeRecurrences = true;
        calItems.Sort("[Start]", Type.Missing);
        Outlook.Items restrictItems = calItems.Restrict(filter);
        if (restrictItems.Count > 0)
        {
            return restrictItems;
        }
        else
        {
            return null;
        }
    }
    catch { return null; }
}
```

## <a name="see-also"></a>Confira também

- [Pesquisar e filtrar](search-and-filter.md)

