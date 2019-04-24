---
title: Obter o endereço SMTP do remetente de uma mensagem
TOCTitle: Get the SMTP address of the sender of a mail item
ms:assetid: 86e0c0aa-1696-4415-b25f-f9c1c29d88a9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184624(v=office.15)
ms:contentKeyID: 55119869
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 74adbf02180e0e993b22e35481f51d304b14e7d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320080"
---
# <a name="get-the-smtp-address-of-the-sender-of-a-mail-item"></a><span data-ttu-id="e2a52-102">Obter o endereço SMTP do remetente de uma mensagem</span><span class="sxs-lookup"><span data-stu-id="e2a52-102">Get the SMTP address of the sender of a mail item</span></span>

<span data-ttu-id="e2a52-103">Este exemplo contém o endereço de email SMTP do remetente para um item de email.</span><span class="sxs-lookup"><span data-stu-id="e2a52-103">This example gets the sender’s Simple Mail Transfer Protocol (SMTP) address for a mail item.</span></span>

## <a name="example"></a><span data-ttu-id="e2a52-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e2a52-104">Example</span></span>

<span data-ttu-id="e2a52-105">Para determinar o endereço SMTP de um item de email recebido, use a propriedade [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) do objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e2a52-105">To determine the SMTP address for a received mail item, use the [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) property of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span> <span data-ttu-id="e2a52-106">No entanto, se o remetente for um membro interno da sua organização, **SenderEmailAddress** não retorna um endereço SMTP, e você deve usar o objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) para retornar o endereço SMTP do remetente.</span><span class="sxs-lookup"><span data-stu-id="e2a52-106">However, if the sender is internal to your organization, **SenderEmailAddress** does not return an SMTP address, and you must use the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object to return the sender’s SMTP address.</span></span>

<span data-ttu-id="e2a52-107">No exemplo de código a seguir, GetSenderSMTPAddress usa o objeto **PropertyAccessor** para obter valores que não são expostos diretamente no modelo de objeto do Outlook.</span><span class="sxs-lookup"><span data-stu-id="e2a52-107">In the following code example, GetSenderSMTPAddress uses the **PropertyAccessor** object to obtain values that are not exposed directly in the Outlook object model.</span></span> <span data-ttu-id="e2a52-108">GetSenderSMTPAddress leva um **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="e2a52-108">GetSenderSMTPAddress takes in a **MailItem**.</span></span> <span data-ttu-id="e2a52-109">Se o valor da propriedade [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) do **MailItem** recebido for "EX", o remetente da mensagem está localizado em um servidor do Exchange na sua organização.</span><span class="sxs-lookup"><span data-stu-id="e2a52-109">If the value of the [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) property of the received **MailItem** is "EX", the sender of the message resides on an Exchange server in your organization.</span></span> <span data-ttu-id="e2a52-110">GetSenderSMTPAddress usa a propriedade [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) do objeto **MailItem** para obter o remetente, representado pelo objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e2a52-110">GetSenderSMTPAddress uses the [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) property of the **MailItem** object to get the sender, represented by the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object.</span></span> <span data-ttu-id="e2a52-111">Se o objeto **AddressEntry** objeto representa um usuário do Exchange, o exemplo chama o método [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) para retornar o objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) do objeto **AddressEntry**.</span><span class="sxs-lookup"><span data-stu-id="e2a52-111">If the **AddressEntry** object represents an Exchange user, the example calls the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method to return the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object of the **AddressEntry** object.</span></span> <span data-ttu-id="e2a52-112">GetSenderSMTPAddress usa a propriedade [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) do objeto **ExchangeUser** para retornar o endereço SMTP do remetente.</span><span class="sxs-lookup"><span data-stu-id="e2a52-112">GetSenderSMTPAddress then uses the [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) property of the **ExchangeUser** object to return the SMTP address of the sender.</span></span> <span data-ttu-id="e2a52-113">Se o objeto **AddressEntry** do remetente não representa um objeto **ExchangeUser**, o método [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) do objeto **PropertyAccessor** é usado, com **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) como argumento, para retornar o endereço do SMTP do remetente.</span><span class="sxs-lookup"><span data-stu-id="e2a52-113">If the **AddressEntry** object for the sender does not represent an **ExchangeUser** object, the [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) method of the **PropertyAccessor** object is used, with **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) as the argument, to return the sender’s SMTP address.</span></span>

<span data-ttu-id="e2a52-114">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e2a52-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e2a52-115">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="e2a52-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e2a52-116">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="e2a52-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetSenderSMTPAddress(Outlook.MailItem mail)
{
    string PR_SMTP_ADDRESS =
        @"https://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    if (mail == null)
    {
        throw new ArgumentNullException();
    }
    if (mail.SenderEmailType == "EX")
    {
        Outlook.AddressEntry sender =
            mail.Sender;
        if (sender != null)
        {
            //Now we have an AddressEntry representing the Sender
            if (sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                //Use the ExchangeUser object PrimarySMTPAddress
                Outlook.ExchangeUser exchUser =
                    sender.GetExchangeUser();
                if (exchUser != null)
                {
                    return exchUser.PrimarySmtpAddress;
                }
                else
                {
                    return null;
                }
            }
            else
            {
                return sender.PropertyAccessor.GetProperty(
                    PR_SMTP_ADDRESS) as string;
            }
        }
        else
        {
            return null;
        }
    }
    else
    {
        return mail.SenderEmailAddress;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="e2a52-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2a52-117">See also</span></span>

- [<span data-ttu-id="e2a52-118">Email</span><span class="sxs-lookup"><span data-stu-id="e2a52-118">Mail</span></span>](mail.md)

