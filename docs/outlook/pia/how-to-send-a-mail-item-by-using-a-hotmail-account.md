---
title: Enviar um item de email usando uma conta do Hotmail
TOCTitle: Send a mail item by using a Hotmail account
ms:assetid: f25853a7-67c0-46a3-a298-5cdf72ebc53f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184652(v=office.15)
ms:contentKeyID: 55119797
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 008f66ff1a43f90e756900c467ba6c086829b769
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331161"
---
# <a name="send-a-mail-item-by-using-a-hotmail-account"></a><span data-ttu-id="5c58e-102">Enviar um item de email usando uma conta do Hotmail</span><span class="sxs-lookup"><span data-stu-id="5c58e-102">Send a mail item by using a Hotmail account</span></span>

<span data-ttu-id="5c58e-103">Este exemplo usa a propriedade [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) para enviar um item de email usando uma conta do Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="5c58e-103">This example uses the [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) property to send a mail item by using a Windows Live Hotmail account.</span></span>

## <a name="example"></a><span data-ttu-id="5c58e-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5c58e-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="5c58e-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="5c58e-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="5c58e-106">Um perfil define uma ou mais contas de email e cada conta de email é associada a um servidor de um tipo específico, como o Microsoft Exchange Server ou o Post Office Protocol 3 (POP3).</span><span class="sxs-lookup"><span data-stu-id="5c58e-106">A profile defines one or more email accounts, and each email account is associated with a server of a specific type, such as Microsoft Exchange Server or Post Office Protocol 3 (POP3).</span></span> <span data-ttu-id="5c58e-107">Como você pode ter várias contas em seu perfil, você deve especificar qual conta de email deseja usar para enviar o item e, em seguida, obter um objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) para representá-lo.</span><span class="sxs-lookup"><span data-stu-id="5c58e-107">Because you may have multiple accounts in your profile, you must specify which email account you want to use to send the item, and then obtain an [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object to represent it.</span></span>

<span data-ttu-id="5c58e-108">No exemplo de código a seguir, uma mensagem é criada com um itinerário anexado e, em seguida, enviada usando uma conta do Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="5c58e-108">In the following code example, a message is created with an attached itinerary and then sent by using a Windows Live Hotmail account.</span></span> <span data-ttu-id="5c58e-109">A conta de email do Hotmail é usada como o objeto **Account** no perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c58e-109">The Hotmail email account is used as the **Account** object in the user’s profile.</span></span> <span data-ttu-id="5c58e-110">O exemplo de código, em seguida, define a propriedade SendUsingAccount para essa conta e chama o método [Send ()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) do objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5c58e-110">The code example then sets the SendUsingAccount property to that Account and calls the [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) method from the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span>

<span data-ttu-id="5c58e-111">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5c58e-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="5c58e-112">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="5c58e-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5c58e-113">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="5c58e-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void SendUsingAccountExample()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Our itinerary";
    mail.Attachments.Add(@"c:\travel\itinerary.doc",
        Outlook.OlAttachmentType.olByValue,
        Type.Missing, Type.Missing);
    Outlook.Account account =
        Application.Session.Accounts["Hotmail"];
    mail.SendUsingAccount = account;
    mail.Send();
}
```

## <a name="see-also"></a><span data-ttu-id="5c58e-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c58e-114">See also</span></span>

- [<span data-ttu-id="5c58e-115">Contas</span><span class="sxs-lookup"><span data-stu-id="5c58e-115">Accounts</span></span>](accounts.md)

