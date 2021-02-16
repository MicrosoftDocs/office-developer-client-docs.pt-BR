---
title: Escrever lógica condicional que determina o ambiente de tempo de executar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- executando no infopath [infopath 2007], ambiente de tempo de execução [InfoPath 2007], executando no navegador [InfoPath 2007],InfoPath 2007, determinando o ambiente de tempo de execução
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: A propriedade Environment da classe Application obtém uma referência a um objeto Environment, que pode ser usado para determinar qual ambiente de tempo de execução (InfoPath, navegador da Web ou navegador móvel) foi usado para abrir o formulário.
ms.openlocfilehash: 31bfd8dcd05d52d6c6e162d4aa4838e423d97e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408597"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a>Escrever lógica condicional que determina o ambiente de tempo de executar

A propriedade [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) obtém uma referência a um objeto [Environment,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) que pode ser usado para determinar qual ambiente de tempo de execução (InfoPath, navegador da Web ou navegador móvel) foi usado para abrir o formulário. 
  
## <a name="example"></a>Exemplo

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a>Determinando em qual ambiente de tempo de execução um formulário está sendo executado

A [classe Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) fornece as propriedades [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) e [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) que permitem determinar qual ambiente de edição foi usado para abrir um modelo de formulário. Se ambas as propriedades **retornarem false**, o modelo de formulário foi aberto no editor do Microsoft InfoPath. Se uma das propriedades retornar **true**, o modelo de formulário foi aberto a partir de uma biblioteca de documentos configurada adequadamente no Microsoft SharePoint Server 2010 executando o InfoPath Forms Services no programa para a propriedade correspondente: um navegador da Web ( propriedade [IsBrowser)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) ou um navegador móvel ( [propriedade IsMobile).](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) 
  
No exemplo a seguir, se o formulário for aberto em um navegador ou navegador móvel, o valor do campo1 (que está ligado a um controle **Caixa** de Texto) será definido como uma cadeia de caracteres para indicar em qual ambiente de tempo de execução o formulário foi aberto. Se o formulário for aberto no InfoPath, o método **System.Windows.Forms.MessageBox.Show** (que não está disponível quando um formulário está sendo executado em um navegador) será usado para exibir uma caixa de mensagem. 
  
> [!IMPORTANT]
> Ao criar o modelo de formulário para  o exemplo de código a seguir, selecione o modelo em branco na guia **Novo** do exibição Backstage. (Como alternativa, você pode selecionar  o Formulário do Navegador  da **Web** na lista de menus menus do tipo formulário na categoria Compatibilidade da caixa de diálogo Opções **de** Formulário.) Para dar suporte **à classe MessageBox,** adicione uma referência a **System.Windows.Forms** no . **Guia NET**  da caixa de diálogo Adicionar Referência no Visual Studio 2012 e, em seguida, adicione uma diretiva **using** ou **Imports** para **System.Windows.Forms** na seção de declarações do módulo de código do formulário. 
  
```cs
if(this.Application.Environment.IsBrowser)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a browser.");
}
else if (this.Application.Environment.IsMobile)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a mobile browser.");
}
else
{
   MessageBox.Show("This form is running in the InfoPath editor.");
}
```

```vb
If (Me.Application.Environment.IsBrowser) Then
   CreateNavigator().SelectSingleNode(_
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a browser.")
ElseIf (Me.Application.Environment.IsMobile) Then
   CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a mobile browser.")
Else
   MessageBox.Show("This form is running in the InfoPath editor.")
End If
```


