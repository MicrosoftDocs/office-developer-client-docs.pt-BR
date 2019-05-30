---
title: Criar um modo de exibição
TOCTitle: Create a view
ms:assetid: 2f8ad187-1030-420a-bc74-c327e3521550
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424468(v=office.15)
ms:contentKeyID: 55119902
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 75f414d95818b618cfcae236822bb2f5dacdf5f2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540802"
---
# <a name="create-a-view"></a><span data-ttu-id="dea00-102">Criar um modo de exibição</span><span class="sxs-lookup"><span data-stu-id="dea00-102">Create a view</span></span>

<span data-ttu-id="dea00-103">Este exemplo mostra como usar o método [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) da coleção [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) para criar um modo de exibição para o objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="dea00-103">This example shows how to use the [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) method of the [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) collection to create a view for a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="dea00-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dea00-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="dea00-105">O exemplo de código a seguir é um trecho da [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="dea00-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="dea00-106">Você pode criar modos de exibição personalizáveis que permitem que você classifique, agrupe e exiba dados de todos os tipo diferentes no Painel de Exibição da janela do explorador do Outlook.</span><span class="sxs-lookup"><span data-stu-id="dea00-106">You can create customizable views that allow you to sort, group, and view data of all different types within the View Pane of the Outlook explorer window.</span></span> <span data-ttu-id="dea00-107">Você também pode personalizar modos de exibição internos de modo programático.</span><span class="sxs-lookup"><span data-stu-id="dea00-107">You can also customize built-in views programmatically.</span></span> <span data-ttu-id="dea00-108">A tabela a seguir lista os objetos que representam os modos de exibição do Outlook.</span><span class="sxs-lookup"><span data-stu-id="dea00-108">The following table lists objects that represent Outlook views.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dea00-109">Nome do Objeto</span><span class="sxs-lookup"><span data-stu-id="dea00-109">Object Name</span></span></p></th>
<th><p><span data-ttu-id="dea00-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="dea00-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dea00-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></span><span class="sxs-lookup"><span data-stu-id="dea00-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></span></span></p></td>
<td><p><span data-ttu-id="dea00-112">Os dados são exibidos como uma série de imagens de cartões de visita eletrônicos.</span><span class="sxs-lookup"><span data-stu-id="dea00-112">Data is viewed as a series of electronic business card images.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dea00-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span><span class="sxs-lookup"><span data-stu-id="dea00-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span></span></p></td>
<td><p><span data-ttu-id="dea00-114">Os dados são exibidos no formato de calendário.</span><span class="sxs-lookup"><span data-stu-id="dea00-114">Data is viewed in a calendar format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dea00-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></span><span class="sxs-lookup"><span data-stu-id="dea00-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></span></span></p></td>
<td><p><span data-ttu-id="dea00-116">Os dados são exibidos em uma série de cartões.</span><span class="sxs-lookup"><span data-stu-id="dea00-116">Data is viewed in a series of cards.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dea00-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></span><span class="sxs-lookup"><span data-stu-id="dea00-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></span></span></p></td>
<td><p><span data-ttu-id="dea00-118">Os dados são exibidos como ícones da pasta Windows ou ícones do explorador.</span><span class="sxs-lookup"><span data-stu-id="dea00-118">Data is viewed as Windows folder icons or explorer icons.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dea00-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></span><span class="sxs-lookup"><span data-stu-id="dea00-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></span></span></p></td>
<td><p><span data-ttu-id="dea00-120">Os dados são exibidos como uma tabela simples baseada em um campo.</span><span class="sxs-lookup"><span data-stu-id="dea00-120">Data is viewed in a simple field-based table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dea00-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></span><span class="sxs-lookup"><span data-stu-id="dea00-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></span></span></p></td>
<td><p><span data-ttu-id="dea00-122">Os dados são exibidos em uma linha do tempo linear personalizável.</span><span class="sxs-lookup"><span data-stu-id="dea00-122">Data is viewed in a customizable linear time line.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dea00-123">Você pode acessar métodos e propriedades que são comuns para todos os modos de exibição usando o objeto[View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="dea00-123">You can access properties and methods that are common to all views by using the [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)) object.</span></span> <span data-ttu-id="dea00-124">Entretanto, para acessar certas propriedades que não são comuns para todos os modos de exibição, você deve converter o objeto **View** em um objeto **View** derivado ao qual pertence a propriedade que você quer acessar.</span><span class="sxs-lookup"><span data-stu-id="dea00-124">However, to access certain properties that are not common to all views, you must cast the **View** object to a derived **View** object that the property you want to access belongs to.</span></span> <span data-ttu-id="dea00-125">Por exemplo, para acessar a propriedade [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) do objeto **Cardview**, converta o objeto **View** no objeto **Cardview**.</span><span class="sxs-lookup"><span data-stu-id="dea00-125">For example, to access the [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) property of the **Cardview** object, cast the **View** object to the **Cardview** object.</span></span> <span data-ttu-id="dea00-126">Se você quiser determinar que tipo de modo de exibição é representado por um objeto **View** específico, use a propriedade [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="dea00-126">If you want to determine which type of view is represented by a particular **View** object, use the [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)) property.</span></span>

