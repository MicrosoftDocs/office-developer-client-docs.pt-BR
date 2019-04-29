---
title: Trabalhar com janelas de formulário usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com o InfoPath 2003, janelas de formulários, janelas de formulários [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003
localization_priority: Normal
ms.assetid: fbcf3a04-ee0f-40a6-8edd-583ae203e2e1
description: Ao trabalhar de forma programática com um formulário do InfoPath, você pode escrever código para acessar o Windows do formulário e, em seguida, personalizar alguns dos itens que eles contêm. O modelo de objeto compatível com o InfoPath 2003 oferece suporte ao acesso a janelas de um formulário por meio do uso da interface WindowObject em associação à interface Windowscollection.
ms.openlocfilehash: f8939fc562cf16c1bce0f6f88bba659e895254f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427574"
---
# <a name="work-with-form-windows-using-the-infopath-2003-object-model"></a>Trabalhar com janelas de formulário usando o modelo de objeto do InfoPath 2003

Ao trabalhar de forma programática com um formulário do InfoPath, você pode escrever código para acessar o Windows do formulário e, em seguida, personalizar alguns dos itens que eles contêm. O modelo de objeto compatível com o InfoPath 2003 oferece suporte ao acesso a janelas de um formulário por [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) meio do uso da interface WindowObject em associação à interface [windowscollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowsCollection.aspx) . 
  
Há dois tipos de janelas no InfoPath:
  
- A janela de edição, que é usada quando um usuário preenche um formulário.
    
- A janela de design, que é usada quando um usuário projeta um modelo de formulário.
    
Ao escrever código em um modelo de formulário, é a janela de edição que fornece a funcionalidade mais útil, porque você pode usar **** uma instância de WindowObject que faz referência a ele para acessar uma variedade de propriedades e métodos que podem ser usados para personalizar o formulário experiência de edição. 
  
## <a name="overview-of-the-windowscollection-interface"></a>Visão geral da interface do Windowscollection

A interface **Windows** contém as propriedades a seguir, que os desenvolvedores de modelos de formulário podem usar para gerenciar as instâncias de **WindowObject** que ela contém. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Count.aspx)  <br/> |Retorna uma contagem do número de objetos **Window** contidos na coleção.  <br/> |
|Propriedade [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Item.aspx)  <br/> |Retorna uma referência ao objeto **Window** especificado.  <br/> **Observação**: o Visual C# acessa coleções usando um indexador em vez de chamar a propriedade **Item** . Por exemplo, `thisApplication.Windows[0].Caption`.           |
   
## <a name="overview-of-the-window-object"></a>Visão geral do objeto Window

A **** interface WindowObject fornece os seguintes métodos e propriedades, que os desenvolvedores de formulários podem usar para interagir com uma janela do InfoPath. O suporte para esses métodos e propriedades diferem dependendo do tipo de janela ( [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) ) com o qual você está trabalhando. Alguns métodos e propriedades funcionam somente com o tipo de janela Editor (**XdWindowType. xdEditorWindow**). Os métodos e propriedades restantes funcionam com o tipo de janela Editor e o tipo de janela designer (**XdWindowType. xdDesignerWindow**). Além disso, como todos os membros do modelo de objeto do InfoPath, quando chamado a partir de um modelo de formulário, o suporte a métodos e propriedades pode variar dependendo do nível de segurança e como o formulário é implantado.
  
