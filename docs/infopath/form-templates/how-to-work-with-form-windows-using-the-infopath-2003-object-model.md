---
title: Trabalhar com Windows de formulário usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário de 2003 compatíveis do InfoPath, janelas de formulário, formam windows [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003
localization_priority: Normal
ms.assetid: fbcf3a04-ee0f-40a6-8edd-583ae203e2e1
description: Ao trabalhar programaticamente com um formulário do InfoPath, você pode escrever código para acessar as janelas de formulários e, em seguida, personalizar alguns dos itens que elas contêm. O modelo de objeto compatível com o InfoPath 2003 oferece suporte ao acesso Windows de um formulário com o uso da interface de WindowObject em associação com a interface WindowsCollection.
ms.openlocfilehash: 4ca0fb53fd8502773d3e770814a5a24c40b2d79f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765631"
---
# <a name="work-with-form-windows-using-the-infopath-2003-object-model"></a>Trabalhar com Windows de formulário usando o modelo de objeto do InfoPath 2003

Ao trabalhar programaticamente com um formulário do InfoPath, você pode escrever código para acessar as janelas de formulários e, em seguida, personalizar alguns dos itens que elas contêm. O modelo de objeto compatível com o InfoPath 2003 oferece suporte ao acesso Windows de um formulário com o uso da interface de [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) em associação com a interface [WindowsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowsCollection.aspx) . 
  
Existem dois tipos de janelas no InfoPath:
  
- A janela de edição, que é usada quando um usuário preenche um formulário.
    
- A janela de criação, que é usada quando um usuário cria um modelo de formulário.
    
Ao escrever código em um modelo de formulário, é a janela de edição que fornece a funcionalidade mais útil, porque você pode usar uma instância de **WindowObject** que faz referência a ele para acessar uma variedade de propriedades e métodos que podem ser usados para personalizar o formulário experiência de edição. 
  
## <a name="overview-of-the-windowscollection-interface"></a>Visão geral da Interface WindowsCollection

A interface de **WindowsCollection** oferece as seguintes propriedades, os desenvolvedores de modelos de formulário podem usar para gerenciar as instâncias de **WindowObject** que ele contém. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Count.aspx)  <br/> |Retorna uma contagem do número de objetos **Window** contido na coleção.  <br/> |
|Propriedade [item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Item.aspx)  <br/> |Retorna uma referência ao objeto **Window** especificado.  <br/> **Observação**: Visual c# acessa coleções usando um indexador em vez de chamar a propriedade **Item** . Por exemplo, `thisApplication.Windows[0].Caption`.           |
   
## <a name="overview-of-the-window-object"></a>Visão geral do objeto Window

A interface de **WindowObject** oferece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir com uma janela do InfoPath. Suporte para os métodos e propriedades são diferentes dependendo do tipo de janela ( [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) ) estiver trabalhando com. Alguns métodos e propriedades funcionam somente com o tipo de janela editor (**XdWindowType.xdEditorWindow**). Os métodos e as propriedades restantes trabalham com tanto o tipo de janela editor como o tipo de janela do designer (**XdWindowType.xdDesignerWindow**). Além disso, como todos os membros de modelo de objeto do InfoPath, quando chamado a partir de um modelo de formulário, suporte para os métodos e propriedades pode variar dependendo do nível de segurança e como o formulário é implantado.
  
