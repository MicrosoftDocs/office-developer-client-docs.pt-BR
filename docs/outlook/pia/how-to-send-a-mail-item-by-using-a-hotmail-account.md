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
# <a name="send-a-mail-item-by-using-a-hotmail-account"></a>Enviar um item de email usando uma conta do Hotmail

Este exemplo usa a propriedade [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) para enviar um item de email usando uma conta do Windows Live Hotmail.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Um perfil define uma ou mais contas de email e cada conta de email é associada a um servidor de um tipo específico, como o Microsoft Exchange Server ou o Post Office Protocol 3 (POP3). Como você pode ter várias contas em seu perfil, você deve especificar qual conta de email deseja usar para enviar o item e, em seguida, obter um objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) para representá-lo.

No exemplo de código a seguir, uma mensagem é criada com um itinerário anexado e, em seguida, enviada usando uma conta do Windows Live Hotmail. A conta de email do Hotmail é usada como o objeto **Account** no perfil do usuário. O exemplo de código, em seguida, define a propriedade SendUsingAccount para essa conta e chama o método [Send ()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) do objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Contas](accounts.md)

