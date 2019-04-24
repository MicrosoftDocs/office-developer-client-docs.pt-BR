---
title: Adicionar opções de votação a um item de email
TOCTitle: Add voting options to a mail item
ms:assetid: 0fb209a8-178d-411e-9551-0a72e041fd65
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424466(v=office.15)
ms:contentKeyID: 55119867
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3befe70363d1e2226b8a3a3a6ebb8db39aa2c6ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359721"
---
# <a name="add-voting-options-to-a-mail-item"></a><span data-ttu-id="3529f-102">Adicionar opções de votação a um item de email</span><span class="sxs-lookup"><span data-stu-id="3529f-102">Add voting options to a mail item</span></span>

<span data-ttu-id="3529f-103">Este exemplo mostra como usar a propriedade [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) do objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) para adicionar opções de votação a uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="3529f-103">This example shows how to use the [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) property of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object to add voting options to an email message.</span></span>

## <a name="example"></a><span data-ttu-id="3529f-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3529f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="3529f-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="3529f-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="3529f-106">As opções de votação nas mensagens são usadas para fornecer aos destinatários da mensagem uma lista de opções e para rastrear suas respostas.</span><span class="sxs-lookup"><span data-stu-id="3529f-106">Voting options on messages are used to give message recipients a list of choices and to track their responses.</span></span> <span data-ttu-id="3529f-107">Para criar opções de votação programaticamente, defina uma cadeia de caracteres que seja uma lista delimitada por ponto-e-vírgula de valores para a propriedade **VotingOptions** de um objeto **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="3529f-107">To create voting options programmatically, set a string that is a semicolon-delimited list of values for the **VotingOptions** property of a **MailItem** object.</span></span> <span data-ttu-id="3529f-108">Os valores da propriedade **VotingOptions** aparecerão sob o comando **Vote** no grupo **Respond** na faixa de opções da mensagem recebida.</span><span class="sxs-lookup"><span data-stu-id="3529f-108">The values for the **VotingOptions** property will appear under the **Vote** command in the **Respond** group in the ribbon of the received message.</span></span>

<span data-ttu-id="3529f-109">No exemplo a seguir, OrderPizza cria opções de votação em uma nova mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="3529f-109">In the following example, OrderPizza creates voting options in a new mail message.</span></span> <span data-ttu-id="3529f-110">OrderPizza primeiro cria um **MailItem** e, em seguida, define a propriedade **VotingOptions** como “Queijo; Cogumelo; Linguiça; Combinação; Combinação de vegetais”, e a propriedade [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) para “Pedido de pizza”.</span><span class="sxs-lookup"><span data-stu-id="3529f-110">OrderPizza first creates a **MailItem**, and then sets the **VotingOptions** property to “Cheese; Mushroom; Sausage; Combo; Veg Combo”, and the [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) property to “Pizza Order”.</span></span> <span data-ttu-id="3529f-111">Quando a mensagem "Pedido de pizza" é enviada, as opções de votação são exibidas para os destinatários.</span><span class="sxs-lookup"><span data-stu-id="3529f-111">When the “Pizza Order” message is sent, the voting options appear to recipients.</span></span> <span data-ttu-id="3529f-112">Para cada resposta recebida, a escolha do destinatário será computada na página **Acompanhamento** da mensagem na pasta Itens Enviados do remetente.</span><span class="sxs-lookup"><span data-stu-id="3529f-112">For each response received, the recipient’s choice will be tallied on the **Tracking** page of the message in the sender’s Sent Items folder.</span></span>

<span data-ttu-id="3529f-113">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="3529f-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3529f-114">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="3529f-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3529f-115">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="3529f-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void OrderPizza()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.CreateItem(
            Outlook.OlItemType.olMailItem);
        mail.VotingOptions = “Cheese; Mushroom; Sausage; Combo; Veg Combo;”
        mail.Subject = “Pizza Order”;
        mail.Display(false);
    }
```

## <a name="see-also"></a><span data-ttu-id="3529f-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="3529f-116">See also</span></span>

- [<span data-ttu-id="3529f-117">Email</span><span class="sxs-lookup"><span data-stu-id="3529f-117">Mail</span></span>](mail.md)

