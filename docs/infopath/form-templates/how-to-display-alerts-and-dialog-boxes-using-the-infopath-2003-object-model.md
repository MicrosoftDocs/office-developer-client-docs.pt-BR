---
title: Exibir alertas e caixas de diálogo usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos [InfoPath 2007], exibindo caixas de diálogo, alertas, de formulário de modelos de formulário compatíveis com 2003 do InfoPath, exibindo caixas de diálogo, exibindo em modelos de formulário compatíveis com o InfoPath 2003, caixas de diálogo, exibindo em compatíveis com o InfoPath 2003 modelos de formulário , Os modelos de formulário compatíveis com o InfoPath 2003, exibindo os alertas
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: Ao escrever código para estender a funcionalidade de um modelo de formulário que utiliza o modelo de objeto do InfoPath 2003, geralmente é útil fornecer ao usuário informações em uma caixa de diálogo.
ms.openlocfilehash: 1cc0f4c7a6696eae2d3b7058898b4119cede79e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765613"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a>Exibir alertas e caixas de diálogo usando o modelo de objeto do InfoPath 2003

Ao escrever código para estender a funcionalidade de um modelo de formulário que utiliza o modelo de objeto do InfoPath 2003, geralmente é útil fornecer ao usuário informações em uma caixa de diálogo. Programaticamente exibir uma caixa de diálogo e os elementos de interface de usuário relacionados é realizada no InfoPath usando os métodos da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
## <a name="overview-of-the-uiobject-interface"></a>Visão geral da Interface UIObject

A interface de [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) fornece os seguintes métodos, os desenvolvedores de formulário podem usar para ter tipos diferentes de caixas de diálogo exibidas para os usuários do InfoPath conforme estiverem preenchendo um formulário. 
  
|Name|Descrição|
|:-----|:-----|
|[Alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |Exibe uma caixa de mensagem simples que contém uma cadeia de caracteres da mensagem especificada. Esse método deve ser usado quando nenhuma entrada será necessária do usuário e apenas uma mensagem precisa ser exibido. A caixa de diálogo exibida está fechada clicando no botão **Okey** .  <br/> |
|[Confirmar](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |Exibe uma caixa de mensagem com botões para entrada de um usuário. O valor retornado é uma das seguintes constantes [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerado.  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |Define o nome de arquivo padrão para um formulário na caixa de diálogo **Salvar como** .  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |Define o local inicial no qual a caixa de diálogo **Salvar como** começa naveguem quando ele é aberto.  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |Cria uma nova mensagem de email no aplicativo de email padrão, com o formulário atualmente aberto anexado à mensagem.  <br/> |
|[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |Exibe uma caixa de diálogo modal, com base nos argumentos posicionais e arquivo. HTML especificado. Este método deve ser usado se você deseja exibir mais do que uma simple mensagem ao usuário e você precisa obter alguns dados do usuário (ultrapassando a confirmação de simple que é fornecido pelo **Sim** | **Não** | **Cancelar** botões exibidos pelo método **Confirm** ).  <br/> |
|[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |Exibe a caixa de diálogo interna do **Assinaturas digitais** .  <br/> |
   
## <a name="using-the-uiobject-interface"></a>Usando a Interface UIObject

A interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) é acessada por meio da propriedade da [interface do usuário](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , que por si só é acessado através do `thisXDocument` variável é inicializado no `_Startup` método da classe de código do formulário. O exemplo a seguir demonstra o uso de métodos [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) e [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
```cs
thisXDocument.UI.ShowMailItem("someone@example.com","", "", 
   "Updated Form", "Here is the updated form that you requested.");
thisXDocument.UI.Alert("The email message has been created.");
```

```vb
thisXDocument.UI.ShowMailItem("someone@example.com", "", "", _
   "Updated Form", "Here is the updated form that you requested.")
thisXDocument.UI.Alert("The email message has been created.")
```

## <a name="using-the-showmodaldialog-method"></a>Usando o método

Este exemplo demonstra como usar o método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) para exibir uma caixa de diálogo personalizada definida no show.html de arquivo HTML. 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Write your code here.
   thisXDocument.UI.ShowModalDialog(
      "show.html",(object)thisXDocument,200,450,50,50);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Write your code here.
   thisXDocument.UI.ShowModalDialog( _
      "show.html", _
      DirectCast(thisXDocument, Object), 200, 450, 50, 50)
End Sub

```

Amostras do Visual c# e Visual Basic dependem de um arquivo HTML chamado "show.html" que define a caixa de diálogo que é chamada pelo [método](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) . Este arquivo HTML exibe alguns dados do formulário e mostra uma caixa de texto para o usuário preencher um valor. O valor na caixa de texto é retornado ao formulário, quando a caixa de diálogo é fechada. 
  
```html
<HTML>
   <HEAD>
      <script language="JScript">
function BtnClick()
{
   xdocument = window.dialogArguments;
   myXml = xdocument.DOM.xml
   aForm = oForm.elements;
   aForm.textBox.value = myXml;
}
      </script>
   </HEAD>
   <BODY>
      <H1><FONT face="Arial">This is a modal dialog box</FONT> &nbsp;
      </H1>
      <BUTTON onclick="BtnClick()" id="BUTTON1" type="button">
         Get XML DOM
      </BUTTON>
      <FORM ID="oForm">
         <INPUT Type="text" name="textBox">
      </FORM>
   </BODY>
</HTML>

```

> [!IMPORTANT]
> [Método](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) requer confiança total executar ou visualizar. Para obter mais informações, consulte [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  

