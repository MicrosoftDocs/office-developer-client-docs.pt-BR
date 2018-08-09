---
title: Sobre o assembly de interoperabilidade primário do InfoPath do Microsoft Office
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2007, o assembly de interoperabilidade primário, InfoPath assembly de interoperabilidade primário, PIAs [InfoPath 2007], assemblies de interoperabilidade primários [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Para oferecer suporte a criação de soluções do InfoPath que usam os idiomas de código gerenciado, como o Visual c# e Visual Basic, a opção de suporte de programação do .NET no programa de instalação do InfoPath instala os assemblies de interoperabilidade três.
ms.openlocfilehash: b6b37254773d758dc064e22045d68f29febe7bbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765504"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Sobre o assembly de interoperabilidade primário do InfoPath do Microsoft Office

O aplicativo InfoPath é criado como um aplicativo (COM Component Object Model) que expõe suas interfaces de programação para automação externa como interfaces COM. Para oferecer suporte a criação de soluções do InfoPath que usam os idiomas de código gerenciado, como o Visual c# e Visual Basic, a opção de **Suporte de programação do .NET** no programa de instalação do InfoPath instala os assemblies de interoperabilidade três. Os assemblies de interoperabilidade são assemblies .NET que agem como uma ponte entre código gerenciado e, mapeamento de membros do objeto COM ao equivalente .NET gerenciado membros. 
  
Os arquivos para os assemblies de interoperabilidade três instalados pelo InfoPath são nomeados:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
Este tópico aborda o modelo de objeto exposto por meio do assembly de interoperabilidade Microsoft.Office.Interop.InfoPath é usado exclusivamente para o código de automação externa. Para obter informações sobre o assembly SemiTrust, que é usado exclusivamente para escrever e executando código gerenciado que executa a partir modelos de formulário do InfoPath (. xsn), consulte [Modelos de objeto do InfoPath 2003 compatíveis](http://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Informações importantes sobre instalação

A opção de instalação padrão do programa de instalação do InfoPath instala o assembly Microsoft.Office.Interop.InfoPath no Global Assembly Cache (GAC), o conteúdo dos quais pode ser exibido na pasta c:\WINDOWS\Assembly. (ou em C:\Windows\assembly\GAC_ MSIL ao visualizar o sistema de arquivos diretamente). Este assembly é conhecido como o "Microsoft Office InfoPath Primary Interop Assembly" e é frequentemente usado em conjunto com o assembly Microsoft.Office.Interop.InfoPath.Xml, que também é instalado no GAC, para automatizar o aplicativo do InfoPath em aplicativos externos que usam o código gerenciado. Para obter informações sobre o assembly Microsoft.Office.Interop.InfoPath.Xml, consulte [Sobre o InfoPath XML Interop Assembly](about-the-infopath-xml-interop-assembly.md).
  
Se o assembly Microsoft.Office.Interop.InfoPath não estiver visível no GAC, você deve confirmar que o InfoPath foi instalado corretamente. Por padrão, a opção de **Suporte à programação do .NET** no programa de instalação é definida para **Executar de Meu computador** desde que o redistribuível do .NET Framework 1.1, .NET Framework 1.1 Software Development Kit (SDK) ou uma versão posterior do .NET Framework está instalado antes de executar a instalação. Se esses assemblies de interoperabilidade não estão disponíveis no seu computador, você deve confirmar que 1.1 ou posterior do .NET Framework é instalado e use **programas e recursos** do **Painel de controle** para alterar a instalação, definindo o **programação do .NET Suporte** opção em **Microsoft Office InfoPath** para **Executar de Meu computador**.
  
Para obter informações sobre como baixar o redistribuível do .NET Framework 1.1, consulte [Redistribuível do .NET Framework 1.1](http://msdn.microsoft.com/netframework/technologyinfo/redist/default.aspx).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>O Namespace Microsoft.Office.Interop.InfoPath

Embora o processo de gravação gerenciada código para uma determinada tarefa é muito semelhante à executando a mesma tarefa usando uma linguagem como o Visual Basic for Applications ou JScript, o modelo de objeto exposto ao visualizar a **Microsoft.Office.Interop.InfoPath** namespace do **Pesquisador de objetos** no Microsoft Visual Studio procura mais complexo. Isso ocorre porque a interoperabilidade com o .NET Framework requer um servidor COM expor todas as suas interfaces públicas, bem como algumas construções adicionais necessárias para o .NET Framework em si. Para obter mais informações sobre como e por que o modelo de objeto exposto por um assembly de interoperabilidade aparece mais complexo, consulte a seção "Como COM objetos são expostos para código gerenciado" do tópico [Modelos de objeto do InfoPath 2003 compatíveis](http://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx) . 
  
### <a name="using-intellisense"></a>Usando o IntelliSense

Os exemplos desta seção pressupõem que tenha estabelecido referências aos assemblies Microsoft.Office.Interop.InfoPath e Microsoft.Office.Interop.InfoPath.Xml. Para obter informações sobre como definir referências e exemplos adicionais de automação externa, consulte [os cenários de automação externa e exemplos](external-automation-scenarios-and-examples.md).
  
Antes de poder usar conclusão da instrução Microsoft IntelliSense no código de automação externa, você deve criar uma variável de objeto para uma instância da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , conforme mostrado na seguinte linha de código. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Depois de criar a variável de objeto, quando você digita o nome da variável seguido por um período, é exibida uma lista suspensa com membros da classe **Application** para selecionar. 
  
Declarar uma variável de objeto do tipo [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) para trabalhar com um formulário do InfoPath e então a inicialize abrindo o formulário da coleção [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) da variável de objeto do **aplicativo** conforme mostrado na seguinte linha de código. 
  
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

A lista de lista suspensa de conclusão de instrução do IntelliSense para membros da classe **XDocument** será exibida quando você digitar o nome da variável seguido por um ponto. 
  
Para trabalhar com o conteúdo do documento XML subjacente do formulário usando o Microsoft XML Core Services (MSXML), você deve criar uma variável do tipo [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) e, em seguida, use a propriedade [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) da classe **XDocument** para atribuir o XML Documento DOM (Object Model) do formulário para a variável. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

A lista de lista suspensa de conclusão de instrução do IntelliSense para membros da classe **IXMLDOMDocument2** será exibida quando você digitar o nome da variável seguido por um período, que permite que você use MSXML para trabalhar com o documento XML. 
  
### <a name="using-the-class-library-reference-documentation"></a>Usando a documentação de referência da biblioteca de classe

A organização do namespace [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) documentação de referência da biblioteca de classes reflete as relações entre as interfaces de co-classe e as interfaces herdadas que eles implementam. 
  
Quando você abre um tópico para uma interface de co-classe, como o [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , o link para os membros da interface co-classe após a descrição da interface no início do tópico exibe um tópico vazio. Para exibir a lista de membros que são implementadas pela interface co-classe, você deve abrir o tópico para a interface mais recente que é herdada pelo co-classe e, em seguida, abra a tabela de seus membros. Um link para a interface herdada é fornecido no início da seção comentários no tópico de interface co-classe. 
  
Quando você pressionar F1 no Editor de código do Visual Studio, o comportamento é semelhante, exceto que o membro no qual você invoca Ajuda F1 será exibido diretamente, porque geralmente estiver trabalhando com membros de uma interface. No entanto, o fato de que o membro pode ser implementado de uma interface versionada pode ser confusas na primeira vez que encontrá-lo. Por exemplo, se você digitar `myXDocument.UI.Alert` e coloque o cursor em `Alert` e pressione F1, um tópico intitulado "UI2. Método de alerta"é exibido. Isso ocorre porque o método de **alerta** é uma implementação de um membro da interface **UI2** . 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Passando parâmetros opcionais para membros do modelo de objeto do InfoPath

Se um membro de modelo de objeto do InfoPath contém um parâmetro opcional e você não especificar um valor para esse parâmetro, você deve passar o campo **Type.Missing** para esse parâmetro. Falha ao passar o campo **Type.Missing** quando um valor real for omitido resultará em um erro de compilação. Isso é verdadeiro para o código gravado em c# e Visual Basic. Por exemplo, o método [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) da interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) inclui dois parâmetros opcionais: _varEndNode_ e _varViewContext_. Uma linha de código que não especifica valores reais desses parâmetros opcionais deve se parecer com os exemplos a seguir.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Confira também

- [Exemplos e cenários de automação externa](external-automation-scenarios-and-examples.md)

