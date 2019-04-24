---
title: Obter informações sobre várias contas
TOCTitle: Get information about multiple accounts
ms:assetid: 363f4058-3069-4ddc-b3ff-113a4dfd58c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184599(v=office.15)
ms:contentKeyID: 55119794
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d065761b9296f1c0eb3043e9b9778e438790f94e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349410"
---
# <a name="get-information-about-multiple-accounts"></a>Obter informações sobre várias contas

O Outlook dá suporte a um perfil que contém uma ou mais contas conectadas a um Exchange Server. Este exemplo mostra como obter e exibir diversas informações sobre cada conta no perfil atual.

## <a name="example"></a>Exemplo

O método a seguir, EnumerateAccounts, exibe o nome da conta, o nome de usuário e o endereço SMTP (Simple Mail Transfer Protocol) de cada conta definida no perfil atual. Se a conta estiver conectada a um servidor do Exchange, EnumerateAccounts exibirá informações sobre a versão e o nome do servidor do Exchange. Se a conta residir em um repositório de entrega, EnumerateAccounts exibirá o nome do repositório de entrega padrão da conta.

EnumerateAccounts acessa a maioria dessas informações do objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)), exceto quando o objeto **Account** não contém informações sobre o nome de usuário e endereço SMTP. Nesse caso, EnumerateAccounts usa os objetos [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) e [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)). 

EnumerateAccounts obtém o objeto **AddressEntry** usando a propriedade [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) do objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) obtido da propriedade [CurrentUser ](https://msdn.microsoft.com/library/ff184864\(v=office.15\)). EnumerateAccounts obtém o objeto **ExchangeUser** usando o método [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) do objeto **AddressEntry**. 

Este é o algoritmo para obter várias informações usando os objetos Account, AddressEntry e ExchangeUser:

- Se o objeto **Account** contiver informações sobre o nome de usuário e o endereço SMTP, use o objeto **Account** para exibir o nome da conta, o nome de usuário e o endereço SMTP, além de informações sobre a versão e o nome do servidor do Exchange, caso se trate de uma conta do Exchange.

- Se o objeto **Account** não contiver informações sobre o nome de usuário e endereço SMTP; continue da seguinte maneira:
    
  - Se a conta não for uma conta do Exchange, use o objeto **AddressEntry** para exibir o nome de usuário e endereço SMTP.
    
  - Se a conta for uma conta do Exchange; continue da seguinte maneira:
        
    1.  Use o objeto **Account** para exibir o nome da conta, o nome do servidor Exchange e as informações de versão do Exchange.
        
    2.  Use o objeto **ExchangeUser** para exibir o nome de usuário e endereço SMTP.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAccounts()
{
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        try
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Account: " + account.DisplayName);
            if (string.IsNullOrEmpty(account.SmtpAddress)
                || string.IsNullOrEmpty(account.UserName))
            {
                Outlook.AddressEntry oAE =
                    account.CurrentUser.AddressEntry
                    as Outlook.AddressEntry;
                if (oAE.Type == "EX")
                {
                    Outlook.ExchangeUser oEU =
                        oAE.GetExchangeUser()
                        as Outlook.ExchangeUser;
                    sb.AppendLine("UserName: " +
                        oEU.Name);
                    sb.AppendLine("SMTP: " +
                        oEU.PrimarySmtpAddress);
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
                else
                {
                    sb.AppendLine("UserName: " +
                        oAE.Name);
                    sb.AppendLine("SMTP: " +
                        oAE.Address);
                }
            }
            else
            {
                sb.AppendLine("UserName: " +
                    account.UserName);
                sb.AppendLine("SMTP: " +
                    account.SmtpAddress);
                if(account.AccountType == 
                    Outlook.OlAccountType.olExchange)
                {
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
            }
            if(account.DeliveryStore !=null)
            {
                sb.AppendLine("Delivery Store: " +
                    account.DeliveryStore.DisplayName);
            }
            sb.AppendLine("---------------------------------");
            Debug.Write(sb.ToString());
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Contas](accounts.md)

