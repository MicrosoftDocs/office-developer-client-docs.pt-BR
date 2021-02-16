---
title: O que o PSI faz e não faz
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: A Interface do Project Server (PSI) pode ajudar a automatizar muitos processos do lado do servidor em instalações locais do Project Server 2013. Porém, várias funções exigem o uso do Microsoft Project Professional 2013.
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346526"
---
# <a name="what-the-psi-does-and-does-not-do"></a>O que o PSI faz e não faz

A Interface do Project Server (PSI) pode ajudar a automatizar muitos processos do lado do servidor em instalações locais do Project Server 2013. Porém, várias funções exigem o uso do Microsoft Project Professional 2013.
  
|||
|:-----|:-----|
|||
   
A PSI foi projetada para complementar os recursos do Project Professional 2013, em vez de fornecer uma alternativa baseada em servidor para todas as funções do Project Professional. Desenvolvedores de terceiros podem usar o PSI para ajudar a criar Web Parts para instalações locais do Project Web App e espaços de trabalho de projeto, criar aplicativos personalizados do Windows e aplicativos Web que interagem com dados do Project Server local, desenvolver lógica de fluxo de trabalho para gerenciamento de portfólio de projeto, desenvolver manipuladores de eventos de confiança total locais e integrar o Project Server com outros aplicativos. A PSI não pode ser usada para o desenvolvimento de aplicativos para a Office Store, dispositivos móveis ou tablets; Para isso, você pode usar o modelo de objeto do lado do cliente (CSOM).
  
> [!NOTE]
> A PSI fornece uma interface programática mais abrangente para o Project Server 2013 do que o CSOM fornece. Mas, a menos que o CSOM não forneça a funcionalidade necessária, recomendamos usar o CSOM para desenvolver novos aplicativos. Para obter mais informações, [consulte O que o CSOM faz e não faz.](what-the-csom-does-and-does-not-do.md) 
  
## <a name="usage-scenarios-for-the-psi"></a>Cenários de uso da PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

A seguir estão exemplos de alguns aplicativos que o PSI suporta para projetos e cálculos do lado do servidor:
  
- **Automatizar a criação ou o gerenciamento de entidades no Project Server** Embora o Project Professional 2013 e o Project Web App juntos sejam projetados para lidar com o gerenciamento e a criação de entidades como projetos, recursos da empresa e campos personalizados, geralmente há casos em que um aplicativo personalizado pode economizar tempo com trabalhos em massa ou repetitivos. O PSI pode automatizar vários tipos de trabalhos que o CSOM não faz, por exemplo, com cubos OLAP, análises de portfólio de projeto, drivers de negócios, notificações, provedores de link de objeto, segurança e interoperabilidade do SharePoint. 
    
- **Obter dados nas tabelas publicadas ou arquivadas do banco de dados do Project** Como o acesso direto ao banco de dados às tabelas de rascunho, publicadas e arquivadas não é suportado, você pode usar o PSI para ler dados que não estão disponíveis nas tabelas ou exibições de relatórios. Por exemplo, obter informações sobre versões do projeto, datas e alterações armazenadas nas tabelas de arquivo morto e preencher um controle de Grade JS em uma Web Part com as informações. 
    
- **Validar dados de status e quadro de horários** Use o PSI em manipuladores de pré-evento locais para validar o status da atribuição ou os dados do quadro de horários que os usuários instem, antes que os dados sejam salvos no Project Web App. 
    
- **Projetos de manutenção** Crie projetos de espaço reservado para usar com planos de recursos. Reserve tempo nos recursos para um trabalho de manutenção ou negócios base. Os projetos de manutenção geralmente não possuem tarefas. 
    
- **Criar projetos financeiros** Crie projetos para captura do tempo em um quadro de horários para integração com um sistema financeiro. Crie uma hierarquia de códigos financeiros que reflitam a estrutura de decomposição de custos do sistema financeiro. Projetos financeiros não exigem agendamento ou atualizações de status. 
    
- **Fazer integrações com sistemas contábeis** Capture os custos e despesas de recursos associados a projetos para alimentar sistemas financeiros e de cobrança e para fins de comparação de orçamento. Sincronizar tarefas, recursos e atribuições entre os sistemas. Capturar dados da planilha em um sistema para alimentar o outro (qual planilha é usada depende das necessidades da organização ou do projeto). 
    
