---
title: Modelos de objeto compatível do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- objeto de modelos de formulário compatíveis com 2003 do InfoPath, modelo, modelo de objeto do InfoPath 2003 compatíveis, modelos de objeto [InfoPath 2003], compatível com o InfoPath 2007, modelos de objeto [InfoPath 2007], compatível com o InfoPath 2003
localization_priority: Normal
ms.assetid: e4511af6-d7e7-44ad-a50d-1b7ee04f8215
description: Microsoft InfoPath está escrito como um aplicativo (COM Component Object Model) e expõe suas interfaces de programação para automação externa e o script de modelo de formulário como interfaces COM.
ms.openlocfilehash: 09ba36b39e520629764bd57a623e8fb490a63a89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765651"
---
# <a name="infopath-2003-compatible-object-models"></a>Modelos de objeto compatível do InfoPath 2003

Microsoft InfoPath está escrito como um aplicativo (COM Component Object Model) e expõe suas interfaces de programação para automação externa e o script de modelo de formulário como interfaces COM. Para oferecer suporte a criação de soluções do InfoPath que usam o Visual c# e Visual Basic linguagens de código gerenciado, o programa de instalação do InfoPath instala os assemblies de interoperabilidade três. Os assemblies de interoperabilidade são assemblies .NET que agem como uma ponte entre código gerenciado e, mapeamento de membros do objeto COM ao equivalente .NET gerenciado membros. 
  
Os arquivos para os assemblies de interoperabilidade três instalados pelo InfoPath são nomeados:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
Este tópico aborda o modelo de objeto exposto por meio do assembly de interoperabilidade SemiTrust é usado exclusivamente para escrever e executando lógica de negócios de código gerenciado do dentro de modelos de formulário do InfoPath (. xsn). 
  
Para obter informações sobre os assemblies Microsoft.Office.Interop.InfoPath e Microsoft.Office.Interop.InfoPath.Xml, consulte a documentação para o [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.aspx) e [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) namespaces. 
  
## <a name="important-installation-information"></a>Informações importantes sobre instalação

Por padrão, a opção de instalação **típica** do programa de instalação do InfoPath instala cópias dos assemblies SemiTrust e Microsoft.Office.Interop.InfoPath.Xml no C:\Program Files\Microsoft Office Pasta do Office14. Os assemblies Microsoft.Office.Interop.InfoPath e Microsoft.Office.Interop.InfoPath.Xml também são instalados no Global Assembly Cache (GAC), o conteúdo dos quais pode ser exibido na pasta c:\WINDOWS\Assembly.. 
  
Se esses assemblies não estiverem instalados, você deve confirmar que o Microsoft InfoPath foi instalado corretamente. Conforme longos como o .NET Framework 2.0 ou posterior é instalado antes de executar a instalação, a opção de **Suporte à programação do .NET** no programa de instalação do InfoPath é definida para **Executar de Meu computador** para uma instalação **típica** do InfoPath. Se esses assemblies de interoperabilidade não estão disponíveis no seu computador, você deve confirmar que o .NET Framework 2.0 ou posterior é instalado e em seguida execute **Adicionar ou remover programas** no **Painel de controle** de e defina o **Suporte à programação do .NET** opção para **Executar de Meu computador**.
  
