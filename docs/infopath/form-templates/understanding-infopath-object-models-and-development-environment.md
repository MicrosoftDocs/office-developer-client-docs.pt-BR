---
title: Noções básicas sobre modelos de objeto do InfoPath e ambiente de desenvolvimento
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, modelos de objeto, modelos de objeto [InfoPath 2007],InfoPath 2007, ambientes de desenvolvimento
localization_priority: Normal
ms.assetid: 29415c5b-9a42-46f4-a9e8-6a7d5bb7bdbf
description: O Microsoft InfoPath 2013 oferece suporte a dois tipos de modelos de programação para o desenvolvimento de lógica de negócios em modelos de formulário e oferece suporte à automação externa do código gerenciado.
ms.openlocfilehash: c2ed1254acf86136ab7144c732aef91ac4c14c53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303455"
---
# <a name="understanding-infopath-object-models-and-development-environment"></a>Noções básicas sobre modelos de objeto do InfoPath e ambiente de desenvolvimento

O Microsoft InfoPath 2013 oferece suporte a dois tipos de modelos de programação para o desenvolvimento de lógica de negócios em modelos de formulário e oferece suporte à automação externa do código gerenciado.
  
O InfoPath Forms Services, que está disponível no SharePoint Server 2013, fornece uma experiência de navegador da Web para preencher formulários do InfoPath. Quando implantado em um servidor que executa o InfoPath Forms Services, os formulários baseados em modelos de formulário compatíveis com navegador (.xsn) podem ser abertos em um navegador da Web de computadores que não tenham o InfoPath instalado, mas serão abertos no InfoPath quando ele for instalado. O InfoPath Forms Services também fornece um modelo de objeto para automatizar tarefas de servidor relacionadas à publicação e administração de modelos de formulário do InfoPath.
  
O InfoPath 2013 dá suporte ao ambiente de programação visual Studio 2012 e suas linguagens de programação associadas, que são descritas posteriormente neste tópico.
  
## <a name="infopath-programming-models"></a>Modelos de programação do InfoPath

O InfoPath 2013 oferece suporte a dois modelos de objeto para o desenvolvimento de lógica de negócios em modelos de formulário:
  
- O modelo de objeto de código gerenciado do InfoPath
    
- O modelo de objeto de código gerenciado compatível com o InfoPath 2003
    
Além disso, o InfoPath 2013 permite escrever código gerenciado para automatizar o InfoPath a partir de um aplicativo externo.
  
O InfoPath Forms Services fornece um modelo de objeto para automatizar tarefas de servidor, como verificar e carregar modelos de formulário do código em execução no servidor, o que requer acesso e permissões de administrador do servidor.
  
> [!NOTE]
> O InfoPath Filler 2013 pode abrir e executar soluções de modelo de formulário do InfoPath criadas em versões anteriores do InfoPath que usam lógica de negócios escrita com linguagens de script (JScript e VBScript). No entanto, o InfoPath Designer 2010 não dá suporte à criação ou modificação de modelos de formulário que usam lógica de negócios escrita com script. 
  
### <a name="the-infopath-managed-code-object-model"></a>O modelo de objeto de código gerenciado do InfoPath

O modelo de objeto de código gerenciado do InfoPath 2013 é implementado em dois assemblies, ambos denominados Microsoft.Office.Infopath.dll.
  
Uma versão do assembly implementa um subconjunto do modelo de objeto do InfoPath que contém apenas os tipos e membros suportados na lógica de negócios de modelos de formulário implantados como modelos de formulário habilitados para navegador em execução no SharePoint Server 2013 com o InfoPath Forms Services. Modelos de formulário com lógica comercial escrita contra este assembly serão abertos e executados no InfoPath Filler e em um navegador da Web.
  
A outra versão do assembly implementa tipos e membros adicionais que fornecem funcionalidades que não são suportadas na lógica de negócios de modelos de formulário habilitados para navegador. Modelos de formulário com lógica comercial escrita em relação às classes e membros adicionais neste assembly serão abertos e executados somente no editor do InfoPath Filler.
  
