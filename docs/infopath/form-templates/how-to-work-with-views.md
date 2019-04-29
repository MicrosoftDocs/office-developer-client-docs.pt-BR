---
title: Trabalhar com modos de exibição
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- classe View [InfoPath 2007], InfoPath 2007, Working with views, views [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar os modos de exibição do formulário e, em seguida, executar uma variedade de ações nos dados que os modos de exibição contêm. O modelo de objeto do InfoPath fornecido pelo namespace Microsoft. Office. InfoPath oferece suporte ao acesso aos modos de exibição de um formulário por meio do uso dos membros da classe View.
ms.openlocfilehash: 829375a87513634ef0b38b6d92de9f33a605e89f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406294"
---
# <a name="work-with-views"></a><span data-ttu-id="46cd7-105">Trabalhar com modos de exibição</span><span class="sxs-lookup"><span data-stu-id="46cd7-105">Work with Views</span></span>

<span data-ttu-id="46cd7-106">Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar os modos de exibição do formulário e, em seguida, executar uma variedade de ações nos dados que os modos de exibição contêm.</span><span class="sxs-lookup"><span data-stu-id="46cd7-106">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain.</span></span> <span data-ttu-id="46cd7-107">O modelo de objeto do InfoPath fornecido pelo namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) oferece suporte ao acesso aos modos de exibição de um formulário por meio do uso dos membros da classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) .</span><span class="sxs-lookup"><span data-stu-id="46cd7-107">The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports access to a form's views through the use of the members of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class.</span></span> 
  
## <a name="overview-of-the-view-class"></a><span data-ttu-id="46cd7-108">Visão geral da classe View</span><span class="sxs-lookup"><span data-stu-id="46cd7-108">Overview of the View Class</span></span>