Para obter informações sobre como baixar o redistribuível do .NET Framework 2.0, consulte [redistribuível do .NET Framework 2.0.](http://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=0856eacb-4362-4b0d-8edd-aab15c5e04f5)
  
## <a name="the-microsoftofficeinteropinfopathsemitrust-namespace"></a>O namespace SemiTrust

Antes do lançamento do Microsoft Office InfoPath 2003 Service Pack 1 e o Microsoft Office InfoPath 2003 Toolkit para o Visual Studio® .NET, toda a lógica de programação para modelos de formulário do InfoPath foi criada usando o Microsoft JScript ou Microsoft VBScript escritos na Ambiente de desenvolvimento do Editor de scripts Microsoft (MSE). Script gravado no MSE será interpretado em tempo de execução e acessa o modelo de objeto COM expostos pela biblioteca de vínculo dinâmico IPEDITOR.dll.
  
Para oferecer suporte a criação de modelos de formulário que usam os idiomas de código gerenciado, como o Visual c# e Visual Basic para lógica de programação, funcionalidade foi adicionada ao InfoPath para habilitar o common language runtime (CLR) de hospedagem e o Assembly de interoperabilidade SemiTrust foi criado para permitir que o código gerenciado interoperar com o modelo de objeto COM expostos pelo InfoPath de forma segura. Para obter informações sobre o modelo de segurança que se aplica a modelos de formulário de código gerenciado do InfoPath, consulte [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md). 
  
Embora o processo de gravação gerenciada código para uma determinada tarefa em um modelo de formulário do InfoPath é muito semelhante à executando a mesma tarefa de programação gravando um script, o modelo de objeto compatível com o InfoPath 2003 exposto ao visualizar a ** SemiTrust** namespace do **Pesquisador de objetos** no Visual Studio 2012 se parece muito mais complexa. Isso ocorre porque a tecnologia de interoperabilidade do .NET Framework usada para dar suporte ao modelo de objeto compatível com o InfoPath 2003 requer um servidor COM expor todas as suas interfaces públicas, bem como algumas construções adicionais necessárias para o próprio .NET Framework. 
  
### <a name="how-com-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Como os objetos COM são expostos para o modelo de objeto compatível do InfoPath 2003

Quando estiver trabalhando nativamente com um servidor COM de idiomas de alto nível, como o JScript, VBScript, ou do Visual Basic (mas não a versão de .NET do Visual Basic e Visual c#), o modelo de objeto que é exposto é mais simples do que as interfaces e classes de COM subjacentes. Por exemplo, quando trabalhando desses idiomas, o InfoPath **UI** expõe objeto um conjunto de sete métodos, como o método de **alerta** para exibir uma mensagem de caixa aos usuários. 
  
No entanto, as construções COM subjacente que suportam o objeto de **interface do usuário** serão realmente compostas por três entidades: duas interfaces denominados **UI** e **UI2**e uma co-classe COM que implementa os membros dessas duas interfaces. Há duas versões da interface **do usuário** porque o framework COM requer a definição de uma interface para permanecem corrigidas para manter a compatibilidade com versões anteriores de programas e componentes que chamar uma implementação dessa interface. 
  
Nesse caso, a interface **do usuário** , que foi definida para a versão inicial do InfoPath, oferece quatro métodos, incluindo o método de **alerta** . A interface **UI2** pode ser considerada uma segunda versão da interface **do usuário** , e ela foi definida para a versão do InfoPath Service Pack 1. A interface **UI2** herda os quatro métodos da interface da **interface do usuário** original e adiciona três novos métodos, como o método **Confirm** . Embora você pode escrever uma linha de código no script ou código gerenciado que chama o método **Confirm** utilizando `XDocument.UI.Confirm`, a base de código realmente é chamar o método **Confirm** da interface **UI2** contra a implementação do método no co-classe COM. 
  
O modelo de objeto conforme ele é exposto a scripting oculta esses detalhes, mas o assembly de interoperabilidade necessários para trabalhar com um servidor COM a partir de código gerenciado expõe o co-classe e ambas as interfaces publicamente. Para o objeto de **interface do usuário** único usado no ambiente de script do MSE, o namespace **SemiTrust** expõe os três itens a seguintes: 
  
- Interface [do usuário](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI.aspx) 
    
- Interface de [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) 
    
- Interface de co-classe [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) 
    
Embora todos os três dessas interfaces são expostos no **Pesquisador de objetos** e estão contidos na documentação de biblioteca de classes para o namespace, você só funciona com a interface de co-classe **UIObject** , que implementa o objeto de **interface do usuário** , e com os membros da interface **UI2** , que é a versão mais atual da interface do que é implementada pela interface co-classe **UIObject** . Para acessar a interface de co-classe **UIObject** de seu objeto [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) pai, assim como em script, você deve usar a propriedade de acessador de [interface do usuário](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) . Exceto para algumas exceções notáveis, esse é o padrão para todos os objetos da versão original do InfoPath que foram atualizados quando o InfoPath Service Pack 1 foi lançado. 
  
Enquanto o padrão é basicamente o mesmo, a situação é um pouco mais simples para os objetos inteiramente novos que foram adicionados no Service Pack 1 do InfoPath, como o objeto de **certificado** . Nesse caso, existem apenas dois itens a se preocupar com: a interface de co-classe [CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) e os membros da interface de [certificado](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Certificate.aspx) , que é a mais recente e apenas interface implementada pelo **CertificateObject** interface de co-classe. Assim como ao usar objetos COM do InfoPath do script, a propriedade de acessador de [certificado](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Certificate.aspx) é usada para acessar o objeto de seu pai. 
  
Esse mesmo padrão se aplica às interfaces para coleções, exceto a interface de co-classe para um conjunto possui "Coleção" acrescentada ao seu nome, em vez de "Objeto". Por exemplo, a interface co-classe para a coleção COM **DataAdapters** é chamada [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) e a interface que ele implementa é aquela [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdapters.aspx) . Da mesma forma, a propriedade de acessador [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) do objeto pai **XDocument** é usada para acessar a coleção. 
  
Há três exceções para este padrão de nomenclatura. As interfaces co-classe para os objetos COM **aplicativos** e **XDocument** não têm "Objeto" acrescentado aos seus nomes. Seus nomes são idênticos aos seus objetos COM correspondentes: [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) e **XDocument**. Além disso, os nomes das interfaces de co-classe **XDocument** da interfaces implementadas pelo **aplicativo** e são prefixados com o caractere de sublinhado (_): [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) e [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) . A terceira exceção é o objeto COM **DataObject** . A interface co-classe para este objeto é chamada [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) , mas, assim como outros objetos COM do InfoPath, a interface que ele implementa é o [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.aspx) . 
  
### <a name="how-microsoft-xml-core-services-msxml-50-for-microsoft-office-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Como o Microsoft XML Core Services (MSXML) 5.0 para objetos do Microsoft Office são expostas para o modelo de objeto compatível do InfoPath 2003

Membros do modelo de objeto fornecido pelo Microsoft XML Core Services (MSXML), que também é um servidor COM, e um subconjunto dos objetos devem ser quebradas por interfaces expostas pelo assembly de interoperabilidade SemiTrust. A razão que isso é necessário é que alguns dos membros do modelo de objeto COM do InfoPath depender MSXML e deve ser capaz de acessar os membros de uma forma segura. Membros do modelo de objeto do MSXML e os nomes das interfaces no namespace **SemiTrust** que envolvem os objetos são os mesmos nomes expostos pelo servidor MSXML COM. Na maioria dos casos, esses nomes são prefixados com "IXMLDOM", porque eles são usados para trabalhar com o XML DOM Document Object Model (). Por exemplo, a propriedade [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) da interface **XDocument** , que é usada para retornar uma referência ao documento XML subjacente de um formulário, retorna a interface de [IXMLDOMDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.IXMLDOMDocument.aspx) é disposta pelo Assembly de interoperabilidade SemiTrust. Você pode chamar e use os membros da interface **IXMLDOMDocument** basicamente da mesma maneira como quando usando o script em modelos de formulário que não usam o código gerenciado. 
  
Para obter mais informações sobre como usar os membros da Microsoft XML Core Services (MSXML) para modelo de objeto do Microsoft Office em modelos de formulário de código gerenciado, consulte [Trabalhando com MSXML e System. XML usando o modelo de objeto do InfoPath 2003](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md).
  
### <a name="using-intellisense"></a>Usando o IntelliSense

Para a maioria do código que você pode escrever em relação ao modelo de objeto compatível com o InfoPath 2003 em um modelo de formulário de código gerenciado, você usará o `thisXDocument` e `thisApplication` variáveis que são inicializados na `_Startup` método do arquivo de classe de FormCode.cs ou FormCode.vb padrão. Você pode usar o `thisXDocument` e `thisApplication` variáveis para acessar os membros do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) e [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) coclass interfaces. Depois de digitar o nome de qualquer variável seguido por um período, conclusão da instrução IntelliSense exibirá os membros da lista da interface co-classe correspondente. Você pode continuar dessa maneira para acessar o membro de modelo de objeto que você deseja trabalhar com. 
  
A seguir mostra um exemplo simples que usa o `thisXDocument` variável para acessar o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) para exibir a versão do aplicativo InfoPath, usando a propriedade [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) acessada a partir do `thisApplication` variável. 
  
