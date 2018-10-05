---
title: Noções básicas sobre o ambiente de desenvolvimento e modelos de objeto do InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, modelos de objeto, [InfoPath 2007], o InfoPath 2007, ambientes de desenvolvimento de modelos de objeto
localization_priority: Normal
ms.assetid: 29415c5b-9a42-46f4-a9e8-6a7d5bb7bdbf
description: Microsoft InfoPath 2013 suporta dois tipos de modelos de programação para desenvolver lógica de negócios nos modelos de formulário e oferece suporte a automação externa do código gerenciado.
ms.openlocfilehash: c2ed1254acf86136ab7144c732aef91ac4c14c53
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400100"
---
# <a name="understanding-infopath-object-models-and-development-environment"></a>Noções básicas sobre o ambiente de desenvolvimento e modelos de objeto do InfoPath

Microsoft InfoPath 2013 suporta dois tipos de modelos de programação para desenvolver lógica de negócios nos modelos de formulário e oferece suporte a automação externa do código gerenciado.
  
InfoPath Forms Services, que está disponível no SharePoint Server 2013, fornece uma experiência de navegador da Web para preencher formulários do InfoPath. Quando implantado em um servidor que executa o InfoPath Forms Services, formulários baseados em formulário compatíveis com navegador modelos (. xsn) podem ser abertos em um navegador da Web de computadores que não tenham o InfoPath instalado, mas eles serão aberto no InfoPath quando ele é instalado. InfoPath Forms Services também fornece um modelo de objeto para automatizar tarefas de servidor relacionadas à administração e publicação de modelo de formulário do InfoPath.
  
InfoPath 2013 oferece suporte para o Visual Studio 2012 programação ambiente e seus associadas linguagens de programação, que são descritas neste tópico.
  
## <a name="infopath-programming-models"></a>Modelos de programação do InfoPath

InfoPath 2013 oferece suporte a dois modelos de objeto para desenvolver lógica de negócios nos modelos de formulário:
  
- O InfoPath gerenciados modelo de objeto de código
    
- O modelo de objeto de código gerenciado do InfoPath 2003 compatíveis
    
Além disso, o InfoPath 2013 permite escrever código gerenciado automatizar o InfoPath de um aplicativo externo.
  
InfoPath Forms Services fornece um modelo de objeto para automatizar tarefas de servidor, verificando e carregar modelos de formulário de código sendo executado no servidor, que exige permissões e acesso de administrador do servidor.
  
> [!NOTE]
> O InfoPath Filler 2013 pode abrir e executar criadas em versões anteriores do InfoPath que usam a lógica de negócios gravadas com linguagens de script (JScript e VBScript) de soluções de modelo de formulário do InfoPath. No entanto, o InfoPath Designer 2010 não oferece suporte a criar ou modificar os modelos de formulário que usam a lógica de negócios gravadas com script. 
  
### <a name="the-infopath-managed-code-object-model"></a>O InfoPath gerenciados modelo de objeto de código

O modelo de objeto de código gerenciado do InfoPath 2013 é implementado em dois assemblies ambos os quais são nomeados Microsoft.Office.Infopath.dll.
  
Uma versão do assembly implementa um subconjunto do modelo de objeto do InfoPath que contém apenas os tipos e os membros que são compatíveis com a lógica de negócios de modelos de formulário implantados como modelos de formulário habilitados para navegador em execução no SharePoint Server 2013 com InfoPath Forms Services. Modelos de formulário com lógica de negócios gravadas contra desse assembly serão aberto e execute do InfoPath Filler e em um navegador da Web.
  
A outra versão do assembly implementa tipos adicionais e os membros que fornecem funcionalidade que não há suporte para a lógica de negócios de modelos de formulário habilitados para navegador. Modelos de formulário com lógica de negócios gravadas contra as classes adicionais e membros nesse assembly serão aberto e executado somente no editor do InfoPath Filler.
  
