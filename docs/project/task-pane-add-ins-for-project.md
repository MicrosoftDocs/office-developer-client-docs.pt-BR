---
title: Suplementos de painel de tarefas para Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 e Project Professional 2013 oferecem suporte a suplementos do Office do painel de tarefas. Você pode usar os suplementos de painel de tarefas para integrar o projeto, tarefa, recurso e exibir dados em um projeto com outros aplicativos cliente do Office 2013, aplicativos do SharePoint, Web Parts, outras páginas da Web e dados externos.
ms.openlocfilehash: 1432f38e9f2c87b7d5d33500d958222b2c15d7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771175"
---
# <a name="task-pane-add-ins-for-project"></a>Suplementos de painel de tarefas para Project

Project Standard 2013 e Project Professional 2013 oferecem suporte a suplementos do Office do painel de tarefas. Você pode usar os suplementos de painel de tarefas para integrar o projeto, tarefa, recurso e exibir dados em um projeto com outros aplicativos cliente do Office 2013, aplicativos do SharePoint, Web Parts, outras páginas da Web e dados externos.
  
Suplementos do Office é um modelo de extensibilidade que é suportado em vários aplicativos de cliente do Office 2013. A plataforma completo suplemento inclui contextual, conteúdo e tipos de suplemento do painel de tarefas. Outlook 2013 oferece suporte a email suplementos, que podem mostrar uma página da Web dentro de uma mensagem de email ou item de compromisso do calendário que está relacionada ao conteúdo no item. Word 2013 e o Excel 2013 suportam conteúdos suplementos, que podem mostrar uma página da Web como conteúdo incorporado em um documento. Word 2013, Excel 2013 e Project Professional 2013 suportam a tarefa painel suplementos, que podem mostrar uma página da Web em um painel de tarefas, onde o conteúdo está relacionado às informações contextuais dentro do projeto.
  
Por exemplo, um suplemento do Project pode resumir dados do projeto ativo e mostrar dados adicionais sobre um recurso ou tarefa selecionada. Dados relacionados em que o suplemento podem provenientes de uma fonte externa, como uma lista do SharePoint, relatórios de tabelas no banco de dados do Project Server, um serviço da web ou outro aplicativo empresarial. Um suplemento de painel tarefas pode ser desenvolvido com outras bibliotecas de JavaScript, 5 de HTML, JavaScript e JQuery. Um suplemento de painel tarefa não oferece suporte direto ActiveX, Silverlight ou componentes Flash. Embora um suplemento do Office possa usar um elemento **IFrame** para acessar um aplicativo web do lado do servidor que usa a biblioteca do .NET Framework 4.5 e ASP.NET, esse tipo de solução não é recomendado ou é suportado. O suplemento pode ser desenvolvido para salvar dados localmente ou gravar dados em um local externo. 
  
> [!NOTE]
> Painel de tarefas suplementos de projeto pode acessar dados do Project Online usando autenticação OAuth. Com o Project Professional 2013, você pode desenvolver tarefa painel complementos que acessam ambas as instalações do local do Project Server 2013 e no local ou online do SharePoint 2013. Por exemplo, consulte [conectar-se um painel de tarefas do projeto suplemento para PWA](http://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) no blog Programmibility do projeto. > Project Standard 2013 não dá suporte a integração direta com dados do Project Server ou listas de tarefas do SharePoint que são sincronizadas com o Project Server. 
  
Para obter mais informações sobre suplementos para o Office 2013, consulte [Office e SharePoint suplementos](http://msdn.microsoft.com/en-us/library/office/fp161507%28v=office.15%29). 
  
## <a name="developing-task-pane-add-ins"></a>Desenvolver suplementos de painel de tarefas

A documentação do desenvolvedor para Office e SharePoint suplementos inclui referências e artigos abrangentes. Para obter uma introdução ao desenvolvimento de suplementos para o Project Professional 2013 e outros aplicativos cliente do Office 2013 e para a referência de JavaScript e a referência de manifesto XML, consulte [Add-ins do Office](http://msdn.microsoft.com/en-us/library/office/apps/jj220060%28v=office.15%29).
  
O download do SDK do Project 2013 inclui o **Teste do Project OM** amostra suplemento que mostra como obter o GUID de uma tarefa, recurso e modo de exibição, como obter propriedades do projeto ativo e como definir uma tarefa, recurso ou exibir o manipulador de eventos de seleção alterada. Quando você extrair e instala o SDK e exemplos no arquivo Project2013SDK.msi, consulte o `\Samples\Apps\Copy_to_AppSource_FileShare` subdiretório e o `\Samples\Apps\Copy_to_AppManifests_FileShare` subdiretório. A amostra de JSOMCall.html usa as funções de JavaScript no arquivo do Office. js e arquivo de projeto-15.js, que estão incluídos no download. Você pode usar os arquivos de depuração correspondentes (office.debug.js e project-15.debug.js) para examinar as funções. 
  
O **HelloProject_OData** amostra suplemento para o Project Professional 2013 foi desenvolvido com o Visual Studio 2012. O suplemento usa uma consulta do restante do serviço **ProjectData** obter relatórios de dados de custo do projeto e outras informações e compara o projeto atual com os valores médios para todos os projetos no Project Web App. 
  
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Suplementos do painel de tarefas para Project](http://msdn.microsoft.com/en-us/library/office/apps/fp161143%28v=office.15%29)
    
- [Conectando um suplemento do painel de tarefas do projeto para PWA](http://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Download do SDK do Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Suplementos do Office e do SharePoint](http://msdn.microsoft.com/en-us/library/office/fp161507%28v=office.15%29)
    
- [Suplementos do Office](http://msdn.microsoft.com/en-us/library/office/apps/jj220060%28v=office.15%29)
    

