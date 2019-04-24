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
# <a name="add-voting-options-to-a-mail-item"></a>Adicionar opções de votação a um item de email

Este exemplo mostra como usar a propriedade [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) do objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) para adicionar opções de votação a uma mensagem de email.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


As opções de votação nas mensagens são usadas para fornecer aos destinatários da mensagem uma lista de opções e para rastrear suas respostas. Para criar opções de votação programaticamente, defina uma cadeia de caracteres que seja uma lista delimitada por ponto-e-vírgula de valores para a propriedade **VotingOptions** de um objeto **MailItem**. Os valores da propriedade **VotingOptions** aparecerão sob o comando **Vote** no grupo **Respond** na faixa de opções da mensagem recebida.

No exemplo a seguir, OrderPizza cria opções de votação em uma nova mensagem de email. OrderPizza primeiro cria um **MailItem** e, em seguida, define a propriedade **VotingOptions** como “Queijo; Cogumelo; Linguiça; Combinação; Combinação de vegetais”, e a propriedade [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) para “Pedido de pizza”. Quando a mensagem "Pedido de pizza" é enviada, as opções de votação são exibidas para os destinatários. Para cada resposta recebida, a escolha do destinatário será computada na página **Acompanhamento** da mensagem na pasta Itens Enviados do remetente.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Email](mail.md)

