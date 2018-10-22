---
title: Adicionar uma ação personalizada como resposta a um item de email
TOCTitle: Add a custom action as a response to a mail item
ms:assetid: 99e8ba6b-9c47-4b10-968b-436b08d199ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424474(v=office.15)
ms:contentKeyID: 55119870
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1858372ec8283b1926e5ed82f2a511a97a8242ec
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406852"
---
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a>Adicionar uma ação personalizada como resposta a um item de email

Este exemplo mostra como adicionar ações personalizadas como resposta a um item de email usando o método [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) do conjunto [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)).

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Você pode criar ações personalizadas programaticamente para serem exibidas na faixa de opções no grupo **Ações** na guia **Mensagem** em uma resposta de email. No exemplo de código a seguir, ReplyWithVoiceMail cria e adiciona uma ação personalizada denominada “Responder com correio de voz” à barra de comandos do inspetor. ReplyWithVoiceMail primeiro obtém um objeto [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) e cria um objeto [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) chamando o método **Add** do conjunto **Actions** que está associado ao **MailItem**. Em seguida, configura a propriedade [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) do objeto **Action** para "Responder com mensagem de voz". As propriedades [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)) e [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) também são definidas. Por fim, o **MailItem** é salvo.


> [!NOTE]
> Você também pode adicionar ações personalizadas no tempo de design usando o Designer de formulários do Outlook.


Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void ReplyWithVoiceMail()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.ActiveInspector().CurrentItem;
        Outlook.Action action = mail.Actions.Add();
        action.Name = “Reply with Voice Mail”;
        action.ReplyStyle = Outlook.OlActionReplyStyle.olUserPreference;
        action.ResponseStyle = Outlook.OlActionResponseStyle.olOpen;
        action.CopyLike = Outlook.OlActionCopyLike.olReply;
        action.MessageClass = “IPM.Post.Voice Message”;
        mail.Save();
    }
```

## <a name="see-also"></a>Confira também

- [Email](mail.md)

