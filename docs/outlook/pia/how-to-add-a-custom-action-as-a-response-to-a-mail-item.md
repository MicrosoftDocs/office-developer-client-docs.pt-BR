---
title: Adicionar uma ação personalizada como resposta a um item de email
TOCTitle: Add a custom action as a response to a mail item
ms:assetid: 99e8ba6b-9c47-4b10-968b-436b08d199ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424474(v=office.15)
ms:contentKeyID: 55119870
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6a82b02d357f86ca37d3ec4987ea6323d6d59cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359749"
---
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a><span data-ttu-id="73e5a-102">Adicionar uma ação personalizada como resposta a um item de email</span><span class="sxs-lookup"><span data-stu-id="73e5a-102">Add a custom action as a response to a mail item</span></span>

<span data-ttu-id="73e5a-103">Este exemplo mostra como adicionar ações personalizadas como resposta a um item de email usando o método [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) do conjunto [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="73e5a-103">This example shows how to add custom actions as a response to an email item by using the [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) method of the [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)) collection.</span></span>

## <a name="example"></a><span data-ttu-id="73e5a-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="73e5a-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="73e5a-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="73e5a-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="73e5a-106">Você pode criar ações personalizadas programaticamente para serem exibidas na faixa de opções no grupo **Ações** na guia **Mensagem** em uma resposta de email.</span><span class="sxs-lookup"><span data-stu-id="73e5a-106">You can create custom actions programmatically to appear on the ribbon in the **Actions** group on the **Message** tab in an email response.</span></span> <span data-ttu-id="73e5a-107">No exemplo de código a seguir, ReplyWithVoiceMail cria e adiciona uma ação personalizada denominada “Responder com correio de voz” à barra de comandos do inspetor.</span><span class="sxs-lookup"><span data-stu-id="73e5a-107">In the following code example, ReplyWithVoiceMail creates and adds a custom action named “Reply with Voice Mail” to the inspector command bar.</span></span> <span data-ttu-id="73e5a-108">ReplyWithVoiceMail primeiro obtém um objeto [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) e cria um objeto [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) chamando o método **Add** do conjunto **Actions** que está associado ao **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="73e5a-108">ReplyWithVoiceMail first gets a [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) object and then creates an [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) object by calling the **Add** method of the **Actions** collection that is associated with the **MailItem**.</span></span> <span data-ttu-id="73e5a-109">Em seguida, configura a propriedade [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) do objeto **Action** para "Responder com mensagem de voz".</span><span class="sxs-lookup"><span data-stu-id="73e5a-109">It then sets the [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) property of the **Action** object to “Reply with Voice Mail”.</span></span> <span data-ttu-id="73e5a-110">As propriedades [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)) e [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) também são definidas.</span><span class="sxs-lookup"><span data-stu-id="73e5a-110">The [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)), and [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) properties are also set.</span></span> <span data-ttu-id="73e5a-111">Por fim, o **MailItem** é salvo.</span><span class="sxs-lookup"><span data-stu-id="73e5a-111">Finally, the **MailItem**is saved.</span></span>


> [!NOTE]
> <span data-ttu-id="73e5a-112">Você também pode adicionar ações personalizadas no tempo de design usando o Designer de formulários do Outlook.</span><span class="sxs-lookup"><span data-stu-id="73e5a-112">You can also add custom actions at design time by using the Outlook Forms Designer.</span></span>


<span data-ttu-id="73e5a-113">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="73e5a-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="73e5a-114">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="73e5a-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="73e5a-115">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="73e5a-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="73e5a-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="73e5a-116">See also</span></span>

- [<span data-ttu-id="73e5a-117">Email</span><span class="sxs-lookup"><span data-stu-id="73e5a-117">Mail</span></span>](mail.md)

