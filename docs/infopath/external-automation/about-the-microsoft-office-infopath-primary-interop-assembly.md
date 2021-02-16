---
title: Sobre o assembly de interoperabilidade primário do InfoPath do Microsoft Office
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007, assembly de interop primário, assembly de interop primário do InfoPath, PIAs [InfoPath 2007],assemblies de interop primária [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Para dar suporte à criação de soluções do InfoPath que usam linguagens de código gerenciado, como Visual C# e Visual Basic, a opção Suporte à Programação .NET no programa de instalação do InfoPath instala três assemblies de interop.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310133"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Sobre o assembly de interoperabilidade primário do InfoPath do Microsoft Office

O aplicativo InfoPath é criado como um aplicativo COM (Component Object Model) que expõe suas interfaces de programação para automação externa como interfaces COM. Para dar suporte à criação de soluções do InfoPath que usam linguagens de código gerenciado, como Visual C# e Visual Basic, a opção Suporte à **Programação .NET** no programa de instalação do InfoPath instala três assemblies de interop. Os assemblies de interoperabilidade são assemblies .NET que atuam como uma ponte entre código gerenciado e não gerenciado, mapeando membros de objeto COM para membros gerenciados .NET equivalentes. 
  
Os arquivos para os três assemblies de interoperabilidade instalados pelo InfoPath são chamados:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
Este tópico discute o modelo de objeto exposto por meio do assembly de interop Microsoft.Office.Interop.InfoPath, que é usado exclusivamente para código de automação externo. Para obter informações sobre o assembly Microsoft.Office.Interop.InfoPath.SemiTrust, que é usado exclusivamente para escrever e executar código gerenciado executado a partir de modelos de formulário do InfoPath (.xsn), consulte Modelos de Objeto Compatíveis com [o InfoPath 2003.](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx)
  
## <a name="important-installation-information"></a>Informações de instalação importantes

A opção de instalação padrão do programa de instalação do InfoPath instala o assembly Microsoft.Office.Interop.InfoPath no GAC (Cache de Assembly Global), que pode ser exibido na pasta C:\Windows\Assembly (ou em C:\Windows\assembly\GAC_MSIL ao exibir o sistema de arquivos diretamente). Esse assembly é conhecido como "Assembly de Interop Primário do Microsoft Office InfoPath" e é frequentemente usado em conjunto com o assembly Microsoft.Office.Interop.InfoPath.Xml, que também é instalado no GAC, para automatizar o aplicativo InfoPath de aplicativos externos que usam código gerenciado. Para obter informações sobre o assembly Microsoft.Office.Interop.InfoPath.Xml, consulte Sobre o Assembly [de Interop XML do InfoPath.](about-the-infopath-xml-interop-assembly.md)
  
Se o assembly Microsoft.Office.Interop.InfoPath não estiver visível no GAC, confirme se o InfoPath foi instalado corretamente. Por padrão, a opção Suporte à Programação **.NET**  no programa de instalação é definida como Executar do Meu Computador, desde que o .NET Framework 1.1 Redistribuível, o .NET Framework 1.1 Software Development Kit (SDK) ou uma versão posterior do .NET Framework seja instalado antes da execução da instalação. Se esses assemblies de interop não estão disponíveis em seu computador, você deve confirmar se o  .NET Framework  1.1 ou posterior está instalado e, em seguida, usar Programas e Recursos do Painel de Controle para alterar a configuração definindo a opção de Suporte de **Programação do .NET** em **Microsoft Office InfoPath** para Executar do **Meu** Computador.
  
Para obter informações sobre como baixar o .NET Framework 1.1 [Redistribuível, consulte .NET Framework 1.1 Redistribuível.](https://www.microsoft.com/en-us/download/details.aspx?id=26)
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>O namespace Microsoft.Office.Interop.InfoPath

Embora o processo de escrever código gerenciado para uma determinada tarefa seja muito semelhante a executar a mesma tarefa usando uma linguagem como Visual Basic for  Applications ou JScript, o modelo de objeto exposto ao exibir o namespace **Microsoft.Office.Interop.InfoPath** do Pesquisador de Objetos no Microsoft Visual Studio parece mais complexo. Isso porque a interoperabilidade com o .NET Framework exige que um servidor COM exponha todas as suas interfaces públicas, bem como algumas construções adicionais exigidas pelo próprio .NET Framework. For more information on how and why the object model exposed by an interop assembly appears more complex, see the "How COM Objects are Exposed to Managed Code" section of the [InfoPath 2003 Compatible Object Models](../form-templates/infopath-2003-compatible-object-models.md) topic. 
  
### <a name="using-intellisense"></a>Como usar o IntelliSense

Os exemplos nesta seção pressupom que você tenha estabelecido referências aos assemblies Microsoft.Office.Interop.InfoPath e Microsoft.Office.Interop.InfoPath.Xml assemblies. Para obter informações sobre como definir referências e exemplos adicionais de automação externa, consulte [Cenários e exemplos](external-automation-scenarios-and-examples.md)de automação externa.
  
Antes de poder usar a conclusão da instrução Microsoft IntelliSense no código de automação externo, você deve criar uma variável de objeto para uma instância da classe [Application,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) conforme mostrado na linha de código a seguir. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Depois de criar a variável de objeto, quando você digita o nome da variável seguido por um ponto, uma listada é exibida com membros da classe **Application** a ser selecionada. 
  
To work with an InfoPath form, declare an object variable of type [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) , and then initialize it by opening the form from the [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) collection of the **Application** object variable as shown in the following line of code. 
  
```cs
XDocument myXDoc = myApp.XDocuments.Open(
    "c:\\temp\\Form1.xml",
    (int) XdDocumentVersionMode.xdFailOnVersionOlder);
```

```vb
Dim myXDoc As XDocument = myApp.XDocuments.Open( _
    "c:\\temp\\Form1.xml", _
    XdDocumentVersionMode.xdFailOnVersionOlder)
```

A lista de conclusão da instrução IntelliSense para membros da classe **XDocument** será exibida quando você digitar o nome da variável seguido de um ponto. 
  
To work with the contents of the underlying XML document for the form using Microsoft XML Core Services (MSXML), you must create a variable of type [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) , and then use the [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) property of the **XDocument** class to assign the XML Document Object Model (DOM) of the form to that variable. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

A lista drop-down de conclusão da instrução IntelliSense para membros da classe **IXMLDOMDocument2** será exibida quando você digitar o nome da variável seguido de um ponto, o que permite que você use MSXML para trabalhar com o documento XML. 
  
### <a name="using-the-class-library-reference-documentation"></a>Usando a documentação de referência da biblioteca de classes

A organização da documentação de referência da Biblioteca de Classes do namespace [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) reflete as relações entre interfaces de coclass e as interfaces herdadas que elas implementam. 
  
Quando você abre um tópico para uma interface de coclass, como [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , o link para os membros da interface de coclasse após a descrição da interface no início do tópico exibe um tópico vazio. Para exibir a lista de membros implementados pela interface de coclass, você deve abrir o tópico da interface mais recente herdada pela coclass e, em seguida, abrir a tabela dos seus membros. Um link para a interface herdada é fornecido no início da seção Comentários no tópico da interface de coclass. 
  
Quando você pressiona F1 no Editor de Código do Visual Studio, o comportamento é semelhante, exceto que o membro no qual você invoca a Ajuda F1 será exibido diretamente, porque você normalmente está trabalhando com membros de uma interface. No entanto, o fato de um membro poder se implementado de uma interface com versão pode parece confuso na primeira vez que você o encontrar. Por exemplo, se você digitar `myXDocument.UI.Alert`, posicionar o cursor sobre `Alert` e pressionar F1, um tópico intitulado "Método de Alerta UI2"é exibido. Isso ocorre porque o método **Alerta** é uma implementação de um membro da interface **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Passagem de parâmetros opcionais para membros do modelo de objeto do InfoPath

Se um membro do modelo de objeto do InfoPath contiver um parâmetro opcional e você não especificar um valor para esse parâmetro, deverá passar o campo **Type.Missing** para esse parâmetro. Não transferir o campo **Type.Missing** quando um valor real for omitido resultará em um erro de compilação. Isso é verdadeiro para código escrito em C# e Visual Basic. Por exemplo, o método [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) da interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) inclui dois parâmetros opcionais: _varEndNode_ e _varViewContext_. Uma linha de código que não especifique valores reais para esses parâmetros opcionais deve parecer com os exemplos a seguir.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Confira também

- [Cenários e exemplos de automação externa](external-automation-scenarios-and-examples.md)