```cs
thisXDocument.UI.Alert(thisApplication.Version);
```

```vb
thisXDocument.UI.Alert(thisApplication.Version)
```

### <a name="using-the-class-library-reference-documentation"></a>Usando a documentação de referência da biblioteca de classes

A organização do namespace **SemiTrust** documentação de referência da biblioteca de classes reflete as relações entre as interfaces de co-classe e as interfaces herdadas que eles implementam. Isso é descrito na seção "Como COM objetos são expostos para código gerenciado", anteriormente neste tópico. 
  
Embora a documentação de referência de organização e nomeação do namespace **SemiTrust** aparece confusas em um primeiro momento, os tópicos estão organizados basicamente da mesma maneira como a referência do modelo de objeto do InfoPath é parte da referência do desenvolvedor do InfoPath, o que está incluída com o InfoPath. Com exceção de tópicos do **aplicativo** e interfaces **XDocument** , todos os tópicos de interface co-classe COM mapeiam aos equivalentes "Do objeto" e "Conjunto" tópicos do InfoPath referência de script. Por exemplo, "UIObject Interface" e os tópicos em "WindowsCollection Interface" da documentação de referência do namespace **SemiTrust** correspondem ao conteúdo semelhante na "Objeto UI" e "Coleção Windows" tópicos da referência de modelo de objeto do InfoPath referência de script. 
  
