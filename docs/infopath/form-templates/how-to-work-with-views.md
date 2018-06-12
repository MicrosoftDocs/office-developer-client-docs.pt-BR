---
title: Trabalhar com modos de exibição
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Exibir classe [infopath 2007], InfoPath 2007, trabalhando com modos de exibição, exibições [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar os modos de exibição do formulário e, em seguida, executar uma variedade de ações nos dados que contêm os modos de exibição. Modelo de objeto do InfoPath fornecida pelo Microsoft.Office.InfoPath namespace suporta acesso aos modos de exibição de um formulário utilizando os membros da classe modo de exibição.
ms.openlocfilehash: 84c32244454e388e50433922c007d556fbef806a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765637"
---
# <a name="work-with-views"></a><span data-ttu-id="5e118-105">Trabalhar com modos de exibição</span><span class="sxs-lookup"><span data-stu-id="5e118-105">Work with Views</span></span>

<span data-ttu-id="5e118-106">Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar os modos de exibição do formulário e, em seguida, executar uma variedade de ações nos dados que contêm os modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="5e118-106">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain.</span></span> <span data-ttu-id="5e118-107">O modelo de objeto do InfoPath fornecido pelo access [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace oferece suporte aos modos de exibição de um formulário utilizando os membros da classe [modo de exibição](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e118-107">The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports access to a form's views through the use of the members of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class.</span></span> 
  
## <a name="overview-of-the-view-class"></a><span data-ttu-id="5e118-108">Visão geral da classe View</span><span class="sxs-lookup"><span data-stu-id="5e118-108">Overview of the View Class</span></span>

<span data-ttu-id="5e118-109">A classe de [modo de exibição](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir com um modo de exibição do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5e118-109">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5e118-110">Os métodos e propriedades da classe [Exibir](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) não estão disponíveis durante o evento de [carregamento](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e118-110">The methods and properties of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class are not available during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
|<span data-ttu-id="5e118-111">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5e118-111">**Name**</span></span>|<span data-ttu-id="5e118-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5e118-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e118-113">Método [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-114">Desabilita a sincronização automática entre o documento XML subjacente de um formulário e o modo de exibição associado.</span><span class="sxs-lookup"><span data-stu-id="5e118-114">Disables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="5e118-115">Método [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-116">Habilita a sincronização automática entre o documento XML subjacente de um formulário e o modo de exibição associado.</span><span class="sxs-lookup"><span data-stu-id="5e118-116">Enables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="5e118-117">Método [ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-118">Executa um comando de edição contra documento XML subjacente de um formulário, com base nos dados selecionados atualmente no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5e118-118">Executes an editing command against a form's underlying XML document, based on the data currently selected in the view.</span></span>  <br/> |
|<span data-ttu-id="5e118-119">Método [ExecuteAction (ActionType, cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-120">Executa um comando de edição contra documento XML subjacente de um formulário, com base no campo especificado ou grupo.</span><span class="sxs-lookup"><span data-stu-id="5e118-120">Executes an editing command against a form's underlying XML document, based on the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="5e118-121">Método [Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-122">Exporta o modo de exibição para um arquivo do formato especificado.</span><span class="sxs-lookup"><span data-stu-id="5e118-122">Exports the view to a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="5e118-123">Método [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-124">Sincronização de força entre o documento XML subjacente de um formulário e o modo de exibição associado.</span><span class="sxs-lookup"><span data-stu-id="5e118-124">Forces synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="5e118-125">Método [GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-126">Obtém uma referência a um objeto **XPathNodeIterator** para iterar nos nós XML retornados começando a partir do nó especificado.</span><span class="sxs-lookup"><span data-stu-id="5e118-126">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes starting from the specified node.</span></span>  <br/> |
|<span data-ttu-id="5e118-127">Método [GetContextNodes (XPathNavigator, cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-128">Obtém uma referência a um objeto **XPathNodeIterator** para iterar nos nós XML retornados na seleção atual dentro do controle vinculado ao campo especificado ou ao grupo.</span><span class="sxs-lookup"><span data-stu-id="5e118-128">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes in the current selection within the control bound to the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="5e118-129">Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-130">Obtém uma referência a um objeto **XPathNodeIterator** para iterar em todos os nós XML na seleção atual dos itens em um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5e118-130">Gets a reference to an **XPathNodeIterator** object for iterating over all XML nodes in the current selection of items in a view.</span></span>  <br/> |
|<span data-ttu-id="5e118-131">Método [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-132">Seleciona um intervalo de nós em um modo de exibição com base no nó XML inicial especificado.</span><span class="sxs-lookup"><span data-stu-id="5e118-132">Selects a range of nodes in a view based on the specified starting XML node.</span></span>  <br/> |
|<span data-ttu-id="5e118-133">Método [SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-134">Seleciona um intervalo de nós em um modo de exibição com base em especificado inicial nó XML e final nó XML.</span><span class="sxs-lookup"><span data-stu-id="5e118-134">Selects a range of nodes in a view based on the specified starting XML node and ending XML node.</span></span>  <br/> |
|<span data-ttu-id="5e118-135">Método [SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-136">Seleciona um intervalo de nós em um modo de exibição com base no controle especificado, o nó XML final e o nó XML inicial especificado.</span><span class="sxs-lookup"><span data-stu-id="5e118-136">Selects a range of nodes in a view based on the specified starting XML node, the ending XML node, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="5e118-137">Método [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-138">Seleciona o texto contido em um controle editável que esteja vinculado ao nó especificado pelo objeto **XPathNavigator** passado para este método.</span><span class="sxs-lookup"><span data-stu-id="5e118-138">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method.</span></span>  <br/> |
|<span data-ttu-id="5e118-139">Método [SelectText (XPathNavigator, cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-140">Seleciona o texto contido em um controle editável que esteja vinculado ao nó especificado pelo objeto **XPathNavigator** passado para este método e o controle especificado.</span><span class="sxs-lookup"><span data-stu-id="5e118-140">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="5e118-141">Método [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) method</span></span>  <br/> |<span data-ttu-id="5e118-142">Cria uma mensagem de email que contém o modo de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="5e118-142">Creates an email message containing the current view.</span></span>  <br/> |
|<span data-ttu-id="5e118-143">Propriedade [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) property</span></span>  <br/> |<span data-ttu-id="5e118-144">Obtém uma referência a um objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associado com o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5e118-144">Gets a reference to a [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span>  <br/> |
|<span data-ttu-id="5e118-145">Propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e118-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="5e118-146">Obtém uma referência a um objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) associado com o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5e118-146">Gets a reference to a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) object associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="5e118-147">O modelo de objeto do InfoPath também fornece as classes [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) e [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , que podem ser usadas para obter informações sobre todas as exibições implementadas em um formulário.</span><span class="sxs-lookup"><span data-stu-id="5e118-147">The InfoPath object model also provides the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) and [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) classes, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-view-class"></a><span data-ttu-id="5e118-148">Usando a classe de modo de exibição</span><span class="sxs-lookup"><span data-stu-id="5e118-148">Using the View Class</span></span>

<span data-ttu-id="5e118-149">A classe de [modo de exibição](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) é acessada por meio da propriedade [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , que é acessada usando a **Este** (c#) ou a palavra-chave **Me** (Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="5e118-149">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class is accessed through the [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class, which is accessed using the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="5e118-150">Para acessar o nome do modo de exibição, você precisa acessar o objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associado com o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5e118-150">To access the name of the view, you need to access the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span> <span data-ttu-id="5e118-151">O exemplo a seguir demonstra como exibir uma caixa de mensagem com o nome do modo de exibição ativo no momento.</span><span class="sxs-lookup"><span data-stu-id="5e118-151">The following example demonstrates how to display a message box with the name of the view that is currently active.</span></span> 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

<span data-ttu-id="5e118-152">Todos os modelos de formulário do InfoPath conter pelo menos um modo de exibição padrão; No entanto, o InfoPath também suporta a criação de vários modos de exibição do documento XML subjacente de um formulário.</span><span class="sxs-lookup"><span data-stu-id="5e118-152">All InfoPath form templates contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document.</span></span> <span data-ttu-id="5e118-153">Quando você tiver vários modos de exibição, o [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) pode ser usado para trabalhar com todas as exibições implementadas no modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="5e118-153">When you have multiple views, the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) can be used to work with all of the views implemented in the form template.</span></span> <span data-ttu-id="5e118-154">Para acessar o [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) de um modelo de formulário, use a propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e118-154">To access the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) of a form template, use the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="5e118-155">Programaticamente, você pode alterar o modo de exibição que está ativo no momento usando o método [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) do [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , conforme o exemplo de código a seguir demonstra.</span><span class="sxs-lookup"><span data-stu-id="5e118-155">You can programmatically change the view that is currently active by using the [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) method of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , as the following code sample demonstrates.</span></span> 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

<span data-ttu-id="5e118-156">O exemplo anterior para alternar entre um modo de exibição funcionará somente depois que o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="5e118-156">The previous example for switching a view will work only after the form is opened.</span></span> <span data-ttu-id="5e118-157">Para definir um modo de exibição padrão durante o evento de [carregamento](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , use a propriedade [inicial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) da classe [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e118-157">To set a default view during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, use the [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) property of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) class as shown in the following example.</span></span> <span data-ttu-id="5e118-158">No entanto, observe que esse valor só terão efeito depois que o formulário está salvo e aberto novamente.</span><span class="sxs-lookup"><span data-stu-id="5e118-158">Note, however, that this value will only take effect after the form is saved and re-opened.</span></span> 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a><span data-ttu-id="5e118-159">Selecionando os controles em um modo de exibição</span><span class="sxs-lookup"><span data-stu-id="5e118-159">Selecting Controls in a View</span></span>

<span data-ttu-id="5e118-160">O InfoPath fornece dois métodos da classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , ambos os quais estão sobrecarregados, para selecionar programaticamente de um controle no modo de exibição atual: os métodos [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) e [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e118-160">InfoPath provides two methods of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class, both of which are overloaded, to programmatically select a control in the current view: the [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) and [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods.</span></span> <span data-ttu-id="5e118-161">O método [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) é usado para controles de entrada de dados, como uma **Caixa de texto**, enquanto o método **SelectNodes** é usado para controles estruturais, como uma **Seção opcional**.</span><span class="sxs-lookup"><span data-stu-id="5e118-161">The [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method is used for data entry controls, such as a **Text Box**, while the **SelectNodes** method is used for structural controls, such as an **Optional Section**.</span></span> <span data-ttu-id="5e118-162">Para selecionar um determinado controle no modo de exibição, você precisa fornecer o nó e, opcionalmente, ID de ViewContext. do controle</span><span class="sxs-lookup"><span data-stu-id="5e118-162">To select a particular control in the view, you need to provide the node and, optionally, the control's ViewContext ID.</span></span> <span data-ttu-id="5e118-163">A ID de ViewContext é necessária quando você tiver vários controles vinculado ao mesmo nó na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="5e118-163">The ViewContext ID is needed when you have multiple controls bound to the same node in the data source.</span></span> <span data-ttu-id="5e118-164">InfoPath fornece as informações de identificação ViewContext quando você cria o formulário.</span><span class="sxs-lookup"><span data-stu-id="5e118-164">InfoPath provides the ViewContext ID information when you design the form.</span></span>
  
<span data-ttu-id="5e118-165">Uma identificação do controle ViewContext é exibida na guia **Avançado** da caixa de diálogo de propriedades do controle, que é acessada pelo botão direito do mouse no controle, clicando em _ControlName_ **Propriedades**e, em seguida, clicando na guia **Avançado** . A ID de ViewContext do controle está listada na seção de **código** , da guia **Avançado** .</span><span class="sxs-lookup"><span data-stu-id="5e118-165">A control's ViewContext ID is displayed on the **Advanced** tab of the control's properties dialog box, which is accessed by right-clicking the control, clicking  _ControlName_ **Properties**, and then clicking the **Advanced** tab. The ViewContext ID of the control is listed in the **Code** section of the **Advanced** tab.</span></span> 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a><span data-ttu-id="5e118-166">Quando usar SelectText e SelectNodes</span><span class="sxs-lookup"><span data-stu-id="5e118-166">When to use SelectText and SelectNodes</span></span>

<span data-ttu-id="5e118-167">Programaticamente, você pode selecionar os seguintes controles de entrada de dados usando o método [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) :</span><span class="sxs-lookup"><span data-stu-id="5e118-167">You can programmatically select the following data entry controls by using the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method:</span></span> 
  
- <span data-ttu-id="5e118-168">Caixa de Texto</span><span class="sxs-lookup"><span data-stu-id="5e118-168">Text Box</span></span>
    
- <span data-ttu-id="5e118-169">Caixa de Rich Text</span><span class="sxs-lookup"><span data-stu-id="5e118-169">Rich Text Box</span></span>
    
- <span data-ttu-id="5e118-170">Selecionador de data</span><span class="sxs-lookup"><span data-stu-id="5e118-170">Date Picker</span></span>
    
<span data-ttu-id="5e118-171">Programaticamente, você pode selecionar os seguintes controles estruturais usando o método [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) :</span><span class="sxs-lookup"><span data-stu-id="5e118-171">You can programmatically select the following structural controls by using the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method:</span></span> 
  
- <span data-ttu-id="5e118-172">Seção opcional</span><span class="sxs-lookup"><span data-stu-id="5e118-172">Optional Section</span></span>
    
- <span data-ttu-id="5e118-173">Seção de escolha</span><span class="sxs-lookup"><span data-stu-id="5e118-173">Choice Section</span></span>
    
- <span data-ttu-id="5e118-174">(Itens) da seção de repetição</span><span class="sxs-lookup"><span data-stu-id="5e118-174">Repeating Section (items)</span></span>
    
- <span data-ttu-id="5e118-175">(Linhas) da tabela de repetição</span><span class="sxs-lookup"><span data-stu-id="5e118-175">Repeating Table (rows)</span></span>
    
- <span data-ttu-id="5e118-176">Seção recursiva de repetição (itens)</span><span class="sxs-lookup"><span data-stu-id="5e118-176">Repeating Recursive Section (items)</span></span>
    
- <span data-ttu-id="5e118-177">Lista com marcadores, numerada e sem formatação</span><span class="sxs-lookup"><span data-stu-id="5e118-177">Bulleted, Numbered, and Plain List</span></span>
    
- <span data-ttu-id="5e118-178">Tabela de repetição horizontal</span><span class="sxs-lookup"><span data-stu-id="5e118-178">Horizontal Repeating Table</span></span>
    
<span data-ttu-id="5e118-179">Não é possível programaticamente select ou definido o foco para, os seguintes controles:</span><span class="sxs-lookup"><span data-stu-id="5e118-179">You cannot programmatically select, or set focus to, the following controls:</span></span>
  
- <span data-ttu-id="5e118-180">Caixa de listagem suspensa</span><span class="sxs-lookup"><span data-stu-id="5e118-180">Drop-Down List Box</span></span>
    
- <span data-ttu-id="5e118-181">Caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="5e118-181">List Box</span></span>
    
- <span data-ttu-id="5e118-182">Caixa de Verificação</span><span class="sxs-lookup"><span data-stu-id="5e118-182">Check Box</span></span>
    
- <span data-ttu-id="5e118-183">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="5e118-183">Option Button</span></span>
    
- <span data-ttu-id="5e118-184">Botão</span><span class="sxs-lookup"><span data-stu-id="5e118-184">Button</span></span>
    
- <span data-ttu-id="5e118-185">Imagem (vinculado ou incluídos)</span><span class="sxs-lookup"><span data-stu-id="5e118-185">Picture (linked or included)</span></span>
    
- <span data-ttu-id="5e118-186">Imagem de tinta</span><span class="sxs-lookup"><span data-stu-id="5e118-186">Ink Picture</span></span>
    
- <span data-ttu-id="5e118-187">Hiperlink</span><span class="sxs-lookup"><span data-stu-id="5e118-187">Hyperlink</span></span>
    
- <span data-ttu-id="5e118-188">Caixa expressão</span><span class="sxs-lookup"><span data-stu-id="5e118-188">Expression Box</span></span>
    
- <span data-ttu-id="5e118-189">Rótulo vertical</span><span class="sxs-lookup"><span data-stu-id="5e118-189">Vertical Label</span></span>
    
- <span data-ttu-id="5e118-190">Seção do ActiveX</span><span class="sxs-lookup"><span data-stu-id="5e118-190">ActiveX Section</span></span>
    
- <span data-ttu-id="5e118-191">Região horizontal</span><span class="sxs-lookup"><span data-stu-id="5e118-191">Horizontal Region</span></span>
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a><span data-ttu-id="5e118-192">Usando o SelectText e métodos SelectNodes</span><span class="sxs-lookup"><span data-stu-id="5e118-192">Using the SelectText and SelectNodes Methods</span></span>

<span data-ttu-id="5e118-193">No exemplo a seguir, a sobrecarga de [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) do método **SelectText** , que fornece um parâmetro _xmlNode_ , é usada para selecionar uma **Caixa de texto** que é vinculado ao "my: field1".</span><span class="sxs-lookup"><span data-stu-id="5e118-193">In the following example, the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides one  _xmlNode_ parameter, is used to select a **Text Box** that is bound to "my:field1".</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

<span data-ttu-id="5e118-194">Se você tiver vários controles ligados aos "my: field1", você deve usar a sobrecarga de [SelectText (XPathNavigator, cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) do método **SelectText** , que fornece um parâmetro adicional _viewContext_ para selecionar um controle específico.</span><span class="sxs-lookup"><span data-stu-id="5e118-194">If you have multiple controls bound to "my:field1", you must use the [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides an additional  _viewContext_ parameter to select a specific control.</span></span> <span data-ttu-id="5e118-195">O exemplo a seguir supõe que existem dois controles de **Caixa de texto** vinculados ao "my: field1", onde o primeiro controle ter uma identificação de ViewContext de "CTRL1" e o segundo controle ter uma identificação de ViewContext de "CTRL8".</span><span class="sxs-lookup"><span data-stu-id="5e118-195">The following example assumes that there are two **Text Box** controls bound to "my:field1", with the first control having a ViewContext ID of "CTRL1" and the second control having a ViewContext ID of "CTRL8".</span></span> <span data-ttu-id="5e118-196">O segundo controle está selecionado.</span><span class="sxs-lookup"><span data-stu-id="5e118-196">The second control is selected.</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

<span data-ttu-id="5e118-197">No exemplo a seguir, a sobrecarga de [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) do método **SelectNodes** , que fornece apenas um parâmetro _startNode_ , é usada para selecionar a primeira linha em uma tabela de repetição vinculada ao grupo de repetição "Meu: funcionário".</span><span class="sxs-lookup"><span data-stu-id="5e118-197">In the following example, the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides only one  _startNode_ parameter, is used to select the first row in a repeating table bound to the repeating group "my:employee".</span></span> 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

<span data-ttu-id="5e118-198">Você também pode selecionar várias linhas em uma tabela de repetição.</span><span class="sxs-lookup"><span data-stu-id="5e118-198">You can also select multiple rows in a repeating table.</span></span> <span data-ttu-id="5e118-199">No exemplo a seguir, as três primeiras linhas de uma tabela de repetição é vinculado ao grupo de repetição "Meu: funcionário" estão selecionadas usando a sobrecarga de [SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) do método **SelectNodes** , que fornece  parâmetros de _startNode_ e _endnodes_ :</span><span class="sxs-lookup"><span data-stu-id="5e118-199">In the following example, the first three rows of a repeating table bound to the repeating group "my:employee" are selected using the [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides  _startNode_ and  _endNode_ parameters:</span></span> 
  
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


