---
title: Enviar um email com o endereço SMTP de uma conta
TOCTitle: Send an email given the SMTP address of an account
ms:assetid: 4ff4aaac-54ba-45c7-8b2e-aeba35af1e56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462095(v=office.15)
ms:contentKeyID: 55119865
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 01eef87c70e27425182b8a2f9f849c9736d43a31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406390"
---
# <a name="send-an-email-given-the-smtp-address-of-an-account"></a>Enviar um email com o endereço SMTP de uma conta

Este tópico mostra como criar um email e enviá-lo de uma conta do Microsoft Outlook, dado o endereço SMTP da conta.

## <a name="example"></a>Exemplo

> [!NOTE] 
> Helmut Obertanner forneceu os exemplos de código a seguir. A experiência de Helmut é em Ferramentas de Desenvolvedor do Office para Visual Studio e Outlook. 


Os exemplos a seguir contêm os métodos SendEmailFromAccount e GetAccountForEmailAddress da classe Sample, implementados como parte de um projeto de suplemento do Outlook. Cada projeto adiciona uma referência ao PIA do Outlook, que se baseia no namespace [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)). O método SendEmailFromAccount aceita como entrada um objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) confiável, além de cadeias de caracteres que representam o assunto, corpo, uma lista de destinatários separada por ponto e vírgula e o endereço SMTP de uma conta de email. SendEmailFromAccount cria um objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) e inicializa as propriedades [To](https://msdn.microsoft.com/library/bb624372\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) e [Body](https://msdn.microsoft.com/library/bb646600\(v=office.15\)) com os argumentos definidos. Para localizar o objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) do qual enviar o email, SendEmailFromAccount chama o método GetAccountForEmailAddress, que corresponde ao endereço SMTP fornecido com a propriedade [SmtpAddress](https://msdn.microsoft.com/library/bb623516\(v=office.15\)) de cada conta do perfil atual. O objeto **Account** correspondente será retornado para SendEmailFromAccount, que inicializará a propriedade [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) de **MailItem** com este objeto **Account** e enviará o **MailItem**.

A seguir está um exemplo de código do Visual Basic, seguido do exemplo de código C\#.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **Imports** ou **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionada antes da declaração de Classe pública. As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.

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

## <a name="see-also"></a>Confira também

- [Email](mail.md)

