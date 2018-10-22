---
title: 'Obter informações sobre subordinados diretos do gerente do usuário atual '
TOCTitle: Get information about direct reports of the current user's manager
ms:assetid: 768bf573-1b10-4776-8947-a7f8dc3ebde0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184617(v=office.15)
ms:contentKeyID: 55119842
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 6237b3455eea449460133fb52a79ef87bcaebc1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406698"
---
# <a name="get-information-about-direct-reports-of-the-current-users-manager"></a><span data-ttu-id="85d2d-102">Obter informações sobre subordinados diretos do gerente do usuário atual </span><span class="sxs-lookup"><span data-stu-id="85d2d-102">Get information about direct reports of the current user's manager</span></span>

<span data-ttu-id="85d2d-103">Este exemplo recebe os subordinados diretos do gerente atual do usuário, se houver algum, e exibe informações sobre cada um deles.</span><span class="sxs-lookup"><span data-stu-id="85d2d-103">This example gets the direct reports of the current user’s manager, if any, and then displays information about each of the manager’s direct reports.</span></span>

## <a name="example"></a><span data-ttu-id="85d2d-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="85d2d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="85d2d-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="85d2d-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="85d2d-106">No exemplo a seguir, o procedimento GetManagerDirectReports chama o método [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) para obter o gerente do usuário, representado por um objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="85d2d-106">In the following example, the GetManagerDirectReports procedure calls the [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method to get the user’s manager, represented by an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object.</span></span> <span data-ttu-id="85d2d-107">Se o usuário atual tiver um gerente, [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) será chamado para retornar um conjunto [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) que representa as entradas de endereço de todos os subordinados diretos do gerente do usuário.</span><span class="sxs-lookup"><span data-stu-id="85d2d-107">If the current user has a manager, [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) is called to return an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection that represents the address entries for all the direct reports of user’s manager.</span></span> <span data-ttu-id="85d2d-108">Se o gerente não tiver subordinados diretos, **GetDirectReports** retornará um conjunto **AddressEntries** com uma contagem de zero.</span><span class="sxs-lookup"><span data-stu-id="85d2d-108">If the manager has no direct reports, **GetDirectReports** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="85d2d-109">Depois que os subordinados diretos do gerente forem obtidos, GetManagerDirectReports gravará informações sobre cada um deles para os ouvintes de rastreamento do conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="85d2d-109">Once the manager’s direct reports are obtained, GetManagerDirectReports writes information about each of the manager’s direct reports to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="85d2d-110">O usuário conectado deve estar online para que esse método retorne um conjunto **AddressEntries**. Caso contrário, **GetDirectReports** retornará uma referência nula.</span><span class="sxs-lookup"><span data-stu-id="85d2d-110">The signed-in user must be online for this method to return an **AddressEntries** collection; otherwise, **GetDirectReports** returns a null reference.</span></span> <span data-ttu-id="85d2d-111">No caso do código de produção, teste se o usuário está offline usando a propriedade [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) ou a propriedade [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) para vários cenários do Exchange.</span><span class="sxs-lookup"><span data-stu-id="85d2d-111">For production code, you must test for the user being offline by using the [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) property, or the [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) property for multiple Exchange scenarios.</span></span>

<span data-ttu-id="85d2d-112">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="85d2d-112">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="85d2d-113">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="85d2d-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="85d2d-114">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="85d2d-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerDirectReports()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.AddressEntries addrEntries =
                manager.GetDirectReports();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Outlook.ExchangeUser exchUser =
                        addrEntry.GetExchangeUser();
                    StringBuilder sb = new StringBuilder();
                    sb.AppendLine("Name: "
                        + exchUser.Name);
                    sb.AppendLine("Title: "
                        + exchUser.JobTitle);
                    sb.AppendLine("Department: "
                        + exchUser.Department);
                    sb.AppendLine("Location: "
                        + exchUser.OfficeLocation);
                    Debug.WriteLine(sb.ToString());
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="85d2d-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="85d2d-115">See also</span></span>

- [<span data-ttu-id="85d2d-116">Usuários do Exchange</span><span class="sxs-lookup"><span data-stu-id="85d2d-116">Exchange users</span></span>](exchange-users.md)