<span data-ttu-id="dea00-127">Para criar um novo modo de exibição, use o método **Add** da coleção **Views** para um objeto **Folder**.</span><span class="sxs-lookup"><span data-stu-id="dea00-127">To create a new view, use the **Add** method of the **Views** collection for a **Folder** object.</span></span> <span data-ttu-id="dea00-128">Em seguida, defina a visibilidade do modo de exibição no momento da criação ou a qualquer momento depois que o modo de exibição for criado.</span><span class="sxs-lookup"><span data-stu-id="dea00-128">Then set the visibility for the view either at the time of creation, or at any time after the view is created.</span></span> <span data-ttu-id="dea00-129">Para definir a visibilidade do modo de exibição no momento da criação, especifique uma constante [OIViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) no parâmetro *SaveOption* do método **Add**.</span><span class="sxs-lookup"><span data-stu-id="dea00-129">To set the visibility for the view at the time of creation, specify an [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) constant in the *SaveOption* parameter of the **Add** method.</span></span> <span data-ttu-id="dea00-130">Para definir a visibilidade a qualquer momento depois da criação do modo de exibição, especifique uma constante **OlViewSaveOption** para a propriedade [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) do objeto **View**.</span><span class="sxs-lookup"><span data-stu-id="dea00-130">To set the visibility at any time after the view is created, specify an **OlViewSaveOption** constant for the [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) property of the **View** object.</span></span> 

<span data-ttu-id="dea00-131">A adição de um novo modo de exibição gera o evento [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) evento da coleção **Views**.</span><span class="sxs-lookup"><span data-stu-id="dea00-131">Adding a new view raises the [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) event of the **Views** collection.</span></span> <span data-ttu-id="dea00-132">Após a criação do modo de exibição, personalize o modo de exibição programaticamente convertendo o objeto **View** em um dos objetos derivados e fazendo as alterações necessárias em seguida.</span><span class="sxs-lookup"><span data-stu-id="dea00-132">Once the view is created, customize the view programmatically by casting the **View** object to one of the derived objects and then making necessary changes.</span></span> <span data-ttu-id="dea00-133">Use o método **Save** do objeto derivado **View**, ou o objeto **View** para salvar quaisquer alterações no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="dea00-133">Use the **Save** method of the derived **View** object or the **View** object to save any changes to the view.</span></span> <span data-ttu-id="dea00-134">Finalmente, use o método **Apply** do objeto derivado **View** ou o objeto **View** para aplicar o modo de exibição ao objeto [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) atual.</span><span class="sxs-lookup"><span data-stu-id="dea00-134">Finally, use the **Apply** method of the derived **View** object or the **View** object to apply the view to the current [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object.</span></span> <span data-ttu-id="dea00-135">Isso gera o evento [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) do objeto **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="dea00-135">This raises the [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) event of the **Explorer** object.</span></span>

<span data-ttu-id="dea00-136">O exemplo de código a seguir, CreateMeetingRequestsView, adiciona um novo modo de exibição chamado “Meeting Requests” à Caixa de Entrada do usuário gerando um objeto **View** para um objeto **TableView**.</span><span class="sxs-lookup"><span data-stu-id="dea00-136">In the following code example, CreateMeetingRequestsView adds a new view named “Meeting Requests” to the user’s Inbox by casting the **View** object to a **TableView** object.</span></span> <span data-ttu-id="dea00-137">CreateMeetingRequestsView chama o método **Add** do objeto **Views** com o parâmetro *Name* definido para “Meeting Requests” e o parâmetro *ViewType* definido para **olTableView**.</span><span class="sxs-lookup"><span data-stu-id="dea00-137">CreateMeetingRequestsView then calls the **Add** method of the **Views** object with the *Name* parameter set to “Meeting Requests” and the *ViewType* parameter set to **olTableView**.</span></span> <span data-ttu-id="dea00-138">A propriedade [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) do objeto **TableView** é definida para uma cadeia de caracteres DAV Searching and Locating (DASL), que faz com que o modo de exibição exiba apenas quando houver itens que contêm “IPM.Schedule” na classe de mensagem do item.</span><span class="sxs-lookup"><span data-stu-id="dea00-138">The [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) property of the **TableView** object is set to a DAV Searching and Locating (DASL) string that causes the view to display only when there are items that contain “IPM.Schedule” in the message class for the item.</span></span> <span data-ttu-id="dea00-139">Então, o novo modo de exibição é salvo e aplicado.</span><span class="sxs-lookup"><span data-stu-id="dea00-139">The new view is then saved and applied.</span></span>

<span data-ttu-id="dea00-140">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="dea00-140">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="dea00-141">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="dea00-141">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="dea00-142">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="dea00-142">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateMeetingRequestsView()
{
    const string PR_MESSAGE_CLASS =
        "http://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.Views views =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Views;
    Outlook.TableView tableView = (Outlook.TableView)
        views.Add("Meeting Requests",
        Outlook.OlViewType.olTableView,
        Outlook.OlViewSaveOption.olViewSaveOptionThisFolderEveryone);
    tableView.Filter = "\"" + PR_MESSAGE_CLASS + "\"" +
        " like 'IPM.Schedule%'";
    tableView.Save();
    tableView.Apply();
}
```

## <a name="see-also"></a><span data-ttu-id="dea00-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="dea00-143">See also</span></span>

- [<span data-ttu-id="dea00-144">Modos de exibição</span><span class="sxs-lookup"><span data-stu-id="dea00-144">Views</span></span>](views.md)