- **Automatize atualizações de membros da equipe** Para projetos que não são gerenciados ativamente, atualize automaticamente os projetos no servidor com o progresso e outras alterações dos membros da equipe do projeto. Os projetos podem ser atualizados e republicados sem que um gerente de projetos precise revisar os resultados ou fazer ajustes no plano. 
    
- **Avaliar dados do Project Server em manipuladores de eventos de confiança total locais** Um manipulador de eventos local para o pré-evento **ProjectCreating** pode usar dados do Project Server da PSI para ajudar a determinar se um evento deve ser cancelado. Por exemplo, antes de criar um projeto, compare a proposta do projeto com os projetos existentes. 
    
- **Criar atividades de fluxo de trabalho personalizadas para gerenciamento de demanda** Use o PSI em atividades locais de fluxo de trabalho de confiança total para modificar e atualizar propostas de projeto com base em modelos de projeto da empresa. Use campos personalizados do projeto para marcar o projeto com as informações necessárias para o processo de iniciação e aprovação. Adicionar tarefas para identificar fases do projeto para as principais etapas ou produtos. Quando propostas de projeto são aprovadas, um fluxo de trabalho pode alterar as propostas em projetos de escala completa que são gerenciados com o Project Professional. 
    
- **Criar extensões psi** (**preterido.** As extensões foram preteridas no Project Server 2013 e não terão suporte em versões futuras.) A PSI pode ser estendida com serviços personalizados usando a interface do Windows Communication Foundation (WCF). As extensões da PSI são executados no computador do Project Server e podem usar a mesma infraestrutura de segurança que os serviços psi integrados usam. As extensões podem consultar as tabelas de relatórios, usar tabelas de banco de dados separadas, consolidar chamadas PSI para economizar largura de banda e integrar-se com aplicativos de terceiros e outros componentes do lado do servidor. Para obter mais informações, consulte [Desenvolvendo extensões da PSI.](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx)
    
- **Usar a representação em aplicativos locais de confiança total** Chamadas para a interface WCF do PSI podem ser personificados, para que um aplicativo assume as permissões de segurança do usuário personificado. A representação deve ser usada com moderação e cuidado. Ler e atualizar informações de status para outros usuários não exige representação. Os novos aplicativos que exigem representação devem usar o CSOM e o protocolo OAuth em vez da PSI. Para obter mais informações sobre a representação com a PSI, consulte [Usar Representação com WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).
    
> [!NOTE]
> Em alguns casos, o PSI pode ser usado em aplicativos cliente com o CSOM e o Project Online. Se você usar um serviço Web da PSI baseado em ASMX, o aplicativo deverá incluir um método para autenticar o objeto [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) no CSOM e um método para autenticar o objeto cliente **System.Web.Services.Protocols.SoapHttpClientProtocol.** Para ver um exemplo que usa um serviço Web com o CSOM do SharePoint, consulte Autenticação Remota no SharePoint Online usando autenticação [baseada em declarações.](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx) > devido a permissões restritas no nível do aplicativo, o PSI não pode ser usado em aplicativos projetados para distribuição na Office Store pública. Nesse caso, você pode usar apenas o CSOM. 
  
## <a name="what-the-psi-does-not-do"></a>O que o PSI não faz
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Embora haja muitas coisas que o PSI pode fazer, há algumas coisas que o PSI não faz. A seguir estão duas coisas que o PSI não pode fazer, mas o CSOM pode fazer.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online e receptores de eventos remotos

A principal limitação da PSI é com o Project Online. Os aplicativos que usam a PSI exigem acesso de confiança total a uma instalação local do Project Server. Por exemplo, o PSI não pode ser usado em receptores de eventos remotos, onde o receptor de evento é instalado como um serviço no Microsoft Azure.
  
### <a name="workflows-and-claims-authentication"></a>Fluxos de trabalho e autenticação de declarações

Uma definição de fluxo de trabalho que usa o Windows Workflow Foundation versão 4 (WF4) requer autenticação de declarações, que o PSI não suporta diretamente. Isso significa que você não pode usar o PSI para criar um projeto no Project Server 2013 que tenha um tipo de projeto empresarial (EPT) com uma definição de fluxo de trabalho WF4.
  
