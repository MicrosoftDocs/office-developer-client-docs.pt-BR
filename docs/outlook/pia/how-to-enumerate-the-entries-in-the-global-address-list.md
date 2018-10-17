---
title: Enumerar entradas na lista de endereços global
TOCTitle: Enumerate the entries in the Global Address List
ms:assetid: f3dfe312-fe91-475d-8435-1c7a0bb2b725
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184654(v=office.15)
ms:contentKeyID: 55119801
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f9e392710940a63f5d7723d303d5cf48569ad92f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407545"
---
# <a name="enumerate-the-entries-in-the-global-address-list"></a><span data-ttu-id="515af-102">Enumerar entradas na lista de endereços global</span><span class="sxs-lookup"><span data-stu-id="515af-102">Enumerate the entries in the Global Address List</span></span>

<span data-ttu-id="515af-103">Este exemplo enumera os primeiros 100 endereços SMTP (Simple Mail Transfer Protocol) principal na GAL (Lista de Endereços Global).</span><span class="sxs-lookup"><span data-stu-id="515af-103">This example enumerates the first 100 primary Simple Mail Transfer Protocol (SMTP) addresses in the Global Address List (GAL).</span></span>

## <a name="example"></a><span data-ttu-id="515af-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="515af-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="515af-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="515af-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="515af-106">No exemplo de código a seguir, o endereço SMTP para um objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) é obtido transmitindo-o para um objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) ou [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) em uma chamada para os métodos [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) ou [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb611805\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="515af-106">In the following code example, the SMTP address for an [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object is obtained by casting it to an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) or [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) object in a call to the [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) or [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb611805\(v=office.15\)) methods.</span></span> <span data-ttu-id="515af-107">Se o objeto **AddressEntry** representar um usuário do Exchange, EnumerateGAL retornará um objeto **ExchangeUser** que expõe as propriedades do objeto **AddressEntry**.</span><span class="sxs-lookup"><span data-stu-id="515af-107">If the **AddressEntry** object represents an Exchange user, EnumerateGAL returns an **ExchangeUser** object that exposes properties of the **AddressEntry** object.</span></span> <span data-ttu-id="515af-108">Use propriedades ExchangeUser, como [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [Alias](https://msdn.microsoft.com/library/bb610682\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)) ou [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)), para expô-las.</span><span class="sxs-lookup"><span data-stu-id="515af-108">Use ExchangeUser properties such as [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [Alias](https://msdn.microsoft.com/library/bb610682\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)), or [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) to expose them.</span></span>

<span data-ttu-id="515af-109">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="515af-109">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="515af-110">A instrução **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="515af-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="515af-111">A seguinte linha de código mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="515af-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateGAL()
{
    Outlook.AddressList gal =
        Application.Session.GetGlobalAddressList();
    if (gal != null)
    {
        for (int i = 1; 
            i <= Math.Min(100, gal.AddressEntries.Count - 1); i++)
        {
            Outlook.AddressEntry addrEntry =
                gal.AddressEntries[i];
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                Outlook.ExchangeUser exchUser =
                    addrEntry.GetExchangeUser();
                Debug.WriteLine(exchUser.Name + " "
                    + exchUser.PrimarySmtpAddress);
            }
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeDistributionListAddressEntry)
            {
                Outlook.ExchangeDistributionList exchDL =
                    addrEntry.GetExchangeDistributionList();
                Debug.WriteLine(exchDL.Name + " "
                    + exchDL.PrimarySmtpAddress);
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="515af-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="515af-112">See also</span></span>

[<span data-ttu-id="515af-113">Catálogo de Endereços</span><span class="sxs-lookup"><span data-stu-id="515af-113">Address Book</span></span>](address-book.md)

