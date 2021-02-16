---
title: Modelos de objeto compatíveis com o InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com infopath 2003, modelo de objeto, modelos de objeto compatíveis com InfoPath 2003, modelos de objeto [InfoPath 2003], compatível com InfoPath 2007, modelos de objeto [InfoPath 2007] compatível com InfoPath 2003
localization_priority: Normal
ms.assetid: e4511af6-d7e7-44ad-a50d-1b7ee04f8215
description: O Microsoft InfoPath foi desenvolvido como um aplicativo Component Object Model (COM) e expõe suas interfaces de programação para automação externa e script de modelo de formulário como interfaces COM.
ms.openlocfilehash: f3351a0fee6e23de0785aa28b0970c6a90361f16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303518"
---
# <a name="infopath-2003-compatible-object-models"></a>Modelos de objeto compatíveis com o InfoPath 2003

O Microsoft InfoPath foi desenvolvido como um aplicativo Component Object Model (COM) e expõe suas interfaces de programação para automação externa e script de modelo de formulário como interfaces COM. Para dar suporte à criação de soluções InfoPath que usam as linguagens de código gerenciado Visual C# e Visual Basic, o programa de instalação do InfoPath instala três interoperabilidades. Os assemblies de interoperabilidade são assemblies .NET que atuam como uma ponte entre código gerenciado e não gerenciado, mapeando membros de objeto COM para membros gerenciados .NET equivalentes. 
  
Os arquivos para os três assemblies de interoperabilidade instalados pelo InfoPath são chamados:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
Este tópico descreve o modelo de objeto exposto por meio do assembly de interoperabilidade Microsoft.Office.Interop.InfoPath.SemiTrust, que é usado exclusivamente para escrever e executar a lógica de negócio com código gerenciado de dentro de modelos de formulário do InfoPath (. xsn). 
  
Para saber mais sobre os assemblies Microsoft.Office.Interop.InfoPath e Microsoft.Office.Interop.InfoPath.Xml, consulte a documentação para os namespaces [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) e [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml). 
  
## <a name="important-installation-information"></a>Informações importantes sobre instalação

Por padrão, a opção de instalação **Típica** do programa de instalação do InfoPath instala cópias dos assemblies Microsoft.Office.Interop.InfoPath.SemiTrust e Microsoft.Office.Interop.InfoPath.Xml na pasta C:\Program Files\Microsoft Office\Office14. Os assemblies Microsoft.Office.Interop.InfoPath e Microsoft.Office.Interop.InfoPath.Xml também são instalados no Cache de Assembly Global (GAC), cujo conteúdo pode ser visto na pasta C:\WINDOWS\Assembly. 
  
Se esses assemblies não estiverem instalados, confirme que o Microsoft InfoPath foi instalado corretamente. Desde que o .NET Framework 2.0 ou posterior esteja instalado antes de executar a instalação, a opção de **Suporte de Programação do .NET** no programa de instalação do InfoPath é definida como **Executar do Meu Computador** para uma instalação **Típica** do InfoPath. Se esses assemblies de interoperabilidade não estiverem disponíveis em seu computador, você deve confirmar se o .NET Framework 2.0 ou posterior está instalado e, em seguida, executar **Adicionar ou Remover Programas** no **Painel de Controle** e definir a opção de **.Suporte de Programação do . NET** para **Executar do Meu Computador**.
  
Para saber mais sobre como baixar o .NET Framework 2.0 Redistribuível, consulte [NET Framework 2.0 Redistribuível. ](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=0856eacb-4362-4b0d-8edd-aab15c5e04f5)
  
## <a name="the-microsoftofficeinteropinfopathsemitrust-namespace"></a>O namespace Microsoft.Office.Interop.InfoPath.SemiTrust

Antes do lançamento do Microsoft Office InfoPath 2003 Service Pack 1 e do kit de ferramentas Microsoft Office InfoPath 2003 para Visual Studio .NET®, toda a lógica de programação para modelos de formulário do InfoPath era criada usando o Microsoft JScript ou o VBScript Microsoft no ambiente de desenvolvimento do Editor de Scripts Microsoft (MSE). Um script escrito no MSE é interpretado como tempo de execução e acessa o modelo de objeto COM exposto pela biblioteca de vínculo dinâmico IPEDITOR.dll.
  
