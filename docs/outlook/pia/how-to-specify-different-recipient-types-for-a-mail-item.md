---
title: Especificar tipos diferentes de destinatários para um item de email
TOCTitle: Specify different recipient types for a mail item
ms:assetid: 2a3ace9f-627c-4fdd-b182-afc1b53af85b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184598(v=office.15)
ms:contentKeyID: 55119871
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf61a7fbb470291eae448a93c80866112c41407a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335508"
---
# <a name="specify-different-recipient-types-for-a-mail-item"></a>Especificar tipos diferentes de destinatários para um item de email

Este exemplo mostra como definir programaticamente diferentes tipos de destinatários (Para, Cc ou Cco) para um item de email.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

O exemplo de código a seguir ilustra como especificar se um destinatário de um objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) é um destinatário de Para, Cc ou Cco. SetRecipientTypeForMail cria um objeto **MailItem**, adiciona três objetos [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) ao conjunto [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) do **MailItem** e, em seguida, define a propriedade [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) de cada objeto **Recipient** como um valor da enumeração [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)).


> [!NOTE]
> A propriedade **Type** do objeto **Recipient** é um tipo int e não está correlacionada a uma enumeração de tipo de destinatário específica.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void SetRecipientTypeForMail()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Sample Message";
    Outlook.Recipient recipTo =
        mail.Recipients.Add("someone@example.com");
    recipTo.Type = (int)Outlook.OlMailRecipientType.olTo;
    Outlook.Recipient recipCc =
        mail.Recipients.Add("someonecc@example.com");
    recipCc.Type = (int)Outlook.OlMailRecipientType.olCC;
    Outlook.Recipient recipBcc =
        mail.Recipients.Add("someonebcc@example.com");
    recipBcc.Type = (int)Outlook.OlMailRecipientType.olBCC;
    mail.Recipients.ResolveAll();
    mail.Display(false);
}
```

## <a name="see-also"></a>Confira também

- [Email](mail.md)

