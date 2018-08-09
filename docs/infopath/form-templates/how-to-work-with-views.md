---
title: Trabalhar com Modos de Exibição
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
# <a name="work-with-views"></a>Trabalhar com Modos de Exibição

Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar os modos de exibição do formulário e, em seguida, executar uma variedade de ações nos dados que contêm os modos de exibição. O modelo de objeto do InfoPath fornecido pelo access [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace oferece suporte aos modos de exibição de um formulário utilizando os membros da classe [modo de exibição](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) . 
  
## <a name="overview-of-the-view-class"></a>Visão geral da classe View

A classe de [modo de exibição](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir com um modo de exibição do InfoPath. 
  
> [!NOTE]
> Os métodos e propriedades da classe [Exibir](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) não estão disponíveis durante o evento de [carregamento](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) . 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)  <br/> |Desabilita a sincronização automática entre o documento XML subjacente de um formulário e o modo de exibição associado.  <br/> |
|Método [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)  <br/> |Habilita a sincronização automática entre o documento XML subjacente de um formulário e o modo de exibição associado.  <br/> |
|Método [ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Executa um comando de edição contra documento XML subjacente de um formulário, com base nos dados selecionados atualmente no modo de exibição.  <br/> |
|Método [ExecuteAction (ActionType, cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Executa um comando de edição contra documento XML subjacente de um formulário, com base no campo especificado ou grupo.  <br/> |
|Método [Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)  <br/> |Exporta o modo de exibição para um arquivo do formato especificado.  <br/> |
|Método [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)  <br/> |Sincronização de força entre o documento XML subjacente de um formulário e o modo de exibição associado.  <br/> |
|Método [GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Obtém uma referência a um objeto **XPathNodeIterator** para iterar nos nós XML retornados começando a partir do nó especificado.  <br/> |
|Método [GetContextNodes (XPathNavigator, cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Obtém uma referência a um objeto **XPathNodeIterator** para iterar nos nós XML retornados na seleção atual dentro do controle vinculado ao campo especificado ou ao grupo.  <br/> |
|Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |Obtém uma referência a um objeto **XPathNodeIterator** para iterar em todos os nós XML na seleção atual dos itens em um modo de exibição.  <br/> |
|Método [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Seleciona um intervalo de nós em um modo de exibição com base no nó XML inicial especificado.  <br/> |
|Método [SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Seleciona um intervalo de nós em um modo de exibição com base em especificado inicial nó XML e final nó XML.  <br/> |
|Método [SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Seleciona um intervalo de nós em um modo de exibição com base no controle especificado, o nó XML final e o nó XML inicial especificado.  <br/> |
|Método [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Seleciona o texto contido em um controle editável que esteja vinculado ao nó especificado pelo objeto **XPathNavigator** passado para este método.  <br/> |
|Método [SelectText (XPathNavigator, cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Seleciona o texto contido em um controle editável que esteja vinculado ao nó especificado pelo objeto **XPathNavigator** passado para este método e o controle especificado.  <br/> |
|Método [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)  <br/> |Cria uma mensagem de email que contém o modo de exibição atual.  <br/> |
|Propriedade [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)  <br/> |Obtém uma referência a um objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associado com o modo de exibição.  <br/> |
|Propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)  <br/> |Obtém uma referência a um objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) associado com o modo de exibição.  <br/> |
   
> [!NOTE]
> O modelo de objeto do InfoPath também fornece as classes [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) e [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , que podem ser usadas para obter informações sobre todas as exibições implementadas em um formulário. 
  
## <a name="using-the-view-class"></a>Usando a classe de modo de exibição

A classe de [modo de exibição](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) é acessada por meio da propriedade [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , que é acessada usando a **Este** (c#) ou a palavra-chave **Me** (Visual Basic). Para acessar o nome do modo de exibição, você precisa acessar o objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associado com o modo de exibição. O exemplo a seguir demonstra como exibir uma caixa de mensagem com o nome do modo de exibição ativo no momento. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Todos os modelos de formulário do InfoPath conter pelo menos um modo de exibição padrão; No entanto, o InfoPath também suporta a criação de vários modos de exibição do documento XML subjacente de um formulário. Quando você tiver vários modos de exibição, o [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) pode ser usado para trabalhar com todas as exibições implementadas no modelo de formulário. Para acessar o [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) de um modelo de formulário, use a propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Programaticamente, você pode alterar o modo de exibição que está ativo no momento usando o método [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) do [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , conforme o exemplo de código a seguir demonstra. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

O exemplo anterior para alternar entre um modo de exibição funcionará somente depois que o formulário é aberto. Para definir um modo de exibição padrão durante o evento de [carregamento](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , use a propriedade [inicial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) da classe [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , conforme mostrado no exemplo a seguir. No entanto, observe que esse valor só terão efeito depois que o formulário está salvo e aberto novamente. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Selecionando os controles em um modo de exibição

O InfoPath fornece dois métodos da classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , ambos os quais estão sobrecarregados, para selecionar programaticamente de um controle no modo de exibição atual: os métodos [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) e [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) . O método [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) é usado para controles de entrada de dados, como uma **Caixa de texto**, enquanto o método **SelectNodes** é usado para controles estruturais, como uma **Seção opcional**. Para selecionar um determinado controle no modo de exibição, você precisa fornecer o nó e, opcionalmente, ID de ViewContext. do controle A ID de ViewContext é necessária quando você tiver vários controles vinculado ao mesmo nó na fonte de dados. InfoPath fornece as informações de identificação ViewContext quando você cria o formulário.
  
Uma identificação do controle ViewContext é exibida na guia **Avançado** da caixa de diálogo de propriedades do controle, que é acessada pelo botão direito do mouse no controle, clicando em _ControlName_ **Propriedades**e, em seguida, clicando na guia **Avançado** . A ID de ViewContext do controle está listada na seção de **código** , da guia **Avançado** . 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Quando usar SelectText e SelectNodes

Programaticamente, você pode selecionar os seguintes controles de entrada de dados usando o método [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) : 
  
- Caixa de Texto
    
- Caixa de Rich Text
    
- Selecionador de data
    
Programaticamente, você pode selecionar os seguintes controles estruturais usando o método [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) : 
  
- Seção opcional
    
- Seção de escolha
    
- (Itens) da seção de repetição
    
- (Linhas) da tabela de repetição
    
- Seção recursiva de repetição (itens)
    
- Lista com marcadores, numerada e sem formatação
    
- Tabela de repetição horizontal
    
Não é possível programaticamente select ou definido o foco para, os seguintes controles:
  
- Caixa de listagem suspensa
    
- Caixa de listagem
    
- Caixa de Verificação
    
- Botão de opção
    
- Botão
    
- Imagem (vinculado ou incluídos)
    
- Imagem de tinta
    
- Hiperlink
    
- Caixa expressão
    
- Rótulo vertical
    
- Seção do ActiveX
    
- Região horizontal
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a>Usando o SelectText e métodos SelectNodes

No exemplo a seguir, a sobrecarga de [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) do método **SelectText** , que fornece um parâmetro _xmlNode_ , é usada para selecionar uma **Caixa de texto** que é vinculado ao "my: field1". 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

Se você tiver vários controles ligados aos "my: field1", você deve usar a sobrecarga de [SelectText (XPathNavigator, cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) do método **SelectText** , que fornece um parâmetro adicional _viewContext_ para selecionar um controle específico. O exemplo a seguir supõe que existem dois controles de **Caixa de texto** vinculados ao "my: field1", onde o primeiro controle ter uma identificação de ViewContext de "CTRL1" e o segundo controle ter uma identificação de ViewContext de "CTRL8". O segundo controle está selecionado. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

No exemplo a seguir, a sobrecarga de [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) do método **SelectNodes** , que fornece apenas um parâmetro _startNode_ , é usada para selecionar a primeira linha em uma tabela de repetição vinculada ao grupo de repetição "Meu: funcionário". 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

Você também pode selecionar várias linhas em uma tabela de repetição. No exemplo a seguir, as três primeiras linhas de uma tabela de repetição é vinculado ao grupo de repetição "Meu: funcionário" estão selecionadas usando a sobrecarga de [SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) do método **SelectNodes** , que fornece  parâmetros de _startNode_ e _endnodes_ : 
  
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