> [!NOTE]
> É possível gravar uma lógica condicional que usa as propriedades da classe [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) para determinar em qual ambiente (InfoPath Filler ou um navegador da Web) o modelo de formulário está sendo executado. Usando essa lógica condicional, sua lógica de negócios pode ramificar entre o código que funciona em um navegador da Web e o código escrito em classes e membros que funcionam somente no editor do InfoPath Filler. Para obter mais informações, [consulte Write Conditional Logic That Determines the Run-time Environment](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
O assembly que o InfoPath usa quando você adiciona e compila  lógica de negócios para o modelo de formulário  depende se você seleciona o modelo de formulário Formulário em Branco ou Formulário em Branco **(InfoPath Filler)** na guia Novo do Microsoft Office Backstage quando você começa a criar um novo formulário no InfoPath Designer. Forms created by using the **Blank Form** form template use the assembly that contains only the types and members that are supported in the business logic of form templates deployed as browser-enabled form templates. Forms created by using the **Blank Form** form template can be opened in both the Web browser and the InfoPath Filler. Os formulários criados usando o modelo de formulário Formulário em Branco **(InfoPath Filler)** usam o assembly que implementa tipos e membros adicionais que fornecem funcionalidades que não são suportadas na lógica comercial de modelos de formulário habilitados para navegador e só podem ser abertos no InfoPath Filler. 
  
> [!TIP]
> Depois de começar a criar um modelo de formulário, você pode alterar qual assembly é usado alterando as configurações de compatibilidade do formulário. Para fazer isso, clique **em Idioma** **na** guia Desenvolvedor e clique em **Compatibilidade** na **lista Categoria.** In the **Form type** list, select Web **Browser Form** to create a form that can be deployed as a browser-compatible form on SharePoint Server 2013. Selecione **o Formulário de Preenchimento do InfoPath** para criar um formulário que só pode ser executado no editor do InfoPath Filler. As outras seleções na **lista** de tipos de formulário oferecem suporte para compatibilidade com o InfoPath 2007 e o InfoPath 2003. 
  
As classes e os membros das duas versões desse modelo de objeto são expostos por meio do namespace [Microsoft.Office.InfoPath.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) A tabela a seguir lista onde os assemblies estão localizados nos diretórios de uma instalação do InfoPath 2013. 
  
|**Assembly**|**Descrição**|
|:-----|:-----|
|Microsoft.Office.InfoPath.dll (localizado em C:\Arquivos de Programas\Microsoft Office\Office15\InfoPathOM\InfoPathOMFormServices)  <br/> |O subconjunto do modelo de objeto que contém apenas tipos e membros que serão executados na lógica de negócios de um modelo de formulário implantado em um servidor que executa o InfoPath Forms Services.  <br/> |
|Microsoft.Office.InfoPath.dll (localizado em C:\Arquivos de Programas\Microsoft Office\Office15\InfoPathOM)  <br/> |O modelo de objeto "completo", incluindo tipos e membros que não serão executados na lógica de negócios de um modelo de formulário implantado no InfoPath Forms Services.  <br/> |
   
> [!NOTE]
> Os assemblies referenciados anteriormente nesta seção são usados no tempo de design quando você escreve e compila o código. Em tempo de executar, o assembly usado quando um modelo de formulário é aberto no InfoPath está localizado no GAC (Cache de Assembly Global) do computador no qual o InfoPath está instalado. Quando um modelo de formulário é aberto em um navegador da Web de um servidor que executa o InfoPath Forms Services, o assembly usado está localizado no servidor. 
  
O fornecimento de dois assemblies ajuda a garantir que sua lógica de negócios conterá somente chamadas para os membros do modelo de objeto apropriados para os editores de formulário com suporte (navegador da Web ou InfoPath Filler). Por exemplo, quando você edita seu código, os recursos do IntelliSense, como a conclusão da instrução e a documentação online, só serão exibidos e funcionarão com os membros apropriados do modelo de objeto para seus editores de formulário de destino.
  
Em ambas as versões do modelo de objeto de código gerenciado exposto pelo assembly Microsoft.Office.InfoPath, navegar e atualizar os armazenamentos de dados XML na lógica de negócios requer chamadas para os membros do **System.Xml. Classe XPath.XPathNavigator.** No InfoPath 2003, navegar e atualizar os armazenamentos de dados XML exige chamar membros de classes MSXML (para lógica de negócios criada usando JScript ou VBScript) ou chamando os wrappers para classes MSXML fornecidos pelo namespace **Microsoft.Office.Interop.InfoPath.SemiTrust** (para lógica de negócios criada usando C# ou Visual Basic e o Microsoft Office InfoPath 2003 Toolkit para Visual Studio .NET). 
  
O uso de membros da classe **XPathNavigator** permite que o mesmo código de lógica de negócios suporte a manipulação de DOM para modelos de formulário abertos no cliente do InfoPath e em formulários habilitados para a Web abertos do SharePoint Server 2013 com o InfoPath Forms Services em um navegador da Web. 
  
Para obter informações sobre como trabalhar com membros da classe **XPathNavigator** na lógica de negócios de modelos de formulário de código gerenciado do InfoPath, consulte Trabalhar com as classes [XPathNavigator e XPathNodeIterator .](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)
  
### <a name="the-infopath-2003-compatible-managed-code-object-model"></a>O modelo de objeto de código gerenciado compatível com o InfoPath 2003

O modelo de objeto de código gerenciado compatível com o InfoPath 2003 foi introduzido no InfoPath 2003 Service Pack 1 junto com o Microsoft Office InfoPath 2003 Toolkit para Visual Studio .NET para escrever lógica de negócios em modelos de formulário com código gerenciado. Esse modelo de objeto ainda tem suporte do InfoPath 2013 para oferecer compatibilidade com o InfoPath 2003.
  
As classes e os membros desse modelo de objeto são expostos por meio do namespace [Microsoft.Office.Interop.InfoPath.SemiTrust.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) Esse modelo de objeto é implementado no seguinte arquivo de assembly que está localizado na pasta C:\Arquivos de Programas\Microsoft Office\Office14. 
  
|**Assembly**|**Descrição**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.SemiTrust.dll  <br/> |Fornece a interop COM em relação ao modelo de objeto COM do InfoPath para a lógica de negócios do modelo de formulário escrita usando C# ou Visual Basic.  <br/> |
   
> [!NOTE]
> Embora a criação de lógica de negócios com o modelo de objeto de código gerenciado de interop COM fornecido pelo assembly Microsoft.Office.Interop.InfoPath.SemiTrust ainda seja suportada pelo InfoPath 2013, a lógica de negócios escrita usando esse modelo de objeto não é suportada para modelos de formulário habilitados para navegador implantados no SharePoint Server 2013 com InfoPath Forms Services. Os modelos de formulário habilitados para navegador devem usar o modelo de objeto de código gerenciado do InfoPath para lógica de negócios personalizada. 
  
### <a name="automating-infopath-from-managed-code"></a>Automatizando o InfoPath a partir do código gerenciado

Além de escrever lógica de negócios com código gerenciado, os desenvolvedores podem automatizar o InfoPath usando código gerenciado em execução em um aplicativo externo. Essa funcionalidade e os assemblies necessários para escrever código foram introduzidos no InfoPath 2003 Service Pack 1. Os objetos e membros para automatizar o InfoPath foram atualizados para fornecer funcionalidade adicional quando você escreve código de automação externo para o InfoPath 2013.
  
As classes e membros usados para automação externa são expostos por meio dos namespaces [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) [ eMicrosoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) externos. Os arquivos de assembly necessários para escrever código de automação estão localizados na pasta C:\Arquivos de Programas\Microsoft Office\Office14. 
  
|**Assembly**|**Descrição**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.dll  <br/> |Fornece a interop COM em relação ao modelo de objeto COM do InfoPath para código de automação externo escrito em C# ou Visual Basic.  <br/> |
|Microsoft.Office.Interop.InfoPath.Xml.dll  <br/> |Fornece a interop COM em relação ao MSXML para operações DOM XML em código de automação externo escrito em C# ou Visual Basic.  <br/> |
   
Para obter mais informações sobre os modelos de objeto fornecidos pelos namespaces **Microsoft.Office.Interop.InfoPath** e **Microsoft.Office.Interop.InfoPath.Xml,** que são usados exclusivamente para automatizar o aplicativo InfoPath usando código gerenciado de aplicativos externos, consulte a Central de Desenvolvedores do [InfoPath.](https://msdn.microsoft.com/office/aa905434.aspx)
  
### <a name="the-infopath-forms-services-object-model"></a>O modelo de objeto do InfoPath Forms Services

O modelo de objeto de código gerenciado para automatizar as tarefas de administração do InfoPath Forms Services é implementado no Microsoft.Office.InfoPath.Server.dll que está localizado na unidade \< \> :\Arquivos de Programas\Microsoft Office Server\15.0\Bin em uma instalação do Microsoft SharePoint Server 2013.
  
|**Assembly**|**Descrição**|
|:-----|:-----|
|Microsoft.Office.InfoPath.Server.dll  <br/> |O modelo de objeto para automatizar tarefas do InfoPath Forms Services, como carregar, ativar ou desativar modelos de formulário habilitados para navegador.  <br/> |
   
Para obter mais informações sobre o modelo de objeto do InfoPath Forms Services, consulte o SharePoint Server 2013 Software Developers Kit (SDK) que está disponível no MSDN.
  
## <a name="infopath-development-environment"></a>Ambiente de desenvolvimento do InfoPath

O desenvolvimento da lógica de negócios em modelos de formulário do InfoPath 2013 pode ser realizado usando o Visual Studio 2012 com o complemento [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) instalado. 
  
> [!NOTE]
> O InfoPath 2013 não oferece suporte à criação ou edição de modelos de formulário que usam lógica de negócios escrita com JScript ou VBScript, embora o InfoPath Filler suporte a abertura de modelos de formulário baseados em script criados em versões anteriores do InfoPath. 
  
## <a name="see-also"></a>Confira também

- [Passo a passo: Criando um modelo de formulário básico com código](walkthrough-creating-a-basic-form-template-with-code.md)
- [Passo a passo: criando e depurando um modelo de formulário básico usando o modelo de objeto do InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)

