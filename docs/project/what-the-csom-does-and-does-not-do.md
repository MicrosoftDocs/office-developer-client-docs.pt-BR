---
title: O que o CSOM faz e não faz
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6828485c-040b-4278-923f-4cc7c8fe0fb1
description: O modelo de objeto do cliente (CSOM) é um conjunto de APIs do Project Server 2013 que foram projetados para ambos online e no local usar em aplicativos que podem ser desenvolvidos para PCs, tablets e dispositivos móveis. Este artigo inclui alguns cenários típicos para usar o CSOM e também lista as limitações do CSOM do.
ms.openlocfilehash: 232152d3d2ee902b438bc1fe3ece06acca713175
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771185"
---
# <a name="what-the-csom-does-and-does-not-do"></a>O que o CSOM faz e não faz

O modelo de objeto do cliente (CSOM) é um conjunto de APIs do Project Server 2013 que foram projetados para ambos online e no local usar em aplicativos que podem ser desenvolvidos para PCs, tablets e dispositivos móveis. Este artigo inclui alguns cenários típicos para usar o CSOM e também lista as limitações do CSOM do.
  
|||
|:-----|:-----|
|||
   
O CSOM permite o desenvolvimento de aplicativos para o Project Server 2013 e integração do Project Server com outros aplicativos. Os aplicativos podem ser desenvolvidos para executar em PCs, dispositivos móveis, como Windows Phone 7.5 do, tablets, como os dispositivos do Windows 8 e dispositivos com Android e iOS. O CSOM fornece APIs que abrangem a funcionalidade da doze mais comumente usadas serviços PSI no Project Server. As APIs de CSOM são organizadas de forma diferente e são mais fáceis de usar do que os serviços PSI baseados em ASMX e WCF. O CSOM não usa conjuntos de dados ADO.NET e pode ser acessada por meio do protocolo OData. Você pode desenvolver com o CSOM usando bibliotecas do .NET Framework 4, JavaScript, ou consultas de transferência de estado representacional (REST).
  
