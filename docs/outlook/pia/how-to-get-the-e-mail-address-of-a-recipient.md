---
title: Obter o endereço de email de um destinatário
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-e-mail-address-of-a-recipient?redirectedfrom=MSDN
ms:contentKeyID: 55119879
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8957cbc92414b0cdac442167a5c9ea025ce318cb
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819333"
---
# <a name="get-the-email-address-of-a-recipient"></a><span data-ttu-id="28c47-102">Obter o endereço de email de um destinatário</span><span class="sxs-lookup"><span data-stu-id="28c47-102">Get the email address of a recipient</span></span>

<span data-ttu-id="28c47-103">Este exemplo mostra como receber o endereço SMTP de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="28c47-103">This example shows how to get the Simple Mail Transfer Protocol (SMTP) address of a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="28c47-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="28c47-104">Example</span></span>

<span data-ttu-id="28c47-105">A seguir, o exemplo de código, o método GetSMTPAddressForRecipients usa um objeto [MailItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mailitem?redirectedfrom=MSDN&view=outlook-pia) como um argumento de entrada e exibe o endereço SMTP de cada destinatário para esse item de email.</span><span class="sxs-lookup"><span data-stu-id="28c47-105">In the following the code example, the GetSMTPAddressForRecipients method takes a [MailItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mailitem?redirectedfrom=MSDN&view=outlook-pia) object as an input argument and then displays the SMTP address of each recipient for that mail item.</span></span> <span data-ttu-id="28c47-106">O método primeiro recupera a coleção [Recipients](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipients?redirectedfrom=MSDN&view=outlook-pia) que representa o conjunto de destinatários especificado para o item de email.</span><span class="sxs-lookup"><span data-stu-id="28c47-106">The method first retrieves the [Recipients](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipients?redirectedfrom=MSDN&view=outlook-pia) collection that represents the set of recipients specified for the mail item.</span></span> <span data-ttu-id="28c47-107">Para cada [destinatário](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient?redirectedfrom=MSDN&view=outlook-pia) na coleção **Recipients,** o método obtém o [objeto PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia)) que corresponde a esse **objeto Recipient** .</span><span class="sxs-lookup"><span data-stu-id="28c47-107">For each [Recipient](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient?redirectedfrom=MSDN&view=outlook-pia) in that **Recipients** collection, the method then obtains the [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia)) object that corresponds to that **Recipient** object.</span></span> <span data-ttu-id="28c47-108">Finalmente, o método usa a propriedade [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_Recipient_PropertyAccessor) para obter o valor da propriedade MAPI , que mapeia para a propriedade https://schemas.microsoft.com/mapi/proptag/0x39FE001E **PR \_ SMTP \_ ADDRESS**   ([PidTagSmtpAddress](https://docs.microsoft.com/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)) do destinatário.</span><span class="sxs-lookup"><span data-stu-id="28c47-108">Finally, the method uses the [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_Recipient_PropertyAccessor) property to get the value of the MAPI property https://schemas.microsoft.com/mapi/proptag/0x39FE001E, which maps to the **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://docs.microsoft.com/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)) property of the recipient.</span></span>

<span data-ttu-id="28c47-109">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="28c47-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="28c47-110">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="28c47-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="28c47-111">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="28c47-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetSMTPAddressForRecipients(Outlook.MailItem mail)
{
    const string PR_SMTP_ADDRESS =
        "http://schemas.microsoft.com/mapi/proptag/0x39FE001E";
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

## <a name="see-also"></a><span data-ttu-id="28c47-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="28c47-112">See also</span></span>

- [<span data-ttu-id="28c47-113">Destinatários</span><span class="sxs-lookup"><span data-stu-id="28c47-113">Recipients</span></span>](recipients.md)