<span data-ttu-id="46cd7-109">A classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulários podem usar para interagir com um modo de exibição do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="46cd7-109">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="46cd7-110">Os métodos e as propriedades da classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) não estão disponíveis durante o evento [loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) .</span><span class="sxs-lookup"><span data-stu-id="46cd7-110">The methods and properties of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class are not available during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
|<span data-ttu-id="46cd7-111">**Nome**</span><span class="sxs-lookup"><span data-stu-id="46cd7-111">**Name**</span></span>|<span data-ttu-id="46cd7-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="46cd7-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="46cd7-113">Método [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-114">Desabilita a sincronização automática entre o documento XML subjacente de um formulário e o modo de exibição associado.</span><span class="sxs-lookup"><span data-stu-id="46cd7-114">Disables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="46cd7-115">Método [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-116">Permite a sincronização automática entre o documento XML subjacente de um formulário e o modo de exibição associado.</span><span class="sxs-lookup"><span data-stu-id="46cd7-116">Enables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="46cd7-117">Método [ExecuteAction (ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-118">Executa um comando de edição em relação ao documento XML subjacente de um formulário, com base nos dados atualmente selecionados no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="46cd7-118">Executes an editing command against a form's underlying XML document, based on the data currently selected in the view.</span></span>  <br/> |
|<span data-ttu-id="46cd7-119">Método [ExecuteAction (ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-120">Executa um comando de edição em relação ao documento XML subjacente de um formulário, com base no campo ou grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="46cd7-120">Executes an editing command against a form's underlying XML document, based on the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="46cd7-121">Método [Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-122">Exporta o modo de exibição para um arquivo do formato especificado.</span><span class="sxs-lookup"><span data-stu-id="46cd7-122">Exports the view to a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="46cd7-123">Método [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-124">Força a sincronização entre o documento XML subjacente de um formulário e o modo de exibição associado.</span><span class="sxs-lookup"><span data-stu-id="46cd7-124">Forces synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="46cd7-125">Método [GetContextNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-126">Obtém uma referência a um objeto **XPathNodeIterator** para iterar sobre os nós XML retornados a partir do nó especificado.</span><span class="sxs-lookup"><span data-stu-id="46cd7-126">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes starting from the specified node.</span></span>  <br/> |
|<span data-ttu-id="46cd7-127">Método [GetContextNodes (XPathNavigator, Cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-128">Obtém uma referência a um objeto **XPathNodeIterator** para iterar nos nós XML retornados na seleção atual dentro do controle acoplado ao campo ou grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="46cd7-128">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes in the current selection within the control bound to the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="46cd7-129">Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-130">Obtém uma referência a um objeto **XPathNodeIterator** para iterar em todos os nós XML na seleção atual de itens em um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="46cd7-130">Gets a reference to an **XPathNodeIterator** object for iterating over all XML nodes in the current selection of items in a view.</span></span>  <br/> |
|<span data-ttu-id="46cd7-131">Método [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-132">Seleciona um intervalo de nós em um modo de exibição com base no nó XML inicial especificado.</span><span class="sxs-lookup"><span data-stu-id="46cd7-132">Selects a range of nodes in a view based on the specified starting XML node.</span></span>  <br/> |
|<span data-ttu-id="46cd7-133">Método [SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-134">Seleciona um intervalo de nós em um modo de exibição com base no nó XML inicial especificado e no nó XML final.</span><span class="sxs-lookup"><span data-stu-id="46cd7-134">Selects a range of nodes in a view based on the specified starting XML node and ending XML node.</span></span>  <br/> |
|<span data-ttu-id="46cd7-135">Método [SelectNodes (XPathNavigator, XPathNavigator, Cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-136">Seleciona um intervalo de nós em um modo de exibição com base no nó XML inicial especificado, o nó XML final e o controle especificado.</span><span class="sxs-lookup"><span data-stu-id="46cd7-136">Selects a range of nodes in a view based on the specified starting XML node, the ending XML node, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="46cd7-137">Método [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-138">Seleciona o texto contido em um controle editável que está vinculado ao nó especificado pelo objeto **XPathNavigator** passado para este método.</span><span class="sxs-lookup"><span data-stu-id="46cd7-138">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method.</span></span>  <br/> |
|<span data-ttu-id="46cd7-139">Método [SelectText (XPathNavigator, Cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-140">Seleciona o texto contido em um controle editável que está vinculado ao nó especificado pelo objeto **XPathNavigator** passado para este método e o controle especificado.</span><span class="sxs-lookup"><span data-stu-id="46cd7-140">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="46cd7-141">Método [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) method</span></span>  <br/> |<span data-ttu-id="46cd7-142">Cria uma mensagem de email contendo o modo de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="46cd7-142">Creates an email message containing the current view.</span></span>  <br/> |
|<span data-ttu-id="46cd7-143">Propriedade [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) property</span></span>  <br/> |<span data-ttu-id="46cd7-144">Obtém uma referência a um objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associado ao modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="46cd7-144">Gets a reference to a [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span>  <br/> |
|<span data-ttu-id="46cd7-145">Propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="46cd7-146">Obtém uma referência a um objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) associado ao modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="46cd7-146">Gets a reference to a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) object associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="46cd7-147">O modelo de objeto do InfoPath também fornece as classes [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) e [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , que podem ser usadas para obter informações sobre todos os modos de exibição implementados em um formulário.</span><span class="sxs-lookup"><span data-stu-id="46cd7-147">The InfoPath object model also provides the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) and [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) classes, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-view-class"></a><span data-ttu-id="46cd7-148">Usando a classe View</span><span class="sxs-lookup"><span data-stu-id="46cd7-148">Using the View Class</span></span>

<span data-ttu-id="46cd7-149">A classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) é acessada através da propriedade [modoatual](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) da classe XmlForm, que é acessada usando a palavra-chave **this** (C#) ou **me** (Visual Basic). [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)</span><span class="sxs-lookup"><span data-stu-id="46cd7-149">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class is accessed through the [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class, which is accessed using the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="46cd7-150">Para acessar o nome do modo de exibição, você precisa acessar o objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associado ao modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="46cd7-150">To access the name of the view, you need to access the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span> <span data-ttu-id="46cd7-151">O exemplo a seguir demonstra como exibir uma caixa de mensagem com o nome do modo de exibição atualmente ativo.</span><span class="sxs-lookup"><span data-stu-id="46cd7-151">The following example demonstrates how to display a message box with the name of the view that is currently active.</span></span> 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

<span data-ttu-id="46cd7-152">Todos os modelos de formulário do InfoPath contêm pelo menos um modo de exibição padrão; no entanto, o InfoPath também dá suporte à criação de vários modos de exibição do documento XML subjacente de um formulário.</span><span class="sxs-lookup"><span data-stu-id="46cd7-152">All InfoPath form templates contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document.</span></span> <span data-ttu-id="46cd7-153">Quando você tem vários modos de exibição, o [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) pode ser usado para trabalhar com todos os modos de exibição implementados no modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="46cd7-153">When you have multiple views, the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) can be used to work with all of the views implemented in the form template.</span></span> <span data-ttu-id="46cd7-154">Para acessar o [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) de um modelo de formulário, use a propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) da [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) classe XmlForm.</span><span class="sxs-lookup"><span data-stu-id="46cd7-154">To access the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) of a form template, use the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="46cd7-155">Você pode alterar programaticamente o modo de exibição que está ativo no momento usando o método [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) do [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , como mostra o exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="46cd7-155">You can programmatically change the view that is currently active by using the [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) method of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , as the following code sample demonstrates.</span></span> 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

<span data-ttu-id="46cd7-156">O exemplo anterior para mudar de um modo de exibição funcionará somente depois que o formulário for aberto.</span><span class="sxs-lookup"><span data-stu-id="46cd7-156">The previous example for switching a view will work only after the form is opened.</span></span> <span data-ttu-id="46cd7-157">Para definir um modo de exibição padrão durante o evento [loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , use a propriedade [inicial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) da classe [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="46cd7-157">To set a default view during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, use the [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) property of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) class as shown in the following example.</span></span> <span data-ttu-id="46cd7-158">Observe, no entanto, que esse valor só entrará em vigor depois que o formulário for salvo e reaberto.</span><span class="sxs-lookup"><span data-stu-id="46cd7-158">Note, however, that this value will only take effect after the form is saved and re-opened.</span></span> 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a><span data-ttu-id="46cd7-159">Selecionar controles em um modo de exibição</span><span class="sxs-lookup"><span data-stu-id="46cd7-159">Selecting Controls in a View</span></span>

<span data-ttu-id="46cd7-160">O InfoPath fornece dois métodos da classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , que são sobrecarregados, para selecionar programaticamente um controle no modo de exibição atual: os métodos [SelectText ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) e [SelectNodes ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) .</span><span class="sxs-lookup"><span data-stu-id="46cd7-160">InfoPath provides two methods of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class, both of which are overloaded, to programmatically select a control in the current view: the [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) and [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods.</span></span> <span data-ttu-id="46cd7-161">O método [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) é usado para controles de entrada de dados, como uma **caixa de texto**, enquanto o método **SelectNodes** é usado para controles estruturais, como uma **seção opcional**.</span><span class="sxs-lookup"><span data-stu-id="46cd7-161">The [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method is used for data entry controls, such as a **Text Box**, while the **SelectNodes** method is used for structural controls, such as an **Optional Section**.</span></span> <span data-ttu-id="46cd7-162">Para selecionar um determinado controle no modo de exibição, você precisa fornecer o nó e, opcionalmente, a ID ViewContext do controle.</span><span class="sxs-lookup"><span data-stu-id="46cd7-162">To select a particular control in the view, you need to provide the node and, optionally, the control's ViewContext ID.</span></span> <span data-ttu-id="46cd7-163">A ID ViewContext é necessária quando você tem vários controles associados ao mesmo nó na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="46cd7-163">The ViewContext ID is needed when you have multiple controls bound to the same node in the data source.</span></span> <span data-ttu-id="46cd7-164">O InfoPath fornece as informações de ID do ViewContext quando você cria o formulário.</span><span class="sxs-lookup"><span data-stu-id="46cd7-164">InfoPath provides the ViewContext ID information when you design the form.</span></span>
  
<span data-ttu-id="46cd7-165">A ID de ViewContext de um controle é exibida na guia **avançado** da caixa de diálogo Propriedades do controle, que é acessada clicando com o botão direito do mouse no controle, clicando em **Propriedades**de _controle_ e, em seguida, clicando na guia **avançado** . A ID ViewContext do controle é listada na seção **código** da guia **avançado** .</span><span class="sxs-lookup"><span data-stu-id="46cd7-165">A control's ViewContext ID is displayed on the **Advanced** tab of the control's properties dialog box, which is accessed by right-clicking the control, clicking  _ControlName_ **Properties**, and then clicking the **Advanced** tab. The ViewContext ID of the control is listed in the **Code** section of the **Advanced** tab.</span></span> 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a><span data-ttu-id="46cd7-166">Quando usar o SelectText e SelectNodes</span><span class="sxs-lookup"><span data-stu-id="46cd7-166">When to use SelectText and SelectNodes</span></span>

<span data-ttu-id="46cd7-167">Você pode selecionar programaticamente os seguintes controles de entrada de dados usando o método [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) :</span><span class="sxs-lookup"><span data-stu-id="46cd7-167">You can programmatically select the following data entry controls by using the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method:</span></span> 
  
- <span data-ttu-id="46cd7-168">Caixa de Texto</span><span class="sxs-lookup"><span data-stu-id="46cd7-168">Text Box</span></span>
    
- <span data-ttu-id="46cd7-169">Caixa de Rich Text</span><span class="sxs-lookup"><span data-stu-id="46cd7-169">Rich Text Box</span></span>
    
- <span data-ttu-id="46cd7-170">Seletor de data</span><span class="sxs-lookup"><span data-stu-id="46cd7-170">Date Picker</span></span>
    
<span data-ttu-id="46cd7-171">Você pode selecionar programaticamente os seguintes controles estruturais usando o método [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) :</span><span class="sxs-lookup"><span data-stu-id="46cd7-171">You can programmatically select the following structural controls by using the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method:</span></span> 
  
- <span data-ttu-id="46cd7-172">Seção opcional</span><span class="sxs-lookup"><span data-stu-id="46cd7-172">Optional Section</span></span>
    
- <span data-ttu-id="46cd7-173">Seção de escolha</span><span class="sxs-lookup"><span data-stu-id="46cd7-173">Choice Section</span></span>
    
- <span data-ttu-id="46cd7-174">Seção de repetição (itens)</span><span class="sxs-lookup"><span data-stu-id="46cd7-174">Repeating Section (items)</span></span>
    
- <span data-ttu-id="46cd7-175">Tabela de repetição (linhas)</span><span class="sxs-lookup"><span data-stu-id="46cd7-175">Repeating Table (rows)</span></span>
    
- <span data-ttu-id="46cd7-176">Seção recursiva de repetição (itens)</span><span class="sxs-lookup"><span data-stu-id="46cd7-176">Repeating Recursive Section (items)</span></span>
    
- <span data-ttu-id="46cd7-177">Lista com marcadores, numerada e sem formatação</span><span class="sxs-lookup"><span data-stu-id="46cd7-177">Bulleted, Numbered, and Plain List</span></span>
    
- <span data-ttu-id="46cd7-178">Tabela de Repetição Horizontal</span><span class="sxs-lookup"><span data-stu-id="46cd7-178">Horizontal Repeating Table</span></span>
    
<span data-ttu-id="46cd7-179">Você não pode selecionar, ou definir o foco, de forma programática, os seguintes controles:</span><span class="sxs-lookup"><span data-stu-id="46cd7-179">You cannot programmatically select, or set focus to, the following controls:</span></span>
  
- <span data-ttu-id="46cd7-180">Caixa de listagem suspensa</span><span class="sxs-lookup"><span data-stu-id="46cd7-180">Drop-Down List Box</span></span>
    
- <span data-ttu-id="46cd7-181">Caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="46cd7-181">List Box</span></span>
    
- <span data-ttu-id="46cd7-182">Caixa de Verificação</span><span class="sxs-lookup"><span data-stu-id="46cd7-182">Check Box</span></span>
    
- <span data-ttu-id="46cd7-183">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="46cd7-183">Option Button</span></span>
    
- <span data-ttu-id="46cd7-184">Botão</span><span class="sxs-lookup"><span data-stu-id="46cd7-184">Button</span></span>
    
- <span data-ttu-id="46cd7-185">Imagem (vinculada ou incluída)</span><span class="sxs-lookup"><span data-stu-id="46cd7-185">Picture (linked or included)</span></span>
    
- <span data-ttu-id="46cd7-186">Imagem à tinta</span><span class="sxs-lookup"><span data-stu-id="46cd7-186">Ink Picture</span></span>
    
- <span data-ttu-id="46cd7-187">Hiperlink</span><span class="sxs-lookup"><span data-stu-id="46cd7-187">Hyperlink</span></span>
    
- <span data-ttu-id="46cd7-188">Caixa de expressões</span><span class="sxs-lookup"><span data-stu-id="46cd7-188">Expression Box</span></span>
    
- <span data-ttu-id="46cd7-189">Rótulo vertical</span><span class="sxs-lookup"><span data-stu-id="46cd7-189">Vertical Label</span></span>
    
- <span data-ttu-id="46cd7-190">Seção ActiveX</span><span class="sxs-lookup"><span data-stu-id="46cd7-190">ActiveX Section</span></span>
    
- <span data-ttu-id="46cd7-191">Região horizontal</span><span class="sxs-lookup"><span data-stu-id="46cd7-191">Horizontal Region</span></span>
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a><span data-ttu-id="46cd7-192">Usando os métodos SelectText e SelectNodes</span><span class="sxs-lookup"><span data-stu-id="46cd7-192">Using the SelectText and SelectNodes Methods</span></span>

<span data-ttu-id="46cd7-193">No exemplo a seguir, a sobrecarga de [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) do método **SelectText** , que fornece um parâmetro _xmlNode_ , é usada para selecionar uma **caixa de texto** associada a "My: campo1".</span><span class="sxs-lookup"><span data-stu-id="46cd7-193">In the following example, the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides one  _xmlNode_ parameter, is used to select a **Text Box** that is bound to "my:field1".</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

<span data-ttu-id="46cd7-194">Se você tiver vários controles vinculados a "My: campo1", você deve usar a sobrecarga [SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) do método **SelectText** , que fornece um parâmetro _ViewContext_ adicional para selecionar um controle específico.</span><span class="sxs-lookup"><span data-stu-id="46cd7-194">If you have multiple controls bound to "my:field1", you must use the [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides an additional  _viewContext_ parameter to select a specific control.</span></span> <span data-ttu-id="46cd7-195">O exemplo a seguir pressupõe que há dois controles de **caixa de texto** acoplados a "My: campo1", com o primeiro controle com uma ID ViewContext de "CTRL1" e o segundo controle com uma ID de VIEWCONTEXT "CTRL8".</span><span class="sxs-lookup"><span data-stu-id="46cd7-195">The following example assumes that there are two **Text Box** controls bound to "my:field1", with the first control having a ViewContext ID of "CTRL1" and the second control having a ViewContext ID of "CTRL8".</span></span> <span data-ttu-id="46cd7-196">O segundo controle é selecionado.</span><span class="sxs-lookup"><span data-stu-id="46cd7-196">The second control is selected.</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

<span data-ttu-id="46cd7-197">No exemplo a seguir, a sobrecarga [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) do método **SelectNodes** , que fornece apenas um parâmetro _startNode_ , é usada para selecionar a primeira linha em uma tabela de repetição vinculada ao grupo de repetição "My: Employee ".</span><span class="sxs-lookup"><span data-stu-id="46cd7-197">In the following example, the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides only one  _startNode_ parameter, is used to select the first row in a repeating table bound to the repeating group "my:employee".</span></span> 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

<span data-ttu-id="46cd7-198">Você também pode selecionar várias linhas em uma tabela de repetição.</span><span class="sxs-lookup"><span data-stu-id="46cd7-198">You can also select multiple rows in a repeating table.</span></span> <span data-ttu-id="46cd7-199">No exemplo a seguir, as três primeiras linhas de uma tabela de repetição vinculadas ao grupo de repetição "My: Employee" são selecionadas usando a sobrecarga [SelectNodes (XPathNavigator, XPathNavigator, Cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) do método **SelectNodes** , que fornece  parâmetros de _startNode_ e endnode: __</span><span class="sxs-lookup"><span data-stu-id="46cd7-199">In the following example, the first three rows of a repeating table bound to the repeating group "my:employee" are selected using the [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides  _startNode_ and  _endNode_ parameters:</span></span> 
  
```cs
// Create XPathNavigators to specify range of nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
XPathNavigator repeatingTableRow3 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:myemployee[3]", NamespaceManager);
// Select range of nodes in specified XPathNavigators.
CurrentView.SelectNodes(repeatingTableRow1, repeatingTableRow3);
```