|**Nome**|**Descrição**|**Suporte de tipo de janela**|
|:-----|:-----|:-----|
|Método [Activate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Activate.aspx)  <br/> |Designa a janela como a janela ativa no momento.  <br/> |Tipos de **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Active](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Active.aspx)  <br/> |Retorna um valor **Boolean** que indica se a janela é a janela ativa no momento.  <br/> |Tipos de **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Caption.aspx)  <br/> |Uma propriedade de leitura/gravação que retorna ou define o texto de legenda da janela representada pelo objeto **Window** .  <br/> |Somente o tipo de **xdEditorWindow**  <br/> |
|Método [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Close.aspx)  <br/> |Fecha uma janela.  <br/> |Somente o tipo de **xdEditorWindow**  <br/> |
|Propriedade [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.CommandBars.aspx)  <br/> |Retorna uma referência ao objeto do Microsoft Office **CommandBars** .  <br/> |Tipos de **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Height](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Height.aspx)  <br/> |Uma propriedade de leitura/gravação de tipo inteiro longo que especifica a altura da janela representada pelo objeto **janela** , medida em pontos.  <br/> |Tipos de **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Left](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Left.aspx)  <br/> |Uma propriedade de leitura/gravação de tipo inteiro longo que especifica a posição horizontal da janela representada pelo objeto **janela** , medida em pontos.  <br/> |Tipos de **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.MailEnvelope.aspx)  <br/> |Retorna uma referência ao objeto [MailEnvelopeObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MailEnvelopeObject.aspx) .  <br/> |Somente o tipo de **xdEditorWindow**  <br/> |
|Propriedade [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.TaskPanes.aspx)  <br/> |Retorna uma referência à coleção [TaskPanesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.TaskPanesCollection.aspx) .  <br/> |Tipos de **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Top](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Top.aspx)  <br/> |Uma propriedade de leitura/gravação de tipo inteiro longo que especifica a posição vertical da janela representada pelo objeto **janela** , medida em pontos.  <br/> |Tipos de **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowType.aspx)  <br/> |Retorna um número que indica o tipo da janela, baseada na enumeração [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) .  <br/> |Tipos de **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Width](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Width.aspx)  <br/> |Uma propriedade de leitura/gravação de tipo inteiro longo que especifica a largura da janela representada pelo objeto **janela** , medida em pontos.  <br/> |Tipos de **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowState.aspx)  <br/> |Uma propriedade de leitura/gravação do tipo [XdWindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowState.aspx) que retorna ou define o estado da janela representada pelo objeto **Window** .  <br/> |Tipos de **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.XDocument.aspx)  <br/> |Retorna uma referência ao objeto [_XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.aspx) associado à janela.  <br/> |Somente o tipo de **xdEditorWindow**  <br/> |
   
## <a name="using-the-windowscollection-and-window-interfaces"></a>Usando o WindowsCollection e Interfaces de janela

A interface **WindowsCollection** pode ser acessada por meio da propriedade [Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Windows.aspx) da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . Ao usar a interface **WindowsCollection** para acessar as janelas de um formulário, use um indexador (para Visual c#) ou passar um inteiro longo para a propriedade **Item** (para Visual Basic) para retornar uma referência a uma instância de interface **WindowObject** . Por exemplo, o código a seguir define uma referência para a primeira **WindowObject** contidos no **WindowsCollection**.
  
```cs
WindowObject objWindow = thisApplication.Windows[0];
```

```vb
Dim objWindow As WindowObject = thisApplication.Windows(0)
```

No entanto, você pode acessar a janela aberta diretamente usando a propriedade [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.ActiveWindow.aspx) da interface do **aplicativo** , sem precisar passar pelo * * WindowsCollection * *, como o código a seguir demonstra.
  
```cs
WindowObject objWindow = thisApplication.ActiveWindow;
```

```vb
Dim objWindow As WindowObject = thisApplication.ActiveWindow
```

> [!NOTE]
> Quando estiver depurando um projeto de código gerenciado do InfoPath, a propriedade **ActiveWindow** sempre retornará **null** porque a janela de depuração estiver ativa. 
  
Um **WindowObject** também pode ser acessado usando a propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) da interface do [modo de exibição](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.aspx) , que é associada ao documento XML de base do formulário. A propriedade **View** da interface **XDocument** é usada para acessar o objeto **View** . Por exemplo, o código a seguir define uma referência para o **WindowObject** associado ao documento XML subjacente do formulário, um modo de exibição. 
  
```cs
WindowObject objWindow = thisXDocument.View.Window;
```

```vb
Dim objWindow As WindowObject = thisXDocument.View.Window
```

> [!NOTE]
> Algumas das propriedades e métodos do objeto JDA **anela** servem apenas para o tipo de janela de edição; Se utilizado com a criação tipo de janela, eles retornará um erro. As propriedades e métodos que são suportados para cada tipo de janela estão listados na tabela mostrada anteriormente neste tópico. Você pode usar a propriedade **WindowType** em seu código para determinar qual tipo de janela que você está trabalhando com. 
  

