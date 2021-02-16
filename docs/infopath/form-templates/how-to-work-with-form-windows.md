---
title: Trabalhar com o Formulário do Windows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- windowscollection [infopath 2007], janelas de formulário [InfoPath 2007],classe Window [InfoPath 2007]
localization_priority: Normal
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: Ao trabalhar programaticamente com um formulário do InfoPath, você pode escrever código para acessar as janelas do formulário e personalizar alguns dos itens que eles contêm. O modelo de objeto do InfoPath fornecido pelo namespace Microsoft.Office.InfoPath dá suporte ao acesso a janelas de um formulário por meio do uso da classe Window em associação com a classe WindowCollection.
ms.openlocfilehash: 018357519e27629c29b2611bd0a88b8d64f0a1eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431061"
---
# <a name="work-with-form-windows"></a>Trabalhar com o Formulário do Windows

Ao trabalhar programaticamente com um formulário do InfoPath, você pode escrever código para acessar as janelas do formulário e personalizar alguns dos itens que eles contêm. O modelo de objeto do InfoPath fornecido pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) dá suporte ao acesso a janelas de um formulário por meio do uso da classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) em associação com a classe [WindowCollection.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) 
  
> [!NOTE]
> The classes for working with a form's windows are available only when working with an **InfoPath Editor Form**. Se a configuração de Compatibilidade **de um** modelo de formulário for Formulário do Navegador da **Web,** essas classes não estarão disponíveis. 
  
Há dois tipos de janelas no InfoPath: 
  
- A janela de edição usada quando um usuário preenche um formulário.
    
- A janela de design que é usada quando um usuário projeta um modelo de formulário.
    
When writing code in a form template, it is the editing window that provides the most useful functionality, because you can use a Window object that represents the [current](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) window to access a variety of properties and methods that can be used to customize the form editing experience. 
  
## <a name="overview-of-the-windowscollection-class"></a>Visão geral da classe WindowsCollection

A [classe WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) fornece as seguintes propriedades, que os desenvolvedores de modelos de formulário podem usar para gerenciar os [objetos Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) que ela contém. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx)  <br/> |Obtém uma contagem do número [de objetos Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) contidos na coleção.  <br/> |
|Propriedade [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx)  <br/> |Obtém uma referência ao objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) especificado.  <br/> |
   
## <a name="overview-of-the-window-class"></a>Visão geral da classe Window

A [classe Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir com uma janela do InfoPath. O suporte a esses métodos e propriedades diferem dependendo do tipo de janela ( [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) ) com o qual você está trabalhando. Alguns métodos e propriedades funcionam apenas com o tipo de janela do editor (**WindowType.Editor**). Os métodos e propriedades restantes funcionam com o tipo de janela do editor e o tipo de janela do designer (**WindowType.Designer**). Além disso, como todos os membros do modelo de objeto do InfoPath, quando chamado de um modelo de formulário, o suporte para métodos e propriedades pode variar dependendo do nível de segurança e de como o formulário é implantado.
  
|**Nome**|**Descrição**|**Suporte a tipos de janela**|
|:-----|:-----|:-----|
|[Método Activate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx)  <br/> |Ativa (dá foco a) a janela.  <br/> |Tipo **de Designer** **e** Editor  <br/> |
|[Propriedade Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx)  <br/> |Obtém **um valor Boolean** indicando se a janela é a janela ativa no momento.  <br/> |Tipo **de Designer** **e** Editor  <br/> |
|[Propriedade Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx)  <br/> |Obtém ou define o texto da legenda da janela representada pelo [objeto Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) .  <br/> |Somente **o tipo de** Editor  <br/> |
|[Método Close()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Fecha a janela solicitando salvar alterações em qualquer formulário não salvo ou formulário com alterações que não foram salvas.  <br/> |Somente **o tipo de** Editor  <br/> |
|[Método Close(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Fecha a janela e, opcionalmente, força um formulário ou formulário não salvo com alterações não salvas a ser fechado sem salvar.  <br/> |Somente **o tipo de** Editor  <br/> |
|[Propriedade CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx)  <br/> |Obtém uma referência à coleção **CommandBars** do Microsoft Office que está associada à janela.  <br/> |Tipo **de Designer** **e** Editor  <br/> |
|[Propriedade Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx)  <br/> |Obtém ou define a altura da janela, medida em pontos.  <br/> |Tipo **de Designer** **e** Editor  <br/> |
|[Propriedade Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx)  <br/> |Obtém ou define a posição horizontal da janela, medida em pontos.  <br/> |Tipo **de Designer** **e** Editor  <br/> |
|[Propriedade MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx)  <br/> |Obtém uma referência para a [classe MailEnvelope.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx)  <br/> |Somente **o tipo de** Editor  <br/> |
|Propriedade [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx)  <br/> |Obtém uma referência à [coleção TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) .  <br/> |Tipo **de Designer** **e** Editor  <br/> |
|[Propriedade Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx)  <br/> |Obtém ou define a posição vertical da janela, medida em pontos.  <br/> |Tipo **de Designer** **e** Editor  <br/> |
|[Propriedade Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx)  <br/> |Obtém ou definir a largura da janela, medida em pontos.  <br/> |Tipo **de Designer** **e** Editor  <br/> |
|[Propriedade WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx)  <br/> |Obtém ou define o estado da janela como um [valor WindowState.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx)  <br/> |Tipo **de Designer** **e** Editor  <br/> |
|[Propriedade WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx)  <br/> |Obtém o tipo da janela como um valor de enumeração [WindowType.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx)  <br/> |Tipo **de Designer** **e** Editor  <br/> |
|[Propriedade XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx)  <br/> |Retorna uma referência ao [objeto XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) associado à janela.  <br/> |Somente **o tipo de** Editor  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>Usando as classes WindowsCollection e Window

A [classe WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) pode ser acessada por meio da [propriedade Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) da classe [Application.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) Ao usar a classe [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) para acessar as janelas de um formulário, você usa um indexador (para Visual C#) ou passa um inteiro longo para a propriedade **Item** (para Visual Basic) para retornar uma referência a uma instância de objeto [Window.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) Por exemplo, o código a seguir define uma referência ao primeiro objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) contido no [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) para a sessão atual do InfoPath. 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

Você pode acessar a janela aberta no momento diretamente usando a propriedade [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) da classe [Application,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) sem passar pela [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) , conforme mostrado na linha de código a seguir. 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

Um [objeto Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) também pode ser acessado usando a propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) da classe [View,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) que representa a exibição atual que está sendo usada para trabalhar com o documento XML subjacente do formulário. A [propriedade CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) é usada para acessar um objeto [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) que representa a exibição atual. Por exemplo, o código a seguir define uma referência à [janela](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) associada ao ponto de exibição atual. 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> Algumas das propriedades e métodos da classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) são apenas para o tipo de janela de edição; se usado com o tipo de janela de design, eles retornarão um erro. Quais propriedades e métodos são suportados para cada tipo de janela estão listados na tabela anterior neste tópico. Você pode usar a [propriedade Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) em seu código para determinar com qual tipo de janela você está trabalhando. 
  

