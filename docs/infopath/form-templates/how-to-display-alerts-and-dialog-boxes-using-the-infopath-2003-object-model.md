---
title: Exibir alertas e caixas de diálogo usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com o InfoPath 2003, exibindo caixas de diálogo, modelos de formulário [InfoPath 2007], exibindo caixas de diálogo, alertas, exibindo em modelos de formulário compatíveis com o InfoPath 2003, exibindo em modelos de formulário compatíveis com o InfoPath 2003 , Modelos de formulário compatíveis com o InfoPath 2003, exibindo alertas
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: Ao escrever código para estender a funcionalidade de um modelo de formulário que usa o modelo de objeto do InfoPath 2003, é sempre útil fornecer informações ao usuário em uma caixa de diálogo.
ms.openlocfilehash: 12088747250037e53a3b7d8d0577936e30d6292c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409479"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a>Exibir alertas e caixas de diálogo usando o modelo de objeto do InfoPath 2003

Ao escrever código para estender a funcionalidade de um modelo de formulário que usa o modelo de objeto do InfoPath 2003, é sempre útil fornecer informações ao usuário em uma caixa de diálogo. Exibir proGramaticamente uma caixa de diálogo e elementos de interface do usuário relacionados são obtidos no InfoPath usando os métodos da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
## <a name="overview-of-the-uiobject-interface"></a>Visão geral da interface UIObject

A interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) fornece os seguintes métodos, que os desenvolvedores de formulários podem usar para ter diferentes tipos de caixas de diálogo exibidas aos usuários do InfoPath à medida que estão preenchendo um formulário. 
  
|Nome|Descrição|
|:-----|:-----|
|[Avisar](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |Exibe uma caixa de mensagem simples que contém uma sequência de caracteres de mensagem especificada. Este método deve ser usado quando nenhuma entrada é necessária do usuário e apenas uma mensagem precisa ser exibida. A caixa de diálogo exibida é fechada clicando no botão **OK** .  <br/> |
|[Confirm](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |Exibe uma caixa de mensagem com botões para entrada de um usuário. O valor retornado é uma das constantes enumeradas [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) .  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |Define o nome de arquivo padrão de um formulário na caixa de diálogo **salvar como** .  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |Define o local inicial em que a caixa de diálogo **salvar como** começa a navegar quando é aberta.  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |Cria uma nova mensagem de email no aplicativo de email padrão, com o formulário atualmente aberto anexado à mensagem.  <br/> |
|[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |Exibe uma caixa de diálogo modal, com base nos argumentos de posição e arquivo. html especificado. Este método deve ser usado se você quiser exibir mais de uma mensagem simples para o usuário e precisar obter alguns dados do usuário (além da confirmação simples fornecida pelo **Sim** ) | **Não** | Botões **Cancelar** exibidos pelo método **Confirm** ).  <br/> |
|[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |Exibe a caixa de diálogo **assinaturas digitais** internas.  <br/> |
   
## <a name="using-the-uiobject-interface"></a>Usando a interface UIObject

A interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) é acessada por meio da propriedade [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , que é acessada por meio da `thisXDocument` variável que `_Startup` é inicializada no método da classe de código de formulário. O exemplo a seguir demonstra o uso dos métodos [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) e [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
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

## <a name="using-the-showmodaldialog-method"></a>Usando o método ShowModalDialog

Este exemplo demonstra como usar o método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) para exibir uma caixa de diálogo personalizada definida no arquivo HTML show. html. 
  
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

Os exemplos do Visual C# e do Visual Basic dependem de um arquivo HTML chamado "show. html" que define a caixa de diálogo invocada pelo método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) . Este arquivo HTML exibe alguns dados do formulário e mostra uma caixa de texto para o usuário preencher um valor. O valor na TextBox é retornado ao formulário quando a caixa de diálogo é fechada. 
  
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
> O método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) requer confiança total para executar ou Visualizar. Para obter mais informações, consulte [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  