Para obter uma visão geral dos artigos que mostram como usar JavaScript e .NET Framework 4 com o CSOM e CSOM, consulte [o modelo de objeto do lado do cliente (CSOM) para o Project Server](client-side-object-model-csom-for-project-2013.md). Para obter mais informações sobre os assemblies CSOM, classes e membros, consulte a referência ao namespace [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
## <a name="usage-scenarios-for-the-csom"></a>Cenários de uso para o CSOM
<a name="pj15_WhatTheCSOM_UsageScenarios"> </a>

Estes são exemplos de alguns tipos de aplicativos que suporta o CSOM. O CSOM pode ser usado em vez da PSI para muitos cenários:
  
- **Aplicativos develop que estendem o Project Server** O objetivo principal do CSOM do é o desenvolvimento de aplicativo do Project Server 2013, onde os aplicativos podem ser criados para uma ampla variedade de dispositivos que incluírem PCs, tablets e dispositivos móveis. Aplicativos podem ser distribuídos dentro de um catálogo de aplicativos privado ou no Office Store pública. 
    
- **Automatize a criação ou o gerenciamento de entidades no Project Server** O CSOM pode executar operações CRUD para entidades como projetos, tarefas, atribuições, recursos da empresa, campos personalizados, tabelas de pesquisa, quadros de horários, manipuladores de eventos e fases do fluxo de trabalho e estágios. Geralmente, há casos em que um aplicativo personalizado pode economizar tempo com trabalhos repetitivos ou em massa. 
    
- **Obter dados nas tabelas do banco de dados de projeto publicados** Porque o banco de dados direto acessar o rascunho, publicado e arquivar tabelas não é suportado, você pode usar o CSOM para ler os dados que não está disponíveis nas tabelas ou modos de exibição de relatórios. Por exemplo, obtenha informações sobre atividades, fases e estágios do fluxo de trabalho. Para ler dados nas tabelas de relatórios, você pode usar as consultas de OData. 
    
- **Validar dados de status e quadro de horários** Use o CSOM em manipuladores de evento local ou receptores de evento remoto para eventos prévia para validar dados de status ou quadro de horários de atribuição que os usuários digitam, antes que os dados são salvos no Project Web App. 
    
- **Criar projetos de financeiros** Crie projetos para captura de tempo por meio do quadro de horários para integração com um sistema financeiro. Crie uma hierarquia de códigos financeiros que refletem a estrutura de divisão de custo do sistema financeiro. Projetos financeiros não exigem atualizações de status ou de agendamento. 
    
- **Integra-se com sistemas de contabilidade** Capture os custos de recursos e as despesas com projetos para alimentar sistemas de cobrança e financeiros e para fins de comparação de orçamento associadas. Sincronize tarefas, recursos e atribuições entre os sistemas. Capturar dados de quadro de horários em um sistema para alimentar outra (qual quadro de horários é usado depende das necessidades da organização ou de projetos individuais). 
    
- **Automatize as atualizações dos membros da equipe** Para projetos que não são gerenciados ativamente, atualize automaticamente os projetos no servidor com o progresso e outras alterações de membros da equipe de projeto. Projetos podem ser atualizados e republicados sem revisão dos resultados ou fazer ajustes ao plano de um gerente de projeto. 
    
    > [!NOTE]
    > O CSOM suporta como enviar atualizações de status, mas atualmente não suporta aprovações de status. 
  
- **Dados de avaliar o Project Server em receptores de evento remoto** Um receptor de evento remoto para um pré-evento de **ProjectCreating** pode usar os dados do Project Server do CSOM para ajudar a determinar se deseja cancelar o evento. Por exemplo, antes de criar um projeto, compare a proposta de projeto com projetos existentes. 
    
- **Fluxos de trabalho do Project Server declarativos suporte** O CSOM permite que os fluxos de trabalho do Project Server que são criados no SharePoint Designer 2013. O CSOM suporta as definições de fluxo de trabalho que usam o Windows Workflow Foundation versão 4 (WF4). (A PSI não oferece suporte para fluxos de trabalho WF4.) 
    
- **Criar complexos fluxos de trabalho do Project Server** Quando você desenvolve fluxos de trabalho com o Visual Studio 2012, você pode usar o CSOM para ações complexas em estágios do fluxo de trabalho ou criar ações personalizadas de fluxo de trabalho. 
    
## <a name="what-the-csom-does-not-do"></a>O que o CSOM não faz
<a name="pj15_WhatTheCSOM_DoesNotDo"> </a>

O CSOM não é uma substituição completa para a PSI. Como o CSOM internamente usa os serviços PSI, CSOM do tem várias limitações funcionais mesmas que tenha a PSI. Além das limitações da PSI, como que não tenham acesso aos dados em projetos locais (arquivos. mpp), o CSOM não inclui a funcionalidade administrativa que normalmente manipula Project Web App. Por exemplo, a criação de grupos de segurança personalizados pode ser administrado nas configurações do Site - página de permissões do Project Web App. 
  
Para obter uma lista de ações que lidam com nem a PSI nem o CSOM, consulte a seção *não faz o que o PSI* , no [qual o PSI e não faz](what-the-psi-does-and-does-not-do.md).
  
### <a name="psi-services-that-the-csom-does-not-cover"></a>Serviços PSI que não cobre CSOM do
<a name="pj15_WhatTheCSOM_PSIServices"> </a>

O CSOM não incluir a funcionalidade dos serviços PSI a seguir:
  
- **Serviço de administração** Para gerenciar as configurações administrativas e operações no Project Server e para sites de projeto relacionadas, criando períodos fiscais e fazendo as configurações do quadro de horários, use os métodos PSI na classe [WebSvcAdmin.Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) . Project Web App em si usa os métodos de **Admin** em muitas das páginas vinculadas a página Configurações do servidor (http:// *ServerName*  /  *ProjectServerName* /_layouts/15/pwa/Admin/Admin.aspx). 
    
- **Serviço de arquivamento** Para salvar e gerenciar entidades como projetos, recursos e campos personalizados nas tabelas de arquivamento, usam os métodos da PSI a classe de [arquivo morto](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) . 
    
- **Serviço CubeAdmin** Para criar e gerenciar cubos OLAP para instalações locais, use os métodos PSI na classe [WebSvcCubeAdmin.CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) ou use a página Gerenciamento de banco de dados OLAP (http:// *ServerName*  /  ** layouts/15/pwa / CubeAdmin/CubeAnalysisAdmin.aspx) no Project Web App. 
    
    > [!NOTE]
    > Project Online não oferece suporte para os cubos OLAP. 
  
- **Serviço de driver** Para criar e gerenciar fatores comerciais para análises de portfólio do project, use os métodos PSI na classe [WebSvcDriver.Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) . 
    
- **Serviço de LoginForms e o serviço de LoginWindows** Autenticação no CSOM do é feita durante a inicialização do objeto **ProjectContext** , com a autenticação OAuth ou Windows. Para criar aplicativos para múltipla autenticação, onde um aplicativo de confiança total local pode usar autenticação de formulários e autenticação do Windows, use métodos PSI na classe [WebSvcLoginForms.LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) e o [ WebSvcLoginWindows.LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) classe. 
    
- **Serviço de notificação** Para criar e gerenciar alertas e lembretes, use os métodos PSI na classe [WebSvcNotifications.Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) . 
    
- **Serviço ObjectLinkProvider** Para criar e gerenciar objetos da web e links para documentos e itens de lista do SharePoint, use os métodos PSI na classe [WebSvcObjectLinkProvider.ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) . 
    
- **Serviço PortfolioAnalyses** Para criar e gerenciar análises de portfólio do project, incluindo as soluções de planejador e soluções do otimizador, use os métodos PSI na classe [WebSvcPortfolioAnalyses.PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) . 
    
- **Serviço QueueSystem** O CSOM pode obter informações básicas sobre trabalhos de fila do Project Server e inclua o método [ProjectContext.WaitForQueue](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WaitForQueue.aspx) . Para o gerenciamento mais abrangente do sistema de enfileiramento do Project Server, use os métodos PSI na classe [WebSvcQueueSystem.QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) . 
    
- **Serviço de segurança** Para criar e gerenciar categorias, modelos e grupos de segurança do Project Server e para verificar permissões para o usuário atual, use os métodos PSI na classe [WebSvcSecurity.Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) . 
    
- **Serviço WssInterop** Para obter informações e gerenciar sites de projeto, use os métodos PSI na classe [WebSvcWssInterop.WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) . 
    
    > [!NOTE]
    > Você pode usar o CSOM no SharePoint Server 2013. Sites de projetos são sites do SharePoint. 
  
O CSOM não habilita extensões, como a PSI pode ter. Por exemplo, se você criar uma extensão PSI para uso local, o CSOM não pode ser modificado para usar a extensão do PSI. Você pode implementar cenários de extensão de outras maneiras:
  
- Agregação de chamadas do CSOM dentro de um componente local ou de um componente que executa o Microsoft Azure.
    
- Use consultas OData de dados de relatórios, em vez de diretamente acessando o relatório de tabelas no banco de dados do Project Server.
    
- Integre as chamadas do CSOM com aplicativos de terceiros por meio da autenticação OAuth do Project Online ou com componentes de servidor para uso no local.
    
- Aplicativos que usam o CSOM também podem usar bancos de dados personalizados localmente ou com o SQL Azure.
    
### <a name="request-limits-of-the-csom"></a>Limites de solicitação de CSOM do
<a name="pj15_WhatTheCSOM_RequestLimits"> </a>

O CSOM no Project Server 2013 baseia-se na implementação CSOM no SharePoint Server 2013 e herda os limites para o tamanho máximo de uma solicitação. SharePoint tem um limite de 2 MB para uma solicitação de operações e um limite de 50 MB para o tamanho de um objeto binário enviado. O tamanho de solicitação é limitado para proteger o servidor de filas excessiva longas das operações e de processamento atrasos para objetos binários grandes.
  
Por exemplo, se você usar o CSOM para criar um projeto e editar o projeto para adicionar 252 tarefas com uma quantidade mínima de informações como um nome curto, a GUID da tarefa e uma duração de 1-d, a quantidade total de dados na solicitação de **DraftProject.Update** é menor que 2 MB. Mas, se você tentar adicionar 253 dessas tarefas para um projeto vazio, o limite de 2 MB for excedido, e você receberá a seguinte exceção: **Microsoft.SharePoint.Client.ServerException: A solicitação usa muitos recursos**
  
Para capturar os dados em uma solicitação de CSOM via HTTP ou HTTPS, você pode usar uma ferramenta como o [Fiddler](http://www.fiddler2.com) de depuração de web (http://www.fiddler2.com). Para obter um exemplo de código que implementa um teste para o tamanho da solicitação e inclui uma solução que quebras de uma solicitação de grande em para grupos menores, consulte [DraftProject.Update](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.DraftProject.Update.aspx) . 
  
## <a name="see-also"></a>Confira também
<a name="pj15_WhatTheCSOM_AR"> </a>

- [Modelo de objeto do cliente (CSOM) para o Project Server](client-side-object-model-csom-for-project-2013.md)
    
- [O que o PSI faz e não faz](what-the-psi-does-and-does-not-do.md)
    
- [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
    

