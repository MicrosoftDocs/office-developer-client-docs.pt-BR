---
title: Trabalhar com Janelas de Formulário usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com infopath 2003, janelas de formulário, janelas de formulário [InfoPath 2007], modelos de formulário compatíveis com InfoPath 2003
localization_priority: Normal
ms.assetid: fbcf3a04-ee0f-40a6-8edd-583ae203e2e1
description: Ao trabalhar programaticamente com um formulário do InfoPath, você pode escrever código para acessar as janelas do formulário e personalizar alguns dos itens que eles contêm. O modelo de objeto compatível com o InfoPath 2003 dá suporte ao acesso a janelas de um formulário por meio do uso da interface WindowObject em associação com a interface WindowsCollection.
ms.openlocfilehash: f8939fc562cf16c1bce0f6f88bba659e895254f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427574"
---
# <a name="work-with-form-windows-using-the-infopath-2003-object-model"></a>Trabalhar com Janelas de Formulário usando o modelo de objeto do InfoPath 2003

Ao trabalhar programaticamente com um formulário do InfoPath, você pode escrever código para acessar as janelas do formulário e personalizar alguns dos itens que eles contêm. O modelo de objeto compatível com o InfoPath 2003 dá suporte ao acesso a janelas de um formulário por meio do uso da interface [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) em associação com a interface [WindowsCollection.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowsCollection.aspx) 
  
Há dois tipos de janelas no InfoPath:
  
- A janela de edição, que é usada quando um usuário preenche um formulário.
    
- A janela de design, que é usada quando um usuário projeta um modelo de formulário.
    
When writing code in a form template, it is the editing window that provides the most useful functionality, because you can use a **WindowObject** instance that references it to access a variety of properties and methods that can be used to customize the form editing experience. 
  
## <a name="overview-of-the-windowscollection-interface"></a>Visão geral da interface WindowsCollection

A interface **WindowsCollection** fornece as seguintes propriedades, que os desenvolvedores de modelos de formulário podem usar para gerenciar as instâncias **de WindowObject** que ela contém. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Count.aspx)  <br/> |Retorna uma contagem do número de **objetos Window** contidos na coleção.  <br/> |
|Propriedade [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Item.aspx)  <br/> |Retorna uma referência ao objeto **Window** especificado.  <br/> **OBSERVAÇÃO:** o Visual C# acessa coleções usando um indexador em vez de chamar a **propriedade Item.** Por exemplo, `thisApplication.Windows[0].Caption`.           |
   
## <a name="overview-of-the-window-object"></a>Visão geral do objeto Window

A interface **WindowObject** fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir com uma janela do InfoPath. O suporte a esses métodos e propriedades diferem dependendo do tipo de janela ( [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) ) com o qual você está trabalhando. Alguns métodos e propriedades funcionam apenas com o tipo de janela do editor (**XdWindowType.xdEditorWindow**). Os métodos e propriedades restantes funcionam com o tipo de janela do editor e o tipo de janela de designer (**XdWindowType.xdDesignerWindow**). Além disso, como todos os membros do modelo de objeto do InfoPath, quando chamado de um modelo de formulário, o suporte para métodos e propriedades pode variar dependendo do nível de segurança e de como o formulário é implantado.
  