Você pode usar o PSI para criar projetos com EPTs que não tenham fluxo de trabalho ou usem uma definição WF3.5 herdada (a versão de fluxo de trabalho no Project Server 2010). Para criar um projeto com um EPT que tenha uma definição WF4, use o CSOM.
  
 **Ações que exigem o Project Professional:**
  
A lista a seguir são coisas que nem a PSI nem o CSOM podem fazer.
  
#### <a name="local-data"></a>Dados locais

- Manipulação de dados em projetos locais (arquivos .mpp). Por exemplo, definir tabelas de taxas de custo ou delimitações de disponibilidade para recursos locais. 
    
- Definindo ou editando calendários base locais ou calendários de recursos, incluindo exceções de calendário.
    
- Definindo campos personalizados locais. (O PSI dá suporte à edição de valores de campo personalizado local em tarefas, recursos e atribuições.)
    
#### <a name="enterprise-data"></a>Dados da empresa

- Fazer check-out ou edição do modelo global da empresa. Os dados globais da empresa no Project Server 2013 são um conjunto de tabelas de dados binários no banco de dados do Project, não um modelo de projeto como no Office Project Server 2007 e em versões anteriores.
    
- Definindo ou editando calendários da empresa. Os [métodos Calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) gerenciam apenas exceções de calendário. 
    
#### <a name="master-projects-and-cross-project-links"></a>Projetos mestres e links entre projetos

- Criação de projetos mestres e inserção de subprojetos.
    
- Agendar um caminho crítico em um projeto mestre. 
    
- Criação de links entre projetos.
    
#### <a name="resources"></a>Recursos

- Solicitando ou executando a nivelamento de recursos.
    
- Alterar o recurso em uma atribuição. (Você pode usar o PSI para excluir a atribuição e criar uma nova.)
    
- Excluir ou substituir um recurso que tenha trabalho real aceito (reais).
    
- Alterar um tipo de recurso entre trabalho, material e custo.
    
- Criando ou editando calendários de recursos.
    
- Ao adicionar um recurso a uma tarefa, o PSI não redistribui automaticamente o trabalho da mesma forma que o Project Professional. Fica a critério do desenvolvedor escolher e definir explicitamente a distribuição de trabalho nas atribuições.
    
#### <a name="cost-resources"></a>Cost resources

- Edição, criação ou exclusão de recursos de custo e atribuições usando os [métodos](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) do Project. Os [métodos Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) podem criar recursos de custo, mas não podem editá-los. 
    
#### <a name="work-contours"></a>Delimitações do trabalho

- Edição de dados de fases.
    
    > [!NOTE]
    > O [método UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) no serviço Web **de Status** pode editar dados reais em fases em atribuições depois que o gerente de projeto atualiza e publica os dados de atribuição. 
  
- Definindo ou alterando o tipo de delimitação de atribuição (como plano, de back-loaded ou de front-loaded).
    
#### <a name="baselines-and-earned-value"></a>Linhas de base e valor agregado

- Salvando uma linha de base ou editando dados de linha de base. 
    
- Definindo uma data de progresso.
    
- Cálculo da variância e do valor agregado. 
    
#### <a name="interactive-scheduling"></a>Agendamento interativo

- Suporte ao agendamento interativo. (Como o Project Server lida com interações de forma assíncrona, o agendamento interativo deve ser feito com o Project Professional.)
    
    > [!NOTE]
    > Para evitar a alteração do comportamento programático, os métodos PSI que são trazidos para frente do Project Server 2010 agem da mesma maneira no Project Server 2013. Por exemplo, [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) ainda tem as mesmas limitações e usa o mecanismo de agendamento mais antigo do lado do servidor. O novo [método QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) remove muitas dessas limitações e usa o novo mecanismo de agendamento do lado do servidor do Project Server 2013, que é o mesmo mecanismo de agendamento que está no Project Professional 2013. 
  
#### <a name="wbs"></a>EDT

- Definindo uma máscara de código de estrutura de divisão de trabalho (BS). 
    
#### <a name="tasks"></a>Tarefas

- Alterar o tipo de tarefa (trabalho fixo, duração ou unidades).
    
- Alterar se uma tarefa é controlada pelo esforço.
    
- Alteração da acumulação de custo fixo da tarefa.
    