No entanto, o link para os membros da interface co-classe após a descrição da interface no início do tópico exibe um tópico vazio. Para exibir a lista de membros que são implementadas pela interface co-classe, você deve abrir o tópico para a interface mais recente que é herdada pelo co-classe e, em seguida, abra a tabela de seus membros. Um link para a interface herdada é fornecido no início da seção comentários no tópico de interface co-classe.
  
Quando você pressionar F1 no Editor de código, o comportamento é semelhante, exceto que o membro no qual você invoca Ajuda F1 será exibido diretamente, porque geralmente estiver trabalhando com membros de uma interface. No entanto, o fato de que o membro pode ser implementado de uma interface versionada pode ser confusas na primeira vez que encontrá-lo. Por exemplo, se você digitar `thisXDocument.UI.Alert` e coloque o cursor em `Alert` e pressione F1, um tópico intitulado "UI2. Método de alerta"é exibido. Isso ocorre porque o método de **alerta** é uma implementação de um membro da interface **UI2** . 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Passando parâmetros opcionais para membros do modelo de objeto do InfoPath

Se um membro de modelo de objeto compatível com o InfoPath 2003 contém um parâmetro opcional e você não especificar um valor para esse parâmetro, você deve passar o campo **Type.Missing** para esse parâmetro em vez disso. Falha ao passar o campo **Type.Missing** quando um valor real for omitido resultará em um erro de compilação. Isso é verdadeiro para códigos escritos em Visual c# e Visual Basic. Por exemplo, o método [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) da interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) inclui dois parâmetros opcionais: _varEndNode_ e _varViewContext_. Uma linha de código que não especifica valores reais desses parâmetros opcionais deve se parecer com os exemplos a seguir.
  
```cs
IXMLDOMNode group1 = 
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1");
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
Dim group1 As IXMLDOMNode = _
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1")
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

### <a name="about-common-language-specification-compliance"></a>Sobre conformidade da especificação de linguagem comum

Internamente, cada interface e o membro no assembly SemiTrust tem seu atributo **CLSCompliant** definido como **false**. Como a documentação de referência é gerada usando o **System. Reflection**em parte, a descrição de cada interface e o membro tem a frase "essa interface/método/propriedade não é compatível com CLS" acrescentado a ele. No entanto, a maioria das interfaces e membros do namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) realmente são compatível com CLS. 
  
## <a name="see-also"></a>Confira também

- [Tarefas comuns para o desenvolvimento de modelos de formulário usando o modelo de objeto do InfoPath 2003](common-tasks-for-developing-form-templates-using-infopath-object-model.md)
- [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
- [Criando modelos de formulário usando o modelo de objeto do InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
- [Compreendendo o modelo de objeto do InfoPath 2003](understanding-the-infopath-2003-object-model.md)

