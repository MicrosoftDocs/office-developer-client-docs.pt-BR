---
title: Verificar a resposta do gerente para uma solicitação de reunião
TOCTitle: Check a manager's response to a meeting request
ms:assetid: 7bdb2163-17e3-47b4-95e5-e051b90506c6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184618(v=office.15)
ms:contentKeyID: 55119847
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba54ba740182eaffc92a0e1932a6fbed1d3804c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359707"
---
# <a name="check-a-managers-response-to-a-meeting-request"></a>Verificar a resposta do gerente para uma solicitação de reunião

Este exemplo mostra como usar os métodos [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) e [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) para verificar o status da resposta do gerente do usuário atual para uma solicitação de reunião.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Para determinar se certo destinatário aceitou ou recusou uma reunião solicitada, use a propriedade [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) do objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) do conjunto [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) associada ao objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).

No exemplo de código a seguir, CheckManagerResponseStatus aceita um objeto **AppointmentItem** como um parâmetro. CheckManagerResponseStatus obtém o objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) chamando o método **GetExchangeUser** no usuário atual. CheckManagerResponseStatus obtém o objeto **ExchangeUser** associado ao gerente do usuário atual chamando o método **GetExchangeUserManager**. Usando o método [CompareEntryIDs (String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), o exemplo verifica se o objeto **Recipient** associado ao objeto **AppointmentItem** é o mesmo que o objeto **ExchangeUser** que representa o gerente do usuário. Se **CompareEntryIDs** retornar **true**, o gerente do usuário estará no conjunto **Recipients** e CheckManagerResponseStatus retornará **MeetingResponseStatus** do gerente. Se **CompareEntryIDs** retornar **false**, CheckManagerResponseStatus retornará uma referência nula.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Object CheckManagerResponseStatus(Outlook.AppointmentItem appt)
{
    try
    {
        if (appt == null)
        {
            throw new ArgumentNullException();
        }
        Outlook.AddressEntry user =
            Application.Session.CurrentUser.AddressEntry;
        Outlook.ExchangeUser userEx = user.GetExchangeUser();
        if (userEx == null)
        {
            return null;
        }
        Outlook.ExchangeUser manager =
            userEx.GetExchangeUserManager();
        if (manager == null)
        {
            return null;
        }
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            if (Application.Session.CompareEntryIDs(
                recip.AddressEntry.ID, manager.ID))
            {
                return recip.MeetingResponseStatus;
            }
        }
        return null;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
        return null;
    }
}
```

## <a name="see-also"></a>Confira também

- [Usuários do Exchange](exchange-users.md)

