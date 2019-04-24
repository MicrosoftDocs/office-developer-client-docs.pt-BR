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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320227"
---
# <a name="get-the-email-address-of-a-recipient"></a>Obter o endereço de email de um destinatário

Este exemplo mostra como receber o endereço SMTP de um destinatário.

## <a name="example"></a>Exemplo

A seguir, o exemplo de código, o método GetSMTPAddressForRecipients usa um objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) como um argumento de entrada e exibe o endereço SMTP de cada destinatário para esse item de email. O método primeiro recupera a coleção [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) que representa o conjunto de destinatários especificado para o item de email. Para cada [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) na coleção **Recipients**, o método obtém o objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) que corresponde ao objeto **Recipient**. Por fim, o método usa a propriedade [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) para obter o valor da propriedade https://schemas.microsoft.com/mapi/proptag/0x39FE001EMAPI, que mapeia para a **propriedade\_PR\_SMTP address** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) do destinatário.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Destinatários](recipients.md)

