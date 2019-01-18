---
title: Acessar informações sobre o usuário atual
TOCTitle: Get information about the current user
ms:assetid: 3802523a-3ccf-4cca-a348-abe2645a0d9c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184601(v=office.15)
ms:contentKeyID: 55119840
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b169eb1baadee92c08bcb68726ae4d18a9d79d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723065"
---
# <a name="get-information-about-the-current-user"></a><span data-ttu-id="0c833-102">Acessar informações sobre o usuário atual</span><span class="sxs-lookup"><span data-stu-id="0c833-102">Get information about the current user</span></span>

<span data-ttu-id="0c833-103">Este exemplo mostra como ter acesso a informações sobre o usuário, como nome, cargo e número de telefone.</span><span class="sxs-lookup"><span data-stu-id="0c833-103">This example shows how to get the current user’s information, such as name, job title, and telephone number.</span></span>

## <a name="example"></a><span data-ttu-id="0c833-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0c833-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0c833-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0c833-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="0c833-106">Para obter um objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) de um objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)), chame o método [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) no objeto **AddressEntry**.</span><span class="sxs-lookup"><span data-stu-id="0c833-106">To obtain an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object from an [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object, call the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method on the **AddressEntry** object.</span></span> <span data-ttu-id="0c833-107">No procedimento a seguir, GetCurrentUserInfo recebe a propriedade [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) para o objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) usando a propriedade [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0c833-107">In the following procedure, GetCurrentUserInfo gets the [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) property for the [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object by using the [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) property.</span></span> <span data-ttu-id="0c833-108">Se o objeto **AddressEntry** representa um usuário de caixa de correio do Exchange, GetCurrentUserInfo chama o método **GetExchangeUser** e um objeto **ExchangeUser** é retornado.</span><span class="sxs-lookup"><span data-stu-id="0c833-108">If the **AddressEntry** object represents an Exchange mailbox user, GetCurrentUserInfo calls the **GetExchangeUser** method and an **ExchangeUser** object is returned.</span></span> <span data-ttu-id="0c833-109">As propriedades [Name](https://msdn.microsoft.com/library/bb622941\(v=office.15\)), [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)), [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb611429\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)) e [MobileTelephoneNumber](https://msdn.microsoft.com/library/bb609292\(v=office.15\)) são gravadas nos ouvintes de rastreamento do conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="0c833-109">The [Name](https://msdn.microsoft.com/library/bb622941\(v=office.15\)), [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)), [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb611429\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)), and [MobileTelephoneNumber](https://msdn.microsoft.com/library/bb609292\(v=office.15\)) properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="0c833-110">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="0c833-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0c833-111">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="0c833-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0c833-112">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="0c833-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserInfo()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser currentUser =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser();
        if (currentUser != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + currentUser.Name);
            sb.AppendLine("STMP address: "
                + currentUser.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + currentUser.JobTitle);
            sb.AppendLine("Department: "
                + currentUser.Department);
            sb.AppendLine("Location: "
                + currentUser.OfficeLocation);
            sb.AppendLine("Business phone: "
                + currentUser.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + currentUser.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="0c833-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c833-113">See also</span></span>

- [<span data-ttu-id="0c833-114">Usuários do Exchange</span><span class="sxs-lookup"><span data-stu-id="0c833-114">Exchange users</span></span>](exchange-users.md)

