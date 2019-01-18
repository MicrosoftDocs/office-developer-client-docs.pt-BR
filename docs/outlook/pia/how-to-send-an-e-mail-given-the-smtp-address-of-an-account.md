---
title: Enviar um email com o endereço SMTP de uma conta
TOCTitle: Send an email given the SMTP address of an account
ms:assetid: 4ff4aaac-54ba-45c7-8b2e-aeba35af1e56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462095(v=office.15)
ms:contentKeyID: 55119865
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0771941581d0edaab1660790582cfb22bef48dc6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698684"
---
# <a name="send-an-email-given-the-smtp-address-of-an-account"></a><span data-ttu-id="862c7-102">Enviar um email com o endereço SMTP de uma conta</span><span class="sxs-lookup"><span data-stu-id="862c7-102">Send an email given the SMTP address of an account</span></span>

<span data-ttu-id="862c7-103">Este tópico mostra como criar um email e enviá-lo de uma conta do Microsoft Outlook, dado o endereço SMTP da conta.</span><span class="sxs-lookup"><span data-stu-id="862c7-103">This topic shows how to create an email and send it from a Microsoft Outlook account, given the Simple Mail Transfer Protocol (SMTP) address of that account.</span></span>

## <a name="example"></a><span data-ttu-id="862c7-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="862c7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="862c7-105">Helmut Obertanner forneceu os exemplos de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="862c7-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="862c7-106">A experiência de Helmut é em Ferramentas de Desenvolvedor do Office para Visual Studio e Outlook.</span><span class="sxs-lookup"><span data-stu-id="862c7-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 


<span data-ttu-id="862c7-107">Os exemplos a seguir contêm os métodos SendEmailFromAccount e GetAccountForEmailAddress da classe Sample, implementados como parte de um projeto de suplemento do Outlook.</span><span class="sxs-lookup"><span data-stu-id="862c7-107">The following code examples contain the SendEmailFromAccount and GetAccountForEmailAddress methods of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="862c7-108">Cada projeto adiciona uma referência ao PIA do Outlook, que se baseia no namespace [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="862c7-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span> <span data-ttu-id="862c7-109">O método SendEmailFromAccount aceita como entrada um objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) confiável, além de cadeias de caracteres que representam o assunto, corpo, uma lista de destinatários separada por ponto e vírgula e o endereço SMTP de uma conta de email.</span><span class="sxs-lookup"><span data-stu-id="862c7-109">The SendEmailFromAccount method accepts as input arguments a trusted [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object, and strings that represent the subject, body, a semicolon-delimited list of recipients, and the SMTP address of an email account.</span></span> <span data-ttu-id="862c7-110">SendEmailFromAccount cria um objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) e inicializa as propriedades [To](https://msdn.microsoft.com/library/bb624372\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) e [Body](https://msdn.microsoft.com/library/bb646600\(v=office.15\)) com os argumentos definidos.</span><span class="sxs-lookup"><span data-stu-id="862c7-110">SendEmailFromAccount creates a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object and initializes the [To](https://msdn.microsoft.com/library/bb624372\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)), and [Body](https://msdn.microsoft.com/library/bb646600\(v=office.15\)) properties with the given arguments.</span></span> <span data-ttu-id="862c7-111">Para localizar o objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) do qual enviar o email, SendEmailFromAccount chama o método GetAccountForEmailAddress, que corresponde ao endereço SMTP fornecido com a propriedade [SmtpAddress](https://msdn.microsoft.com/library/bb623516\(v=office.15\)) de cada conta do perfil atual.</span><span class="sxs-lookup"><span data-stu-id="862c7-111">To find the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object from which to send the email, SendEmailFromAccount calls the GetAccountForEmailAddress method, which matches the given SMTP address with the [SmtpAddress](https://msdn.microsoft.com/library/bb623516\(v=office.15\)) property of each account for the current profile.</span></span> <span data-ttu-id="862c7-112">O objeto **Account** correspondente será retornado para SendEmailFromAccount, que inicializará a propriedade [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) de **MailItem** com este objeto **Account** e enviará o **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="862c7-112">The matching **Account** object is returned to SendEmailFromAccount, which then initializes the [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) property of the **MailItem** with this **Account** object, and sends the **MailItem**.</span></span>

<span data-ttu-id="862c7-113">A seguir está um exemplo de código do Visual Basic, seguido do exemplo de código C\#.</span><span class="sxs-lookup"><span data-stu-id="862c7-113">The following is the Visual Basic code example, followed by the C\# code example.</span></span>

<span data-ttu-id="862c7-114">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="862c7-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="862c7-115">A instrução **Imports** ou **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionada antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="862c7-115">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="862c7-116">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="862c7-116">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        
        Shared Sub SendEmailFromAccount(ByVal application As Outlook.Application, _
            ByVal subject As String, ByVal body As String, ByVal recipients As String, ByVal smtpAddress As String)

            ' Create a new MailItem and set the To, Subject, and Body properties.
            Dim newMail As Outlook.MailItem = DirectCast(application.CreateItem(Outlook.OlItemType.olMailItem), Outlook.MailItem)
            newMail.To = recipients
            newMail.Subject = subject
            newMail.Body = body

            ' Retrieve the account that has the specific SMTP address.
            Dim account As Outlook.Account = GetAccountForEmailAddress(application, smtpAddress)
            ' Use this account to send the email.
            newMail.SendUsingAccount = account
            newMail.Send()
        End Sub

        Shared Function GetAccountForEmailAddress(ByVal application As Outlook.Application, ByVal smtpAddress As String) As Outlook.Account

            ' Loop over the Accounts collection of the current Outlook session.
            Dim accounts As Outlook.Accounts = application.Session.Accounts
            Dim account As Outlook.Account
            For Each account In accounts
                ' When the email address matches, return the account.
                If account.SmtpAddress = smtpAddress Then
                    Return account
                End If
            Next
            Throw New System.Exception(String.Format("No Account with SmtpAddress: {0} exists!", smtpAddress))
        End Function

    End Class
End Namespace
```


```csharp
using System;
using System.Text;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        public static void SendEmailFromAccount(Outlook.Application application, string subject, string body, string to, string smtpAddress)
        {

            // Create a new MailItem and set the To, Subject, and Body properties.
            Outlook.MailItem newMail = (Outlook.MailItem)application.CreateItem(Outlook.OlItemType.olMailItem);
            newMail.To = to;
            newMail.Subject = subject;
            newMail.Body = body;

            // Retrieve the account that has the specific SMTP address.
            Outlook.Account account = GetAccountForEmailAddress(application, smtpAddress);
            // Use this account to send the email.
            newMail.SendUsingAccount = account;
            newMail.Send();
        }


        public static Outlook.Account GetAccountForEmailAddress(Outlook.Application application, string smtpAddress)
        {

            // Loop over the Accounts collection of the current Outlook session.
            Outlook.Accounts accounts = application.Session.Accounts;
            foreach (Outlook.Account account in accounts)
            {
                // When the email address matches, return the account.
                if (account.SmtpAddress == smtpAddress)
                {
                    return account;
                }
            }
            throw new System.Exception(string.Format("No Account with SmtpAddress: {0} exists!", smtpAddress));
        }

    }
}
```

## <a name="see-also"></a><span data-ttu-id="862c7-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="862c7-117">See also</span></span>

- [<span data-ttu-id="862c7-118">Email</span><span class="sxs-lookup"><span data-stu-id="862c7-118">Mail</span></span>](mail.md)

