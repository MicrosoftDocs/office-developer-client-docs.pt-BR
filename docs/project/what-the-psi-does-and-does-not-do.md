---
title: O que o PSI faz e não faz
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: A interface do Project Server (PSI) pode ajudar a automatizar vários processos do lado do servidor em instalações locais do Project Server 2013. No enTanto, várias funções exigem o uso do Microsoft Project Professional 2013.
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346526"
---
# <a name="what-the-psi-does-and-does-not-do"></a>O que o PSI faz e não faz

A interface do Project Server (PSI) pode ajudar a automatizar vários processos do lado do servidor em instalações locais do Project Server 2013. No enTanto, várias funções exigem o uso do Microsoft Project Professional 2013.
  
|||
|:-----|:-----|
|||
   
A PSI é projetada para complementar os recursos do Project Professional 2013, em vez de fornecer uma alternativa baseada em servidor para todas as funções do Project Professional. Os desenvolvedores terceirizados podem usar o PSI para ajudar a criar Web Parts para instalações locais do Project Web App e espaços de trabalho do projeto, criar aplicativos Web e aplicativos Web personalizados que interagem com os dados do Project Server local, desenvolver fluxos de trabalho lógica para o gerenciamento de portfólio de projetos, desenvolver manipuladores de eventos de confiança total locais e integrar o Project Server com outros aplicativos. O PSI não pode ser usado para o desenvolvimento de aplicativos para a Office Store, dispositivos móveis ou tablets; para isso, você pode usar o modelo de objeto do lado do cliente (CSOM).
  
> [!NOTE]
> A PSI fornece uma interface programática mais abrangente para o Project Server 2013 do que o CSOM fornece. Mas, a menos que o CSOM não forneça a funcionalidade necessária, recomendamos que você use o CSOM para desenvolver novos aplicativos. Para obter mais informações, consulte [o que o CSOM faz e não faz](what-the-csom-does-and-does-not-do.md). 
  
## <a name="usage-scenarios-for-the-psi"></a>Cenários de uso do PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

Veja a seguir exemplos de alguns aplicativos que o PSI suporta para projetos e cálculos do lado do servidor:
  
- **Automatizar a criação ou o gerenciamento de entidades no Project Server** Embora o Project Professional 2013 e o Project Web App juntos sejam projetados para gerenciar o gerenciamento e a criação de entidades como projetos, recursos da empresa e campos personalizados, há muitas vezes em que um aplicativo personalizado pode economizar tempo com massa ou trabalhos repetitivos. O PSI pode automatizar vários tipos de trabalhos que o CSOM não faz, por exemplo, com cubos OLAP, análises de portfólios de projetos, fatores comerciais, notificações, provedores de link de objeto, segurança e interoperabilidade do SharePoint. 
    
- **Obter dados nas tabelas publicadas ou de arquivamento do banco de dados de projeto** Como não há suporte para o acesso ao banco de dados direto para as tabelas rascunho, publicado e arquivo morto, você pode usar o PSI para ler os dados que não estão disponíveis nas tabelas ou modos de exibição de relatório. Por exemplo, obtenha informações sobre versões, datas e alterações do projeto armazenadas nas tabelas de arquivo morto e, em seguida, preencha um controle de grade JS em uma Web Part com as informações. 
    
- **Validar dados de status e quadro de horários** Use o PSI em manipuladores de eventos locais para validar os dados de status de atribuição ou de quadro de horários que os usuários inserem, antes de os dados serem salvos no Project Web App. 
    
- **Projetos de manutenção** Criar projetos de espaço reservado para usar com planos de recursos. Reserve tempo nos recursos para um trabalho de manutenção ou negócios base. Os projetos de manutenção geralmente não possuem tarefas. 
    
- **Criar projetos financeiros** Crie projetos para captura do tempo em um quadro de horários para integração com um sistema financeiro. Crie uma hierarquia de códigos financeiros que reflitam a estrutura de decomposição de custos do sistema financeiro. Projetos financeiros não exigem agendamento ou atualizações de status. 
    
