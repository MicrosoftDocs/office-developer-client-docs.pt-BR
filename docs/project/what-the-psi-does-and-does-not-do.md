---
title: O que o PSI faz e não faz
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: O Project Server Interface (PSI) pode ajudar a automatizar muitos processos do servidor em instalações de local do Project Server 2013. Porém, várias funções exigem o uso do Microsoft Project Professional 2013.
ms.openlocfilehash: 0afdcdf43c4748fff42f7b5bc74af6c4b59b0b07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771186"
---
# <a name="what-the-psi-does-and-does-not-do"></a>O que o PSI faz e não faz

O Project Server Interface (PSI) pode ajudar a automatizar muitos processos do servidor em instalações de local do Project Server 2013. Porém, várias funções exigem o uso do Microsoft Project Professional 2013.
  
|||
|:-----|:-----|
|||
   
A PSI destina-se complementam os recursos do Project Professional 2013, ao invés de oferecer uma alternativa baseada em servidor para todas as funções do Project Professional. Desenvolvedores de terceiros podem usar a PSI para ajudar a criar Web Parts para instalações do local do Project Web App e espaços de trabalho de projeto, criar aplicativos personalizados do Windows e os aplicativos web que interagem com dados do Project Server no local, desenvolver o fluxo de trabalho a lógica para gerenciamento de portfólio de projetos, desenvolver manipuladores de evento de confiança total local e integrar o Project Server com outros aplicativos. A PSI não pode ser usada para o desenvolvimento de aplicativos para o Office Store, dispositivos móveis ou tablets; Para fazer isso, você pode usar o modelo de objeto do cliente (CSOM).
  
> [!NOTE]
> A PSI fornece uma interface de programação mais abrangente do Project Server 2013 que fornece o CSOM. Porém, a menos que o CSOM não fornece a funcionalidade necessária, é recomendável que você use o CSOM para desenvolver novos aplicativos. Para obter mais informações, consulte [o que o CSOM e não faz](what-the-csom-does-and-does-not-do.md). 
  
## <a name="usage-scenarios-for-the-psi"></a>Cenários de uso para a PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

A seguir estão exemplos de alguns aplicativos que ofereça suporte a PSI, para projetos do lado do servidor e os cálculos:
  
- **Automatize a criação ou o gerenciamento de entidades no Project Server** Embora o Project Professional 2013 e Project Web App juntas são projetados para lidar com o gerenciamento e a criação de entidades como projetos, campos personalizados e recursos da empresa, geralmente, há casos em que um aplicativo personalizado pode economizar tempo com em massa ou trabalhos repetitivos. A PSI pode automatizar vários tipos de trabalhos que não faz o CSOM, por exemplo, com os cubos OLAP, análises de portfólio do project, fatores comerciais, notificações, provedores de vínculo de objeto, segurança e interoperabilidade do SharePoint. 
    
- **Obter dados no publicado ou tabelas de arquivamento do banco de dados do Project** Porque o banco de dados direto acessar o rascunho, publicado e arquivar tabelas não é suportado, você pode usar a PSI para ler os dados que não está disponíveis nas tabelas ou modos de exibição de relatórios. Por exemplo, obter informações sobre versões do projeto, datas e alterações que são armazenadas nas tabelas de arquivamento e preencher um controle de JS Grid em uma web part com as informações. 
    
- **Validar dados de status e quadro de horários** Use a PSI locais manipuladores de eventos prévia para validar os dados de status ou quadro de horários de atribuição que os usuários digitam, antes que os dados são salvos no Project Web App. 
    
- **Projetos de manutenção** Crie projetos usem com planos de recurso de espaço reservado. Catálogo ou reserva tempo contra recursos para o trabalho de manutenção ou business base. Projetos de manutenção geralmente não têm tarefas. 
    
- **Criar projetos de financeiros** Crie projetos para captura de tempo por meio do quadro de horários para integração com um sistema financeiro. Crie uma hierarquia de códigos financeiros que refletem a estrutura de divisão de custo do sistema financeiro. Projetos financeiros não exigem atualizações de status ou de agendamento. 
    
