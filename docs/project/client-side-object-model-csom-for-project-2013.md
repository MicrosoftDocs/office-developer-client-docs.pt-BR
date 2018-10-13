---
title: Modelo de objeto do cliente (CSOM) para o Project 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: O modelo de objeto do cliente do Project Server 2013 (CSOM) implementa funcionalidade de servidores comuns. O Project Server CSOM inclui um Microsoft .NET CSOM, um Microsoft Silverlight CSOM, um Windows Phone 8 CSOM e um modelo de objeto do JavaScript (JSOM). Além disso, o CSOM inclui um serviço de OData que habilita uma interface REST. A interface REST destina-se principalmente ao desenvolvimento de aplicativos em plataformas que não são do Windows como iOS e Android.
ms.openlocfilehash: 8be603fbee35f228dea0fa6b6be087b8e09c30e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394444"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Modelo de objeto do cliente (CSOM) para o Project 2013

O modelo de objeto do cliente do Project Server 2013 (CSOM) implementa funcionalidade de servidores comuns. O Project Server CSOM inclui um Microsoft .NET CSOM, um Microsoft Silverlight CSOM, um Windows Phone 8 CSOM e um modelo de objeto do JavaScript (JSOM). Além disso, o CSOM inclui um serviço de OData que habilita uma interface REST. A interface REST destina-se principalmente ao desenvolvimento de aplicativos em plataformas que não são do Windows como iOS e Android.
  
> [!NOTE]
> Soluções para o Project Online devem usar o CSOM. No entanto, os aplicativos no local podem usar o CSOM ou o Project Server Interface (PSI). Se o CSOM inclui a funcionalidade que você planejar usar, é recomendável usar o CSOM para novos aplicativos. 
  
Nas extensões do CSOM, o objeto **ProjectContext** fornece o ponto de entrada para o conteúdo e funcionalidade do servidor. O CSOM .NET ,o CSOM Silverlight e o Windows Phone CSOM usam o objeto[Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx)e a JSOM usa o objeto**PS ProjectContext**. As propriedades**ProjectContext**fornecem acesso direto ao objetos principais do Project Server no atual conjunto de sites do Project Web App. Confira informações sobre o local de arquivo JavaScript e assemblies CSOM [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
 Os aplicativos**Aplicativos e o modelo de segurança**devem usar o CSOM para as operações CRUD (criar, ler, atualizar e excluir) com o Project Server 2013 e no Project Online. Aplicativos de projeto não usam o modelo de autenticação somente aplicativo no SharePoint 2013. Um aplicativo do Project Server requer um escopo de solicitação de permissão específico que especifica qual comandos estão sendo executados. 
  
 **Consultas REST** criar consultas do REST do serviço OData do CSOM sem consumir metadados. Algumas ferramentas de terceiros habilitam usando assemblies .NET para que o CSOM desenvolva aplicativos para outros dispositivos. Por exemplo, pesquise na Internet "ferramentas de desenvolvimento multiplataforma .NET para iOS ou Android." 
  
> [!NOTE]
> Embora a `$metadata` opção para o serviço de relatório**ProjectData** seja válido ( `https://ServerName/pwaName/_api/ProjectData/$metadata`), a `$metadata` opção para  o serviço **ProjectServer** do CSOM é removida na versão do Project Server 2013. Para localizar os objetos do CSOM e membros que estão disponíveis como pontos de extremidade do REST, confira a[referência de biblioteca JavaScript biblioteca e REST para o Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md). 
  
Para ver as entidades disponíveis no CSOM por meio da interface do REST, você pode usar a `https://ServerName/pwaName/_api/ProjectServer` consulta. Para consultas REST, a entidade semelhante**ProjectServer**espelha propriedades do objeto[ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) na montagem gerenciada Microsoft.ProjectServer.Client.dll e no objeto[PS ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) JSOM. Por exemplo, você pode usar o navegador para obter informações do CSOM sobre projetos no Project Web App, tarefas em um projeto específico e nome da tarefa de uma tarefa especificada para um recurso específico, usando as seguintes consultas (cada consulta usa o mesmo `https://ServerName/pwaName/_api` prefixo URL). Os GUIDs são valores de exemplo para **Project.Id**, **EnterpriseResource.Id**, e **Assignment.Id**.
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

Ao contrário da interface do OData para o serviço **ProjectData**,que é somente leitura para relatórios, você pode fazer operações CRUD usando consultas REST com o serviço **ProjectServer**. Consultas REST para o Project Server CSOM destinam-se principalmente para plataformas de trabalho diferentes do Windows, como Android, iOS e Windows RT. Para o Windows desktop e para as plataformas de servidor, como o Windows 7, Windows 8 e Windows Server 2008 R2, você pode usar conjuntos gerenciados CSOM. Para aplicativos web, você pode usar PS.js para JavaScript. Confira informações sobre como fazer operações CRUD usando consultas REST em[Usar operações de consulta OData nas solicitações REST no SharePoint](https://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx) em tópicos SDK do SharePoint 2013. Para saber mais sobre como usar o serviço **ProjectData**, confira [consultar feeds OData dos dados dos relatórios do Project](https://msdn.microsoft.com/library/office/jj163048.aspx).
  
A tabela 1 lista as propriedades **ProjectContext**que representam objetos do Project Server. Você pode usar esses objetos para recuperar outras entidades do Project Server 2013, como tarefas. 
  
**Tabela 1. Propriedades ProjectContext que fornecem acesso a seus objetos Project Server CSOM e JSOM**

|**CSOM (.NET Silverlight e Windows Phone)**|**JSOM**|
|:-----|:-----|
|[CustomFields](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |customFields  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[EntityTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |entityTypes  <br/> |
|[EventHandlers](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |EventHandlers  <br/> |
|[Eventos](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |eventos  <br/> |
|[LookupTables](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |lookupTables  <br/> |
|[Fases](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |fases  <br/> |
|[Projetos](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |Projetos  <br/> |
|[Estágios](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |Estágios  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |WorkflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |
   
## <a name="in-this-section"></a>Nesta seção

[A introdução ao Project Server CSOM e .NET](getting-started-with-the-project-server-csom-and-net.md) fornece uma visão geral sobre o Project Server CSOM e .NET, instruções sobre como criar uma extensão .NET CSOM simples no Visual Studio 2012 e exemplos de código de suporte. 
  
[A introdução ao objeto de modelo JavaScript do Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md) fornece uma visão geral sobre o Project Server CSOM e .NET, instruções sobre como criar uma extensão .NET CSOM simples no Visual Studio 2012 e exemplos de código de suporte. 
  
Além disso, confira estes artigos que mostram como usar o CSOM:
  
- [Atualizar campos personalizados em massa e criar sites de projeto a partir de um fluxo de trabalho no Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
    
- [Trabalhar com projetos usando o modelo de objeto do JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    
> [!NOTE]
> Você também pode usar o Visual Studio 2010 para o desenvolvimento do .NET Framework 4 com o CSOM. 
  
## <a name="reference"></a>Referências

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>Confira também



[Arquitetura do Project Server 2013](project-server-2013-architecture.md)


[Escolha o conjunto de APIs certo no SharePoint 2013](https://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)

