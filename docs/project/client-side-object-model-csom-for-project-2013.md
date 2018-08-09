---
title: Modelo de objeto do cliente (CSOM) para o Project 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: O modelo de objeto do cliente do Project Server 2013 (CSOM) implementa a funcionalidade de servidor comum. O Project Server CSOM inclui um Microsoft.NET CSOM, um Microsoft Silverlight CSOM, um CSOM do Windows Phone 8 e um modelo de objeto JavaScript (JSOM). Além disso, o CSOM inclui um serviço OData que permite uma interface REST. A interface REST destina-se principalmente para desenvolvimento de aplicativos em plataformas de não-Windows, como iOS e Android.
ms.openlocfilehash: a17dc816cd2033ff0057821ef029f0163881f9ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771033"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Modelo de objeto do cliente (CSOM) para o Project 2013

O modelo de objeto do cliente do Project Server 2013 (CSOM) implementa a funcionalidade de servidor comum. O Project Server CSOM inclui um Microsoft.NET CSOM, um Microsoft Silverlight CSOM, um CSOM do Windows Phone 8 e um modelo de objeto JavaScript (JSOM). Além disso, o CSOM inclui um serviço OData que permite uma interface REST. A interface REST destina-se principalmente para desenvolvimento de aplicativos em plataformas de não-Windows, como iOS e Android.
  
> [!NOTE]
> Soluções para o Project Online devem usar o CSOM. No entanto, os aplicativos locais podem usar o CSOM ou o Project Server Interface (PSI). Se o CSOM inclui a funcionalidade que você planeja usar, recomendamos que você use o CSOM para novos aplicativos. 
  
Em extensões CSOM, o objeto **ProjectContext** fornece o ponto de entrada para o conteúdo do servidor e a funcionalidade. CSOM do .NET, CSOM do Silverlight e CSOM do Windows Phone, use o objeto [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) e o JSOM usa o **PS. ProjectContext** objeto. Propriedades de **ProjectContext** fornecem acesso direto aos objetos do Project Server core no conjunto de sites atual do Project Web App. Para obter informações sobre o local dos assemblies CSOM e o arquivo de JavaScript, consulte [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
 **O modelo de segurança e de aplicativos** Aplicativos devem usar o CSOM para CRUD (criar, ler, atualizar e excluir) operações com o Project Server 2013 e Project Online. Aplicativos do projeto não usar o modelo de autenticação somente app no SharePoint 2013. Um aplicativo do Project Server requer um escopo de solicitação de permissão específicos que especifica em cujo nome comandos estão sendo executados. 
  
 **Consultas do REST** Você pode criar consultas do restante do serviço OData CSOM sem consumir os metadados. Permitem que algumas ferramentas de terceiros usando os assemblies do .NET para o CSOM para desenvolver aplicativos para outros dispositivos. Por exemplo, pesquisar na Internet para "plataforma cruzada ferramentas de desenvolvimento .NET para iOS ou Android." 
  
> [!NOTE]
> Embora o `$metadata` opção para **ProjectData** reporting service é válida ( `http://ServerName/pwaName/_api/ProjectData/$metadata`), o `$metadata` opção para o serviço de **ProjectServer** do CSOM do é removido na versão lançada do Project Server 2013. Para localizar os objetos CSOM e os membros que estão disponíveis como pontos de extremidade do REST, consulte a [biblioteca JavaScript e referência do restante do Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md). 
  
Para ver as entidades disponíveis no CSOM por meio da interface REST, você pode usar o `http://ServerName/pwaName/_api/ProjectServer` consulta. Para consultas REST, a entidade **ProjectServer** espelha estritamente as propriedades do objeto [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) no assembly Microsoft.ProjectServer.Client.dll gerenciados e o [PS. ProjectContext](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) objeto o JSOM. Por exemplo, você pode usar seu navegador para obter informações do CSOM do sobre projetos no Project Web App, as atribuições em um projeto especificado e o nome da tarefa de uma atribuição especificada para um recurso especificado, usando as seguintes consultas (cada consulta usa o mesmo `http://ServerName/pwaName/_api` prefixo de URL). Os GUIDs são valores de amostra para **Project.Id**, **EnterpriseResource.Id**e **Assignment.Id**.
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

Ao contrário da interface do OData para o serviço **ProjectData** , que é somente leitura para relatórios, você poderá fazer operações CRUD usando consultas do REST com o serviço de **ProjectServer** . Consultas do REST para o Project Server CSOM destinam-se principalmente para plataformas que não seja a área de trabalho do Windows, como Windows RT, iOS e Android. Para as plataformas Windows desktop e servidor, como o Windows 7, Windows 8 e Windows Server 2008 R2, você pode usar os assemblies CSOM gerenciado. Para aplicativos web, você pode usar PS.js para JavaScript. Para obter informações sobre como fazer operações CRUD usando REST consultas, consulte o tópico de [OData de uso de operações de consulta em solicitações REST do SharePoint](http://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx) no SDK do SharePoint 2013. Para obter informações sobre como usar o serviço **ProjectData** , consulte [OData consultando feeds para os dados de relatórios do Project](https://msdn.microsoft.com/en-us/library/office/jj163048.aspx).
  
A tabela 1 lista as propriedades de **ProjectContext** que representam os objetos do Project Server. Você pode usar esses objetos para recuperar outras entidades do Project Server 2013, como tarefas e atribuições. 
  
**Tabela 1. Propriedades de ProjectContext que fornecem acesso aos objetos do Project Server no CSOM and JSOM**

|**CSOM (.NET, Silverlight e Windows Phone)**|**JSOM**|
|:-----|:-----|
|[CustomFields](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |customFields  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[EntityTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |entityTypes  <br/> |
|[EventHandlers](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |eventHandlers  <br/> |
|[Eventos](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |events  <br/> |
|[LookupTables](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |lookupTables  <br/> |
|[Fases](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |fases  <br/> |
|[Projects](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |projetos  <br/> |
|[Estágios](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |estágios  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |workflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |
   
## <a name="in-this-section"></a>Nesta seção

[Introdução ao Project Server CSOM e .NET](getting-started-with-the-project-server-csom-and-net.md) fornece informações gerais sobre o Project Server CSOM e .NET, instruções sobre como criar uma extensão do .NET CSOM simples no Visual Studio 2012 e exemplos de código de suporte. 
  
[Introdução ao modelo de objeto JavaScript do Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md) fornece informações gerais sobre o Project Server JSOM, instruções sobre como criar uma extensão JSOM simples no Visual Studio 2012 e exemplos de código de suporte. 
  
Além disso, confira estes artigos que mostram como usar o CSOM:
  
- [Atualizar campos personalizados em massa e criar sites de projeto a partir de um fluxo de trabalho no Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
    
- [Trabalhar com projetos usando o modelo de objeto do JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    
> [!NOTE]
> Você também pode usar o Visual Studio 2010 para desenvolvimento do .NET Framework 4 com o CSOM. 
  
## <a name="reference"></a>Referência

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>Confira também



[Arquitetura do Project Server 2013](project-server-2013-architecture.md)


[Escolha o conjunto de APIs certo no SharePoint 2013](http://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)

