---
title: Criar um item de contato
TOCTitle: Create a Contact item
ms:assetid: b316294a-7f70-4e54-9375-4dc515e9fd11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184633(v=office.15)
ms:contentKeyID: 55119823
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11bfe40d29832577186712e269f9c0971e1e2be6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359672"
---
# <a name="create-a-contact-item"></a><span data-ttu-id="ade42-102">Criar um item de contato</span><span class="sxs-lookup"><span data-stu-id="ade42-102">Create a Contact item</span></span>

<span data-ttu-id="ade42-103">Este exemplo mostra como criar um item de contato e definir várias propriedades para o contato.</span><span class="sxs-lookup"><span data-stu-id="ade42-103">This example shows how to create a contact item and set various properties for the contact.</span></span>

## <a name="example"></a><span data-ttu-id="ade42-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ade42-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ade42-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="ade42-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="ade42-106">Um objeto [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) do Outlook tem mais de 100 propriedades internas, como [Departament](https://msdn.microsoft.com/library/bb610564\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)) e [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ade42-106">An Outlook [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object has more than 100 built-in properties such as [Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)), and [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)).</span></span> <span data-ttu-id="ade42-107">Você pode adicionar propriedades personalizadas, se uma propriedade interna não estiver disponível, usando a coleção [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ade42-107">You can add custom properties, if a built-in property is not available, by using the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection.</span></span> <span data-ttu-id="ade42-108">Depois de criar um **ContactItem**, você pode definir suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ade42-108">Once you create a **ContactItem**, you can set its properties.</span></span>

<span data-ttu-id="ade42-109">No exemplo de código a seguir, CreateContactExample cria um **ContactItem** e define propriedades comumente usadas para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="ade42-109">In the following code example, CreateContactExample creates a **ContactItem** and sets commonly used properties for that object.</span></span> <span data-ttu-id="ade42-110">Em seguida, chama o método [ShowCheckPhoneDialog (OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\)) no objeto **ContactItem**.</span><span class="sxs-lookup"><span data-stu-id="ade42-110">It then calls the [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\)) method on the **ContactItem** object.</span></span> <span data-ttu-id="ade42-111">O método **ShowCheckPhoneDialog** permite que o usuário resolva um número de telefone com base nas convenções de discagem local.</span><span class="sxs-lookup"><span data-stu-id="ade42-111">The **ShowCheckPhoneDialog** method allows the user to resolve a phone number based on local dialing conventions.</span></span>

<span data-ttu-id="ade42-112">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ade42-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ade42-113">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="ade42-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ade42-114">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="ade42-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateContactExample()
{
    Outlook.ContactItem contact = Application.CreateItem(
        Outlook.OlItemType.olContactItem) as Outlook.ContactItem;
    contact.FirstName = "Mellissa";
    contact.LastName = "MacBeth";
    contact.JobTitle = "Account Representative";
    contact.CompanyName = "Contoso Ltd.";
    contact.OfficeLocation = "36/2529";
    contact.BusinessTelephoneNumber = "4255551212 x432";
    contact.WebPage = "https://www.contoso.com";
    contact.BusinessAddressStreet = "1 Microsoft Way";
    contact.BusinessAddressCity = "Redmond";
    contact.BusinessAddressState = "WA";
    contact.BusinessAddressPostalCode = "98052";
    contact.BusinessAddressCountry =
        "United States of America";
    contact.Email1Address = "melissa@contoso.com";
    contact.Email1AddressType = "SMTP";
    contact.Email1DisplayName =
        "Melissa MacBeth (mellissa@contoso.com)";
    contact.Display(false);
    contact.ShowCheckPhoneDialog(
        Outlook.OlContactPhoneNumber.
        olContactPhoneBusiness);
}
```

## <a name="see-also"></a><span data-ttu-id="ade42-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="ade42-115">See also</span></span>

- [<span data-ttu-id="ade42-116">Contatos</span><span class="sxs-lookup"><span data-stu-id="ade42-116">Contacts</span></span>](contacts.md)

