---
title: Suplementos do Painel de Tarefas para Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: O Project Standard 2013 e o Project Professional 2013 são compatíveis com o painel de tarefas Suplementos do Office. Você pode usar os suplementos do painel de tarefas para integrar projetos, tarefas, recursos e exibir dados de um projeto com outros aplicativos de cliente do Office 2013, aplicativos do SharePoint, Web Parts, outras páginas da Web e dados externos.
ms.openlocfilehash: 26942cab1d1b127872a230a46fbc6242ab27b754
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396012"
---
# <a name="task-pane-add-ins-for-project"></a>Suplementos do Painel de Tarefas para Project

O Project Standard 2013 e o Project Professional 2013 são compatíveis com o painel de tarefas Suplementos do Office. Você pode usar os suplementos do painel de tarefas para integrar projetos, tarefas, recursos e exibir dados de um projeto com outros aplicativos de cliente do Office 2013, aplicativos do SharePoint, Web Parts, outras páginas da Web e dados externos.
  
Suplementos do Office é um modelo de extensibilidade compatível com vários aplicativos de cliente do Office 2013. A plataforma completa de suplementos inclui tipos de suplementos contextuais, de conte[udo e do painel de tarefas. Outlook 2013 é compatível com suplementos de email, que podem exibir uma p[agina da web dentro de uma mensagem de email ou item de compromisso do calendário relacionado ao conteúdo do item. O Word 2013 e o Excel 2013 suportam suplementos de conteúdo, que podem exibir uma página da web como conteúdo inserido em um documento. O Word 2013, o Excel 2013 e o Project Professional 2013 suportam suplementos do painel de tarefas, que podem exibir uma página da web em um painel de tarefas no qual o conteúdo esteja relacionado às informações contextuais do projeto.
  
Por exemplo, um suplemento do projeto pode resumir dados no projeto ativo e mostrar dados adicionais sobre um recurso ou uma tarefa selecionados. Os dados relacionados do suplementos podem vir de uma fonte externa, como uma lista do SharePoint, tabelas de relatórios da base de dados do Project Server, um serviço da web ou outro aplicativo corporativo. Um suplemento do painel tarefas pode ser desenvolvido com HTML 5, JavaScript, JQuery e outras bibliotecas do JavaScript. Um suplemento do painel de tarefas não é diretamente compatível com componentes do ActiveX, Silverlight ou Flash. Embora um suplemento do Office possa usar um elemento do **IFrame** para acessar um aplicativo da web do lado do servidor que utiliza ASP.NET e a biblioteca do .NET Framework 4.5, esse tipo de solução não é recomendado ou suportado. O suplemento pode ser desenvolvido para salvar os dados localmente ou gravar dados em um local externo. 
  
> [!NOTE]
> Os suplementos do Project no painel de tarefas podem acessar dados do Project Online usando uma autenticação OAuth. Com o Project Professional 2013, você pode desenvolver suplementos do painel de tarefas que acessam tanto as instalações locais do Project Server 2013 quanto o SharePoint 2013, local ou online. Por exemplo, confira [Conectar um suplemento do painel de tarefas do Project ao PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) no blog de Programabilidade do Project. > O Project Standard 2013 não suporta a integração direta com os dados do Project Server ou com as listas de tarefas do SharePoint que estão sincronizadas com o Project Server. 
  
Para saber mais sobre suplementos do Office 2013, confira [Suplementos do Office e do SharePoint](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29). 
  
## <a name="developing-task-pane-add-ins"></a>Desenvolvimento de suplementos do painel de tarefas

A documentação de desenvolvedor de suplementos do Office e do SharePoint inclui artigos e referências abrangentes. Para uma Introdução ao desenvolvimento de suplementos para o Project Professional 2013 e outros aplicativos de cliente do Office 2013, e para a referência de JavaScript e a referência de manifesto do XML, confira [Suplementos do Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29).
  
O download do SDK do Project 2013 inclui o suplemento de amostra do **Teste do Project OM** que mostra como obter o GUID de uma tarefa, recurso e visualização, como obter propriedades do projeto ativo e como definir uma tarefa, recurso ou visualizar um manipulador de eventos de seleção alterada. Ao extrair e instalar o SDK e amostras no arquivo Project2013SDK.msi, confira o subdiretório `\Samples\Apps\Copy_to_AppSource_FileShare`  e o subdiretório `\Samples\Apps\Copy_to_AppManifests_FileShare`. A amostra JSOMCall.html usa funções do JavaScript no arquivo office.js e no arquivo project-15.js, que são incluídos no download. Você pode usar os arquivos de depuração correspondentes (office.debug.js e project-15.debug.js) para examinar as funções. 
  
O suplemento de amostra **HelloProject_OData** do Project Professional 2013 foi desenvolvido com Visual Studio 2012. O suplemento usa uma consulta REST do serviço **ProjectData** para obter dados de relatórios de custo de projeto e outras informações, e depois compara o projeto atual a valores médios de todos os projetos no Aplicativo Web do Project. 
  
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Suplementos do Painel de Tarefas para Project](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [Conectar um suplemento de painel de tarefas do Project ao PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Download do SDK do Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Suplementos do Office e do SharePoint](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Suplementos do Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    

