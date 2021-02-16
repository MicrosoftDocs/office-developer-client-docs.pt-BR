---
title: Obter informações sobre todas as listas de distribuição das quais o usuário atual participa
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bbc87250ab77f662e0fc5a71f9857e734637dd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349424"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a><span data-ttu-id="7c9a7-102">Obter informações sobre todas as listas de distribuição das quais o usuário atual participa</span><span class="sxs-lookup"><span data-stu-id="7c9a7-102">Get information about all distribution lists of which the current user is a member</span></span>

<span data-ttu-id="7c9a7-103">Este exemplo usa o método [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) para obter informações sobre todas as listas de distribuição das quais o usuário atual participa.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-103">This example uses the [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) method to get information about all distribution lists of which the current user is a member.</span></span>

## <a name="example"></a><span data-ttu-id="7c9a7-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7c9a7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7c9a7-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="7c9a7-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="7c9a7-106">No exemplo a seguir, GetCurrentUserMembership chama o método **GetMemberOfList** para obter um conjunto [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) para todas as listas de distribuição das quais o usuário do Exchange é membro.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-106">In the following example, GetCurrentUserMembership calls the **GetMemberOfList** method to get an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection for all distribution lists of which the Exchange user is a member.</span></span> <span data-ttu-id="7c9a7-107">Se o usuário não for membro de nenhuma lista de distribuição, **GetMemberOfList** retornará um conjunto **AddressEntries** com uma contagem de zero.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-107">If the user is not a member of any distribution lists, **GetMemberOfList** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="7c9a7-108">O usuário conectado deve estar online para que **GetMemberOfList** retorne um conjunto **AddressEntries**. Caso contrário, **GetMemberOfList** retornará uma referência nula.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-108">The user must be online for **GetMemberOfList** to return an **AddressEntries** collection; otherwise, **GetMemberOfList** returns a null reference.</span></span> <span data-ttu-id="7c9a7-109">GetCurrentUserMembership usa o método [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)), que retorna o objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) atual para testar se o usuário está online.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-109">GetCurrentUserMembership uses the [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) method, which returns the current [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object, to test whether the user is online.</span></span> <span data-ttu-id="7c9a7-110">Depois que as entradas de endereço são obtidas, o exemplo grava informações sobre cada uma das listas de distribuição do usuário para os ouvintes de rastreamento do conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="7c9a7-110">Once the address entries are obtained, the example writes information about each of the user’s distribution lists to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="7c9a7-111">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7c9a7-112">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7c9a7-113">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserMembership()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser exchUser =
            currentUser.GetExchangeUser();
        if (exchUser != null)
        {
            Outlook.AddressEntries addrEntries =
                exchUser.GetMemberOfList();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Debug.WriteLine(addrEntry.Name);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="7c9a7-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c9a7-114">See also</span></span>

- [<span data-ttu-id="7c9a7-115">Usuários do Exchange</span><span class="sxs-lookup"><span data-stu-id="7c9a7-115">Exchange users</span></span>](exchange-users.md)