- **Fazer integrações com sistemas contábeis** Capture os custos e despesas de recursos associados a projetos para alimentar sistemas financeiros e de cobrança e para fins de comparação de orçamento. Sincronizar tarefas, recursos e atribuições entre os sistemas. Capturar dados da planilha em um sistema para alimentar o outro (qual planilha é usada depende das necessidades da organização ou do projeto). 
    
- **Automatize atualizações de membros da equipe** Para projetos que não são gerenciados ativamente, atualize automaticamente os projetos no servidor com o progresso e outras alterações dos membros da equipe do projeto. Os projetos podem ser atualizados e republicados sem que um gerente de projetos precise revisar os resultados ou fazer ajustes no plano. 
    
- **Avaliar dados do Project Server em manipuladores de eventos de confiança total locais** Um manipulador de eventos local para o **ProjectCreating** pré-evento pode usar os dados do Project Server do psi para ajudar a determinar se um evento deve ser cancelado. Por exemplo, antes de criar um projeto, compare a proposta do projeto com os projetos existentes. 
    
- **Criar atividades personalizadas de fluxo de trabalho para gerenciamento de demanda** Use o PSI em atividades de fluxo de trabalho de confiança total e local para modificar e atualizar propostas de projeto com base em modelos de projeto corporativo. Use os campos personalizados do projeto para marcar o projeto com as informações necessárias para o processo de inicialização e aprovação. Adicionar tarefas para identificar fases do projeto para as principais etapas ou produtos. Quando as propostas de projeto são aprovadas, um fluxo de trabalho pode alterar as propostas em projetos de escala inteira que são gerenciados com o Project Professional. 
    
