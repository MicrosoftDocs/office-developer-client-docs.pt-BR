---
title: Noções básicas sobre o ambiente de desenvolvimento e modelos de objeto do InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, modelos de objeto, modelos de objeto [InfoPath 2007], InfoPath 2007, ambientes de desenvolvimento
localization_priority: Normal
ms.assetid: 29415c5b-9a42-46f4-a9e8-6a7d5bb7bdbf
description: O Microsoft InfoPath 2013 oferece suporte a dois tipos de modelos de programação para desenvolver a lógica de negócios em modelos de formulário e oferece suporte à automação externa do código gerenciado.
ms.openlocfilehash: c2ed1254acf86136ab7144c732aef91ac4c14c53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303455"
---
# <a name="understanding-infopath-object-models-and-development-environment"></a>Noções básicas sobre o ambiente de desenvolvimento e modelos de objeto do InfoPath

O Microsoft InfoPath 2013 oferece suporte a dois tipos de modelos de programação para desenvolver a lógica de negócios em modelos de formulário e oferece suporte à automação externa do código gerenciado.
  
O InfoPath Forms Services, disponível no SharePoint Server 2013, oferece uma experiência de navegador da Web para o preenchimento de formulários do InfoPath. Quando implantado em um servidor que executa o InfoPath Forms Services, os formulários baseados em modelos de formulário compatíveis com o navegador (. xsn) podem ser abertos em um navegador da Web de computadores que não têm o InfoPath instalado, mas serão abertos no InfoPath quando ele for instalado. O InfoPath Forms Services também fornece um modelo de objeto para automatizar tarefas de servidor relacionadas à publicação e à administração do modelo de formulário do InfoPath.
  
O InfoPath 2013 oferece suporte ao ambiente de programação do Visual Studio 2012 e às linguagens de programação associadas, que são descritas posteriormente neste tópico.
  
## <a name="infopath-programming-models"></a>Modelos de programação do InfoPath

O InfoPath 2013 oferece suporte a dois modelos de objeto para o desenvolvimento de lógica de negócios em modelos de formulário:
  
- O modelo de objeto de código gerenciado do InfoPath
    
- O modelo de objeto de código gerenciado compatível com o InfoPath 2003
    
Além disso, o InfoPath 2013 permite escrever código gerenciado para automatizar o InfoPath de um aplicativo externo.
  
O InfoPath Forms Services fornece um modelo de objeto para automatizar tarefas de servidor, como verificar e carregar modelos de formulário de código em execução no servidor, o que exige permissões e acesso de administrador de servidor.
  
> [!NOTE]
> O InfoPath Filler 2013 pode abrir e executar soluções de modelo de formulário do InfoPath criadas em versões anteriores do InfoPath que usam a lógica de negócios escrita com linguagens de script (JScript e VBScript). No enTanto, o InfoPath Designer 2010 não suporta a criação ou modificação de modelos de formulário que usam lógica de negócios escrita com script. 
  
### <a name="the-infopath-managed-code-object-model"></a>O modelo de objeto de código gerenciado do InfoPath

O modelo de objeto de código gerenciado do InfoPath 2013 é implementado em dois assemblies, ambos denominados Microsoft. Office. InfoPath. dll.
  
Uma versão do assembly implementa um subconjunto do modelo de objeto do InfoPath que contém apenas os tipos e membros suportados na lógica de negócios dos modelos de formulário implantados como modelos de formulário habilitados para navegador em execução no SharePoint Server 2013 com InfoPath Forms Services. Modelos de formulário com lógica de negócios gravada nesse assembly serão abertos e executados no InfoPath Filler e em um navegador da Web.
  
A outra versão do assembly implementa outros tipos e membros que fornecem funcionalidade que não é suportada na lógica de negócios dos modelos de formulário habilitados para navegador. Modelos de formulário com lógica de negócios gravadas em relação às classes e membros adicionais neste assembly serão abertos e executados somente no editor de preenchimento do InfoPath.
  
