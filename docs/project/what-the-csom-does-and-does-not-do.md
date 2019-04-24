---
title: O que o CSOM faz e não faz
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 6828485c-040b-4278-923f-4cc7c8fe0fb1
description: O modelo de objeto no lado do cliente (CSOM) é um conjunto de APIs para o Project Server 2013 projetadas para uso online e local em aplicativos que podem ser desenvolvidos para PCs, dispositivos móveis e tablets. Este artigo inclui alguns cenários típicos para usar o CSOM e também lista as suas limitações.
localization_priority: Priority
ms.openlocfilehash: 6cdcb72c24e352365b6dcc9268ddf0bd249369af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315222"
---
# <a name="what-the-csom-does-and-does-not-do"></a>O que o CSOM faz e não faz

O modelo de objeto no lado do cliente (CSOM) é um conjunto de APIs para o Project Server 2013 projetadas para uso online e local em aplicativos que podem ser desenvolvidos para PCs, dispositivos móveis e tablets. Este artigo inclui alguns cenários típicos para usar o CSOM e também lista as suas limitações.
  
|||
|:-----|:-----|
|||
   
O CSOM permite o desenvolvimento de aplicativos para o Project Server 2013 e a integração do Project Server com outros aplicativos. Os aplicativos podem ser desenvolvidos para serem executados em PCs, dispositivos móveis como o Windows Phone 7.5, tablets como dispositivos Windows 8 e dispositivos iOS e Android. O CSOM fornece APIs que abrangem a funcionalidade dos doze serviços PSI mais usados no Project Server. As APIs do CSOM são organizadas de maneira diferente e são mais fáceis de usar do que os serviços PSI com base em ASMX e WCF. O CSOM não usa conjuntos de dados ADO.NET e é acessível por meio do protocolo OData. Você pode desenvolver com o CSOM usando bibliotecas do .NET Framework 4, JavaScript ou consultas REST (Transferência de Estado Representacional).
  