> [!NOTE]
> É possível gravar lógica condicional que usa as propriedades da classe [ambiente](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) para determinar qual ambiente (InfoPath Filler ou um navegador da Web) o modelo de formulário está sendo executado no. Usando essa lógica condicional, a lógica de negócios pode branch entre o código que trabalha em um navegador da Web e o código gravado contra as classes e os membros que funcionam somente no editor do InfoPath Filler. Para obter mais informações, consulte [gravar lógica condicional que determina o ambiente de tempo de execução](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
O assembly que usa o InfoPath quando você adiciona e compila a lógica de negócios do modelo de formulário depende se você selecionar o modelo de formulário **Em branco** ou **Formulário em branco (InfoPath Filler)** na guia **New** do Microsoft Office Backstage quando começar a criar um novo formulário no Designer do InfoPath. Formulários criados usando o modelo de formulário de **Formulário em branco** usam o assembly que contém apenas os tipos e os membros que são compatíveis com a lógica de negócios de modelos de formulário implantados como modelos de formulário habilitados para navegador. Formulários criados usando o modelo de formulário de **Formulário em branco** podem ser abertos no navegador da Web e do InfoPath Filler. Formulários criados usando o modelo de formulário de **Formulário em branco (InfoPath Filler)** usam o assembly que implementa a tipos adicionais e os membros que fornecem funcionalidade que não há suporte para a lógica de negócios de modelos de formulário habilitados para navegador e só pode ser aberto do InfoPath Filler. 
  
> [!TIP]
> Depois de você começa a criar um modelo de formulário, você pode alterar qual assembly é usado, alterando as configurações de compatibilidade do formulário. Para fazer isso, clique em **idioma** , na guia **desenvolvedor** e, em seguida, clique em **compatibilidade** na lista **categoria** . Na lista **tipo de formulário** , selecione o **Formulário de navegador da Web** para criar um formulário que pode ser implantado como um formulário compatíveis com navegador no SharePoint Server 2013. Selecione o **Formulário do InfoPath Filler** para criar um formulário que pode ser executado somente no editor do InfoPath Filler. Outras seleções na lista **tipo de formulário** oferecem suporte para compatibilidade com o InfoPath 2007 e InfoPath 2003. 
  
As classes e os membros das duas versões desse modelo de objeto são expostos por meio do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . A tabela a seguir lista onde os assemblies estão localizados nos diretórios de uma instalação do InfoPath 2013. 
  
|**Assembly**|**Descrição**|
|:-----|:-----|
|Microsoft.Office.InfoPath.dll (localizada em C:\Program Files\Microsoft Office\Office15\InfoPathOM\InfoPathOMFormServices)  <br/> |O subconjunto do modelo de objeto que contém apenas tipos e membros que serão executados na lógica de negócios de um modelo de formulário implantado em um servidor que executa o InfoPath Forms Services.  <br/> |
|Microsoft.Office.InfoPath.dll (localizada em C:\Program Files\Microsoft Office\Office15\InfoPathOM)  <br/> |O modelo de objeto de "completo" incluindo os tipos e membros que não serão executados na lógica de negócios de um modelo de formulário implantado no InfoPath Forms Services.  <br/> |
   
> [!NOTE]
> Os assemblies mencionados anteriormente nesta seção são usados em tempo de design ao escrever e compilar código. Em tempo de execução, o assembly usado quando um modelo de formulário é aberto no InfoPath está localizado no Cache de Assembly Global (GAC) do computador no qual o InfoPath está instalado. Quando um modelo de formulário é aberto em um navegador da Web de um servidor que executa o InfoPath Forms Services, o assembly usado está localizado no servidor. 
  
Fornecer dois assemblies ajuda a garantir que a lógica de negócios conterá apenas chamadas para os membros do modelo de objeto apropriado para os editores de formulário com suporte (navegador da Web ou InfoPath Filler). Por exemplo, quando você editar seu código, o IntelliSense recursos como conclusão da instrução e documentação em linha será apenas exibir e trabalhar em relação aos membros do modelo de objeto apropriado para suas editores de formulário de destino.
  
Nas duas versões do modelo de objeto de código gerenciado expostas pelo assembly Microsoft.Office.InfoPath, navegando e a atualização de repositórios de dados XML na lógica de negócios exige chamadas para os membros da classe **System.Xml.XPath.XPathNavigator** . No InfoPath 2003, navegando e atualizar os armazenamentos de dados XML requer a chamada membros das classes MSXML (para a lógica de negócios criada usando o JScript ou VBScript) ou chamando-se por meio de wrappers para MSXML classes que são fornecido pelo ** SemiTrust** namespace (para a lógica de negócios criada usando-se em c# ou Visual Basic e o Microsoft Office InfoPath 2003 Toolkit para o Visual Studio .NET). 
  
O uso de membros da classe **XPathNavigator** permite que o mesmo código de lógica de negócios oferecer suporte a manipulação de DOM para modelos de formulário que são abertos no cliente do InfoPath e nos formulários habilitados para a Web abertos a partir do SharePoint Server 2013 com formulários do InfoPath Serviços em um navegador da Web. 
  
Para obter informações sobre como trabalhar com membros da classe **XPathNavigator** na lógica de negócios do InfoPath modelos de formulário de código gerenciado, consulte [trabalhar com o XPathNavigator e Classes de XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="the-infopath-2003-compatible-managed-code-object-model"></a>O modelo de objeto de código gerenciado do InfoPath 2003 compatíveis

O modelo de objeto de código gerenciado compatível com o InfoPath 2003 foi introduzido no InfoPath 2003 Service Pack 1 em conjunto com o Microsoft Office InfoPath 2003 Toolkit para o Visual Studio .NET para escrever uma lógica de negócios nos modelos de formulário com código gerenciado. Este modelo de objeto ainda é suportado pelo InfoPath 2013 para fornecer compatibilidade com o InfoPath 2003.
  
As classes e os membros desse modelo de objeto são expostos por meio do namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . Este modelo de objeto é implementado no seguinte arquivo de assembly que está localizado na pasta C:\Program Files\Microsoft Office\Office14. 
  
|**Assembly**|**Descrição**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.SemiTrust.dll  <br/> |Fornece interoperabilidade COM base no modelo de objeto COM do InfoPath para a lógica de negócios de modelo de formulário gravadas usando c# ou Visual Basic.  <br/> |
   
> [!NOTE]
> Embora a criação de lógica de negócios com o modelo de objeto de código gerenciado interoperabilidade de COM fornecido pelo assembly SemiTrust ainda é suportado pelo InfoPath 2013, escrita usando esse modelo de objeto, para que ele não é suportado a lógica de negócios modelos de formulário habilitados para navegador implantados para o SharePoint Server 2013 com o InfoPath Forms Services. Modelos de formulário habilitados para navegador devem usar o modelo de objeto de código gerenciado do InfoPath para a lógica de negócios personalizado. 
  
### <a name="automating-infopath-from-managed-code"></a>Automatizando o InfoPath do código gerenciado

Além de escrever lógica de negócios com código gerenciado, os desenvolvedores podem automatizar InfoPath usando código gerenciado em execução em um aplicativo externo. Essa funcionalidade e os assemblies necessários para escrever código foram introduzidos no InfoPath 2003 Service Pack 1. Os objetos e membros para automatizar o InfoPath foram atualizados para fornecer funcionalidade adicional ao escrever código de automação externa do InfoPath 2013.
  
As classes e os membros usados para automação externa são expostos por meio dos namespaces [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) e [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) . Os arquivos de assembly que são necessários para escrever o código de automação estão localizados na pasta C:\Program Files\Microsoft Office\Office14. 
  
|**Assembly**|**Descrição**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.dll  <br/> |Fornece a interoperabilidade COM base no modelo de objeto COM do InfoPath para o código de automação externa escrito usando c# ou Visual Basic.  <br/> |
|Microsoft.Office.Interop.InfoPath.Xml.dll  <br/> |Fornece a interoperabilidade COM contra o MSXML para operações de XML DOM no código de automação externa escrito usando c# ou Visual Basic.  <br/> |
   
Para obter mais informações sobre os modelos de objeto fornecido pelos namespaces **Microsoft.Office.Interop.InfoPath** e **Microsoft.Office.Interop.InfoPath.Xml** , que são usados exclusivamente para automatizar a aplicação do InfoPath usando gerenciados código de aplicativos externos, consulte o [Centro do desenvolvedor do InfoPath](https://msdn.microsoft.com/office/aa905434.aspx).
  
### <a name="the-infopath-forms-services-object-model"></a>O modelo de objeto do InfoPath Forms Services

O modelo de objeto de código gerenciado para automatizar tarefas de administração de InfoPath Forms Services é implementado no Microsoft.Office.InfoPath.Server.dll que está localizado em \<unidade\>: \Program Files\Microsoft Server\15.0\Bin Office em um Instalação do Microsoft SharePoint Server 2013.
  
|**Assembly**|**Descrição**|
|:-----|:-----|
|Microsoft.Office.InfoPath.Server.dll  <br/> |O modelo de objeto para automação de tarefas do InfoPath Forms Services, como o carregamento, ativando ou desativando modelos de formulário habilitados para navegador.  <br/> |
   
Para obter mais informações sobre o modelo de objeto do InfoPath Forms Services, consulte o SharePoint Server 2013 Software Developers Kit (SDK) que está disponível no MSDN.
  
## <a name="infopath-development-environment"></a>Ambiente de desenvolvimento do InfoPath

O desenvolvimento de lógica de negócios nos modelos de formulário do InfoPath 2013 pode ser executado usando o Visual Studio 2012 com o complemento do [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) instalado. 
  
> [!NOTE]
> InfoPath 2013 não oferece suporte à criação ou edição de modelos de formulário que usam a lógica de negócios gravada com JScript ou VBScript, embora o InfoPath Filler oferece suporte a modelos de formulário baseado em script de abertura que foram criados nas versões anteriores do InfoPath. 
  
## <a name="see-also"></a>Confira também

- [Passo a passo: criar um modelo de formulário básico com código](walkthrough-creating-a-basic-form-template-with-code.md)
- [Passo a passo: Criando e depurando um modelo de formulário básico usando o modelo de objeto do InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)