> [!NOTE]
> É possível gravar lógica condicional que usa as propriedades da classe [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) para determinar qual ambiente (InfoPath Filler ou um navegador da Web) o modelo de formulário está sendo executado no. Usando essa lógica condicional, sua lógica de negócios pode ramificar entre o código que funciona em um navegador da Web e código escrito em relação a classes e membros que funcionam somente no editor de preenchimento do InfoPath. Para obter mais informações, consulte [Write Conditional Logic que determina o ambiente de tempo de execução](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
O assembly que o InfoPath usa quando você adiciona e compila a lógica de negócios para o modelo de formulário depende de você selecionar o modelo de formulário **formulário em branco** ou **formulário em branco (InfoPath Filler)** na **nova** guia do Microsoft Office Backstage quando Você começa a criar um novo formulário no designer do InfoPath. Os formulários criados com o uso do modelo de formulário de **formulário em branco** usam o assembly que contém apenas os tipos e membros suportados na lógica de negócios dos modelos de formulário implantados como modelos de formulário habilitados para navegador. Formulários criados com o uso do modelo de formulário de **formulário em branco** podem ser abertos no navegador da Web e no InfoPath Filler. Formulários criados usando o **formulário em branco (InfoPath Filler)** modelo de formulário use o assembly que implementa tipos adicionais e membros que fornecem funcionalidade que não é suportada na lógica de negócios dos modelos de formulário habilitados para navegador e só pode ser aberto no InfoPath Filler. 
  
> [!TIP]
> Depois de começar a criar um modelo de formulário, você pode alterar qual assembly é usado alterando as configurações de compatibilidade de formulários. Para fazer isso, clique em **idioma** na guia **desenvolvedor** e, em seguida, clique em **compatibilidade** na lista **categoria** . Na lista **tipo de formulário** , selecione **formulário de navegador da Web** para criar um formulário que pode ser implantado como um formulário compatível com o navegador no SharePoint Server 2013. Selecione **formulário de preenchimento do InfoPath** para criar um formulário que pode ser executado somente no editor de preenchimento do InfoPath. As outras seleções na lista **tipo de formulário** oferecem suporte para compatibilidade com o InfoPath 2007 e o InfoPath 2003. 
  
As classes e membros de ambas as versões desse modelo de objeto são expostos através do namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . A tabela a seguir lista onde os assemblies estão localizados nos diretórios de uma instalação do InfoPath 2013. 
  
|**Defletor**|**Descrição**|
|:-----|:-----|
|Microsoft. Office. InfoPath. dll (localizado em C:\Arquivos de Programas\microsoft Office\Office15\InfoPathOM\InfoPathOMFormServices)  <br/> |O subconjunto do modelo de objeto que contém apenas os tipos e membros que serão executados na lógica de negócios de um modelo de formulário implantado em um servidor que executa o InfoPath Forms Services.  <br/> |
|Microsoft. Office. InfoPath. dll (localizado em C:\Arquivos de Programas\microsoft Office\Office15\InfoPathOM)  <br/> |O modelo de objeto "completo", incluindo tipos e membros que não serão executados na lógica de negócios de um modelo de formulário implantado no InfoPath Forms Services.  <br/> |
   
> [!NOTE]
> Os assemblies referenciados anteriormente nesta seção são usados no tempo de design quando você escreve e compila o código. Em tempo de execução, o assembly usado quando um modelo de formulário é aberto no InfoPath está localizado no cache de assembly global (GAC) do computador no qual o InfoPath está instalado. Quando um modelo de formulário é aberto em um navegador da Web a partir de um servidor que executa o InfoPath Forms Services, o assembly usado fica localizado no servidor. 
  
Fornecer dois assemblies ajuda a garantir que sua lógica de negócios conterá apenas chamadas para os membros do modelo de objeto adequados para os editores de formulário suportados (navegador da Web ou InfoPath Filler). Por exemplo, quando você edita o código, os recursos do IntelliSense, como conclusão da instrução e documentação na linha, só serão exibidos e funcionarão em relação aos membros do modelo de objeto adequados para seus editores de formulário de destino.
  
Em ambas as versões do modelo de objeto de código gerenciado expostos pelo assembly Microsoft. Office. InfoPath, a navegação e atualização de repositórios de dados XML na lógica de negócios requer chamadas para os membros da classe **System. xml. XPath. XPathNavigator** . No InfoPath 2003, a navegação e a atualização de repositórios de dados XML requer a chamada de membros de classes MSXML (para que a lógica comercial seja criada usando JScript ou VBScript) ou chamando através dos wrappers para as classes MSXML fornecidas pelo ** Microsoft. Office. Interop. InfoPath. SemiTrust** namespace (para lógica de negócios criada usando C# ou Visual Basic e o Microsoft Office InfoPath 2003 Toolkit para Visual Studio .net). 
  
O uso de membros da classe **XPathNavigator** permite que o mesmo código de lógica de negócios ofereça suporte à manipulação de dom para modelos de formulário abertos no cliente InfoPath e em formulários habilitados para Web abertos do SharePoint Server 2013 com formulários do InfoPath Serviços em um navegador da Web. 
  
Para obter informações sobre como trabalhar com membros da classe **XPathNavigator** na lógica de negócios dos modelos de formulário de código gerenciado do InfoPath, consulte [trabalhar com as classes XPathNavigator e XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="the-infopath-2003-compatible-managed-code-object-model"></a>O modelo de objeto de código gerenciado compatível com o InfoPath 2003

O modelo de objeto de código gerenciado compatível com o InfoPath 2003 foi introduzido no InfoPath 2003 Service Pack 1 junto com o Microsoft Office InfoPath 2003 Toolkit para Visual Studio .NET para escrever lógica de negócios em modelos de formulário com código gerenciado. Este modelo de objeto ainda tem suporte no InfoPath 2013 para fornecer compatibilidade com o InfoPath 2003.
  
As classes e os membros desse modelo de objeto são expostos através do namespace [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . Este modelo de objeto é implementado no seguinte arquivo de assembly que está localizado na pasta C:\Arquivos de Programas\microsoft Office\Office14 
  
|**Defletor**|**Descrição**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.SemiTrust.dll  <br/> |Fornece interoperabilidade COM no modelo de objeto COM do InfoPath para a lógica de negócios do modelo de formulário escrita usando C# ou Visual Basic.  <br/> |
   
> [!NOTE]
> Embora a criação da lógica de negócios com o modelo de objeto de interoperabilidade COM de interoperabilidade de COM do Microsoft. Office. Interop. InfoPath. SemiTrust ainda seja suportada pelo InfoPath 2013, a lógica de negócios escrita usando esse modelo de objeto, não há suporte para modelos de formulário habilitados para navegador implantados no SharePoint Server 2013 com o InfoPath Forms Services. Modelos de formulário habilitados para navegador devem usar o modelo de objeto de código gerenciado do InfoPath para lógica de negócios personalizada. 
  
### <a name="automating-infopath-from-managed-code"></a>Automatizando o InfoPath do código gerenciado

Além de escrever a lógica de negócios com código gerenciado, os desenvolvedores podem automatizar o InfoPath usando código gerenciado em execução em um aplicativo externo. Essa funcionalidade e os assemblies necessários para escrever código foram introduzidos no InfoPath 2003 Service Pack 1. Os objetos e membros para automatizar o InfoPath foram atualizados para fornecer funcionalidade adicional quando você escreve o código de automação externo para o InfoPath 2013.
  
As classes e membros usados para automação externa são expostos através dos namespaces [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) e [Microsoft. Office. Interop. InfoPath. xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) . Os arquivos de assembly necessários para escrever código de automação estão localizados na pasta C:\Arquivos de Programas\microsoft Office\Office14 
  
|**Defletor**|**Descrição**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.dll  <br/> |Fornece interoperabilidade COM contra o modelo de objeto do InfoPath COM para o código de automação externo escrito usando C# ou Visual Basic.  <br/> |
|Microsoft.Office.Interop.InfoPath.Xml.dll  <br/> |Fornece interoperabilidade COM contra as operações DOM do MSXML para XML no código de automação externo escrito usando C# ou Visual Basic.  <br/> |
   
Para obter mais informações sobre os modelos de objeto fornecidos pelos namespaces **Microsoft. Office. Interop. InfoPath** e **Microsoft. Office. Interop. InfoPath. xml** , que são usados exclusivamente para automatizar o aplicativo InfoPath usando o gerenciamento código de aplicativos externos, confira a [central de desenvolvedores do InfoPath](https://msdn.microsoft.com/office/aa905434.aspx).
  
### <a name="the-infopath-forms-services-object-model"></a>O modelo de objeto do InfoPath Forms Services

O modelo de objeto de código gerenciado para automatizar tarefas de administração do InfoPath Forms Services é implementado no Microsoft. Office. InfoPath. Server. dll, \<que\>está localizado em unidade: \Arquivos de Programas\Microsoft Office Server\15.0\Bin em um Instalação do Microsoft SharePoint Server 2013.
  
|**Defletor**|**Descrição**|
|:-----|:-----|
|Microsoft. Office. InfoPath. Server. dll  <br/> |O modelo de objeto para automatizar tarefas do InfoPath Forms Services, como carregar, ativar ou desativar modelos de formulário habilitados para navegador.  <br/> |
   
Para obter mais informações sobre o modelo de objeto do InfoPath Forms Services, consulte o SDK (Software Developers Kit) do SharePoint Server 2013 que está disponível no MSDN.
  
## <a name="infopath-development-environment"></a>Ambiente de desenvolvimento do InfoPath

O desenvolvimento de lógica comercial nos modelos de formulário do InfoPath 2013 pode ser executado usando o Visual Studio 2012 com o complemento [Microsoft Visual Studio Tools for applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) instalado. 
  
> [!NOTE]
> O InfoPath 2013 não oferece suporte à criação ou edição de modelos de formulário que usam lógica de negócios escrita com JScript ou VBScript, embora o InfoPath Filler suporte a abertura de modelos de formulário baseados em script que foram criados em versões anteriores do InfoPath. 
  
## <a name="see-also"></a>Confira também

- [Passo a passo: Criando um modelo de formulário básico com código](walkthrough-creating-a-basic-form-template-with-code.md)
- [Passo a passo: Criando e dePurando um modelo de formulário básico usando o modelo de objeto do InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)

