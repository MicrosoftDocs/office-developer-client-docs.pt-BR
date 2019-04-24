---
title: Obter informações da conta
TOCTitle: Get account information
ms:assetid: 02825449-50eb-42d0-8e45-361db5f473df
ms:contentKeyID: 55119795
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b80a6c47373842437b9944ea25c212810a9de107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320185"
---
# <a name="get-account-information"></a><span data-ttu-id="4c7e9-102">Obter informações da conta</span><span class="sxs-lookup"><span data-stu-id="4c7e9-102">Get account information</span></span>

<span data-ttu-id="4c7e9-103">Este tópico obtém como argumento de entrada um objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) confiável do Outlook e usa o objeto **Account** para exibir os detalhes de cada conta que está disponível para o perfil atual do Outlook.</span><span class="sxs-lookup"><span data-stu-id="4c7e9-103">This topic takes as an input argument a trusted Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object, and uses the **Account** object to display the details of each account that is available for the current Outlook profile.</span></span>

## <a name="example"></a><span data-ttu-id="4c7e9-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4c7e9-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="4c7e9-105">Helmut Obertanner forneceu os exemplos de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c7e9-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="4c7e9-106">A experiência de Helmut é em Office Developer Tools para Visual Studio e Outlook.</span><span class="sxs-lookup"><span data-stu-id="4c7e9-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 

<span data-ttu-id="4c7e9-107">Os exemplos de código a seguir contêm o método DisplayAccountInformation da classe Sample, implementados como parte de um projeto de suplemento do Outlook.</span><span class="sxs-lookup"><span data-stu-id="4c7e9-107">The following code examples contain the DisplayAccountInformation method of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="4c7e9-108">Cada projeto adiciona uma referência para o Outlook PIA, que se baseia no namespace [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="4c7e9-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="4c7e9-109">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="4c7e9-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="4c7e9-110">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="4c7e9-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="4c7e9-111">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="4c7e9-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="4c7e9-112">A seguir está um exemplo de código do Visual Basic, seguido do exemplo de código C\#.</span><span class="sxs-lookup"><span data-stu-id="4c7e9-112">The following is the Visual Basic code example, followed by the C\# code example.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        Shared Sub DisplayAccountInformation(ByVal application As Outlook.Application)

            ' The Namespace Object (Session) has a collection of accounts.
            Dim accounts As Outlook.Accounts = application.Session.Accounts

            ' Concatenate a message with information about all accounts.
            Dim builder As StringBuilder = New StringBuilder()

            ' Loop over all accounts and print detail account information.
            ' All properties of the Account object are read-only.
            Dim account As Outlook.Account
            For Each account In accounts

                ' The DisplayName property represents the friendly name of the account.
                builder.AppendFormat("DisplayName: {0}" & vbNewLine, account.DisplayName)

                ' The UserName property provides an account-based context to determine identity.
                builder.AppendFormat("UserName: {0}" & vbNewLine, account.UserName)

                ' The SmtpAddress property provides the SMTP address for the account.
                builder.AppendFormat("SmtpAddress: {0}" & vbNewLine, account.SmtpAddress)

                ' The AccountType property indicates the type of the account.
                builder.Append("AccountType: ")
                Select Case (account.AccountType)

                    Case Outlook.OlAccountType.olExchange
                        builder.AppendLine("Exchange")


                    Case Outlook.OlAccountType.olHttp
                        builder.AppendLine("Http")


                    Case Outlook.OlAccountType.olImap
                        builder.AppendLine("Imap")


                    Case Outlook.OlAccountType.olOtherAccount
                        builder.AppendLine("Other")


                    Case Outlook.OlAccountType.olPop3
                        builder.AppendLine("Pop3")


                End Select

                builder.AppendLine()
            Next


            ' Display the account information.
            Windows.Forms.MessageBox.Show(builder.ToString())
        End Sub


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
        public static void DisplayAccountInformation(Outlook.Application application)
        {

            // The Namespace Object (Session) has a collection of accounts.
            Outlook.Accounts accounts = application.Session.Accounts;

            // Concatenate a message with information about all accounts.
            StringBuilder builder = new StringBuilder();

            // Loop over all accounts and print detail account information.
            // All properties of the Account object are read-only.
            foreach (Outlook.Account account in accounts)
            {

                // The DisplayName property represents the friendly name of the account.
                builder.AppendFormat("DisplayName: {0}\n", account.DisplayName);

                // The UserName property provides an account-based context to determine identity.
                builder.AppendFormat("UserName: {0}\n", account.UserName);

                // The SmtpAddress property provides the SMTP address for the account.
                builder.AppendFormat("SmtpAddress: {0}\n", account.SmtpAddress);

                // The AccountType property indicates the type of the account.
                builder.Append("AccountType: ");
                switch (account.AccountType)
                {

                    case Outlook.OlAccountType.olExchange:
                        builder.AppendLine("Exchange");
                        break;

                    case Outlook.OlAccountType.olHttp:
                        builder.AppendLine("Http");
                        break;

                    case Outlook.OlAccountType.olImap:
                        builder.AppendLine("Imap");
                        break;

                    case Outlook.OlAccountType.olOtherAccount:
                        builder.AppendLine("Other");
                        break;

                    case Outlook.OlAccountType.olPop3:
                        builder.AppendLine("Pop3");
                        break;
                }

                builder.AppendLine();
            }

            // Display the account information.
            System.Windows.Forms.MessageBox.Show(builder.ToString());
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="4c7e9-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c7e9-113">See also</span></span>

- [<span data-ttu-id="4c7e9-114">Contas</span><span class="sxs-lookup"><span data-stu-id="4c7e9-114">Accounts</span></span>](accounts.md)