|**Nome**|**Descrição**|**Suporte ao tipo de janela**|
|:-----|:-----|:-----|
|Método [Activate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Activate.aspx)  <br/> |Designa a janela como a janela ativa no momento.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Active](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Active.aspx)  <br/> |Retorna um valor **Boolean** que indica se a janela é a janela ativa no momento.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Caption.aspx)  <br/> |Uma propriedade de leitura/gravação que retorna ou define o texto de legenda para a janela representada pelo objeto **Window** .  <br/> |Somente o tipo **xdEditorWindow**  <br/> |
|Método[Fechar](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Close.aspx)  <br/> |Fecha uma janela.  <br/> |Somente o tipo **xdEditorWindow**  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.CommandBars.aspx) Propriedade CommandBars  <br/> |Retorna uma referência ao objeto CommandBars **** do Microsoft Office.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Height](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Height.aspx)  <br/> |Uma propriedade de leitura/gravação do tipo inteiro longo que especifica a altura da janela representada pelo objeto **Window** , medida em pontos.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Left](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Left.aspx)  <br/> |Uma propriedade de leitura/gravação do tipo inteiro longo que especifica a posição horizontal da janela representada pelo objeto **Window** , medida em pontos.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.MailEnvelope.aspx)  <br/> |Retorna uma referência ao objeto [MailEnvelopeObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MailEnvelopeObject.aspx) .  <br/> |Somente o tipo **xdEditorWindow**  <br/> |
|Propriedade [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.TaskPanes.aspx)  <br/> |Retorna uma referência à coleção [TaskPanesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.TaskPanesCollection.aspx) .  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Top](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Top.aspx)  <br/> |Uma propriedade de leitura/gravação do tipo inteiro longo que especifica a posição vertical da janela representada pelo objeto **Window** , medida em pontos.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowType.aspx) Propriedade windowtype  <br/> |Retorna um número que indica o tipo da janela, com base na enumeração [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) .  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [Width](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Width.aspx)  <br/> |Uma propriedade de leitura/gravação do tipo inteiro longo que especifica a largura da janela representada pelo objeto **Window** , medida em pontos.  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowState.aspx) Propriedade WindowState  <br/> |Uma propriedade de leitura/gravação do tipo [XdWindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowState.aspx) que retorna ou define o estado da janela representada pelo objeto **Window** .  <br/> |Os tipos **xdDesignWindow** e **xdEditorWindow**  <br/> |
|Propriedade [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.XDocument.aspx)  <br/> |Retorna uma referência ao objeto [_XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.aspx) associado à janela.  <br/> |Somente o tipo **xdEditorWindow**  <br/> |
   
## <a name="using-the-windowscollection-and-window-interfaces"></a>Usando o Windowscollection e interfaces de janela

A **** interface windowscollection pode ser acessada por meio da propriedade [Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Windows.aspx) da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . Ao usar a **** interface windowscollection para acessar as janelas de um formulário, você usa um indexador (para Visual C#) ou passa um inteiro longo para a propriedade **Item** (para Visual Basic) para retornar uma referência a uma instância da interface **WindowObject** . Por exemplo, o código a seguir define uma referência para o **** primeiro WindowObject contido no **windowscollection**.
  
```cs
WindowObject objWindow = thisApplication.Windows[0];
```

```vb
Dim objWindow As WindowObject = thisApplication.Windows(0)
```

No enTanto, você pode acessar a janela atualmente aberta diretamente usando a propriedade [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.ActiveWindow.aspx) da interface do **aplicativo** , sem passar pelo * * windowscollection * *, conforme demonstra o código a seguir.
  
```cs
WindowObject objWindow = thisApplication.ActiveWindow;
```

```vb
Dim objWindow As WindowObject = thisApplication.ActiveWindow
```

> [!NOTE]
> Ao depurar um projeto de código gerenciado do InfoPath, a propriedade **ActiveWindow** sempre retornará **NULL** , pois a janela de depuração está ativa. 
  
Um **WindowObject** também pode ser acessado usando a propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) da interface [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.aspx) , que está associada ao documento XML subjacente do formulário. A propriedade **View** da interface **XDocument** é usada para acessar o objeto **View** . Por exemplo, o código a seguir define uma referência ao **WindowObject** que está associado ao modo de exibição do documento XML subjacente de um formulário. 
  
```cs
WindowObject objWindow = thisXDocument.View.Window;
```

```vb
Dim objWindow As WindowObject = thisXDocument.View.Window
```

> [!NOTE]
> Algumas das propriedades e métodos do objeto **Window** são apenas para o tipo de janela de edição; Se usado com o tipo de janela de design, ele retornará um erro. As propriedades e os métodos com suporte para cada tipo de janela são listados na tabela mostrada anteriormente neste tópico. Você pode usar a **** Propriedade windowtype no seu código para determinar qual tipo de janela você está trabalhando. 
  