- **Integra-se com sistemas de contabilidade** Capture os custos de recursos e as despesas com projetos para alimentar sistemas de cobrança e financeiros e para fins de comparação de orçamento associadas. Sincronize tarefas, recursos e atribuições entre os sistemas. Capturar dados de quadro de horários em um sistema para alimentar outra (qual quadro de horários é usado depende das necessidades da organização ou de projetos individuais). 
    
- **Automatize as atualizações dos membros da equipe** Para projetos que não são gerenciados ativamente, atualize automaticamente os projetos no servidor com o progresso e outras alterações de membros da equipe de projeto. Projetos podem ser atualizados e republicados sem revisão dos resultados ou fazer ajustes ao plano de um gerente de projeto. 
    
- **Avaliar o Project Server dados nos manipuladores de eventos de confiança total local** Um manipulador de eventos local para o pré-evento de **ProjectCreating** pode usar os dados do Project Server de PSI para ajudar a determinar se deseja cancelar um evento. Por exemplo, antes de criar um projeto, compare a proposta de projeto com projetos existentes. 
    
- **Criar atividades de fluxo de trabalho personalizado para gerenciamento de demanda** Use a PSI em atividades de fluxo de trabalho local, confiança total para modificar e atualizar propostas de projeto com base em modelos de projeto corporativo. Use os campos personalizados do projeto para marcar o projeto com as informações necessárias para que o processo de inicialização e aprovação. Adicione tarefas para identificar as fases de projeto para principais marcos ou resultados finais. Quando são aprovadas propostas de projeto, um fluxo de trabalho pode alterar as propostas em projetos de larga escala que são gerenciados com o Project Professional. 
    
