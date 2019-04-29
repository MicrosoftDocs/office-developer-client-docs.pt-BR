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
# <a name="work-with-views"></a>Trabalhar com modos de exibição

Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar os modos de exibição do formulário e, em seguida, executar uma variedade de ações nos dados que os modos de exibição contêm. O modelo de objeto do InfoPath fornecido pelo namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) oferece suporte ao acesso aos modos de exibição de um formulário por meio do uso dos membros da classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) . 
  
## <a name="overview-of-the-view-class"></a>Visão geral da classe View

A classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulários podem usar para interagir com um modo de exibição do InfoPath. 
  
> [!NOTE]
> Os métodos e as propriedades da classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) não estão disponíveis durante o evento [loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) . 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)  <br/> |Desabilita a sincronização automática entre o documento XML subjacente de um formulário e o modo de exibição associado.  <br/> |
|Método [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)  <br/> |Permite a sincronização automática entre o documento XML subjacente de um formulário e o modo de exibição associado.  <br/> |
|Método [ExecuteAction (ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Executa um comando de edição em relação ao documento XML subjacente de um formulário, com base nos dados atualmente selecionados no modo de exibição.  <br/> |
|Método [ExecuteAction (ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Executa um comando de edição em relação ao documento XML subjacente de um formulário, com base no campo ou grupo especificado.  <br/> |
|Método [Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)  <br/> |Exporta o modo de exibição para um arquivo do formato especificado.  <br/> |
|Método [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)  <br/> |Força a sincronização entre o documento XML subjacente de um formulário e o modo de exibição associado.  <br/> |
|Método [GetContextNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Obtém uma referência a um objeto **XPathNodeIterator** para iterar sobre os nós XML retornados a partir do nó especificado.  <br/> |
|Método [GetContextNodes (XPathNavigator, Cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Obtém uma referência a um objeto **XPathNodeIterator** para iterar nos nós XML retornados na seleção atual dentro do controle acoplado ao campo ou grupo especificado.  <br/> |
|Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |Obtém uma referência a um objeto **XPathNodeIterator** para iterar em todos os nós XML na seleção atual de itens em um modo de exibição.  <br/> |
|Método [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Seleciona um intervalo de nós em um modo de exibição com base no nó XML inicial especificado.  <br/> |
|Método [SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Seleciona um intervalo de nós em um modo de exibição com base no nó XML inicial especificado e no nó XML final.  <br/> |
|Método [SelectNodes (XPathNavigator, XPathNavigator, Cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Seleciona um intervalo de nós em um modo de exibição com base no nó XML inicial especificado, o nó XML final e o controle especificado.  <br/> |
|Método [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Seleciona o texto contido em um controle editável que está vinculado ao nó especificado pelo objeto **XPathNavigator** passado para este método.  <br/> |
|Método [SelectText (XPathNavigator, Cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Seleciona o texto contido em um controle editável que está vinculado ao nó especificado pelo objeto **XPathNavigator** passado para este método e o controle especificado.  <br/> |
|Método [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)  <br/> |Cria uma mensagem de email contendo o modo de exibição atual.  <br/> |
|Propriedade [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)  <br/> |Obtém uma referência a um objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associado ao modo de exibição.  <br/> |
|Propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)  <br/> |Obtém uma referência a um objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) associado ao modo de exibição.  <br/> |
   
> [!NOTE]
> O modelo de objeto do InfoPath também fornece as classes [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) e [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , que podem ser usadas para obter informações sobre todos os modos de exibição implementados em um formulário. 
  
## <a name="using-the-view-class"></a>Usando a classe View

A classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) é acessada através da propriedade [modoatual](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) da classe XmlForm, que é acessada usando a palavra-chave **this** (C#) ou **me** (Visual Basic). [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Para acessar o nome do modo de exibição, você precisa acessar o objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associado ao modo de exibição. O exemplo a seguir demonstra como exibir uma caixa de mensagem com o nome do modo de exibição atualmente ativo. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Todos os modelos de formulário do InfoPath contêm pelo menos um modo de exibição padrão; no entanto, o InfoPath também dá suporte à criação de vários modos de exibição do documento XML subjacente de um formulário. Quando você tem vários modos de exibição, o [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) pode ser usado para trabalhar com todos os modos de exibição implementados no modelo de formulário. Para acessar o [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) de um modelo de formulário, use a propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) da [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) classe XmlForm. Você pode alterar programaticamente o modo de exibição que está ativo no momento usando o método [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) do [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , como mostra o exemplo de código a seguir. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

O exemplo anterior para mudar de um modo de exibição funcionará somente depois que o formulário for aberto. Para definir um modo de exibição padrão durante o evento [loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , use a propriedade [inicial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) da classe [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , conforme mostrado no exemplo a seguir. Observe, no entanto, que esse valor só entrará em vigor depois que o formulário for salvo e reaberto. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Selecionar controles em um modo de exibição

O InfoPath fornece dois métodos da classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , que são sobrecarregados, para selecionar programaticamente um controle no modo de exibição atual: os métodos [SelectText ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) e [SelectNodes ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) . O método [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) é usado para controles de entrada de dados, como uma **caixa de texto**, enquanto o método **SelectNodes** é usado para controles estruturais, como uma **seção opcional**. Para selecionar um determinado controle no modo de exibição, você precisa fornecer o nó e, opcionalmente, a ID ViewContext do controle. A ID ViewContext é necessária quando você tem vários controles associados ao mesmo nó na fonte de dados. O InfoPath fornece as informações de ID do ViewContext quando você cria o formulário.
  
A ID de ViewContext de um controle é exibida na guia **avançado** da caixa de diálogo Propriedades do controle, que é acessada clicando com o botão direito do mouse no controle, clicando em **Propriedades**de _controle_ e, em seguida, clicando na guia **avançado** . A ID ViewContext do controle é listada na seção **código** da guia **avançado** . 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Quando usar o SelectText e SelectNodes

Você pode selecionar programaticamente os seguintes controles de entrada de dados usando o método [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) : 
  
- Caixa de Texto
    
- Caixa de Rich Text
    
- Seletor de data
    
Você pode selecionar programaticamente os seguintes controles estruturais usando o método [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) : 
  
- Seção opcional
    
- Seção de escolha
    
- Seção de repetição (itens)
    
- Tabela de repetição (linhas)
    
- Seção recursiva de repetição (itens)
    
- Lista com marcadores, numerada e sem formatação
    
- Tabela de Repetição Horizontal
    
Você não pode selecionar, ou definir o foco, de forma programática, os seguintes controles:
  
- Caixa de listagem suspensa
    
- Caixa de listagem
    
- Caixa de Verificação
    
- Botão de opção
    
- Botão
    
- Imagem (vinculada ou incluída)
    
- Imagem à tinta
    
- Hiperlink
    
- Caixa de expressões
    
- Rótulo vertical
    
- Seção ActiveX
    
- Região horizontal
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a>Usando os métodos SelectText e SelectNodes

No exemplo a seguir, a sobrecarga de [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) do método **SelectText** , que fornece um parâmetro _xmlNode_ , é usada para selecionar uma **caixa de texto** associada a "My: campo1". 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

Se você tiver vários controles vinculados a "My: campo1", você deve usar a sobrecarga [SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) do método **SelectText** , que fornece um parâmetro _ViewContext_ adicional para selecionar um controle específico. O exemplo a seguir pressupõe que há dois controles de **caixa de texto** acoplados a "My: campo1", com o primeiro controle com uma ID ViewContext de "CTRL1" e o segundo controle com uma ID de VIEWCONTEXT "CTRL8". O segundo controle é selecionado. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

No exemplo a seguir, a sobrecarga [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) do método **SelectNodes** , que fornece apenas um parâmetro _startNode_ , é usada para selecionar a primeira linha em uma tabela de repetição vinculada ao grupo de repetição "My: Employee ". 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

Você também pode selecionar várias linhas em uma tabela de repetição. No exemplo a seguir, as três primeiras linhas de uma tabela de repetição vinculadas ao grupo de repetição "My: Employee" são selecionadas usando a sobrecarga [SelectNodes (XPathNavigator, XPathNavigator, Cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) do método **SelectNodes** , que fornece  parâmetros de _startNode_ e endnode: __ 
  
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