- **Criar extensões psi** (**Preterido.** As extensões são preteridas no Project Server 2013 e não serão suportadas em versões futuras. O PSI pode ser estendido com serviços personalizados usando a interface do Windows Communication Foundation (WCF). As extensões PSI são executadas no computador do Project Server e podem usar a mesma infraestrutura de segurança que os serviços de PSI internos usam. As extensões podem consultar as tabelas de relatórios, usar tabelas de banco de dados separadas, consolidar chamadas PSI para salvar largura de banda e integrar com aplicativos de terceiros e outros componentes do lado do servidor. Para obter mais informações, consulte [developING psi Extensions](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx).
    
- **Usar representação em aplicativos locais, de confiança total** As chamadas para a interface do WCF do PSI podem ser representadas, para que um aplicativo assuma as permissões de segurança do usuário representado. A representação deve ser usada com moderação e com cuidado. A leitura e a atualização de informações de status de outros usuários não requerem representação. Novos aplicativos que requerem representação devem usar o CSOM e o protocolo OAuth em vez do PSI. Para obter mais informações sobre representação com a PSI, consulte [usar representação com o WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).
    
> [!NOTE]
> Em alguns casos, a PSI pode ser usada em aplicativos clientes com o CSOM e o Project online. Se você usar um serviço Web do PSI baseado em ASMX, o aplicativo deve incluir um método para autenticar o objeto [Microsoft. ProjectServer. Client. ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) no CSOM e um método para autenticar o ** Objeto System. Web. Services. Protocols. SoapHttpClientProtocol** Client. Para obter um exemplo que usa um serviço Web com o CSOM do SharePoint, confira [autenticação remota no SharePoint online usando a autenticação baseada em declarações](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx). > por causa de permissões de nível de aplicativo restritas, o PSI não pode ser usado em aplicativos projetados para distribuição na Office Store pública. Nesse caso, você pode usar somente o CSOM. 
  
## <a name="what-the-psi-does-not-do"></a>O que o PSI não faz
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Embora haja muitas coisas que o PSI pode fazer, há algumas coisas que o PSI não faz. Veja a seguir duas coisas que o PSI não pode fazer, mas o CSOM pode fazer.
  
### <a name="project-online-and-remote-event-receivers"></a>Receptores de eventos remotos e do Project online

A principal limitação do PSI é com o Project online. Os aplicativos que usam a PSI exigem acesso de confiança total a uma instalação local do Project Server. Por exemplo, o PSI não pode ser usado em receptores de eventos remotos, onde o receptor de eventos é instalado como um serviço no Microsoft Azure.
  
### <a name="workflows-and-claims-authentication"></a>Fluxos de trabalho e autenticação de declarações

Uma definição de fluxo de trabalho que usa o Windows Workflow Foundation versão 4 (WF4) requer autenticação de declarações, que o PSI não suporta diretamente. Isso significa que você não pode usar o PSI para criar um projeto no Project Server 2013 que tenha um tipo de projeto corporativo (EPT) com uma definição de fluxo de trabalho do WF4.
  
Você pode usar o PSI para criar projetos com o EPTs que não têm fluxos de trabalho ou usar uma definição herdada do WF 3.5 (a versão do fluxo de trabalho no Project Server 2010). Para criar um projeto com um EPT que tenha uma definição de WF4, use o CSOM.
  
 **Ações que exigem o Project Professional:**
  
A lista a seguir são itens que nem o PSI nem o CSOM podem fazer.
  
#### <a name="local-data"></a>Dados locais

- Manipulação de dados em projetos locais (arquivos. mpp). Por exemplo, definir as tabelas de taxas de custo ou os contornos de disponibilidade para recursos locais. 
    
- Definir ou editar calendários base ou calendários de recursos locais, incluindo exceções de calendário.
    
- Definição de campos personalizados locais. (O PSI oferece suporte à edição de valores de campos personalizados locais em tarefas, recursos e atribuições.)
    
#### <a name="enterprise-data"></a>Dados da empresa

- Fazer check-out ou editar o modelo global da empresa. Os dados globais da empresa no Project Server 2013 são um conjunto de tabelas de dados binários no banco de dados do Project, e não um modelo de projeto, como no Office Project Server 2007 e versões anteriores.
    
- Definição ou edição de calendários da empresa. Os métodos de [calendário](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) gerenciam apenas exceções de calendário. 
    
#### <a name="master-projects-and-cross-project-links"></a>Projetos mestres e links entre projetos

- Criação de projetos mestres e inserção de subprojetos.
    
- Agendamento de um caminho crítico em um projeto mestre. 
    
- Criar vínculos entre projetos.
    
#### <a name="resources"></a>Recursos

- Solicitação ou execução de redistribuição de recursos.
    
- Alterar o recurso em uma atribuição. (Você pode usar o PSI para excluir a atribuição e criar uma nova.)
    
- Excluir ou substituir um recurso que tem o trabalho real aceito (reals).
    
- Alterar um tipo de recurso entre trabalho, material e custo.
    
- Criando ou editando calendários de recursos.
    
- Ao adicionar um recurso a uma tarefa, a PSI não redistribui automaticamente o funcionamento do Project Professional. O desenvolvedor pode escolher e definir explicitamente a distribuição de trabalho nas atribuições.
    
#### <a name="cost-resources"></a>Cost resources

- Edição, criação ou exclusão de recursos de custo e atribuições usando os métodos de [projeto](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) . Os métodos de [recurso](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) podem criar recursos de custo, mas não editá-los. 
    
#### <a name="work-contours"></a>Delimitações de trabalho

- Edição de dados divididos em fases.
    
    > [!NOTE]
    > O método [updateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) no serviço Web de **status** pode editar dados efetivos dividido em fases nas atribuições depois que o gerente de projeto atualiza e publica os dados de atribuição. 
  
- Definir ou alterar o tipo de contorno da atribuição (como simples, carregado de volta ou carregado).
    
#### <a name="baselines-and-earned-value"></a>Linhas de base e valor acumulado

- Salvar uma linha de base ou editar dados de linha de base. 
    
- Definir uma data de progresso.
    
- Cálculo da variância e do valor acumulado. 
    
#### <a name="interactive-scheduling"></a>Agendamento interativo

- Suporte à programação interativa. (Como o Project Server trata as interações de forma assíncrona, o agendamento interativo deve ser feito com o Project Professional.)
    
    > [!NOTE]
    > Para evitar a alteração do comportamento de programação, os métodos de PSI que são trazidos para frente a partir do Project Server 2010 agem da mesma maneira no Project Server 2013. Por exemplo, o [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) ainda tem as mesmas limitações e usa o mecanismo de agendamento do lado do servidor mais antigo. O novo método [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) remove muitas dessas limitações e usa o novo mecanismo de agendamento do servidor do project Server 2013, que é o mesmo mecanismo de agendamento do project Professional 2013. 
  
#### <a name="wbs"></a>EDT

- Definição de uma máscara de código de estrutura de detalhamento de trabalho (EDT). 
    
#### <a name="tasks"></a>Tarefas

- Alterar o tipo de tarefa (trabalho fixo, duração ou unidades).
    
- Alterar se uma tarefa é controlada pelo empenho.
    
- Alteração da acumulação de custo fixo da tarefa.
    
- Alterar o conteúdo do campo [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) . O PSI pode ler apenas a parte de texto das anotações de tarefa, que são dados binários. rtf. No enTanto, você pode editar anotações de atribuição ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ), que são dados de texto. O banco de dados de relatórios não inclui anotações sobre tarefas ou atribuições. 
    
