---
title: Obter informações de disponibilidade do gerente de um usuário do Exchange
TOCTitle: Get availability information for an Exchange user's manager
ms:assetid: b59dd875-50c2-4f24-ba91-24429abf1b72
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646996(v=office.15)
ms:contentKeyID: 55119849
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 927389609e7a16a538cb480cc24891873ec1650c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405893"
---
# <a name="get-availability-information-for-an-exchange-users-manager"></a><span data-ttu-id="d8122-102">Obter informações de disponibilidade do gerente de um usuário do Exchange</span><span class="sxs-lookup"><span data-stu-id="d8122-102">Get availability information for an Exchange user's manager</span></span>

<span data-ttu-id="d8122-103">Este exemplo exibe o próximo intervalo de tempo de 60 minutos disponível no calendário para o gerente de um usuário.</span><span class="sxs-lookup"><span data-stu-id="d8122-103">This example displays the next free 60-minute time slot in the calendar for a user's manager.</span></span>

## <a name="example"></a><span data-ttu-id="d8122-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d8122-104">Example</span></span>

<span data-ttu-id="d8122-105">Este exemplo de código verifica se o usuário atual é um usuário do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8122-105">This code sample checks whether the current user is an Exchange user.</span></span> <span data-ttu-id="d8122-106">Em caso afirmativo e se o usuário tiver um gerente, o código obterá informações do gerente chamando o método [GetExchangeUser](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) do objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) e o método [GetExchangeUserManager ](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) do objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d8122-106">If so, and if the current user has a manager, it obtains the manager's information by calling the [GetExchangeUser](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method of the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object and the [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method of the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object.</span></span> <span data-ttu-id="d8122-107">As informações do gerente estão contidas em um objeto **ExchangeUser** que inclui o cronograma de disponibilidade do gerente.</span><span class="sxs-lookup"><span data-stu-id="d8122-107">The manager's information is contained in an **ExchangeUser** object that includes the manager's Free/Busy schedule.</span></span>

<span data-ttu-id="d8122-108">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="d8122-108">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="d8122-109">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="d8122-109">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="d8122-110">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="d8122-110">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub GetManagerOpenInterval()
    Const slotLength As Integer = 60
    Dim addrEntry As Outlook.AddressEntry = _
        Application.Session.CurrentUser.AddressEntry
    If addrEntry.Type = "EX" Then
        Dim manager As Outlook.ExchangeUser = _
            Application.Session.CurrentUser. _
            AddressEntry.GetExchangeUser(). _
            GetExchangeUserManager()
        If Not (manager Is Nothing) Then
            Dim freeBusy As String = _
            manager.GetFreeBusy(DateTime.Now, slotLength, True)
            For i As Integer = 1 To freeBusy.Length - 1
                If (freeBusy.Substring(i, 1) = "0") Then
                    ' Get number of minutes into
                    ' the day for free interval
                    Dim busySlot As Double = (i - 1) * slotLength
                    ' Get an actual date/time
                    Dim dateBusySlot As DateTime = _
                        DateTime.Now.Date.AddMinutes(busySlot)
                    If (dateBusySlot.TimeOfDay >= _
                        DateTime.Parse("8:00 AM").TimeOfDay And _
                        dateBusySlot.TimeOfDay <= _
                        DateTime.Parse("5:00 PM").TimeOfDay And _
                        Not (dateBusySlot.DayOfWeek = _
                        DayOfWeek.Saturday Or _
                        dateBusySlot.DayOfWeek = DayOfWeek.Sunday))Then
                        Dim sb As StringBuilder = New StringBuilder()
                        sb.AppendLine( _
                            manager.Name & " first open interval:")
                        sb.AppendLine(dateBusySlot.ToString("f"))
                        Debug.WriteLine(sb.ToString())
                    End If
                End If
            Next
        End If
    End If
End Sub
```


```csharp
private void GetManagerOpenInterval()
{
    const int slotLength = 60;
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            string freeBusy = manager.GetFreeBusy(
                DateTime.Now, slotLength, true);
            for (int i = 1; i < freeBusy.Length; i++)
            {
                if (freeBusy.Substring(i, 1) == "0")
                {
                    // Get number of minutes into
                    // the day for free interval
                    double busySlot = (i - 1) * slotLength;
                    // Get an actual date/time
                    DateTime dateBusySlot =
                        DateTime.Now.Date.AddMinutes(busySlot);
                    if (dateBusySlot.TimeOfDay >=
                        DateTime.Parse("8:00 AM").TimeOfDay &
                        dateBusySlot.TimeOfDay <=
                        DateTime.Parse("5:00 PM").TimeOfDay &
                        !(dateBusySlot.DayOfWeek == 
                        DayOfWeek.Saturday |
                        dateBusySlot.DayOfWeek == DayOfWeek.Sunday))
                    {
                        StringBuilder sb = new StringBuilder();
                        sb.AppendLine(manager.Name
                            + " first open interval:");
                        sb.AppendLine(dateBusySlot.ToString("f"));
                        Debug.WriteLine(sb.ToString());
                    }
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="d8122-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8122-111">See also</span></span>

- [<span data-ttu-id="d8122-112">Usuários do Exchange</span><span class="sxs-lookup"><span data-stu-id="d8122-112">Exchange users</span></span>](exchange-users.md)