Para dar suporte à criação de modelos de formulário com linguagens de código gerenciado como Visual C# e o Visual Basic para lógica de programação, uma funcionalidade foi adicionada ao InfoPath para habilitar hospedagem a Common Language Runtime (CLR), enquanto o assembly de interoperabilidade Microsoft.Office.Interop.InfoPath.SemiTrust foi criado para permitir que um código gerenciado tenha interoperabilidade com o modelo de objeto COM exposto pelo InfoPath de maneira segura. Para saber mais sobre o modelo de segurança que se aplica aos modelos de formulário de código gerenciado do InfoPath, consulte [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md). 
  
Embora o processo de escrever códigos gerenciados para uma determinada tarefa em um modelo de formulário do InfoPath seja muito semelhante a executar a mesma tarefa de programação escrevendo script, o modelo de objeto compatível com InfoPath 2003 exposto ao exibir o namespace **Microsoft.Office.Interop.InfoPath.SemiTrust** no **Pesquisador de Objetos** do Visual Studio 2012 parece muito mais complexo. Isso ocorre porque a tecnologia de interoperabilidade do .NET Framework usada para dar suporte ao modelo de objeto compatível com InfoPath 2003 requer um servidor COM para expor todas as suas interfaces públicas, bem como algumas construções adicionais exigidas pelo próprio .NET Framework. 
  
### <a name="how-com-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Como os objetos COM são expostos para o modelo de objeto compatível com InfoPath 2003

