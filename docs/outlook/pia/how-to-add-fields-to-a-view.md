---
title: Adicionar campos a um modo de exibição
TOCTitle: Add fields to a view
ms:assetid: ea371f27-ea65-47ef-ae44-ef843a78ab6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424481(v=office.15)
ms:contentKeyID: 55119934
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4b850bf87be4024152ee808624ad93836b904897
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359693"
---
# <a name="add-fields-to-a-view"></a>Adicionar campos a um modo de exibição

Este exemplo mostra como personalizar um modo de exibição usando o método [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) do conjunto [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) para adicionar campos a um modo de exibição.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


É possível especificar que propriedades de item do Outlook são exibidas em um modo de exibição adicionando uma ou mais propriedades à coleção **ViewFields** para apenas os objetos [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) e [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)). Para outros objetos **View** derivados, como [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)) e [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)), use outros métodos para determinar quais propriedades de item do Outlook são exibidas no modo de exibição. Por exemplo, os campos exibidos para o objeto **BusinessCardView** são determinados pelo layout de cartão de visita eletrônico (CVE) associado a cada item do Outlook exibido.

Para acessar o conjunto **ViewFields** de um modo de exibição, use a propriedade **ViewFields** do objeto **View** associado (por exemplo, os objetos **CardView** ou **TableView**). O método **Add** do conjunto **ViewFields** é usado para criar um objeto [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) que representa a propriedade de item do Outlook a ser exibida no modo de exibição. Um objeto **ViewField** não apenas identifica a propriedade de um item do Outlook a ser exibida no modo de exibição, mas também descreve de que forma os valores da propriedade devem ser exibidos. Você pode alterar como as propriedades de coluna individuais são exibidas em um modo de exibição modificando a propriedade [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) do objeto **ViewField**.

No exemplo de código a seguir, ModifyMeetingRequestsView recebe o objeto **TableView**, que representa todos os modos de exibição da Caixa de Entrada do usuário que sejam modos de exibição "Solicitações de Reunião". O exemplo, em seguida, usa o método **Add** para adicionar campos "Start" e "End" ao objeto **ViewFields** que corresponde ao objeto **TableView**. Ele também altera o rótulo do campo "From" para "Organized By". ModifyMeetingRequestsView salva o objeto **TableView** modificado.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ModifyMeetingRequestsView()
{
    Outlook.TableView tableView = null;
    Outlook.ViewField startField = null;
    Outlook.ViewField endField = null;
    Outlook.ViewField fromField = null;
    try
    {
        tableView =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            .Views["Meeting Requests"] as Outlook.TableView;
    }
    catch { }
    if (tableView != null)
    {
        try
        {
            startField = tableView.ViewFields["Start"];
        }
        catch{}
        if (startField == null)
        {
            startField = tableView.ViewFields.Add("Start");
        }
        try
        {
            endField = tableView.ViewFields["End"];
        }
        catch{}
        if (endField == null)
        {
            endField = tableView.ViewFields.Add("End");
        }
        try
        {
            fromField = tableView.ViewFields["From"];
        }
        catch{}
        if (fromField != null)
        {
            fromField.ColumnFormat.Label = "Organized By";
        }
        try
        {
            tableView.Save();
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Modos de exibição](views.md)