- Alterando o conteúdo do [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) campo. A PSI pode ler somente a parte de texto das anotações da tarefa, que são dados binários .rtf. Porém, você pode editar anotações de [atribuição ( ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ), que são dados de texto. O banco de dados Relatórios não inclui anotações de tarefa ou atribuição. 
    
- Criação ou edição de tarefas recorrentes.
    
- Atribuindo ou alterando o calendário de tarefas em tarefas existentes.
    
- Criar uma nova tarefa com um calendário de tarefas.
    
- Alterar o valor do campo [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) campo (a tarefa ignora o calendário de recursos). 
    
- Alterar o status ativo de uma tarefa usando [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , se alterações adicionais são feitas na mesma chamada. Para obter mais informações, consulte a *seção Agendamento do Project no Servidor* na programação do Project [Server.](project-server-programmability.md)
    
#### <a name="summary-tasks"></a>Tarefas de resumo

- Criar ou alterar atribuições em tarefas de resumo.
    
    > [!NOTE]
    > Recomendamos que você não faça atribuições em tarefas de resumo usando o Project Professional ou de outra forma. Para obter mais informações, consulte a *seção Agendamento do Project no Servidor* na programação do Project [Server.](project-server-programmability.md) 
  
- Edição de campos de tarefa de resumo que normalmente são rolados a partir da subtarefa. Os projetos do lado do servidor sempre roll up summary information, instead of setting information on the summary task and pushing it down to the subtasks. Você pode editar apenas os seguintes campos em tarefas de resumo:
    
  - Dependências de tarefas
    
  - Campos personalizados que não são de fórmula
    
  - [TASK_NAME](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [TASK_OUTLINE_LEVEL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [TASK_IS_MARKED](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [TASK_CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [TASK_CONSTRAINT_DATE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [TASK_PRIORITY](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [TASK_DEADLINE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [TASK_FIXED_COST](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (definir o valor somente ao criar a tarefa) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
Para a tarefa de resumo do projeto, as limitações da PSI são as mesmas do Project Professional. O PSI pode editar atribuições de orçamento, incluindo orçamentos de custo.
  
#### <a name="project-level-calculation-options"></a>Opções de cálculo no nível do projeto

- Alterar um tipo de projeto entre o Schedule From Start (SFS) e o Schedule From Finish (SFF). (O PSI pode criar um projeto como SFS ou SFF, mas uma vez criado pode ser alterado somente no Project Professional.)
    
- Alterar o calendário base do projeto[(CAL_UID)](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) após a criação do projeto. 
    
- Alterar opções para cálculos. Você pode usar o PSI para definir as opções de cálculo a seguir quando o projeto é criado, mas alterar as opções requer o Project Professional. (No exibição Backstage, escolha **Opções** e, em seguida, escolha a guia **Agenda** na caixa de diálogo **Opções** do Projeto.) 
    
  - [PROJ_OPT_CALC_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CALC_ACT_COSTS.aspx)
    
  - [PROJ_OPT_CRITICAL_SLACK_LIMIT](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CRITICAL_SLACK_LIMIT.aspx)
    
  - [PROJ_OPT_HONOR_CONSTRAINTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_HONOR_CONSTRAINTS.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_IF_LATER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_IF_LATER.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_TO_STATUS.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_IF_EARLIER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_IF_EARLIER.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_TO_STATUS.aspx)
    
  - [PROJ_OPT_MULT_CRITICAL_PATHS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MULT_CRITICAL_PATHS.aspx)
    
  - [PROJ_OPT_SPLIT_IN_PROGRESS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPLIT_IN_PROGRESS.aspx)
    
  - [PROJ_OPT_SPREAD_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_ACT_COSTS.aspx)
    
  - [PROJ_OPT_SPREAD_PCT_COMP](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_PCT_COMP.aspx)
    
  - [PROJ_OPT_TASK_UPDATES_RES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_TASK_UPDATES_RES.aspx)
    
## <a name="see-also"></a>Confira também

- [O que o CSOM faz e não faz](what-the-csom-does-and-does-not-do.md)  
- [Programabilidade do Project Server](project-server-programmability.md)   
- [Autenticação remota no SharePoint Online usando autenticação baseada em declarações](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)  
- [Suplementos do Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) 
    

