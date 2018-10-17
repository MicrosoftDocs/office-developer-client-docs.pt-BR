---
title: Obter o endereço SMTP do remetente de uma mensagem
TOCTitle: Get the SMTP address of the sender of a mail item
ms:assetid: 86e0c0aa-1696-4415-b25f-f9c1c29d88a9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184624(v=office.15)
ms:contentKeyID: 55119869
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2346257dd2c23f09b77a72b08e17ba51f3f514d1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405550"
---
# <a name="get-the-smtp-address-of-the-sender-of-a-mail-item"></a>Obter o endereço SMTP do remetente de uma mensagem

Este exemplo contém o endereço de email SMTP do remetente para um item de email.

## <a name="example"></a>Exemplo

Para determinar o endereço SMTP de um item de email recebido, use a propriedade [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) do objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)). No entanto, se o remetente for um membro interno da sua organização, **SenderEmailAddress** não retorna um endereço SMTP, e você deve usar o objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) para retornar o endereço SMTP do remetente.

No exemplo de código a seguir, GetSenderSMTPAddress usa o objeto **PropertyAccessor** para obter valores que não são expostos diretamente no modelo de objeto do Outlook. GetSenderSMTPAddress leva um **MailItem**. Se o valor da propriedade [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) do **MailItem** recebido for "EX", o remetente da mensagem está localizado em um servidor do Exchange na sua organização. GetSenderSMTPAddress usa a propriedade [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) do objeto **MailItem** para obter o remetente, representado pelo objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)). Se o objeto **AddressEntry** objeto representa um usuário do Exchange, o exemplo chama o método [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) para retornar o objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) do objeto **AddressEntry**. GetSenderSMTPAddress usa a propriedade [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) do objeto **ExchangeUser** para retornar o endereço SMTP do remetente. Se o objeto **AddressEntry** do remetente não representa um objeto **ExchangeUser**, o método [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) do objeto **PropertyAccessor** é usado, com **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) como argumento, para retornar o endereço do SMTP do remetente.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. O ** que usa a instrução** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Email](mail.md)

