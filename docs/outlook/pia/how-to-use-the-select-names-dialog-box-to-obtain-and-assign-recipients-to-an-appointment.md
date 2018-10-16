---
title: Use a caixa de diálogo Selecionar Nomes para obter e atribuir destinatários a um compromisso
TOCTitle: Use the Select Names dialog box to obtain and assign recipients to an appointment
ms:assetid: b9bcb341-1912-425c-8d75-ed5be233145a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184636(v=office.15)
ms:contentKeyID: 55119878
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 57a7c99efa2bd82e1bc3d3f0855a90b62109719c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406999"
---
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a><span data-ttu-id="204d5-102">Use a caixa de diálogo Selecionar Nomes para obter e atribuir destinatários a um compromisso</span><span class="sxs-lookup"><span data-stu-id="204d5-102">Use the Select Names dialog box to obtain and assign recipients to an appointment</span></span>

<span data-ttu-id="204d5-103">Este exemplo mostra como usar a caixa de diálogo **Selecionar Nomes** para obter e atribuir destinatários a um item de compromisso.</span><span class="sxs-lookup"><span data-stu-id="204d5-103">This example shows how to use the **Select Names** dialog box to obtain and assign recipients to an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="204d5-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="204d5-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="204d5-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="204d5-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="204d5-106">Para exibir a caixa de diálogo **Selecionar Nomes**, chame o método [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) do objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="204d5-106">To display the **Select Names** dialog box, call the [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) method of the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object.</span></span> <span data-ttu-id="204d5-107">Depois que a caixa de diálogo **Selecionar Nomes** é exibida para o usuário, a execução de código é interrompida até que o usuário clique em **OK** ou feche a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="204d5-107">Once the **Select Names** dialog box is displayed to the user, code execution halts until the user clicks **OK** or closes the dialog box.</span></span> <span data-ttu-id="204d5-108">Para definir destinatários iniciais a exibir na caixa de diálogo, ou para obter os destinatários selecionados na caixa de diálogo, use a propriedade [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) do objeto **SelectNamesDialog**.</span><span class="sxs-lookup"><span data-stu-id="204d5-108">To set initial recipients to display in the dialog box, or to get the recipients selected in the dialog box, use the [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) property of the **SelectNamesDialog** object.</span></span> <span data-ttu-id="204d5-109">Isso retornará um conjunto [destinatários](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) associado a **SelectNamesDialog**.</span><span class="sxs-lookup"><span data-stu-id="204d5-109">This returns a [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that is associated with the **SelectNamesDialog**.</span></span> <span data-ttu-id="204d5-110">Para adicionar um objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) ao conjunto **Recipients** de **SelectNamesDialog**, use o método [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) para o conjunto e especifique a propriedade [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) do objeto **Recipient**.</span><span class="sxs-lookup"><span data-stu-id="204d5-110">To add a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object to the **Recipients** collection for the **SelectNamesDialog**, use the [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) method for the collection and specify the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of the **Recipient** object.</span></span>

<span data-ttu-id="204d5-111">No exemplo de código a seguir, DemoSelectNamesDialogRecipients cria um objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) e define algumas das suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="204d5-111">In the following code example, DemoSelectNamesDialogRecipients creates an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object and sets some of its properties.</span></span> <span data-ttu-id="204d5-112">Em seguida, cria um **SelectNamesDialog** e usa o método [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) para configurar um modo de exibição de reunião para a caixa de diálogo **Selecionar Nomes**.</span><span class="sxs-lookup"><span data-stu-id="204d5-112">It then creates a **SelectNamesDialog** and uses the [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) method to set a meeting display mode for the **Select Names** dialog box.</span></span> <span data-ttu-id="204d5-113">O exemplo preenche o seletor de destinatário **Resource** com a cadeia "Conf Room 36/2739".</span><span class="sxs-lookup"><span data-stu-id="204d5-113">The example populates the **Resource** recipient selector with the string "Conf Room 36/2739".</span></span> <span data-ttu-id="204d5-114">Depois que a caixa de diálogo é exibida para o usuário, o código enumera o conjunto **Recipients** que é associado a essa instância de **SelectNamesDialog** e adiciona esses destinatários ao compromisso que foi criado.</span><span class="sxs-lookup"><span data-stu-id="204d5-114">Once the dialog box is displayed to the user, the code enumerates the **Recipients** collection that is associated with this instance of **SelectNamesDialog** and adds those recipients to the appointment that was created.</span></span> <span data-ttu-id="204d5-115">Por fim, o exemplo a exibe a solicitação de reunião para o usuário.</span><span class="sxs-lookup"><span data-stu-id="204d5-115">Finally, the example displays the meeting request to the user.</span></span>

<span data-ttu-id="204d5-116">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="204d5-116">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="204d5-117">O \*\* que usa a instrução\*\* não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="204d5-117">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="204d5-118">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="204d5-118">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoSelectNamesDialogRecipients()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Subject = "Team Morale Event";
    appt.Start = DateTime.Parse("5/17/2007 11:00 AM");
    appt.End = DateTime.Parse("5/17/2007 12:00 PM");
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    snd.SetDefaultDisplayMode(
        Outlook.OlDefaultSelectNamesDisplayMode.olDefaultMeeting);
    Outlook.Recipient confRoom =
        snd.Recipients.Add("Conf Room 36/2739");
    // Explicitly specify Recipient.Type.
    confRoom.Type = (int)Outlook.OlMeetingRecipientType.olResource;
    snd.Recipients.ResolveAll();
    snd.Display();
    // Add Recipients to meeting request.
    Outlook.Recipients recips = snd.Recipients;
    if (recips.Count > 0)
    {
        foreach (Outlook.Recipient recip in recips)
        {
            appt.Recipients.Add(recip.Name);
        }
    }
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="204d5-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="204d5-119">See also</span></span>

- [<span data-ttu-id="204d5-120">Recipients</span><span class="sxs-lookup"><span data-stu-id="204d5-120">Recipients</span></span>](recipients.md)

