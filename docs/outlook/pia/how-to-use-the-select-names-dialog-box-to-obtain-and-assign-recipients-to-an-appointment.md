---
title: Use a caixa de diálogo Selecionar Nomes para obter e atribuir destinatários a um compromisso
TOCTitle: Use the Select Names dialog box to obtain and assign recipients to an appointment
ms:assetid: b9bcb341-1912-425c-8d75-ed5be233145a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184636(v=office.15)
ms:contentKeyID: 55119878
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 408d2fbdc3c89b7f2bad1fe9c2c76c1f47ae05ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335375"
---
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a>Use a caixa de diálogo Selecionar Nomes para obter e atribuir destinatários a um compromisso

Este exemplo mostra como usar a caixa de diálogo **Selecionar Nomes** para obter e atribuir destinatários a um item de compromisso.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Para exibir a caixa de diálogo **Selecionar Nomes**, chame o método [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) do objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)). Depois que a caixa de diálogo **Selecionar Nomes** é exibida para o usuário, a execução de código é interrompida até que o usuário clique em **OK** ou feche a caixa de diálogo. Para definir destinatários iniciais a exibir na caixa de diálogo, ou para obter os destinatários selecionados na caixa de diálogo, use a propriedade [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) do objeto **SelectNamesDialog**. Isso retornará um conjunto [destinatários](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) associado a **SelectNamesDialog**. Para adicionar um objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) ao conjunto **Recipients** de **SelectNamesDialog**, use o método [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) para o conjunto e especifique a propriedade [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) do objeto **Recipient**.

No exemplo de código a seguir, DemoSelectNamesDialogRecipients cria um objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) e define algumas das suas propriedades. Em seguida, cria um **SelectNamesDialog** e usa o método [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) para configurar um modo de exibição de reunião para a caixa de diálogo **Selecionar Nomes**. O exemplo preenche o seletor de destinatário **Resource** com a cadeia "Conf Room 36/2739". Depois que a caixa de diálogo é exibida para o usuário, o código enumera o conjunto **Recipients** que é associado a essa instância de **SelectNamesDialog** e adiciona esses destinatários ao compromisso que foi criado. Por fim, o exemplo a exibe a solicitação de reunião para o usuário.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Destinatários](recipients.md)

