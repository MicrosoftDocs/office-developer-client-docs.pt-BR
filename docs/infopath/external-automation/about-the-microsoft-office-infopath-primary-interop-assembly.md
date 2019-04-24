---
title: Sobre o assembly de interoperabilidade primário do InfoPath do Microsoft Office
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2007, assembly de interoperabilidade primário, assembly de interoperabilidade primário do InfoPath, PIAs [InfoPath 2007], assemblies de interoperabilidade primário [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Para dar suporte à criação de soluções do InfoPath que usem linguagens de código gerenciado, como Visual C# e Visual Basic, a opção de suporte à programação do .NET no programa de instalação do InfoPath instala três assemblies de interoperabilidade.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310133"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Sobre o assembly de interoperabilidade primário do InfoPath do Microsoft Office

O aplicativo InfoPath é criado como um aplicativo de modelo de objeto de componente (COM) que expõe suas interfaces de programação para automação externa como interfaces COM. Para dar suporte à criação de soluções do InfoPath que usem linguagens de código gerenciado, como Visual C# e Visual Basic, a opção de **suporte à programação do .net** no programa de instalação do InfoPath instala três assemblies de interoperabilidade. Os assemblies de interoperabilidade são assemblies .NET que atuam como uma ponte entre código gerenciado e não gerenciado, mapeando membros de objeto COM para membros gerenciados .NET equivalentes. 
  
Os arquivos para os três assemblies de interoperabilidade instalados pelo InfoPath são chamados:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
Este tópico discute o modelo de objeto exposto por meio do assembly de interoperabilidade Microsoft. Office. Interop. InfoPath, que é usado exclusivamente para o código de automação externa. Para obter informações sobre o assembly Microsoft. Office. Interop. InfoPath. SemiTrust, que é usado exclusivamente para gravar e executar o código gerenciado que é executado de dentro dos modelos de formulário do InfoPath (. xsn), confira [modelos de objeto compatíveis com o infopath 2003](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Informações importantes de instalação

A opção de instalação padrão do programa de instalação do InfoPath instala o assembly Microsoft. Office. Interop. InfoPath no cache de assembly global (GAC), o conteúdo do qual pode ser exibido na pasta C:\Windows\Assembly (ou no C:\Windows\assembly\GAC_ MSIL ao exibir diretamente o sistema de arquivos). Esse assembly é conhecido como o assembly de interOperabilidade primário do Microsoft Office InfoPath e é freqüentemente usado em conjunto com o assembly Microsoft. Office. Interop. InfoPath. xml, que também é instalado no GAC, para automatizar o aplicativo InfoPath do aplicativos externos que usam código gerenciado. Para obter informações sobre o assembly Microsoft. Office. Interop. InfoPath. xml, consulte [sobre o assembly de InteroperaBILIDADE XML do InfoPath](about-the-infopath-xml-interop-assembly.md).
  
Se o assembly Microsoft. Office. Interop. InfoPath não estiver visível no GAC, você deverá confirmar que o InfoPath foi instalado corretamente. Por padrão, a opção de **suporte à programação do .net** no programa de instalação está definida para **executar a partir do meu computador** , desde que o .NET Framework 1,1 Redistributable, o .NET Framework 1,1 Software Development Kit (SDK) ou uma versão posterior do .NET Framework é instalado antes de executar a instalação. Se esses assemblies de interoperabilidade não estiverem disponíveis em seu computador, você deve confirmar se o .NET Framework 1,1 ou posterior está instalado e, em seguida, usar **programas e recursos** no **painel de controle** para alterar a configuração configurando a **programação do .net **Opção de suporte no **Microsoft Office InfoPath** para **executar a partir de meu computador**.
  
Para obter informações sobre como baixar o .NET Framework 1,1 Redistributable, consulte [.NET framework 1,1 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=26).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>O namespace Microsoft. Office. Interop. InfoPath

Embora o processo de gravação de código gerenciado para uma determinada tarefa seja muito semelhante à execução da mesma tarefa usando uma linguagem como Visual Basic for Applications ou JScript, o modelo de objeto exposto ao exibir o **Microsoft. Office. Interop. InfoPath** o namespace do **pesquisador de objetos** no Microsoft Visual Studio parece mais complexo. Isso ocorre porque a interoperabilidade com o .NET Framework requer um servidor COM para expor todas as interfaces públicas, bem como algumas construções adicionais necessárias para o próprio .NET Framework. Para obter mais informações sobre como e por que o modelo de objeto exposto por um assembly de interoperabilidade parece mais complexo, consulte a seção "como os objetos COM são expostos ao código gerenciado" do tópico [modelos de objeto compatíveis com o InfoPath 2003](../form-templates/infopath-2003-compatible-object-models.md) . 
  
### <a name="using-intellisense"></a>Como usar o IntelliSense

Os exemplos nesta seção supõem que você tenha estabelecido referências aos assemblies Microsoft. Office. Interop. InfoPath e Microsoft. Office. Interop. InfoPath. xml. Para obter informações sobre como definir referências e exemplos adicionais de automação externa, consulte [cenários e exemplos de automação externa](external-automation-scenarios-and-examples.md).
  
Antes de poder usar a conclusão da instrução Microsoft IntelliSense no código de automação externo, você deve criar uma variável de objeto para uma instância da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , conforme mostrado na seguinte linha de código. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Após criar a variável de objeto, quando você digita o nome da variável seguido por um ponto, uma lista suspensa é exibida com membros da classe de **aplicativo** a ser selecionada. 
  
Para trabalhar com um formulário do InfoPath, declare uma variável de objeto do tipo [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) e, em seguida, inicialize-a abrindo o formulário da coleção [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) da variável de objeto **Application** , conforme mostrado na linha de código a seguir. 
  
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

A lista suspensa de conclusão da instrução IntelliSense para os membros da classe **XDocument** será exibida quando você digitar o nome da variável seguida por um ponto. 
  
Para trabalhar com o conteúdo do documento XML subjacente para o formulário usando o Microsoft XML Core Services (MSXML), você deve criar uma variável do tipo [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) e, em seguida, usar a propriedade [dom](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) da classe **XDocument** para atribuir o XML Modelo de objeto de documento (DOM) do formulário para essa variável. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

A lista suspensa de conclusão da instrução IntelliSense para os membros da classe **IXMLDOMDocument2** será exibida quando você digitar o nome da variável seguida por um ponto, o que permite usar o MSXML para trabalhar com o documento XML. 
  
### <a name="using-the-class-library-reference-documentation"></a>Usando a documentação de referência da biblioteca de classes

A organização da documentação de referência da biblioteca de classes do namespace [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) reflete as relações entre interfaces de coclass e as interfaces herdadas que elas implementam. 
  
Quando você abre um tópico para uma interface de coclass, como [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , o link para os membros da interface de coclass após a descrição da interface no início do tópico exibe um tópico vazio. Para exibir a lista de membros implementados pela interface de coclass, você deve abrir o tópico da interface mais recente herdada pela coclass e, em seguida, abrir a tabela dos seus membros. Um link para a interface herdada é fornecido no início da seção Comentários no tópico da interface de coclass. 
  
Quando você pressiona F1 no editor de código do Visual Studio, o comportamento é semelhante, exceto pelo fato de que o membro no qual você invoca a ajuda F1 será exibido diretamente, porque você está mais trabalhando com membros de uma interface. No entanto, o fato de um membro poder se implementado de uma interface com versão pode parece confuso na primeira vez que você o encontrar. Por exemplo, se você digitar `myXDocument.UI.Alert`, posicionar o cursor sobre `Alert` e pressionar F1, um tópico intitulado "Método de Alerta UI2"é exibido. Isso ocorre porque o método **Alerta** é uma implementação de um membro da interface **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Passando parâmetros opcionais para membros do modelo de objeto do InfoPath

Se um membro do modelo de objeto do InfoPath contiver um parâmetro opcional e você não especificar um valor para esse parâmetro, você deverá passar o **tipo. campo ausente** para esse parâmetro. Não transferir o campo **Type.Missing** quando um valor real for omitido resultará em um erro de compilação. Isso se aplica ao código escrito em C# e Visual Basic. Por exemplo, o método [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) da interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) inclui dois parâmetros opcionais: _varEndNode_ e _varViewContext_. Uma linha de código que não especifique valores reais para esses parâmetros opcionais deve parecer com os exemplos a seguir.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Confira também

- [Cenários e exemplos de automação externa](external-automation-scenarios-and-examples.md)

