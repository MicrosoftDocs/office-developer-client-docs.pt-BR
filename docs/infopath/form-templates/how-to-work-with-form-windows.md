---
title: Trabalhar com janelas de formulários
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- windowscollection [InfoPath 2007], formulário Windows [InfoPath 2007], classe de janela [InfoPath 2007]
localization_priority: Normal
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: Ao trabalhar de forma programática com um formulário do InfoPath, você pode escrever código para acessar o Windows do formulário e, em seguida, personalizar alguns dos itens que eles contêm. O modelo de objeto do InfoPath fornecido pelo namespace Microsoft. Office. InfoPath oferece suporte ao acesso a janelas de um formulário por meio do uso da classe Window em associação com a classe WindowCollection.
ms.openlocfilehash: 018357519e27629c29b2611bd0a88b8d64f0a1eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431061"
---
# <a name="work-with-form-windows"></a>Trabalhar com janelas de formulários

Ao trabalhar de forma programática com um formulário do InfoPath, você pode escrever código para acessar o Windows do formulário e, em seguida, personalizar alguns dos itens que eles contêm. O modelo de objeto do InfoPath fornecido pelo namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) oferece suporte ao acesso a janelas de um formulário por meio do uso da classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) em associação com a classe [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) . 
  
> [!NOTE]
> As classes para trabalhar com as janelas de um formulário estão disponíveis somente quando se trabalha com um **formulário do editor do InfoPath**. Se a configuração de **compatibilidade** de um modelo de formulário for **formulário de navegador da Web**, essas classes não estarão disponíveis. 
  
Há dois tipos de janelas no InfoPath: 
  
- A janela de edição que é usada quando um usuário preenche um formulário.
    
- A janela de design que é usada quando um usuário projeta um modelo de formulário.
    
Ao escrever código em um modelo de formulário, é a janela de edição que fornece a funcionalidade mais útil, porque você pode usar um objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) que representa a janela atual para acessar uma variedade de propriedades e métodos que podem ser usados para personalizar o experiência de edição de formulários. 
  
## <a name="overview-of-the-windowscollection-class"></a>Visão geral da classe Windowscollection

A [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) classe WindowCollection fornece as seguintes propriedades, que os desenvolvedores de modelos de formulário podem usar para gerenciar os objetos [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) que ele contém. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx)  <br/> |Obtém uma contagem do número de objetos [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) contidos na coleção.  <br/> |
|Propriedade [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx)  <br/> |Obtém uma referência para o objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) especificado.  <br/> |
   
## <a name="overview-of-the-window-class"></a>Visão geral da classe Window

A classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulários podem usar para interagir com uma janela do InfoPath. O suporte para esses métodos e propriedades diferem dependendo do tipo de janela [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) (windowtype) com o qual você está trabalhando. Alguns métodos e propriedades funcionam somente com o tipo de janela Editor (**windowtype. editor**). Os métodos e propriedades restantes funcionam com o tipo de janela Editor e o tipo de janela designer (**windowtype. designer**). Além disso, como todos os membros do modelo de objeto do InfoPath, quando chamado a partir de um modelo de formulário, o suporte a métodos e propriedades pode variar dependendo do nível de segurança e como o formulário é implantado.
  
|**Nome**|**Descrição**|**Suporte ao tipo de janela**|
|:-----|:-----|:-----|
|Método [Activate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx)  <br/> |Ativa (fornece foco) a janela.  <br/> |O **Designer** e o tipo de **Editor**  <br/> |
|Propriedade [Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx)  <br/> |Obtém um valor **Boolean** que indica se a janela é a janela ativa no momento.  <br/> |O **Designer** e o tipo de **Editor**  <br/> |
|Propriedade [Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx)  <br/> |Obtém ou define o texto de legenda para a janela representada pelo objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) .  <br/> |Somente tipo de **Editor**  <br/> |
|Método [Close ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Fecha a janela solicitando salvar as alterações em qualquer formulário não salvo ou formulário com alterações que não foram salvas.  <br/> |Somente tipo de **Editor**  <br/> |
|Método [Close (Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Fecha a janela e, opcionalmente, força um formulário ou formulário não salvo com alterações não salvas a ser fechado sem salvar.  <br/> |Somente tipo de **Editor**  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) Propriedade CommandBars  <br/> |Obtém uma referência à coleção CommandBars **** do Microsoft Office que está associada à janela.  <br/> |O **Designer** e o tipo de **Editor**  <br/> |
|Propriedade [Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx)  <br/> |Obtém ou define a altura da janela, medida em pontos.  <br/> |O **Designer** e o tipo de **Editor**  <br/> |
|Propriedade [Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx)  <br/> |Obtém ou define a posição horizontal da janela, medida em pontos.  <br/> |O **Designer** e o tipo de **Editor**  <br/> |
|Propriedade [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx)  <br/> |Obtém uma referência à classe [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) .  <br/> |Somente tipo de **Editor**  <br/> |
|Propriedade [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx)  <br/> |Obtém uma referência para a coleção [TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) .  <br/> |O **Designer** e o tipo de **Editor**  <br/> |
|Propriedade [Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx)  <br/> |Obtém ou define a posição vertical da janela, medida em pontos.  <br/> |O **Designer** e o tipo de **Editor**  <br/> |
|Propriedade [Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx)  <br/> |Obtém ou define a largura da janela, medida em pontos.  <br/> |O **Designer** e o tipo de **Editor**  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx) Propriedade WindowState  <br/> |Obtém ou define o estado da janela como um valor [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) .  <br/> |O **Designer** e o tipo de **Editor**  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx) Propriedade windowtype  <br/> |Obtém o tipo da janela como um valor [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) de enumeração windowtype.  <br/> |O **Designer** e o tipo de **Editor**  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx) Propriedade XmlForm  <br/> |Retorna uma referência ao objeto [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) associado à janela.  <br/> |Somente tipo de **Editor**  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>Usando as classes Windowscollection e Window

A [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) classe WindowCollection pode ser acessada por meio da propriedade [Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . Ao usar a [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) classe WindowCollection para acessar as janelas de um formulário, você usa um indexador (para Visual C#) ou passa um inteiro longo para a propriedade **Item** (para Visual Basic) para retornar uma referência a uma instância de objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) . Por exemplo, o código a seguir define uma referência para o primeiro objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) contido no [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) da sessão atual do InfoPath. 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

Você pode acessar a janela aberta no momento usando a propriedade [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) , sem passar pelo WindowCollection [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) , conforme mostrado na seguinte linha de código. 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

Um objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) também pode ser acessado usando a propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) da classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , que representa o modo de exibição atual que está sendo usado para trabalhar com o documento XML subjacente do formulário. A propriedade [modoatual](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) é usada para acessar um objeto [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) que representa o modo de exibição atual. Por exemplo, o código a seguir define uma referência à [janela](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) associada ao modo de exibição atual. 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> Algumas das propriedades e métodos da classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) são apenas para o tipo de janela de edição; Se usado com o tipo de janela de design, ele retornará um erro. Quais propriedades e métodos são suportados para cada tipo de janela estão listados na tabela anteriormente neste tópico. Você pode usar a propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) no seu código para determinar qual tipo de janela você está trabalhando. 
  