|**Nome**|**Descrição**|**Suporte a tipos de janela**|
|:-----|:-----|:-----|
|[Método Activate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Activate.aspx)  <br/> |Designa a janela como a janela ativa no momento.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[Propriedade Active](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Active.aspx)  <br/> |Retorna um **valor Boolean** indicando se a janela é a janela ativa no momento.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[Propriedade Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Caption.aspx)  <br/> |Uma propriedade de leitura/gravação que retorna ou define o texto da legenda da janela representada pelo **objeto Window** .  <br/> |Somente o **tipo xdEditorWindow**  <br/> |
|Método[Fechar](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Close.aspx)  <br/> |Fecha uma janela.  <br/> |Somente o **tipo xdEditorWindow**  <br/> |
|[Propriedade CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.CommandBars.aspx)  <br/> |Retorna uma referência ao objeto **CommandBars do** Microsoft Office.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[Propriedade Height](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Height.aspx)  <br/> |Uma propriedade de leitura/gravação do tipo inteiro longo que especifica a altura da janela representada pelo objeto **Window,** medida em pontos.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[Propriedade Left](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Left.aspx)  <br/> |Uma propriedade de leitura/gravação do tipo inteiro longo que especifica a posição horizontal da janela representada pelo objeto **Window,** medida em pontos.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[Propriedade MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.MailEnvelope.aspx)  <br/> |Retorna uma referência ao [objeto MailEnvelopeObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MailEnvelopeObject.aspx) .  <br/> |Somente o **tipo xdEditorWindow**  <br/> |
|Propriedade [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.TaskPanes.aspx)  <br/> |Retorna uma referência à [coleção TaskPanesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.TaskPanesCollection.aspx) .  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[Propriedade Top](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Top.aspx)  <br/> |Uma propriedade de leitura/gravação do tipo inteiro longo que especifica a posição vertical da janela representada pelo objeto **Window,** medida em pontos.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[Propriedade WindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowType.aspx)  <br/> |Retorna um número que indica o tipo da janela, com base na [enumeração XdWindowType.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx)  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[Propriedade Width](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Width.aspx)  <br/> |Uma propriedade de leitura/gravação do tipo inteiro longo que especifica a largura da janela representada pelo objeto **Window,** medida em pontos.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[Propriedade WindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowState.aspx)  <br/> |Uma propriedade de leitura/gravação do tipo [XdWindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowState.aspx) que retorna ou define o estado da janela representada pelo **objeto Window.**  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[Propriedade XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.XDocument.aspx)  <br/> |Retorna uma referência ao [_XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.aspx) objeto associado à janela.  <br/> |Somente o **tipo xdEditorWindow**  <br/> |
   
## <a name="using-the-windowscollection-and-window-interfaces"></a>Usando as interfaces WindowsCollection e Window

A interface **WindowsCollection** pode ser acessada por meio da propriedade [Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Windows.aspx) da interface [application.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) Ao usar a interface **WindowsCollection** para acessar as janelas de um formulário, você usa um indexador (para Visual C#) ou passa um inteiro longo para a propriedade **Item** (para Visual Basic) para retornar uma referência a uma instância da interface **WindowObject.** Por exemplo, o código a seguir define uma referência ao primeiro **WindowObject** contido no **WindowsCollection**.
  
```cs
WindowObject objWindow = thisApplication.Windows[0];
```

```vb
Dim objWindow As WindowObject = thisApplication.Windows(0)
```

No entanto, você pode acessar a janela aberta no momento diretamente usando a propriedade [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.ActiveWindow.aspx) da **interface** de aplicativo, sem passar pelo ** WindowsCollection **, como demonstra o código a seguir.
  
```cs
WindowObject objWindow = thisApplication.ActiveWindow;
```

```vb
Dim objWindow As WindowObject = thisApplication.ActiveWindow
```

> [!NOTE]
> Ao depurar um projeto de código gerenciado do InfoPath, a propriedade **ActiveWindow** sempre retornará nulo porque a janela de depuração está ativa.  
  
Um **WindowObject** também pode ser acessado usando a propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) da [interface](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.aspx) View, que é associada ao documento XML subjacente do formulário. A **propriedade View** da interface **XDocument** é usada para acessar o objeto **View** . Por exemplo, o código a seguir define uma referência ao **WindowObject** que está associado à exibição do documento XML subjacente de um formulário. 
  
```cs
WindowObject objWindow = thisXDocument.View.Window;
```

```vb
Dim objWindow As WindowObject = thisXDocument.View.Window
```

> [!NOTE]
> Algumas das propriedades e métodos do objeto **Window** são apenas para o tipo de janela de edição; se usado com o tipo de janela de design, eles retornarão um erro. As propriedades e os métodos com suporte para cada tipo de janela estão listados na tabela mostrada anteriormente neste tópico. Você pode usar a **propriedade WindowType** em seu código para determinar com qual tipo de janela você está trabalhando. 
  

