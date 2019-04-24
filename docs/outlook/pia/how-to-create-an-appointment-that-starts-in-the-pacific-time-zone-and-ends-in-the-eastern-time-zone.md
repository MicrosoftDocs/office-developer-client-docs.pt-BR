---
title: Criar um compromisso que começa no Fuso Horário do Pacífico e termina no Fuso Horário da Costa Leste dos EUA
TOCTitle: Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone
ms:assetid: ba19532b-df31-4384-8816-e64e6eecbe53
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623388(v=office.15)
ms:contentKeyID: 55119808
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e9a1b9d5f65d8683c08821d4cf0851f599f32030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349452"
---
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a>Criar um compromisso que começa no Fuso Horário do Pacífico e termina no Fuso Horário da Costa Leste dos EUA

Ocasionalmente, um compromisso pode se estender por um período de tempo durante o qual o usuário pode ter percorrido um fuso horário diferente do que quando o compromisso é iniciado. Este exemplo cria um compromisso que começa no fuso horário do Pacífico (UTC-8) e termina no fuso horário da costa leste (UTC-5).

## <a name="example"></a>Exemplo

Este exemplo de código usa [](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) o objeto TimeZones que representa todos os fusos horários reconhecidos no Microsoft Windows. Também usa o objeto [timezone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) para definir ou obter a propriedade [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) e a propriedade [endtimezone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) no objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) .

O Outlook exibe todas as datas no horário local, que são expressas no fuso horário atual do usuário, controladas pelas configurações do usuário no painel de controle do Windows. O Outlook também define ou obtém Propriedades, como [início](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) e [fim](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), em hora local. No enTanto, o Outlook armazena valores de data e hora como UTC (tempo Universal Coordenado) em vez de horário local. Se você examinar o valor interno de compromisso. Start usando o objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) , você encontraria o valor de data e hora interna é igual ao valor de data e hora local convertido para o valor de data e hora UTC equivalente.

O Outlook usa as informações de fuso horário para mapear o compromisso para a hora UTC correta quando ele salva um compromisso e na hora local correta quando exibe o item no calendário. A alteração de StartTimeZone afeta o valor de compromisso. Start, que é sempre expresso no fuso horário local, representado pela propriedade [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) do objeto retornado por TimeZones. [](https://msdn.microsoft.com/library/bb645170\(v=office.15\)) Da mesma forma, alterar o endTimeZone afeta o valor de compromisso. end, que é sempre expresso no fuso horário local, representado pela propriedade CurrentTimeZone do objeto retornado por Application. timeZones.

Você pode recuperar um TimeZone específico do objeto timeZones usando a chave independente de localidade para o fuso horário no registro do Windows. As chaves de fuso horário independentes de localidade estão listadas na `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`seguinte chave:.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```



```vb
Private Sub TimeZoneExample()
    Dim appt As Outlook.AppointmentItem = _
        CType(Application.CreateItem( _
        Outlook.OlItemType.olAppointmentItem), Outlook.AppointmentItem)
    Dim tzs As Outlook.TimeZones = Application.TimeZones
    ' Obtain timezone using indexer and locale-independent key
    Dim tzEastern As Outlook.TimeZone = tzs("Eastern Standard Time")
    Dim tzPacific As Outlook.TimeZone = tzs("Pacific Standard Time")
    appt.Subject = "SEA - JFK Flight"
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM")
    appt.StartTimeZone = tzPacific
    appt.End = DateTime.Parse("8/9/2006 5:30 PM")
    appt.EndTimeZone = tzEastern
    appt.Display(False)
End Sub
```



```csharp
private void TimeZoneExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    Outlook.TimeZones tzs = Application.TimeZones;
    // Obtain timezone using indexer and locale-independent key
    Outlook.TimeZone tzEastern = tzs["Eastern Standard Time"];
    Outlook.TimeZone tzPacific = tzs["Pacific Standard Time"];
    appt.Subject = "SEA - JFK Flight";
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM");
    appt.StartTimeZone = tzPacific;
    appt.End = DateTime.Parse("8/9/2006 5:30 PM");
    appt.EndTimeZone = tzEastern; 
    appt.Display(false);
}
```

## <a name="see-also"></a>Confira também

- [Compromissos](appointments.md)

