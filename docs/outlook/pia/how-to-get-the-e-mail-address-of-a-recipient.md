---
title: Obter o endereço de email de um destinatário
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184647(v=office.15)
ms:contentKeyID: 55119879
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 030908f7202301ec7849e655d5ff7cc1d7cffc13
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719324"
---
# <a name="get-the-email-address-of-a-recipient"></a><span data-ttu-id="c6320-102">Obter o endereço de email de um destinatário</span><span class="sxs-lookup"><span data-stu-id="c6320-102">Get the email address of a recipient</span></span>

<span data-ttu-id="c6320-103">Este exemplo mostra como receber o endereço SMTP de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="c6320-103">This example shows how to get the Simple Mail Transfer Protocol (SMTP) address of a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="c6320-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c6320-104">Example</span></span>

<span data-ttu-id="c6320-105">A seguir, o exemplo de código, o método GetSMTPAddressForRecipients usa um objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) como um argumento de entrada e exibe o endereço SMTP de cada destinatário para esse item de email.</span><span class="sxs-lookup"><span data-stu-id="c6320-105">In the following the code example, the GetSMTPAddressForRecipients method takes a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object as an input argument and then displays the SMTP address of each recipient for that mail item.</span></span> <span data-ttu-id="c6320-106">O método primeiro recupera a coleção [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) que representa o conjunto de destinatários especificado para o item de email.</span><span class="sxs-lookup"><span data-stu-id="c6320-106">The method first retrieves the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that represents the set of recipients specified for the mail item.</span></span> <span data-ttu-id="c6320-107">Para cada [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) na coleção **Recipients**, o método obtém o objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) que corresponde ao objeto **Recipient**.</span><span class="sxs-lookup"><span data-stu-id="c6320-107">For each [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) in that **Recipients** collection, the method then obtains the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object that corresponds to that **Recipient** object.</span></span> <span data-ttu-id="c6320-108">Finalmente, o método usa a propriedade [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) para obter o valor da propriedade MAPI https://schemas.microsoft.com/mapi/proptag/0x39FE001E, que é mapeado para o **PR\_SMTP\_endereço** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) de propriedade do destinatário.</span><span class="sxs-lookup"><span data-stu-id="c6320-108">Finally, the method uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) property to get the value of the MAPI property https://schemas.microsoft.com/mapi/proptag/0x39FE001E, which maps to the **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) property of the recipient.</span></span>

<span data-ttu-id="c6320-109">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c6320-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c6320-110">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="c6320-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c6320-111">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="c6320-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetSMTPAddressForRecipients(Outlook.MailItem mail)
{
    const string PR_SMTP_ADDRESS =
        "https://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    Outlook.Recipients recips = mail.Recipients;
    foreach (Outlook.Recipient recip in recips)
    {
        Outlook.PropertyAccessor pa = recip.PropertyAccessor;
        string smtpAddress =
            pa.GetProperty(PR_SMTP_ADDRESS).ToString();
        Debug.WriteLine(recip.Name + " SMTP=" + smtpAddress);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c6320-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6320-112">See also</span></span>

- [<span data-ttu-id="c6320-113">Destinatários</span><span class="sxs-lookup"><span data-stu-id="c6320-113">Recipients</span></span>](recipients.md)

