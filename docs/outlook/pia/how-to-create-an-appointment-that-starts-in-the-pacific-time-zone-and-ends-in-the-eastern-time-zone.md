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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698712"
---
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a><span data-ttu-id="5fff4-102">Criar um compromisso que começa no Fuso Horário do Pacífico e termina no Fuso Horário da Costa Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="5fff4-102">Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone</span></span>

<span data-ttu-id="5fff4-103">Ocasionalmente, um compromisso pode abranger um período de tempo durante o qual o usuário pode ter viajado para um fuso horário diferente quando o compromisso é iniciado.</span><span class="sxs-lookup"><span data-stu-id="5fff4-103">Occasionally, an appointment may span over a period of time during which the user may have traveled to a different time zone than when the appointment starts.</span></span> <span data-ttu-id="5fff4-104">Este exemplo cria um compromisso que começa no Fuso Horário do Pacífico (UTC-8) e termina no Fuso Horário da Costa Leste dos EUA (UTC-5).</span><span class="sxs-lookup"><span data-stu-id="5fff4-104">This example creates an appointment that begins in the Pacific Time Zone (UTC-8) and ends in the Eastern Time Zone (UTC-5).</span></span>

## <a name="example"></a><span data-ttu-id="5fff4-105">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5fff4-105">Example</span></span>

<span data-ttu-id="5fff4-106">A amostra de código a seguir usa o objeto [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) que representa todos os fusos horários reconhecidos no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5fff4-106">This code sample uses the [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) object that represents all the time zones recognized in Microsoft Windows.</span></span> <span data-ttu-id="5fff4-107">Também usa o objeto [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) para definir ou obter a propriedade [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) e a propriedade [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) no objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5fff4-107">It also uses the [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) object to set or get the [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) property and the [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) property on the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="5fff4-108">O Outlook exibe todas as datas no horário local, que é expresso no fuso horário atual do usuário, controlado pelas configurações do usuário no Painel de Controle do Windows.</span><span class="sxs-lookup"><span data-stu-id="5fff4-108">Outlook displays all dates in local time, which is expressed in the user's current time zone, controlled by the user's settings in the Windows Control Panel.</span></span> <span data-ttu-id="5fff4-109">O Outlook também define ou obtém propriedades, como [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) e [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), no horário local.</span><span class="sxs-lookup"><span data-stu-id="5fff4-109">Outlook also sets or gets properties, such as [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), in local time.</span></span> <span data-ttu-id="5fff4-110">Porém, o Outlook armazena valores de data e hora como Tempo Universal Coordenado (UTC) em vez de horário local.</span><span class="sxs-lookup"><span data-stu-id="5fff4-110">However, Outlook stores date and time values as Coordinated Universal Time (UTC) rather than local time.</span></span> <span data-ttu-id="5fff4-111">Se você examinar o valor interno de Appointment.Start usando o objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)), vai descobrir que o valor interno de data e hora é igual ao valor local de data e hora convertido para o valor de data e hora equivalente em UTC.</span><span class="sxs-lookup"><span data-stu-id="5fff4-111">If you examine the internal value of Appointment.Start by using the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object, you would find the internal date and time value is equal to the local date and time value converted to the equivalent UTC date and time value.</span></span>

<span data-ttu-id="5fff4-112">O Outlook usa as informações de fuso horário para mapear o compromisso para a hora UTC correta quando o compromisso é salvo e para a hora local correta quando o item é exibido no calendário.</span><span class="sxs-lookup"><span data-stu-id="5fff4-112">Outlook uses the time zone information to map the appointment to the correct UTC time when it saves an appointment, and into the correct local time when it displays the item in the calendar.</span></span> <span data-ttu-id="5fff4-113">A alteração de StartTimeZone afeta o valor de Appointment.Start, que é sempre expresso no fuso horário local, representado pela propriedade [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) do objeto retornado por [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5fff4-113">Changing StartTimeZone affects the value of Appointment.Start, which is always expressed in the local time zone, represented by the [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) property of the object returned by [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)).</span></span> <span data-ttu-id="5fff4-114">De modo semelhante, a alteração de EndTimeZone afeta o valor de Appointment.End, que é sempre expresso no fuso horário local, representado pela propriedade CurrentTimeZone do objeto retornado por Application.TimeZones.</span><span class="sxs-lookup"><span data-stu-id="5fff4-114">Similarly, changing EndTimeZone affects the value of Appointment.End, which is always expressed in the local time zone, represented by the CurrentTimeZone property of the object returned by Application.TimeZones.</span></span>

<span data-ttu-id="5fff4-115">É possível recuperar um TimeZone específico de um objeto TimeZones usando uma chave independente de localidade para o TimeZone no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="5fff4-115">You can retrieve a specific TimeZone from the TimeZones object by using the locale-independent key for the TimeZone in the Windows registry.</span></span> <span data-ttu-id="5fff4-116">As chaves TimeZone independentes de localidade são listadas sob a seguinte chave: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.</span><span class="sxs-lookup"><span data-stu-id="5fff4-116">Locale-independent TimeZone keys are listed under the following key: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.</span></span>

<span data-ttu-id="5fff4-117">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5fff4-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="5fff4-118">A instrução **Imports** ou **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionada antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="5fff4-118">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5fff4-119">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="5fff4-119">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


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

## <a name="see-also"></a><span data-ttu-id="5fff4-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fff4-120">See also</span></span>

- [<span data-ttu-id="5fff4-121">Compromissos</span><span class="sxs-lookup"><span data-stu-id="5fff4-121">Appointments</span></span>](appointments.md)