- Criar ou editar tarefas recorrentes.
    
- Atribuir ou alterar o calendário de tarefas em tarefas existentes.
    
- Criar uma nova tarefa com um calendário de tarefas.
    
- Alterar o valor do campo [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) (Task ignora o calendário de recursos). 
    
- Alterar o status ativo de uma tarefa usando o [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , se forem feitas alterações adicionais na mesma chamada. Para obter mais informações, consulte o *planejamento de projeto na seção servidor* na programação do [Project Server](project-server-programmability.md).
    
#### <a name="summary-tasks"></a>Tarefas de resumo

- Criar ou alterar atribuições em tarefas de resumo.
    
    > [!NOTE]
    > Recomendamos que você não faça atribuições em tarefas de resumo usando o Project Professional ou qualquer outra maneira. Para obter mais informações, consulte o *planejamento de projeto na seção servidor* na programação do [Project Server](project-server-programmability.md). 
  
- Edição campos de tarefa de resumo que são normalmente acumulados a partir da subtarefa. Projetos do lado do servidor sempre acumulam informações resumidas, em vez de definir informações sobre a tarefa de resumo e enviá-las para as subtarefas. Você pode editar apenas os seguintes campos nas tarefas de Resumo:
    
  - Dependências de tarefas
    
  - Campos personalizados de não-fórmula
    
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
    
Para a tarefa de resumo do projeto, as limitações PSI são as mesmas do Project Professional. O PSI pode editar atribuições de orçamento, incluindo orçamentos de custo.
  
#### <a name="project-level-calculation-options"></a>Opções de cálculo no nível do projeto

- Alterar um tipo de projeto entre cronograma de início (SFS) e agendar de término (SFF). (O PSI pode criar um projeto como o SFS ou o SFF, mas depois de criá-lo só pode ser alterado no Project Professional.)
    
- Alterar o calendário base do projeto ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) após a criação do projeto. 
    
- Alterar opções para cálculos. Você pode usar o PSI para definir as opções de cálculo a seguir quando o projeto é criado, mas alterar as opções requer o Project Professional. (No modo de exibição Backstage, escolha **Opções**e, em seguida, escolha a guia **agenda** na caixa de diálogo **Opções do projeto** .) 
    
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
- [Autenticação remota no SharePoint online usando autenticação baseada em declarações](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)  
- [Suplementos do Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) 
    

