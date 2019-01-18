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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722533"
---
# <a name="check-a-managers-response-to-a-meeting-request"></a><span data-ttu-id="8c549-102">Verificar a resposta do gerente para uma solicitação de reunião</span><span class="sxs-lookup"><span data-stu-id="8c549-102">Check a manager's response to a meeting request</span></span>

<span data-ttu-id="8c549-103">Este exemplo mostra como usar os métodos [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) e [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) para verificar o status da resposta do gerente do usuário atual para uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="8c549-103">This example illustrates how to use the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) and [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) methods to check the status of the response of the current user's manager to a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="8c549-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8c549-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="8c549-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="8c549-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="8c549-106">Para determinar se certo destinatário aceitou ou recusou uma reunião solicitada, use a propriedade [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) do objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) do conjunto [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) associada ao objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="8c549-106">To determine whether a given recipient has accepted or declined a requested meeting, use the [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) property of the [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object from the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection associated with the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="8c549-107">No exemplo de código a seguir, CheckManagerResponseStatus aceita um objeto **AppointmentItem** como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8c549-107">In the following code example, CheckManagerResponseStatus takes in an **AppointmentItem** object as a parameter.</span></span> <span data-ttu-id="8c549-108">CheckManagerResponseStatus obtém o objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) chamando o método **GetExchangeUser** no usuário atual.</span><span class="sxs-lookup"><span data-stu-id="8c549-108">CheckManagerResponseStatus gets the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object by calling the **GetExchangeUser** method on the current user.</span></span> <span data-ttu-id="8c549-109">CheckManagerResponseStatus obtém o objeto **ExchangeUser** associado ao gerente do usuário atual chamando o método **GetExchangeUserManager**.</span><span class="sxs-lookup"><span data-stu-id="8c549-109">CheckManagerResponseStatus then gets the **ExchangeUser** object that is associated with the current user’s manager by calling the **GetExchangeUserManager** method.</span></span> <span data-ttu-id="8c549-110">Usando o método [CompareEntryIDs (String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), o exemplo verifica se o objeto **Recipient** associado ao objeto **AppointmentItem** é o mesmo que o objeto **ExchangeUser** que representa o gerente do usuário.</span><span class="sxs-lookup"><span data-stu-id="8c549-110">By using the [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object, the example then checks whether the **Recipient** object associated with the **AppointmentItem** object is the same as the **ExchangeUser** object that represents the user’s manager.</span></span> <span data-ttu-id="8c549-111">Se **CompareEntryIDs** retornar **true**, o gerente do usuário estará no conjunto **Recipients** e CheckManagerResponseStatus retornará **MeetingResponseStatus** do gerente.</span><span class="sxs-lookup"><span data-stu-id="8c549-111">If **CompareEntryIDs** returns **true**, the user’s manager is found in the **Recipients** collection, and CheckManagerResponseStatus returns the manager’s **MeetingResponseStatus**.</span></span> <span data-ttu-id="8c549-112">Se **CompareEntryIDs** retornar **false**, CheckManagerResponseStatus retornará uma referência nula.</span><span class="sxs-lookup"><span data-stu-id="8c549-112">If **CompareEntryIDs** returns **false**, CheckManagerResponseStatus returns a null reference.</span></span>

<span data-ttu-id="8c549-113">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="8c549-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="8c549-114">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="8c549-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="8c549-115">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="8c549-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="8c549-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c549-116">See also</span></span>

- [<span data-ttu-id="8c549-117">Usuários do Exchange</span><span class="sxs-lookup"><span data-stu-id="8c549-117">Exchange users</span></span>](exchange-users.md)

