---
title: Gravar lógica condicional que determina o ambiente do tempo de execução
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- ambiente de tempo de execução [InfoPath 2007], executando no navegador [InfoPath 2007], InfoPath 2007, determinando o ambiente de tempo de execução em execução no infopath [infopath 2007]
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: A propriedade ambiente da classe Application obtém uma referência a um objeto de ambiente, que pode ser usado para determinar qual ambiente de tempo de execução (InfoPath, navegador da Web ou navegador móvel) foi usada para abrir o formulário.
ms.openlocfilehash: b854d6a3b65fcc37375480bef9f1909d84407b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765611"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a>Gravar lógica condicional que determina o ambiente do tempo de execução

A propriedade [ambiente](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) obtém uma referência a um objeto de [ambiente](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) , que pode ser usado para determinar qual ambiente de tempo de execução (InfoPath, navegador da Web ou navegador móvel) foi usada para abrir o formulário. 
  
## <a name="example"></a>Exemplo

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a>Determinando qual Runtime Environment um formulário está em execução no

A classe de [ambiente](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) fornece as propriedades [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) e [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) que permitem determinar qual ambiente de edição foi usada para abrir um modelo de formulário. Se ambas as propriedades retornarem **false**, o modelo de formulário foi aberto no editor do Microsoft InfoPath. Se a propriedade retorna **true**, o modelo de formulário foi aberto em uma biblioteca de documentos devidamente configurado no Microsoft SharePoint Server 2010 executando o InfoPath Forms Services no programa para a propriedade correspondente: um navegador da Web ([ IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) propriedade) ou um navegador móvel (propriedade [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) ). 
  
No exemplo a seguir, se o formulário é aberto em um navegador ou o navegador móvel, o valor Field1 (que é acoplado a um controle de **Caixa de texto** ) é definido como uma cadeia de caracteres para indicar qual ambiente de tempo de execução, o formulário foi aberto no. Se o formulário for aberto no InfoPath, o método **System.Windows.Forms.MessageBox.Show** (que não está disponível quando um formulário está sendo executado em um navegador) é usado para exibir uma caixa de mensagem. 
  
> [!IMPORTANT]
> Quando você cria o modelo de formulário para o exemplo de código a seguir, selecione o modelo **em branco** na guia **New** do modo de exibição Backstage. (Como alternativa, você pode selecionar **Formulário de navegador da Web** na lista suspensa **tipo de formulário** sob a categoria de **compatibilidade** da caixa de diálogo **Opções de formulário** ). Para oferecer suporte a classe **MessageBox** , adicione uma referência ao **System.Windows.Forms** na. **NET** guia da caixa de diálogo **Adicionar referência** caixa no Visual Studio 2012 e adicione um **usando** ou a diretiva de **importações** para **System.Windows.Forms** na seção Declaração do módulo do formulário de código. 
  
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


