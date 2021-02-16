---
title: Trabalhar com exibições
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- classe view [infopath 2007],InfoPath 2007, trabalhando com exibições,exibições [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain. O modelo de objeto do InfoPath fornecido pelo namespace Microsoft.Office.InfoPath dá suporte ao acesso a exibições de um formulário por meio do uso dos membros da classe View.
ms.openlocfilehash: 829375a87513634ef0b38b6d92de9f33a605e89f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406294"
---
# <a name="work-with-views"></a>Trabalhar com exibições

When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain. O modelo de objeto do InfoPath fornecido pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) dá suporte ao acesso a exibições de um formulário por meio do uso dos membros da classe [View.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) 
  
## <a name="overview-of-the-view-class"></a>Visão geral da classe View

A [classe View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir com um modo de exibição do InfoPath. 
  
> [!NOTE]
> Os métodos e propriedades da classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) não estão disponíveis durante o [evento Loading.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[Método DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)  <br/> |Desabilita a sincronização automática entre o documento XML subjacente de um formulário e o modo de exibição associado.  <br/> |
|[Método EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)  <br/> |Habilita a sincronização automática entre o documento XML subjacente de um formulário e o modo de exibição associado.  <br/> |
|[Método ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Executa um comando de edição no documento XML subjacente de um formulário, com base nos dados selecionados no modo de exibição.  <br/> |
|[Método ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Executa um comando de edição no documento XML subjacente de um formulário, com base no campo ou grupo especificado.  <br/> |
|[Método Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)  <br/> |Exporta o exibição para um arquivo do formato especificado.  <br/> |
|[Método ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)  <br/> |Força a sincronização entre o documento XML subjacente de um formulário e a exibição associada.  <br/> |
|[Método GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Obtém uma referência a um objeto **XPathNodeIterator** para iterar sobre os nós XML retornados a partir do nó especificado.  <br/> |
|[Método GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Obtém uma referência a um objeto **XPathNodeIterator** para iterar sobre os nós XML retornados na seleção atual dentro do controle vinculado ao campo ou grupo especificado.  <br/> |
|Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |Obtém uma referência a um objeto **XPathNodeIterator** para iterar em todos os nós XML na seleção atual de itens em um exibição.  <br/> |
|[Método SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Seleciona um intervalo de nós em uma exibição com base no nó XML inicial especificado.  <br/> |
|[Método SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Seleciona um intervalo de nós em uma exibição com base no nó XML inicial especificado e no nó XML final.  <br/> |
|[Método SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Seleciona um intervalo de nós em uma exibição com base no nó XML inicial especificado, no nó XML final e no controle especificado.  <br/> |
|[Método SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Seleciona o texto contido em um controle editável vinculado ao nó especificado pelo objeto **XPathNavigator** passado para esse método.  <br/> |
|[Método SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Seleciona o texto contido em um controle editável vinculado ao nó especificado pelo objeto **XPathNavigator** passado para esse método e o controle especificado.  <br/> |
|[Método ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)  <br/> |Cria uma mensagem de email que contém a exibição atual.  <br/> |
|[Propriedade ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)  <br/> |Obtém uma referência a [um objeto ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associado ao visualização.  <br/> |
|[Propriedade Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)  <br/> |Obtém uma referência a [um objeto Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) associado ao visualização.  <br/> |
   
> [!NOTE]
> O modelo de objeto do InfoPath também fornece as classes [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) e [ViewInfo,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) que podem ser usadas para obter informações sobre todas as exibições implementadas em um formulário. 
  
## <a name="using-the-view-class"></a>Usando a classe View

A [classe View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) é acessada por meio da propriedade [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) da classe [XmlForm,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) que é acessada usando esta palavra-chave (C#) ou **Me** (Visual Basic).  Para acessar o nome do exibição, você precisa acessar o [objeto ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associado ao ponto de exibição. O exemplo a seguir demonstra como exibir uma caixa de mensagem com o nome da exibição que está ativa no momento. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Todos os modelos de formulário do InfoPath contêm pelo menos um modo de exibição padrão; No entanto, o InfoPath também oferece suporte à criação de várias exibições do documento XML subjacente de um formulário. Quando você tiver vários exibições, [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) poderá ser usado para trabalhar com todos os exibições implementados no modelo de formulário. Para acessar [ViewInfoCollection de](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) um modelo de formulário, use a [propriedade ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) da [classe XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Você pode alterar programaticamente o modo de exibição que está ativo no momento usando o método [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) do [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , como demonstra o exemplo de código a seguir. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

O exemplo anterior para alternar um ponto de vista funcionará somente depois que o formulário for aberto. Para definir um modo de exibição padrão durante o evento [Loading,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) use a propriedade [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) da classe [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) conforme mostrado no exemplo a seguir. Observe, no entanto, que esse valor só terá efeito depois que o formulário for salvo e reaberto. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Selecionando controles em um ponto de exibição

O InfoPath fornece dois métodos da classe [View,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) ambos sobrecarregados, para selecionar programaticamente um controle no modo de exibição atual: os métodos [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) e [SelectNodes().](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) O método [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) é usado para controles de entrada de dados, como uma caixa de **texto,** enquanto o **método SelectNodes** é usado para controles estruturais, como uma **seção opcional**. Para selecionar um determinado controle na exibição, você precisa fornecer o nó e, opcionalmente, a ID viewContext do controle. A ID de ViewContext é necessária quando você tem vários controles vinculados ao mesmo nó na fonte de dados. O InfoPath fornece as informações de ID de ViewContext quando você projeta o formulário.
  
A ID viewContext de um controle  é exibida na guia Avançado da caixa de diálogo propriedades do controle, que é acessada  clicando com o botão direito do mouse no controle, clicando em _Propriedades de ControlName_ e clicando na guia Avançado. A ID viewContext do controle está listada na seção **Código** da **guia** Avançado. 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Quando usar SelectText e SelectNodes

Você pode selecionar programaticamente os seguintes controles de entrada de dados usando o [método SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) : 
  
- Caixa de Texto
    
- Caixa Rich Text
    
- Se picker de data
    
Você pode selecionar programaticamente os seguintes controles estruturais usando o [método SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) : 
  
- Seção Opcional
    
- Seção Choice
    
- Seção Repeating (items)
    
- Tabela de Repetição (linhas)
    
- Seção Recursiva de Repetição (itens)
    
- Lista com marcador, numerada e simples
    
- Tabela de Repetição Horizontal
    
Você não pode selecionar ou definir o foco de forma programática para os seguintes controles:
  
- Drop-Down listagem
    
- Caixa de listagem
    
- Caixa de Verificação
    
- Botão De opção
    
- Botão
    
- Imagem (vinculada ou incluída)
    
- Imagem à tinta
    
- Hiperlink
    
- Caixa de expressão
    
- Rótulo Vertical
    
- Seção ActiveX
    
- Região Horizontal
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a>Usando os métodos SelectText e SelectNodes

No exemplo **a** seguir, a sobrecarga [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) do método **SelectText,** que fornece um _parâmetro xmlNode,_ é usada para selecionar uma caixa de texto que está vinculada a "my:field1". 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

Se você tiver vários controles vinculados a "my:field1", deverá usar a sobrecarga [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) do método **SelectText,** que fornece um parâmetro  _viewContext_ adicional para selecionar um controle específico. O exemplo a seguir assume que há dois controles **Text Box** ligados a "my:field1", com o primeiro controle tendo uma ID viewContext de "CTRL1" e o segundo controle com uma ID viewContext de "CTRL8". O segundo controle é selecionado. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

No exemplo a seguir, a sobrecarga [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) do método **SelectNodes,** que fornece apenas um parâmetro  _startNode,_ é usada para selecionar a primeira linha em uma tabela de repetição vinculada ao grupo repetido "my:employee". 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

Você também pode selecionar várias linhas em uma tabela de repetição. No exemplo a seguir, as três primeiras linhas de uma tabela de repetição vinculada ao grupo de repetição "my:employee" são selecionadas usando a sobrecarga [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) do método **SelectNodes,** que fornece parâmetros _startNode_ e _endNode:_ 
  
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