Ao trabalhar nativamente com um servidor COM usando linguagens de alto nível como JScript, VBScript, ou Visual Basic (mas não a versão .NET do Visual Basic e do Visual C#), o modelo de objeto exposto é mais simples do que as classes e interfaces COM equivalentes. Por exemplo, ao trabalhar usando essas linguagens, o objeto de **interface do usuário** do InfoPath expõe um conjunto de sete métodos, como o método **Alerta**, para exibir uma caixa de mensagem para os usuários. 
  
No entanto, as construções COM subjacentes que dão suporte ao objeto de **interface do usuário** são compostas de três entidades: duas interfaces chamadas **UI** e **UI2** e uma coclass COM que implementa os membros dessas duas interfaces. Há duas versões da **interface do usuário** porque a estrutura COM exige que a definição de uma interface permaneça fixa para manter a compatibilidade com versões anteriores de programas e componentes que requerem uma implementação dessa interface. 
  
Nesse caso, a interface **UI**, que foi definida para a versão inicial do InfoPath, fornece quatro métodos, incluindo o método **Alerta**. A interface **UI2** pode ser considerada uma segunda versão da **UI**, tendo sido definida para a versão InfoPath Service Pack 1. A interface **UI2** herda os quatro métodos da **UI** original e adiciona três novos métodos, como o método **Confirmar**. Embora você possa escrever uma linha de código em script ou em código gerenciado que chama o método **Confirmar** usando `XDocument.UI.Confirm`, o código subjacente na verdade chamará o método **Confirmar** da interface **UI2** por meio da implementação desse método na coclass COM. 
  
Ao ser exposto para script, o modelo de objeto oculta esses detalhes, mas o assembly de interoperabilidade exigido para trabalhar com um servidor COM a partir de código gerenciado expõe a coclass e ambas as interfaces publicamente. Para o único objeto de **interface do usuário** utilizado no ambiente de script MSE, o namespace **Microsoft.Office.Interop.InfoPath.SemiTrust** expõe os seguintes três itens: 
  
- Interface [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI.aspx) 
    
- Interface [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) 
    
- Interface de coclass [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) 
    
Embora todas essas três interfaces sejam expostas no **Pesquisador de Objetos** e estejam contidas na documentação da Biblioteca de Classes para o namespace, você pode trabalhar apenas com a interface de coclass **UIObject**, que implementa o objeto **UI**, e com membros da interface **UI2**, que é a versão mais recente da interface implementada pela interface de coclass **UIObject**. Para acessar a interface de coclass **UIObject** de seu objeto pai [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx), assim como em scripts, você deve usar a propriedade de acesso [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx). Exceto para algumas exceções notáveis, esse é o padrão para todos os objetos da versão original do InfoPath que foram atualizados quando o InfoPath Service Pack 1 foi lançado. 
  
Embora o padrão seja basicamente o mesmo, a situação é um pouco mais simples para objetos totalmente novos que foram adicionados no InfoPath Service Pack 1, como o objeto **Certificado**. Nesse caso, há apenas dois itens com que se preocupar: a interface de coclass [CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) e os membros da interface [Certificado](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Certificate.aspx), que é a interface mais recente e a única implementada pela interface de coclass **CertificateObject**. Da mesma forma que objetos COM do InfoPath são usados a partir de script, a propriedade de acesso [Certificado](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Certificate.aspx) é usada para acessar o objeto a partir de seu pai. 
  
Esse mesmo padrão se aplica às interfaces de conjuntos, com a exceção de que a interface de coclass para um conjunto tem "Collection" acrescentado ao respectivo nome em vez de "Object". Por exemplo, a interface de coclass para o conjunto COM **DataAdapters** é denominada [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx), e a interface que ela implementa é a interface [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdapters.aspx). Da mesma forma, a propriedade de acesso [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) do objeto pai **XDocument** é usada para acessar o conjunto. 
  
Há três exceções para essa nomenclatura padrão. As interfaces de coclass para os objetos COM **Application** e **XDocument** não têm "Object" acrescentado aos seus nomes. Seus nomes são idênticos aos objetos COM correspondentes: [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) e **XDocument**. Além disso, os nomes das interfaces implementadas pelas interfaces de coclass **Application** e **XDocument** são prefixados com o caractere sublinhado (_): [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) e [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) . A terceira exceção é o objeto COM **DataObject**. A interface de coclass para esse objeto é denominada [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx), mas, assim como outros objetos COM do InfoPath, a interface que ela implementa é a interface [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.aspx). 
  
### <a name="how-microsoft-xml-core-services-msxml-50-for-microsoft-office-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Como o Microsoft XML Core Services (MSXML) 5.0 para objetos do Microsoft Office é exposto para modelos de objeto compatíveis com InfoPath 2003

Um subconjunto dos objetos e membros do modelo de objeto fornecidos pelo Microsoft XML Core Services (MSXML), que também é um servidor COM, é encapsulado por interfaces expostas pelo assembly de interoperabilidade Microsoft.Office.Interop.InfoPath.SemiTrust. O motivo pelo qual que isso é necessário é que alguns dos membros do modelo de objeto COM do InfoPath dependem do MSXML e devem ser capazes de acessar esses membros de maneira segura. Os nomes dos interfaces no namespace **Microsoft.Office.Interop.InfoPath.SemiTrust** que encapsula os objetos e membros do modelo de objeto do MSXML são os mesmos nomes expostos pelo servidor COM do MSXML. Na maioria dos casos, esses nomes recebem o prefixo "IXMLDOM", pois são usados para trabalhar com o Modelo de Objeto de Documento XML (DOM). Por exemplo, a propriedade [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) da interface **XDocument**, que é usada para retornar uma referência para um documento XML subjacente de um formulário, retorna a interface [IXMLDOMDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.IXMLDOMDocument.aspx), que é encapsulada pela assembly de interoperabilidade Microsoft.Office.Interop.InfoPath.SemiTrust. Você chama e usa os membros da interface **IXMLDOMDocument** praticamente da mesma forma como usaria um script em modelos de formulário que não usam código gerenciado. 
  
Para saber mais sobre como usar membros do Microsoft XML Core Services (MSXML) para modelos de objeto do Microsoft Office em modelos de formulário de código gerenciado, consulte [Trabalhando com MSXML e System.Xml usando o modelo de objeto do InfoPath 2003](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md).
  
### <a name="using-intellisense"></a>Como usar o IntelliSense

Para a maior parte dos códigos que você escreve com base no modelo de objeto compatível com InfoPath 2003 em um modelo de formulário de código gerenciado, você usará as variáveis `thisXDocument` e `thisApplication` que são inicializadas no método do `_Startup` arquivo de classe padrão FormCode.cs ou FormCode.vb. Você pode usar as variáveis `thisXDocument` e `thisApplication` para acessar os membros das interfaces de coclass [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) e [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx). Depois de digitar o nome de uma dessas variáveis seguido por um ponto, o preenchimento de instruções do IntelliSense exibirá os membros da lista da interface do coclass correspondente. Você poderá continuar dessa maneira para acessar o membro do modelo de objeto com que deseja trabalhar. 
  
Veja a seguir um exemplo simples que usa a variável `thisXDocument` para acessar o método [Alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) para exibir a versão do aplicativo InfoPath usando a propriedade [Versão](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) acessada a partir da variável `thisApplication`. 
  
```cs
thisXDocument.UI.Alert(thisApplication.Version);
```

```vb
thisXDocument.UI.Alert(thisApplication.Version)
```

### <a name="using-the-class-library-reference-documentation"></a>Usar a documentação de referência da Biblioteca de Classes

A organização da documentação de referência da Biblioteca de Classes do namespace **Microsoft.Office.Interop.InfoPath.SemiTrust** reflete a relação entre as interfaces de coclass e as interfaces herdadas que elas implementam. Isso é descrito na seção anterior deste tópico "Como objetos COM são expostos para código gerenciado". 
  
Embora a organização e a nomenclatura da documentação de referência do namespace **Microsoft.Office.Interop.InfoPath.SemiTrust** possam parecer confusas a princípio, os tópicos são basicamente organizados da mesma forma que na Referência do Modelo de Objeto do InfoPath que faz parte da Referência do Desenvolvedor do InfoPath incluída no InfoPath. Com exceção de tópicos para as interfaces **Application** e **XDocument**, todos os tópicos referentes a interfaces de coclasse COM remetem aos tópicos "Object" e "Collection" equivalentes da referência de script do InfoPath. Por exemplo, os tópicos "Interface UIObject" e "Interface WindowsCollection " da documentação de referência do namespace **Microsoft.Office.Interop.InfoPath.SemiTrust** correspondem a conteúdo semelhante nos tópicos "UIObject" e "Windows Collection" na referência de script da Referência do Modelo de Objeto do InfoPath. 
  
No entanto, o link para os membros da interface de coclass que acompanha a descrição da interface no início do tópico exibe um tópico vazio. Para exibir a lista de membros implementados pela interface de coclass, você deve abrir o tópico da interface mais recente herdada pela coclass e, em seguida, abrir a tabela dos seus membros. Um link para a interface herdada é fornecido no início da seção Comentários no tópico da interface de coclass.
  
Quando você pressiona F1 no Editor de código, o comportamento é semelhante, com a exceção de que o membro para o qual você invocar a Ajuda F1 será exibido diretamente, uma vez que você normalmente estará trabalhando com membros de uma interface. No entanto, o fato de um membro poder se implementado de uma interface com versão pode parece confuso na primeira vez que você o encontrar. Por exemplo, se você digitar `thisXDocument.UI.Alert`, posicionar o cursor sobre `Alert` e pressionar F1, um tópico intitulado "Método de Alerta UI2"é exibido. Isso ocorre porque o método **Alerta** é uma implementação de um membro da interface **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Transferindo parâmetros opcionais para membros de modelos de objeto do InfoPath

Se um membro de modelo de objeto compatível com InfoPath 2003 contiver um parâmetro opcional, e você não especificar um valor para esse parâmetro, você deve transferir o campo **Type.Missing** para esse parâmetro. Não transferir o campo **Type.Missing** quando um valor real for omitido resultará em um erro de compilação. Isso se aplica a códigos escritos em Visual C# e Visual Basic. Por exemplo, o método [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) da interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) inclui dois parâmetros opcionais: _varEndNode_ e _varViewContext_. Uma linha de código que não especifique valores reais para esses parâmetros opcionais deve parecer com os exemplos a seguir.
  
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

### <a name="about-common-language-specification-compliance"></a>Sobre conformidade de especificação de linguagens comuns

Internamente, cada interface e membro do assembly Microsoft.Office.Interop.InfoPath.SemiTrust tem seu atributo **CLSCompliant** definido para **false**. Mas, como a documentação de referência é parcialmente gerada usando **System.Reflection**, a descrição de cada interface e membro tem a frase "Esta interface/método/propriedade não é compatível com CLS" adicionada a ela. No entanto, a maioria das interfaces e dos membros do namespace [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) é, na verdade, compatível com CLS. 
  
## <a name="see-also"></a>Confira também

- [Tarefas comuns de desenvolvimento de modelo de formulário usando o modelo de objeto InfoPath 2003](common-tasks-for-developing-form-templates-using-infopath-object-model.md)
- [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
- [Criar modelos de formulário usando o modelo de objeto do InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
- [Compreender o modelo de objeto do InfoPath 2003](understanding-the-infopath-2003-object-model.md)