- **Extensões de criar PSI** (**Preteridos.** Extensões são reduzidas no Project Server 2013 e não serão suportadas em versões futuras.) A PSI pode ser estendida com serviços personalizados usando a interface do Windows Communication Foundation (WCF). Extensões PSI executado no computador do Project Server e podem usar a mesma infraestrutura de segurança que usam os serviços PSI internos. Extensões podem consultar as tabelas de relatório, use as tabelas de banco de dados separado, consolidar chamadas PSI para salvar a largura de banda e integração com aplicativos de terceiros e outros componentes do lado do servidor. Para obter mais informações, consulte [Desenvolvendo extensões de PSI](http://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx).
    
- **Representação de uso no locais, confiança total de aplicativos** Chamadas para a interface WCF de PSI podem ser representadas, para que as permissões de segurança do usuário representado supõe que um aplicativo. Representação deve ser usada com moderação e cuidadosamente. Lendo e atualizando as informações de status para outros usuários não exigem representação. Novos aplicativos que exigem a representação devem usar o protocolo de OAuth e CSOM do, em vez da PSI. Para obter mais informações sobre representação com a PSI, consulte [Usar representação com WCF](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).
    
> [!NOTE]
> Em alguns casos, a PSI pode ser utilizada nos aplicativos de cliente com o CSOM e o Project Online. Se você usar um serviço da web com base em ASMX PSI, o aplicativo deve incluir um método para autenticar o objeto [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) em CSOM do e um método para autenticar o ** System.Web.Services.Protocols.SoapHttpClientProtocol** o objeto de cliente. Para obter um exemplo que usa um serviço web com o CSOM do SharePoint, consulte [Autenticação remota no SharePoint Online Using Claims-Based autenticação](http://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx). > Causa de permissões restritas em nível de aplicativo, a PSI não pode ser usada nos aplicativos que foram projetados para distribuição no Office Store pública. Nesse caso, você pode usar somente o CSOM. 
  
## <a name="what-the-psi-does-not-do"></a>O que a PSI não faz
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Embora existam muitas coisas que a PSI pode fazer, há algumas coisas que a PSI não faz. Estes são duas coisas a PSI não podem fazer, mas pode ser feito o CSOM.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online e receptores de evento remoto

A limitação principal a PSI é ao Project Online. Aplicativos que usam a PSI requerem acesso de confiança total para uma instalação local do Project Server. Por exemplo, a PSI não pode ser usada em receptores de evento remoto, onde o receptor de evento está instalado como um serviço no Microsoft Azure.
  
### <a name="workflows-and-claims-authentication"></a>Autenticação de declarações e fluxos de trabalho

Uma definição de fluxo de trabalho que usa a versão do Windows Workflow Foundation 4 (WF4) requer autenticação de declarações, o qual a PSI não oferece suporte direto. Isso significa que você não pode usar a PSI para criar um projeto no Project Server 2013 que tenha um tipo de projeto corporativo (EPT) com uma definição de fluxo de trabalho WF4.
  
Você pode usar a PSI para criar projetos com os EPTs que não têm nenhum fluxo de trabalho ou usam uma definição de WF3.5 herdada (a versão do fluxo de trabalho no Project Server 2010). Para criar um projeto com um EPT que tem uma definição de WF4, use o CSOM.
  
 **Ações que requerem o Project Professional:**
  
A lista a seguir são os que não a PSI nem o CSOM pode fazer.
  
#### <a name="local-data"></a>Dados locais

- Manipulação de dados em projetos locais (arquivos. mpp). Por exemplo, definindo as tabelas de taxas de custo ou delimitações de disponibilidade de recursos locais. 
    
- Definindo ou editando calendários base locais ou calendários de recursos, incluindo as exceções de calendário.
    
- A definição de campos personalizados locais. (A PSI suporta a edição de valores de campo personalizado local em recursos, tarefas e atribuições.)
    
#### <a name="enterprise-data"></a>Dados corporativos

- Fazer check-out ou Editar modelo global da empresa. Os dados globais da empresa no Project Server 2013 são um conjunto de dados binários tabelas no banco de dados do Project, não um modelo de projeto, como no Office Project Server 2007 e versões anteriores.
    
- Definindo ou editando calendários da empresa. Os métodos de [calendário](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) gerenciam somente as exceções de calendário. 
    
#### <a name="master-projects-and-cross-project-links"></a>Projetos mestres e links entre projetos

- Criar projetos mestres e inserção de subprojetos.
    
- Agendar um caminho crítico entre um projeto mestre. 
    
- Criação de links entre projetos.
    
#### <a name="resources"></a>Resources

- Solicitando ou realizando a redistribuição de recursos.
    
- Alterando o recurso em uma atribuição. (Você pode usar a PSI para excluir a atribuição e crie um novo).
    
- Excluir ou substituir um recurso que possui o trabalho real aceitos (dados efetivos).
    
- Alterar um tipo de recurso entre o trabalho, material e custo.
    
- Criando ou editando calendários de recursos.
    
- Ao adicionar um recurso a uma tarefa, a PSI não redistribuir automaticamente funciona da maneira que Project Professional. É até o desenvolvedor para escolher e definir explicitamente a distribuição de trabalho nas atribuições.
    
#### <a name="cost-resources"></a>Recursos de custo

- Editando, criar ou excluir recursos de custo e atribuições usando os métodos de [projeto](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) . Os métodos de [recurso](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) podem criar recursos de custo, mas não podem editá-los. 
    
#### <a name="work-contours"></a>Delimitações de trabalho

- Editando dados divididos em fases.
    
    > [!NOTE]
    > O método [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) no serviço da Web de **status** pode editar dados efetivos de divisão em fases nas atribuições depois que o gerente de projeto atualiza e publica os dados de atribuição. 
  
- Configurando ou alterando a atribuição delimitar tipo (por exemplo, o plano, back-carregado ou delimitação).
    
#### <a name="baselines-and-earned-value"></a>Linhas de base e valor acumulado

- Salvar linha de base ou editando dados de linha de base. 
    
- Definindo uma data de andamento.
    
- Cálculo de variação e valor acumulado. 
    
#### <a name="interactive-scheduling"></a>Agendamento interativo

- Oferecendo suporte ao agendamento interativo. (Porque o Project Server manipula interações de forma assíncrona, interativo de agendamento deve ser feito com o Project Professional.)
    
    > [!NOTE]
    > Para evitar a alterar o comportamento de programação, os métodos PSI são trazidos direta do Project Server 2010 agir da mesma maneira no Project Server 2013. Por exemplo, [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) ainda tem as mesmas limitações e usa o mecanismo de agendamento mais antigo do lado do servidor. O novo método de [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) remove muitas dessas limitações e usa o novo Project Server 2013 no servidor mecanismo de agendamento, que é o mesmo mecanismo de agendamento que esteja no Project Professional 2013. 
  
#### <a name="wbs"></a>WBS

- Definindo uma máscara de código de estrutura (EDT) de divisão de trabalho. 
    
#### <a name="tasks"></a>Tarefas

- Alterando o tipo de tarefa (trabalho fixo, duração ou unidades).
    
- Alterando se uma tarefa é controlada pelo esforço.
    
- Alterando acumulação de custo fixo da tarefa.
    
- Alterando o conteúdo do campo [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) . A PSI pode ler somente a parte de texto das anotações de tarefa, que são dados binários. rtf. Porém, você pode editar as anotações das atribuições ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ), que são os dados de texto. O banco de dados de relatórios não inclui anotações da tarefa ou atribuição. 
    
- Criando ou editando tarefas recorrentes.
    
- Atribuindo ou alterando o calendário de tarefas em tarefas existentes.
    
- Criando uma nova tarefa com um calendário de tarefa.
    
- A alteração do valor do campo [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) (tarefa ignora o calendário de recursos). 
    
- Alterando o status ativo de uma tarefa usando [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , se alterações adicionais são feitas na mesma chamada. Para obter mais informações, consulte a seção de *Agendamento de projetos no servidor* na [programação do Project Server](project-server-programmability.md).
    
#### <a name="summary-tasks"></a>Tarefas de resumo

- Criando ou alterando atribuições nas tarefas de resumo.
    
    > [!NOTE]
    > Recomendamos que você não faça atribuições nas tarefas de resumo usando o Project Professional ou qualquer outro método. Para obter mais informações, consulte a seção de *Agendamento de projetos no servidor* na [programação do Project Server](project-server-programmability.md). 
  
- Editando campos de tarefa de resumo que normalmente forem acumulados de subtarefa. No servidor de projetos sempre acumulam informações de resumo, em vez de informações de configuração da tarefa de resumo e publicando-o para baixo até as subtarefas. Você pode editar os seguintes campos nas tarefas de resumo:
    
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
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (definir o valor somente quando a criação da tarefa) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
Para a tarefa de resumo do projeto, as limitações de PSI são iguais do Project Professional. A PSI pode editar atribuições de orçamento — incluindo orçamentos de custo.
  
#### <a name="project-level-calculation-options"></a>Opções de cálculo de nível de projeto

- Alterar um tipo de projeto entre o agendamento de iniciar (SFS) e agendamento do término (SFF). (A PSI pode criar um projeto como uma busca de site Catalogado ou SFF, mas uma vez criado ele pode ser alterado somente no Project Professional.)
    
- Alterando o calendário base do projeto ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) após a criação do projeto. 
    
- Alterando as opções para cálculos. Você pode usar a PSI para definir as seguintes opções de cálculo quando o projeto é criado, mas alterar as opções requer o Project Professional. (No modo de exibição Backstage, escolha **Opções**e, em seguida, escolha a guia **agenda** na caixa de diálogo **Opções do projeto** ). 
    
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
<a name="pj14_WhatPSIDoes_AR"> </a>

- [O que o CSOM faz e não faz](what-the-csom-does-and-does-not-do.md)
    
- [Programabilidade do Project Server](project-server-programmability.md)
    
- [Autenticação remota no SharePoint Online usando autenticação baseada em declarações](http://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)
    
- [Suplementos do Office](http://msdn.microsoft.com/library/1e123201-6e70-45c1-a48c-d5b955896ddb%28Office.15%29.aspx)
    