Para obter uma visão geral do CSOM e acessar artigos que mostram como usar o JavaScript e o .NET Framework 4 com o CSOM, consulte [Modelo de objeto no lado do cliente (CSOM) para o Project Server](client-side-object-model-csom-for-project-2013.md). Para saber mais sobre assemblies, classes e membros do CSOM, consulte a referência ao namespace [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
  
## <a name="usage-scenarios-for-the-csom"></a>Cenários de uso para o CSOM
<a name="pj15_WhatTheCSOM_UsageScenarios"> </a>

Os exemplos a seguir representam alguns tipos de aplicativos compatíveis com o CSOM. O CSOM pode ser usado no lugar do PSI para muitos cenários:
  
- **Desenvolver aplicativos que ampliam o Project Server** O principal objetivo do CSOM é o desenvolvimento de aplicativos para o Project Server 2013, no qual é possível criar aplicativos para uma ampla variedade de dispositivos, incluindo PCs, dispositivos móveis e tablets. Esses aplicativos podem ser distribuídos em um catálogo particular de aplicativos ou na Office Store pública. 
    
- **Automatizar a criação ou o gerenciamento de entidades no Project Server** O CSOM pode realizar operações CRUD para entidades como projetos, tarefas, atribuições, recursos da empresa, campos personalizados, tabelas de pesquisa, quadros de horários, manipuladores de eventos e fases e estágios de fluxos de trabalho. São comuns os casos em que um aplicativo personalizado pode economizar tempo com trabalhos em massa ou repetitivos. 
    
- **Obter dados nas tabelas publicadas do banco de dados do Project** Como não há suporte para acesso direto do banco de dados às tabelas de rascunho, publicadas e de arquivo morto, você pode usar o CSOM para ler dados que não estão disponíveis nas tabelas ou exibições de relatórios. Por exemplo, é possível obter informações sobre estágios, fases e atividades de fluxos de trabalho. Para ler dados nas tabelas de relatórios, você pode usar consultas OData. 
    
- **Validar o status e dados de quadros de horários** Use o CSOM em manipuladores de eventos locais ou em receptores de eventos remotos para pré-eventos, a fim de validar dados de status de atribuição ou de quadros de horários inseridos pelos usuários antes que esses dados sejam salvos no Project Web App. 
    
- **Criar projetos financeiros** Crie projetos para captura do tempo em um quadro de horários para integração com um sistema financeiro. Crie uma hierarquia de códigos financeiros que reflitam a estrutura de decomposição de custos do sistema financeiro. Projetos financeiros não exigem agendamento ou atualizações de status. 
    
- **Fazer integrações com sistemas contábeis** Capture os custos e despesas de recursos associados a projetos para alimentar sistemas financeiros e de cobrança e para fins de comparação de orçamento. Sincronizar tarefas, recursos e atribuições entre os sistemas. Capturar dados da planilha em um sistema para alimentar o outro (qual planilha é usada depende das necessidades da organização ou do projeto). 
    
- **Automatize atualizações de membros da equipe** Para projetos que não são gerenciados ativamente, atualize automaticamente os projetos no servidor com o progresso e outras alterações dos membros da equipe do projeto. Os projetos podem ser atualizados e republicados sem que um gerente de projetos precise revisar os resultados ou fazer ajustes no plano. 
    
    > [!NOTE]
    > O CSOM permite o envio de atualizações de status, mas atualmente não é compatível com aprovações de status. 
  
- **Avaliar dados do Project Server em receptores de eventos remotos** Um receptor de eventos remoto para um pré-evento **ProjectCreating** pode usar os dados do Project Server provenientes do CSOM para ajudar a determinar se deve cancelar esse evento. Por exemplo, antes de criar um projeto, compare a proposta do projeto com os projetos existentes. 
    
- **Oferecer suporte a fluxos de trabalho declarativos do Project Server** O CSOM permite fluxos de trabalho do Project Server criados no SharePoint Designer 2013. O CSOM oferece suporte para definições de fluxo de trabalho que usam o Windows Workflow Foundation versão 4 (WF4). (O PSI não é compatível com fluxos de trabalho do WF4.) 
    
- **Criar fluxos de trabalho complexos do Project Server** Ao desenvolver fluxos de trabalho com o Visual Studio 2012, você pode usar o CSOM para ações complexas em estágios de fluxo de trabalho ou criar ações de fluxo de trabalho personalizadas. 
    
## <a name="what-the-csom-does-not-do"></a>O que o CSOM não faz
<a name="pj15_WhatTheCSOM_DoesNotDo"> </a>

O CSOM não é um substituto completo para o PSI. Como o CSOM usa os serviços PSI internamente, ele tem muitas das mesmas limitações funcionais do PSI. Além das limitações do PSI, como a falta de acesso a dados em projetos locais (arquivos .mpp), o CSOM não inclui a funcionalidade administrativa com a qual o Project Web App costuma lidar. Por exemplo, a criação de grupos de segurança personalizados pode ser feita na página Configurações do Site > Permissões do Project Web App. 
  
Para obter uma lista de ações que nem o PSI, nem o CSOM podem manipular, consulte a seção *O que o PSI não faz* em [O que o PSI faz e não faz](what-the-psi-does-and-does-not-do.md).
  
### <a name="psi-services-that-the-csom-does-not-cover"></a>Serviços PSI que o CSOM não abrange
<a name="pj15_WhatTheCSOM_PSIServices"> </a>

O CSOM não inclui a funcionalidade dos seguintes serviços PSI:
  
- **Serviço de administração** Para gerenciar configurações e operações administrativas no Project Server e para sites de projetos relacionados, como a criação de períodos fiscais e a criação de configurações de quadros de horários, use métodos PSI na classe [WebSvcAdmin.Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx). O Project Web App propriamente ditos usa métodos **Admin** em muitas das páginas que estão vinculadas à página Configurações do Servidor (https://*NomeServidor*  /  *NomeProjectServer*/_layouts/15/pwa/Admin/Admin.aspx). 
    
- **Serviço Archive** Para salvar e gerenciar entidades, como projetos, recursos e campos personalizados, nas tabelas de arquivo morto, use métodos PSI na classe [Archive](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx). 
    
- **Serviço CubeAdmin** Para criar e gerenciar cubos OLAP em instalações locais, use métodos PSI na classe [WebSvcCubeAdmin.CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) ou use a página Gerenciamento de Banco de Dados OLAP (https://*NomeServidor*  /  *NomeProjectServer*/_layouts/15/pwa/CubeAdmin/CubeAnalysisAdmin.aspx) no Project Web App. 
    
    > [!NOTE]
    > O Project Online não oferece suporte a cubos OLAP. 
  
- **Serviço Driver** Para criar e gerenciar drivers de negócios para análises de portfólio de projetos, use os métodos PSI na classe [WebSvcDriver.Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx). 
    
- **Serviço LoginForms e serviço LoginWindows** A autenticação no CSOM é feita durante a inicialização do objeto **ProjectContext**, com a autenticação OAuth ou do Windows. Para criar aplicativos de autenticação múltipla, nos quais um aplicativo local de confiança total pode usar a autenticação do Forms e a autenticação do Windows, use métodos PSI na classe [WebSvcLoginForms.LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) e na classe [WebSvcLoginWindows.LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx). 
    
- **Serviço Notification** Para criar e gerenciar alertas e lembretes, use métodos PSI na classe [WebSvcNotifications.Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx). 
    
- **Serviço ObjectLinkProvider** Para criar e gerenciar objetos e links da Web para documentos e itens de lista do SharePoint, use os métodos PSI na classe [WebSvcObjectLinkProvider.ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx). 
    
- **Serviço PortfolioAnalyses** Para criar e gerenciar análises de portfólio de projeto, incluindo soluções planejadoras e soluções otimizadoras, use os métodos PSI na classe [WebSvcPortfolioAnalyses.PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx). 
    
- **Serviço QueueSystem** O CSOM pode obter informações básicas sobre trabalhos de fila do Project Server e inclui o método [ProjectContext.WaitForQueue](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WaitForQueue.aspx). Para um gerenciamento mais extensivo do Sistema de Enfileiramento do Project Server, use os métodos PSI na classe [WebSvcQueueSystem.QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx). 
    
- **Serviço Security** Para criar e gerenciar grupos, modelos e categorias de segurança do Project Server e para verificar as permissões do usuário atual, use os métodos PSI na classe [WebSvcSecurity.Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx). 
    
- **Serviço WssInterop** Para saber mais sobre sites de projeto e como gerenciá-los, use métodos PSI na classe [WebSvcWssInterop.WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx). 
    
    > [!NOTE]
    > Você pode usar o CSOM no SharePoint Server 2013. Sites de projeto são sites do SharePoint. 
  
O CSOM não permite extensões como as que o PSI pode ter. Por exemplo, se você criar uma extensão PSI para uso local, o CSOM não pode ser modificado para usar essa extensão PSI. É possível implementar cenários de extensão de outras maneiras:
  
- Agregue chamadas CSOM em um componente local ou em um componente executado no Microsoft Azure.
    
- Use consultas OData dos dados de relatórios ao invés de acessar diretamente as tabelas de relatórios no banco de dados do Project Server.
    
- Integre chamadas CSOM com aplicativos de terceiros por meio da autenticação OAuth do Project Online ou com componentes no lado do servidor para uso local.
    
- Aplicativos que usam o CSOM também podem usar bancos de dados personalizados no local ou com o SQL Azure.
    
### <a name="request-limits-of-the-csom"></a>Limites de solicitações do CSOM
<a name="pj15_WhatTheCSOM_RequestLimits"> </a>

O CSOM no Project Server 2013 acompanha a implementação CSOM do SharePoint Server 2013 e herda os limites para o tamanho máximo de uma solicitação. O SharePoint tem um limite de 2 MB para uma solicitação de operações e um limite de 50 MB para o tamanho de um objeto binário enviado. O tamanho da solicitação é limitado para proteger o servidor contra filas excessivamente longas de operações e contra atrasos de processamento de objetos binários grandes.
  
Por exemplo, se você usar o CSOM para criar um projeto e, em seguida, editar esse projeto para adicionar 252 tarefas com uma quantidade mínima de informações, como um nome abreviado, o GUID de tarefa e uma duração de 1d, a quantidade total de dados na solicitação **DraftProject.Update** será menor que 2 MB. Porém, se você tentar adicionar 253 tarefas desse tipo a um projeto vazio, o limite de 2 MB será excedido, e você obterá a seguinte exceção: **Microsoft.SharePoint.Client.ServerException: a solicitação usa muitos recursos**
  
Para capturar os dados em uma solicitação CSOM via HTTP ou HTTPS, você pode usar uma ferramenta de depuração da Web, como o [Fiddler](https://www.fiddler2.com) (https://www.fiddler2.com). Para um exemplo de código que implementa um teste para o tamanho da solicitação e inclui uma solução que divide uma solicitação grande em grupos menores, consulte [DraftProject.Update](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.DraftProject.Update.aspx) . 
  
## <a name="see-also"></a>Confira também
<a name="pj15_WhatTheCSOM_AR"> </a>

- [Modelo de objeto no lado do cliente (CSOM) para o Project Server](client-side-object-model-csom-for-project-2013.md)
    
- [O que o PSI faz e não faz](what-the-psi-does-and-does-not-do.md)
    
- [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
    

