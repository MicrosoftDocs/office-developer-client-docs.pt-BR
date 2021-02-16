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
# <a name="add-fields-to-a-view"></a><span data-ttu-id="01b00-102">Adicionar campos a um modo de exibição</span><span class="sxs-lookup"><span data-stu-id="01b00-102">Add fields to a view</span></span>

<span data-ttu-id="01b00-103">Este exemplo mostra como personalizar um modo de exibição usando o método [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) do conjunto [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) para adicionar campos a um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="01b00-103">This example shows how to customize a view by using the [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) method of the [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) collection to add fields to a view.</span></span>

## <a name="example"></a><span data-ttu-id="01b00-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="01b00-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="01b00-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="01b00-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="01b00-106">É possível especificar que propriedades de item do Outlook são exibidas em um modo de exibição adicionando uma ou mais propriedades à coleção **ViewFields** para apenas os objetos [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) e [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="01b00-106">You can specify which Outlook item properties are displayed in a view by adding one or more properties to the **ViewFields** collection for only the [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) and [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) objects.</span></span> <span data-ttu-id="01b00-107">Para outros objetos **View** derivados, como [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)) e [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)), use outros métodos para determinar quais propriedades de item do Outlook são exibidas no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="01b00-107">For other derived **View** objects such as [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)), and [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)) objects, use other methods of determining which Outlook item properties are displayed within the view.</span></span> <span data-ttu-id="01b00-108">Por exemplo, os campos exibidos para o objeto **BusinessCardView** são determinados pelo layout de cartão de visita eletrônico (CVE) associado a cada item do Outlook exibido.</span><span class="sxs-lookup"><span data-stu-id="01b00-108">For example, the fields displayed for the **BusinessCardView** object are determined by the electronic business card (EBC) layout associated with each displayed Outlook item.</span></span>

<span data-ttu-id="01b00-109">Para acessar o conjunto **ViewFields** de um modo de exibição, use a propriedade **ViewFields** do objeto **View** associado (por exemplo, os objetos **CardView** ou **TableView**).</span><span class="sxs-lookup"><span data-stu-id="01b00-109">To get the **ViewFields** collection for a view, use the **ViewFields** property of the associated **View** object (for example, the **CardView** or **TableView** objects).</span></span> <span data-ttu-id="01b00-110">O método **Add** do conjunto **ViewFields** é usado para criar um objeto [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) que representa a propriedade de item do Outlook a ser exibida no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="01b00-110">The **Add** method of the **ViewFields** collection is used to create a [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) object that represents the Outlook item property to be displayed in the view.</span></span> <span data-ttu-id="01b00-111">Um objeto **ViewField** não apenas identifica a propriedade de um item do Outlook a ser exibida no modo de exibição, mas também descreve de que forma os valores da propriedade devem ser exibidos.</span><span class="sxs-lookup"><span data-stu-id="01b00-111">A **ViewField** object not only identifies an Outlook item property to display within the view, but it also describes how the values for that property should be displayed.</span></span> <span data-ttu-id="01b00-112">Você pode alterar como as propriedades de coluna individuais são exibidas em um modo de exibição modificando a propriedade [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) do objeto **ViewField**.</span><span class="sxs-lookup"><span data-stu-id="01b00-112">You can change how individual column properties are displayed in a view by modifying the [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) property of the **ViewField** object.</span></span>

<span data-ttu-id="01b00-113">No exemplo de código a seguir, ModifyMeetingRequestsView recebe o objeto **TableView**, que representa todos os modos de exibição da Caixa de Entrada do usuário que sejam modos de exibição "Solicitações de Reunião".</span><span class="sxs-lookup"><span data-stu-id="01b00-113">In the following code example, ModifyMeetingRequestsView gets the **TableView** object that represents all the views from the user’s Inbox that are “Meeting Requests” views.</span></span> <span data-ttu-id="01b00-114">O exemplo, em seguida, usa o método **Add** para adicionar campos "Start" e "End" ao objeto **ViewFields** que corresponde ao objeto **TableView**.</span><span class="sxs-lookup"><span data-stu-id="01b00-114">The example then uses the **Add** method to add the “Start” and “End” fields to the **ViewFields** object that corresponds to the **TableView** object.</span></span> <span data-ttu-id="01b00-115">Ele também altera o rótulo do campo "From" para "Organized By".</span><span class="sxs-lookup"><span data-stu-id="01b00-115">It also changes the label for the “From” field to “Organized By”.</span></span> <span data-ttu-id="01b00-116">ModifyMeetingRequestsView salva o objeto **TableView** modificado.</span><span class="sxs-lookup"><span data-stu-id="01b00-116">ModifyMeetingRequestsView then saves the modified **TableView** object.</span></span>

<span data-ttu-id="01b00-117">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="01b00-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="01b00-118">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="01b00-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="01b00-119">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="01b00-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="01b00-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="01b00-120">See also</span></span>

- [<span data-ttu-id="01b00-121">Modos de exibição</span><span class="sxs-lookup"><span data-stu-id="01b00-121">Views</span></span>](views.md)

