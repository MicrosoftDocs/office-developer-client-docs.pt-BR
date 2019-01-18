---
title: Criar um item de email, anexar um relatório e enviar o item de email ao gerente do usuário
TOCTitle: Create a mail item, attach a report, and send the mail item to the user's manager
ms:assetid: 15c26c3b-5e86-4e28-92c5-7389572521da
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644320(v=office.15)
ms:contentKeyID: 55119866
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 32c40e1fbda3f0f851b52d29c073d95a5d636620
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710290"
---
# <a name="create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-users-manager"></a><span data-ttu-id="605ac-102">Criar um item de email, anexar um relatório e enviar o item de email ao gerente do usuário</span><span class="sxs-lookup"><span data-stu-id="605ac-102">Create a mail item, attach a report, and send the mail item to the user's manager</span></span>

<span data-ttu-id="605ac-103">Este exemplo cria um item de email, anexa um relatório e envia o item de email ao gerente do usuário.</span><span class="sxs-lookup"><span data-stu-id="605ac-103">This example creates a mail item that has an attachment, and then sends the mail item to the user's manager.</span></span>

## <a name="example"></a><span data-ttu-id="605ac-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="605ac-104">Example</span></span>

<span data-ttu-id="605ac-105">Este exemplo é executado corretamente apenas em uma conta do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="605ac-105">This example runs correctly only against a Microsoft Exchange Server account.</span></span> <span data-ttu-id="605ac-106">É necessário estabelecer uma relação de gerente para usuários no serviço de diretório Active Directory.</span><span class="sxs-lookup"><span data-stu-id="605ac-106">A manager relationship for users must be established in the Active Directory directory service.</span></span> <span data-ttu-id="605ac-107">O exemplo usa o objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) para determinar o gerente do usuário atual chamando o método [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="605ac-107">The example uses the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object to determine the current user's manager by calling the [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method.</span></span>

<span data-ttu-id="605ac-108">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="605ac-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="605ac-109">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="605ac-109">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="605ac-110">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="605ac-110">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SendSalesReport()
    Dim mail As Outlook.MailItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olMailItem), Outlook.MailItem)
    mail.Subject = "Quarterly Sales Report FY06 Q4"
    Dim currentUser As Outlook.AddressEntry = _
        Application.Session.CurrentUser.AddressEntry
    If currentUser.Type = "EX" Then
        Dim manager As Outlook.ExchangeUser = _
            currentUser.GetExchangeUser().GetExchangeUserManager()
        ' Add recipient using display name, alias, or smtp address
        mail.Recipients.Add(manager.PrimarySmtpAddress)
        mail.Recipients.ResolveAll()
        mail.Attachments.Add("c:\sales reports\fy06q4.xlsx", _
            Outlook.OlAttachmentType.olByValue)
        mail.Send()
    End If
End Sub
```


```csharp
private void SendSalesReport()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Quarterly Sales Report FY06 Q4";
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        // Add recipient using display name, alias, or smtp address
        mail.Recipients.Add(manager.PrimarySmtpAddress);
        mail.Recipients.ResolveAll();
        mail.Attachments.Add(@"c:\sales reports\fy06q4.xlsx",
            Outlook.OlAttachmentType.olByValue, Type.Missing,
            Type.Missing);
        mail.Send();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="605ac-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="605ac-111">See also</span></span>

- [<span data-ttu-id="605ac-112">Email</span><span class="sxs-lookup"><span data-stu-id="605ac-112">Mail</span></span>](mail.md)

