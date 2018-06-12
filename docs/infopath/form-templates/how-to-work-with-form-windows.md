---
title: Trabalhar com janelas de formulários
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- windowscollection [infopath 2007], janelas de formulário [InfoPath 2007], a classe de janela [InfoPath 2007]
localization_priority: Normal
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: Ao trabalhar programaticamente com um formulário do InfoPath, você pode escrever código para acessar as janelas de formulários e, em seguida, personalizar alguns dos itens que elas contêm. O modelo de objeto do InfoPath fornecido pelo access Microsoft.Office.InfoPath namespace suporta Windows de um formulário com o uso a classe de janela em associação com a classe WindowCollection.
ms.openlocfilehash: 5b24798e92849a2d79bf836e12dd91845ee58942
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765633"
---
# <a name="work-with-form-windows"></a>Trabalhar com janelas de formulários

Ao trabalhar programaticamente com um formulário do InfoPath, você pode escrever código para acessar as janelas de formulários e, em seguida, personalizar alguns dos itens que elas contêm. O modelo de objeto do InfoPath fornecido pelo access [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace suporta Windows de um formulário com o uso a classe de [janela](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) em associação com a classe [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) . 
  
> [!NOTE]
> As classes para trabalhar com janelas de formulário estão disponíveis somente quando estiver trabalhando com um **Formulário do InfoPath Editor**. Se a configuração de **compatibilidade** de um modelo de formulário for um **Formulário de navegador da Web**, essas classes não estão disponíveis. 
  
Existem dois tipos de janelas no InfoPath: 
  
- A janela de edição que é usada quando um usuário preenche um formulário.
    
- A janela de criação que é usada quando um usuário cria um modelo de formulário.
    
Ao escrever código em um modelo de formulário, é a janela de edição que fornece a funcionalidade mais útil, porque você pode usar um objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) que representa a janela atual para acessar uma variedade de propriedades e métodos que podem ser usados para personalizar o experiência de edição de formulário. 
  
## <a name="overview-of-the-windowscollection-class"></a>Visão geral da classe WindowsCollection

A classe [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) fornece as seguintes propriedades, os desenvolvedores de modelos de formulário podem usar para gerenciar os objetos de [janela](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) que ela contém. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx)  <br/> |Obtém uma contagem do número de objetos [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) contido na coleção.  <br/> |
|Propriedade [item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx)  <br/> |Obtém uma referência ao objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) especificado.  <br/> |
   
## <a name="overview-of-the-window-class"></a>Visão geral da classe janela

A classe de [janela](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir com uma janela do InfoPath. Suporte para os métodos e propriedades são diferentes dependendo do tipo de janela ( [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) ) estiver trabalhando com. Alguns métodos e propriedades funcionam somente com o tipo de janela editor (**WindowType.Editor**). Os métodos e as propriedades restantes trabalham com tanto o tipo de janela editor como o tipo de janela do designer (**WindowType.Designer**). Além disso, como todos os membros de modelo de objeto do InfoPath, quando chamado a partir de um modelo de formulário, suporte para os métodos e propriedades pode variar dependendo do nível de segurança e como o formulário é implantado.
  
|**Nome**|**Descrição**|**Suporte de tipo de janela**|
|:-----|:-----|:-----|
|Método [Activate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx)  <br/> |Ativa (oferece o foco para) a janela.  <br/> |Tipo de **Designer** e **Editor**  <br/> |
|Propriedade [Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx)  <br/> |Obtém um valor **Boolean** que indica se a janela é a janela ativa no momento.  <br/> |Tipo de **Designer** e **Editor**  <br/> |
|Propriedade [Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx)  <br/> |Obtém ou define o texto de legenda da janela representada pelo objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) .  <br/> |Somente o tipo de **Editor**  <br/> |
|Método [Close)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Fecha a janela solicitando para salvar alterações qualquer não salvas ou um formulário com alterações que não foram salvos.  <br/> |Somente o tipo de **Editor**  <br/> |
|Método [Close(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Fecha a janela e, opcionalmente, força um formulário que não foram salvo ou o formulário com alterações não salvas a ser fechado sem salvar.  <br/> |Somente o tipo de **Editor**  <br/> |
|Propriedade [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx)  <br/> |Obtém uma referência à coleção do Microsoft Office **CommandBars** que está associada à janela.  <br/> |Tipo de **Designer** e **Editor**  <br/> |
|Propriedade [Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx)  <br/> |Obtém ou define a altura da janela, medida em pontos.  <br/> |Tipo de **Designer** e **Editor**  <br/> |
|Propriedade [Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx)  <br/> |Obtém ou define a posição horizontal da janela, medida em pontos.  <br/> |Tipo de **Designer** e **Editor**  <br/> |
|Propriedade [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx)  <br/> |Obtém uma referência para a classe [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) .  <br/> |Somente o tipo de **Editor**  <br/> |
|Propriedade [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx)  <br/> |Obtém uma referência à coleção [TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) .  <br/> |Tipo de **Designer** e **Editor**  <br/> |
|Propriedade [Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx)  <br/> |Obtém ou define a posição vertical da janela, medida em pontos.  <br/> |Tipo de **Designer** e **Editor**  <br/> |
|Propriedade [Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx)  <br/> |Obtém ou definir a largura da janela, medida em pontos.  <br/> |Tipo de **Designer** e **Editor**  <br/> |
|Propriedade [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx)  <br/> |Obtém ou define o estado da janela como um valor [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) .  <br/> |Tipo de **Designer** e **Editor**  <br/> |
|Propriedade [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx)  <br/> |Obtém o tipo da janela como um valor de enumeração [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) .  <br/> |Tipo de **Designer** e **Editor**  <br/> |
|Propriedade [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx)  <br/> |Retorna uma referência ao objeto [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) associado à janela.  <br/> |Somente o tipo de **Editor**  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>Usando o WindowsCollection e Classes de janela

A classe [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) pode ser acessada por meio da propriedade [Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . Ao usar a classe [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) para acessar as janelas de um formulário, use um indexador (para Visual c#) ou passar um inteiro longo para a propriedade **Item** (para Visual Basic) para retornar uma referência a uma instância do objeto de [janela](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) . Por exemplo, o código a seguir define uma referência ao objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) primeiro contido no [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) para a sessão atual do InfoPath. 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

Você pode acessar a janela aberta diretamente usando a propriedade [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) , sem precisar passar por meio do [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) , conforme mostrado na seguinte linha de código. 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

Um objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) também pode ser acessado usando-se a propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) da classe [modo de exibição](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , que representa o modo de exibição atual que está sendo usado para trabalhar com o documento XML de base do formulário. A propriedade [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) é usada para acessar um objeto [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) que representa o modo de exibição atual. Por exemplo, o código a seguir define uma referência para a [janela](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) que está associado com o modo de exibição atual. 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> Algumas das propriedades e métodos da classe [janela](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) servem apenas para o tipo de janela de edição; Se utilizado com a criação tipo de janela, eles retornará um erro. Quais propriedades e métodos são suportados para cada tipo de janela estão listados na tabela anteriormente neste tópico. Você pode usar a propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) em seu código para determinar qual tipo de janela que você está trabalhando com. 
  

