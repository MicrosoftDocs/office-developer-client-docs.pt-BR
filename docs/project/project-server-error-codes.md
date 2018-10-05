---
title: Códigos de erro do Project Server
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- error codes
- errors
- Project Server errors
- PSErrorID
- PSI errors
keywords:
- PSI, códigos de erro, códigos de erro, Project Server, PSErrorID, Interface do Project Server, códigos de erro de códigos, Project Server, de erro
localization_priority: Normal
ms.assetid: db78a09c-ebef-47cc-8623-40abe117aa08
description: Este tópico contém tabelas de códigos de erro para o Project Server Interface (PSI) no Project Server 2013. As tabelas são organizadas por área funcional e pelo intervalo de códigos de erro.
ms.openlocfilehash: 7fdfafa562492fe4d5671f1335ca58cf50c91e88
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401780"
---
# <a name="project-server-error-codes"></a>Códigos de erro do Project Server

Este tópico contém tabelas de códigos de erro para o Project Server Interface (PSI) no Project Server 2013. As tabelas são organizadas por área funcional e pelo intervalo de códigos de erro.
   
Processos do Project Server 2013 e métodos PSI tiverem números de código de erro que geralmente são organizados por área funcional. A enumeração [Microsoft.Office.Project.Server.Library.PSErrorID](https://msdn.microsoft.com/library/microsoft.office.project.server.library.pserrorid_di_pj14mref(v=office.14).aspx) é duplicada em [WebSvcProject.PSErrorID](https://msdn.microsoft.com/library/office/websvcproject.pserrorid_di_pj14mref.aspx); eles listam os códigos de erro em ordem alfabética por nome. Este tópico lista os códigos de erro nas tabelas que são organizadas por classe PSI ou área funcional e pelo número de identificador (ID) de erro. 
  
> [!NOTE]
>  Muitos dos códigos de erro são gerais e podem ter várias causas possíveis. Para saber mais sobre erros, você poderá fazer o seguinte: 
> - Para aplicativos baseados em ASMX, use **System.Web.Services.Protocols.SoapException** com o objeto **PSClientError** para mostrar uma lista ou hierarquia de erros em uma chamada ao método da PSI. Consulte [Exemplo de código de erro para ASMX](#pj15_ErrorCodes_ASMXExample). 
> - Para aplicativos baseados em WCF, você poderá usar **System.ServiceModel.FaultException** para obter um objeto **PSClientError** e também para obter informações de erro adicionais. Consulte [Exemplo de código de erro para WCF](#pj15_ErrorCodes_WCFExample). 
> - Use o log de eventos de aplicativo no computador do Project Server.
> - Use os logs de rastreamento de serviço de log unificado (ULS). Para obter uma explicação, consulte a seção de *Verificação de erros* no [Guia de Introdução ao desenvolvimento para Project 2010](https://msdn.microsoft.com/library/gg607685.aspx). 
> - Para obter mais informações sobre como usar os logs ULS, consulte o artigo do blog de suporte do Project [Project Server 2010: o que esperar quando você obtiver o inesperado](https://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx)e pesquisar o blog de "leitura ULS logs". 
> - Para ajudar a localizar ou assista a problemas específicos nos dados do ULS, use o [Visualizador do ULS](https://www.codeproject.com/Articles/458052/ULS-Log-Viewer). 
> - Use o Microsoft SQL Server Profiler para ajudar a capturar ou a monitorar erros de banco de dados. Para saber mais, consulte [SQL Server Profiler](https://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx). 
> - Muitos dos códigos de erro são usados apenas internamente. Por exemplo, como os serviços Web **ExchangeSync** e **PWA** não têm suporte para desenvolvimento de terceiros, provavelmente você não verá códigos de erro de métodos nessas áreas, como os métodos **Rules** e **StatusReports**. No entanto, as tabelas deste artigo incluem todos os códigos de erro do Project Server. 
  
## <a name="table-1-error-code-functional-areas-and-related-number-ranges"></a>Tabela 1. Áreas funcionais de código de erro e intervalos de números relacionados

|Área funcional do Project Server|Intervalos de números de códigos de erro|
|:-----|:-----|
|[Tabela 3: Códigos de erros gerais](#pj15_ErrorCodes_General) <br/> |0 - 99; 500 - 999; 9131; 10000 - 10099; 20000 - 20099; 26000 - 26099  <br/> |
|[Tabela 4: Cache ativo](#pj15_ErrorCodes_ActiveCache) <br/> |12000 - 12099  <br/> |
|[Tabela 5: Sincronização do Active Directory](#pj15_ErrorCodes_ActiveDirectory) <br/> |27000 - 27999  <br/> |
|[Tabela 6: Serviço Web de Administração](#pj15_ErrorCodes_Admin) <br/> |16600 - 16699; 19011, 19012 e 19032; 20003 e 25000 - 25099  <br/> |
|[Tabela 7: Arquivo Morto (backup e restauração)](#pj15_ErrorCodes_Archive) <br/> |25000 - 25999 e 29000 - 29099  <br/> |
|[Tabela 8: Atribuições](#pj15_ErrorCodes_Assignments) <br/> |120 - 199  <br/> |
|[Tabela 9: Calendário](#pj15_ErrorCodes_Calendar) <br/> |77 e 13000 - 13999  <br/> |
|[Tabela 10: Serviço de Criação do Cubo (CBS)](#pj15_ErrorCodes_CBS) <br/> |17000 - 17999  <br/> |
|[A tabela 11: Check-in - check-out](#pj15_ErrorCodes_CICO) <br/> |10100 - 10199  <br/> |
|[Tabela 12: Campos personalizados](#pj15_ErrorCodes_CustomFields) <br/> |11500 - 11999  <br/> |
|[Tabela 13: Tabelas de pesquisa](#pj15_ErrorCodes_LookupTables) <br/> |11000 - 11499  <br/> |
|[Tabela 14: Diversos](#pj15_ErrorCodes_Miscellaneous) <br/> |11000 - 11499  <br/> |
|[Tabela 15: Notificações](#pj15_ErrorCodes_Notifications) <br/> |16000 - 16599  <br/> |
|[Tabela 16: Otimizador](#pj15_ErrorCodes_Optimizer) (análise de portfólio de projeto)  <br/> |29000 - 29999  <br/> |
|[Tabela 17: Planejador](#pj15_ErrorCodes_Planner) (análise de portfólio de projeto)  <br/> |28000 - 28999  <br/> |
|[Tabela 18: Projetos](#pj15_ErrorCodes_Projects) <br/> |100 - 499; 1000 - 1199; 9100 - 9199; e 23000-23999  <br/> |
|[Tabela 19: Serviço de Dados de Relatório](#pj15_ErrorCodes_RDS) (RDS)  <br/> |24000 - 24999  <br/> |
|[Tabela 20: Recursos](#pj15_ErrorCodes_Resources) <br/> |2000 - 2999  <br/> |
|[Tabela 21: Planejamentos de recursos](#pj15_ErrorCodes_ResourcePlans) <br/> |30000 - 30999  <br/> |
|[Tabela 22: Regras](#pj15_ErrorCodes_Rules) <br/> |21000 - 21099  <br/> |
|[Tabela 23: Segurança](#pj15_ErrorCodes_Security) <br/> |19000 - 19099  <br/> |
|[Tabela 24: Eventos de servidor](#pj15_ErrorCodes_Events) <br/> |19033 e 22000 - 22999  <br/> |
|[Tabela 25: Status](#pj15_ErrorCodes_Statusing) <br/> |3100 - 3199  <br/> |
|[Tabela 26: Relatórios de status](#pj15_ErrorCodes_StatusReports) <br/> |12100 - 12299  <br/> |
|[Tabela 27: Tarefas](#pj15_ErrorCodes_Tasks) <br/> |7000 - 7099  <br/> |
|[Tabela 28: Quadros de horários](#pj15_ErrorCodes_Timesheets) <br/> |3200 - 3299  <br/> |
|[Tabela 29: Delegação de usuário](#pj15_ErrorCodes_UserDelegation) <br/> |43000 - 43500  <br/> |
|[Tabela 30: Fluxo de trabalho](#pj15_ErrorCodes_Workflow) <br/> |35000 - 35999: Fluxo de trabalho  <br/> |
|[Tabela 31: WSSInterop e ObjectLinkProvider (integração do SharePoint)](#pj15_ErrorCodes_WSS) <br/> |16400 - 16499: Integração e espaços de trabalho de projeto do SharePoint  <br/> 18000 - 18099: Importação de projeto do Object Link Provider e do SharePoint  <br/> |
   
## <a name="table-2-error-code-table-by-number-range"></a>Tabela 2. Tabela de códigos de erro por intervalo de números

|Intervalo de códigos de erro|Tabela de códigos de erros|
|:-----|:-----|
|0 - 99  <br/> |[Tabela 3: Códigos de erro gerais](#pj15_ErrorCodes_General), exceto 77, que está na [Tabela 9: Calendário](#pj15_ErrorCodes_Calendar) <br/> |
|100 - 119  <br/> |[Tabela 18: Projetos](#pj15_ErrorCodes_Projects) <br/> |
|120 - 199  <br/> |[Tabela 8: Atribuições](#pj15_ErrorCodes_Assignments) <br/> |
|500 - 999  <br/> |[Tabela 3: Códigos de erros gerais](#pj15_ErrorCodes_General) <br/> |
|1000 - 1199  <br/> |[Tabela 18: Projetos](#pj15_ErrorCodes_Projects) <br/> |
|2000 - 2999  <br/> |[Tabela 20: Recursos](#pj15_ErrorCodes_Resources) <br/> |
|3100 - 3199  <br/> |[Tabela 25: Status](#pj15_ErrorCodes_Statusing) <br/> |
|3200 - 3299  <br/> |[Tabela 28: Quadros de horários](#pj15_ErrorCodes_Timesheets) <br/> |
|7000 - 7099  <br/> |[Tabela 27: Tarefas](#pj15_ErrorCodes_Tasks) <br/> |
|9100 - 9199  <br/> |[Tabela 18: Projetos](#pj15_ErrorCodes_Projects), exceto 9131, que está em [Tabela 3: Códigos de erro gerais](#pj15_ErrorCodes_General) <br/> |
|10000 - 10099  <br/> |[Tabela 3: Códigos de erros gerais](#pj15_ErrorCodes_General) <br/> |
|10100 - 10199  <br/> |[A tabela 11: Check-in - check-out](#pj15_ErrorCodes_CICO) <br/> |
|11000 - 11499  <br/> |[Tabela 13: Tabelas de pesquisa](#pj15_ErrorCodes_LookupTables) <br/> |
|11500 - 11999  <br/> |[Tabela 12: Campos personalizados](#pj15_ErrorCodes_CustomFields) <br/> |
|12000 - 12099  <br/> |[Tabela 4: Cache ativo](#pj15_ErrorCodes_ActiveCache) <br/> |
|12100 - 12299  <br/> |[Tabela 26: Relatórios de status](#pj15_ErrorCodes_StatusReports) <br/> |
|13000 - 13999  <br/> |[Tabela 9: Calendário](#pj15_ErrorCodes_Calendar) <br/> |
|16000 - 16399  <br/> |[Tabela 15: Notificações](#pj15_ErrorCodes_Notifications) <br/> |
|16400 - 16499  <br/> |[Tabela 31: WssInterop e Object Link Provider (integração do SharePoint)](#pj15_ErrorCodes_WSS) <br/> |
|16600 - 16699  <br/> |[Tabela 6: Serviço Web de Administração](#pj15_ErrorCodes_Admin) <br/> |
|17000 - 17999  <br/> |[Tabela 10: Serviço de Criação do Cubo (CBS)](#pj15_ErrorCodes_CBS) <br/> |
|18000 - 18099  <br/> |[Tabela 31: Integração do SharePoint](#pj15_ErrorCodes_WSS) <br/> |
|19000 - 19099  <br/> |[Tabela 23: Segurança](#pj15_ErrorCodes_Security), exceto 19011, 19012 e 19032, que são códigos relacionados a segurança na [Tabela 6: Serviço Web de Administração](#pj15_ErrorCodes_Admin) <br/> |
|20000 - 20099  <br/> |[Tabela 3: Códigos de erro gerais](#pj15_ErrorCodes_General), exceto 20003, que está na [Tabela 6: Serviço Web de Administração](#pj15_ErrorCodes_Admin) <br/> |
|21000 - 21099  <br/> |[Tabela 22: Regras](#pj15_ErrorCodes_Rules) <br/> |
|22000 - 22999  <br/> |[Tabela 24: Eventos de servidor](#pj15_ErrorCodes_Events) <br/> |
|23000 - 23999  <br/> |[Tabela 18: Projetos](#pj15_ErrorCodes_Projects) <br/> |
|24000 - 24999  <br/> |[Tabela 19: Serviço de Dados de Relatório](#pj15_ErrorCodes_RDS) (RDS)  <br/> |
|25000 - 25999  <br/> |[Tabela 7: Arquivo Morto (backup e restauração)](#pj15_ErrorCodes_Archive), exceto 25004, 25006, que estão na [Tabela 6: Serviço Web de Administração](#pj15_ErrorCodes_Admin) <br/> |
|26000 - 26099  <br/> |[Tabela 3: Códigos de erros gerais](#pj15_ErrorCodes_General) <br/> |
|27000 - 27999  <br/> |[Tabela 5: Sincronização do Active Directory](#pj15_ErrorCodes_ActiveDirectory) <br/> |
|28000 - 28999  <br/> |[Tabela 17: Planejador](#pj15_ErrorCodes_Planner) (análise de portfólio de projeto)  <br/> |
|29000 - 29999  <br/> |[Tabela 16: Otimizador](#pj15_ErrorCodes_Optimizer) (análise de portfólio de projeto), exceto 29021, que está na [Tabela 7: Arquivo Morto](#pj15_ErrorCodes_Archive) <br/> |
|30000 - 30999  <br/> |[Tabela 21: Planejamentos de recursos](#pj15_ErrorCodes_ResourcePlans) <br/> |
|31000 - 31999  <br/> 32000 - 32100  <br/> |[Tabela 14: Diversos](#pj15_ErrorCodes_Miscellaneous) (Auditoria; não usada)  <br/> Páginas de detalhes do projeto  <br/> |
|35000 - 35999  <br/> 40000 - 40499  <br/> |[Tabela 30: Fluxo de trabalho](#pj15_ErrorCodes_Workflow) <br/> |
|40500 - 40999  <br/> 42000 - 42999  <br/> |[Tabela 14: Diversos](#pj15_ErrorCodes_Miscellaneous) (**ExchangeSync**; uso interno)  <br/> Linha do tempo do Project Web App  <br/> |
|43000 - 43500  <br/> |[Tabela 29: Delegação de usuário](#pj15_ErrorCodes_UserDelegation) <br/> |
|50000 - 51999  <br/> |[Tabela 14: Diversos](#pj15_ErrorCodes_Miscellaneous) (erros de banco de dados)  <br/> |

<a name="pj15_ErrorCodes_General"></a>

## <a name="table-3-general-error-codes"></a>Tabela 3. Códigos de erro gerais

|Código de erro geral|Descrição|
|:-----|:-----|
|NoError = 0; Success = 0  <br/> |Nenhum erro ou êxito.  <br/> |
|GeneralRequestInvalidParameter = 6  <br/> |Um dos nós ou parâmetros da solicitação não é válido ou não é válido no contexto da solicitação.  <br/> |
|GeneralInvalidValue = 11  <br/> |O valor da solicitação não é válido; por exemplo, um GUID especificado como 0.  <br/> |
|GeneralStartDateGTorEQFinishDate = 26  <br/> |O intervalo de datas especificado não é válido.  <br/> |
|GeneralQueueOperationInProcess = 29  <br/> |Erro genérico para uma operação que ainda está sendo processada na fila.  <br/> |
|GeneralUnhandledException = 42  <br/> |Ocorreu uma exceção sem tratamento.  <br/> |
|GeneralDuplicateGUIDSpecified = 66  <br/> |Há um GUID duplicado na solicitação.  <br/> |
|GeneralDateNotValid = 69  <br/> |As datas devem estar no intervalo entre 1/1/1984 e 12/12/2049.  <br/> |
|GeneralCostInvalid = 70  <br/> |Um parâmetro de custo não é válido.  <br/> |
|GeneralWorkInvalid = 71  <br/> |Um parâmetro de trabalho não é válido.  <br/> |
|GeneralDurationInvalid = 72  <br/> |Um parâmetro de duração não é válido.  <br/> |
|GeneralUnitsInvalid = 73  <br/> |A unidade especificada não é válida.  <br/> |
|GeneralOnlyInsertsAllowed = 74  <br/> |Somente inserções são permitidas.  <br/> |
|GeneralOnlyUpdatesAllowed = 75  <br/> |Somente atualizações são permitidas.  <br/> |
|GeneralSessionInvalid = 76  <br/> |O parâmetro de sessão não é válido.  <br/> |
|GeneralDependencyUidInvalid = 78  <br/> |O GUID de dependência não é válido.  <br/> |
|GeneralNumberInvalid = 79  <br/> |Um número não é válido.  <br/> |
|GeneralInvalidDataStore = 80  <br/> |O banco de dados especificado não existe. Use um banco de dados [DataStoreEnum](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.DataStoreEnum.aspx) .  <br/> |
|GeneralDurationOrWorkFormatInvalid = 513  <br/> |A duração ou o formato do trabalho não é válida.  <br/> |
|GeneralRateFormatInvalid = 518  <br/> |O formato da taxa não é válido.  <br/> |
|GeneralQueueException = 9131  <br/> |Exceção: há um erro geral no Serviço de Enfileiramento.  <br/> |
|GeneralItemDoesNotExist = 10000  <br/> |Um item especificado não existe.  <br/> |
|GeneralLCIDInvalid = 10001  <br/> |O identificador de localidade (ID do idioma) não é válido.  <br/> |
|GeneralRowDoesNotExist = 10002  <br/> |A linha especificada em uma **DataTable** não existe.  <br/> |
|GeneralInvalidColumnValue = 20000  <br/> |Um valor de coluna em uma **DataTable** não é válido.  <br/> |
|GeneralInvalidDataRowState = 20001  <br/> |Um estado do **DataRow** não é válido.  <br/> |
|GeneralDuplicatedNames = 20004  <br/> |Há um nome duplicado. Os nomes devem ser exclusivos.  <br/> |
|GeneralReadOnlyColumn = 20005  <br/> |A coluna é somente leitura.  <br/> |
|GeneralReadOnlyRow = 20006  <br/> |A linha é somente leitura.  <br/> |
|GeneralNotNullColumn = 20007  <br/> |A coluna não pode ser nula.  <br/> |
|GeneralObjectAlreadyExists = 20008  <br/> |O objeto já existe.  <br/> |
|GeneralInvalidObject = 20009  <br/> |O objeto não é válido.  <br/> |
|GeneralSecurityAccessDenied = 20010  <br/> |O acesso foi negado por causa das permissões de segurança.  <br/> |
|GeneralInvalidOperation = 20011  <br/> |A operação não é válida.  <br/> |
|GeneralInvalidCharacters = 20012  <br/> |Alguns caracteres não são válidos. O caractere de tabulação, além de caracteres a seguir não são válidos em um nome de projeto: ' \ / ":; < > | , . ' ? * #` <br/> |
|GeneralNameTooLong = 20013  <br/> |O nome é muito longo.  <br/> |
|GeneralNameCannotBeBlank = 20014  <br/> |O nome não pode ficar em branco. Não use uma cadeia de caracteres nula ou vazia.  <br/> |
|GeneralInvalidOperationOnReadOnlyValue = 20016  <br/> |A tentativa de operação em um valor somente leitura não é válida.  <br/> |
|GeneralInvalidDateOverlap = 20018  <br/> |A solicitação contém datas sobrepostas.  <br/> |
|GeneralParameterCannotBeNull = 20020  <br/> |O parâmetro não pode ser nulo.  <br/> |
|GeneralDescTooLong = 20021  <br/> |A descrição é muito longa.  <br/> |
|GeneralCategoryPermissionDenied = 20022  <br/> |A permissão de categoria foi negada.  <br/> |
|GeneralNotLicensed = 20024  <br/> |O usuário não é licenciado para o Project Server.  <br/> |
|GeneralGlobalPermissionDenied = 20023  <br/> |A permissão global foi negada.  <br/> |
|GeneralActionCanceledByEventHandler = 22000  <br/> |O manipulador de eventos cancelou a ação.  <br/> |
|GeneralActionCanceledBecauseServerEventServiceNotFound = 22001  <br/> |O Serviço de Eventos do Project Server não foi encontrado.  <br/> |
|GeneralActionCanceledBecauseServerEventServiceProblem = 22002  <br/> |Há um problema no Serviço de Eventos do Project Server.  <br/> |
|GeneralQueueJobFailed = 26000  <br/> |O trabalho de fila falhou.  <br/> |
|GeneralQueueInvalidJobUID = 26001  <br/> |O GUID do trabalho para a fila não é válido.  <br/> |
|GeneralQueueInvalidTrackingUID = 26002  <br/> |O GUID de rastreamento para a fila não é válido.  <br/> |
|GeneralQueueInvalidJobInfoUID = 26003  <br/> |O GUID de informações do trabalho para a fila não é válido.  <br/> |
|GeneralQueueInvalidCorrelationUID = 26004  <br/> |O GUID de correlação de fila não é válido.  <br/> |
|GeneralQueueCorrelationBlocked = 26005  <br/> |A correlação de fila está bloqueada.  <br/> |
|GeneralQueueInvalidMessageType = 26006  <br/> |O tipo de mensagem da fila não é válido.  <br/> |
|GeneralQueueInvalidJobState = 26007  <br/> |O estado do trabalho de fila não é válido.  <br/> |
|GeneralQueueInvalidGroupState = 26008  <br/> |O estado do grupo na fila não é válido.  <br/> |
|GeneralQueueInvalidGroupPriority = 26009  <br/> |A prioridade do grupo na fila não é válida.  <br/> |
|GeneralQueueInvalidCorrelationPriority = 26010  <br/> |A prioridade de correlação na fila não é válida.  <br/> |
|GeneralQueueInvalidQueueID = 26011  <br/> |O número de identificação da fila não é válido.  <br/> |
|GeneralQueueInvalidAdminAction = 26012  <br/> |A ação **Admin** não é válida para a fila.  <br/> |
|GeneralQueueInvalidStatType = 26013  <br/> |O tipo de status da fila não é válido.  <br/> |
|GeneralQueueInvalidBlockPolicy = 26014  <br/> |A política de bloqueio da fila não é válida.  <br/> |
|GeneralQueueCannotRetryJob = 26015  <br/> |A fila não pode repetir o trabalho.  <br/> |
|GeneralQueueInvalidSetting = 26016  <br/> |Uma configuração para a fila não é válida.  <br/> |
|GeneralQueueInvalidRendezvousUID = 26017  <br/> |O GUID de encontro da fila não é válido.  <br/> |
|GeneralDalErrorGettingConnectionStrings = 26018  <br/> |Erro ao obter cadeias de conexão para a camada de acesso a dados (DAL).  <br/> |
|GeneralDalErrorConnectingToDatabase = 26019  <br/> |Erro na conexão da DAL ao banco de dados.  <br/> |
|GeneralDalInvalidArgumentCountCreatingFilter = 26020  <br/> |O número de argumentos para a criação de um filtro não é válido.  <br/> |
|GeneralDataTableCannotBeNull = 26024  <br/> |Uma **DataTable** não pode ser **null**.  <br/> |
|GeneralDatasetConstraints = 26025  <br/> |Erro em restrições do **DataSet**.  <br/> |
|GeneralInvalidDataSetStructure = 26027  <br/> |A estrutura **DataSet** não é válida.  <br/> |
|GeneralDalNoRowsUpdated = 26028  <br/> |Nenhuma linha foi atualizada na camada de acesso a dados (DAL).  <br/> |
|GeneralDataTableCannotBeEmpty = 26029  <br/> |A **DataTable** não pode ficar vazia.  <br/> |
|GeneralWSSContentDBNotWritable = 26030  <br/> |Não é possível gravar no banco de dados de conteúdo do SharePoint. O banco de dados de conteúdo é somente leitura ou há um bloqueio no nível do conjunto de sites.  <br/> |
|GeneralSPValidateFormDigestError = 26031  <br/> |Erro ao validar o resumo do formulário em um retorno de chamada do Project Web App, geralmente devido a um tempo limite.  <br/> |
|GeneralDelegationActiveForCurrentUser = 26032  <br/> |O usuário atual tem uma delegação ativa. Este erro foi gerado por métodos da Web no serviço **WinProj** para o Project Professional.<br/> |

<a name="pj15_ErrorCodes_ActiveCache"></a>

## <a name="table-4-active-cache"></a>Tabela 4. Cache ativo

|Código de erro do cache ativo|Descrição|
|:-----|:-----|
|ActiveCacheInvalidDataFormat = 12000  <br/> |O formato de dados não é válido.  <br/> |
|ActiveCacheUnsupportedDataFormatVersion = 12001  <br/> |A versão do formato de dados não tem suporte.  <br/> |
|ActiveCacheInvalidQueuedMessageType = 12003  <br/> |O tipo de mensagem enfileirada não é válido.  <br/> |
|ActiveCacheNullQueuedMessage = 12004  <br/> |A mensagem enfileirada é nula.  <br/> |
|ActiveCacheQueuedMessageExecutionError = 12005  <br/> |Há um erro de execução para a mensagem enfileirada.  <br/> |
|ActiveCacheInvalidDataSize = 12006  <br/> |O tamanho dos dados não é válido.  <br/> |
|ActiveCacheQueueJobAlreadyStarted = 12007  <br/> |A fila de trabalhos já foi iniciada.  <br/> |
|ActiveCacheInvalidQueuedMessageFormat = 12008  <br/> |O formato da mensagem na fila não é válido.  <br/> |
|ActiveCacheUnsupportedQueuedMessageVersion = 12009  <br/> |A versão da mensagem na fila não é válida.  <br/> |
|ActiveCacheUnsupportedQueueDataType = 12011  <br/> |O tipo de dados na fila não tem suporte.  <br/> |
|ActiveCacheInvalidVersionStampForSave = 12012  <br/> |O carimbo de versão para a operação de salvamento não é válido.  <br/> |
|ActiveCacheProjectTypeMismatch = 12013  <br/> |O tipo de projeto não corresponde ao tipo esperado.  <br/> |
|ActiveCacheDataValidationFailed = 12014  <br/> |A validação de dados falhou.  <br/> |
|ActiveCacheUnsupportedProjectProfessionalVersion = 12015  <br/> |A versão do Project Professional não tem suporte.  <br/> |
|ActiveCacheGeneralSQLException = 12016  <br/> |Há um erro geral de SQL.  <br/> |

<a name="pj15_ErrorCodes_ActiveDirectory"></a>

## <a name="table-5-active-directory-synchronization"></a>Tabela 5. Sincronização do Active Directory

|Código de erro de sincronização do Active Directory|Descrição|
|:-----|:-----|
|AdSyncUpdateTimerJobFailed = 27002  <br/> |O trabalho do temporizador de atualização falhou para a sincronização com serviços de diretório do Active Directory.  <br/> |
|AdSyncDeleteTimerJobFailed = 27003  <br/> |O trabalho do temporizador de exclusão falhou para a sincronização com o Active Directory.  <br/> |
|AdSyncAdConnectFail = 27006  <br/> |Não é possível se conectar ao Active Directory.  <br/> |
|AdMaximumGroupsCountExceeded = 27007  <br/> |A contagem máxima de grupos foi excedida.  <br/> |
|SRAInvalidVersion = 27300  <br/> |Versão inválida do SRA.  <br/> |
|SRADelayedUpgradeFailed = 27301  <br/> |A ação de atualização assíncrona do SRA falhou.  <br/> |
|(27000 - 27999)  <br/> |Outros erros de sincronização do Active Directory não foram enumerados no Project Server.  <br/> |

<a name="pj15_ErrorCodes_Admin"></a>

## <a name="table-6-admin-web-service"></a>Tabela 6. Serviço web de administração

|Código de erro de serviço de web de administração|Descrição|
|:-----|:-----|
|AdminViewNameAlreadyExists = 16600  <br/> |O nome do modo de exibição já existe. Os nomes devem ser exclusivos.  <br/> |
|AdminViewInvalidDividerPosition = 16601  <br/> |A posição do divisor não é válida.  <br/> |
|AdminViewDataWasTampered = 16602  <br/> |Os dados foram alterados.  <br/> |
|AdminViewMaxDisplayedFieldsNumberExceeded = 16603  <br/> |A exibição excede o número máximo de campos.  <br/> |
|AdminViewCannotDeleteDefaultView = 16604  <br/> |Não é possível excluir o modo de exibição padrão.  <br/> |
|AdminViewCannotCopyDefaultView = 16605  <br/> |Não é possível copiar o modo de exibição padrão.  <br/> |
|AdminLocalCustomFieldInvalid = 19011  <br/> |O campo personalizado local não é válido.  <br/> |
|AdminEnterpriseCustomFieldInvalid = 19012  <br/> |O campo personalizado empresarial não é válido.  <br/> |
|AdminNTAccountNotFound = 19032  <br/> |A conta do Windows (NTLM) não foi encontrada.  <br/> |
|AdminUnableToMerge = 20003  <br/> |Não é possível mesclar os dados.  <br/> |
|AdminDeleteArchivedProjectsFailed = 25004  <br/> |A operação de exclusão de projetos arquivados falhou.  <br/> |
|AdminUpdateArchiveScheduleFailed = 25006  <br/> |Falha ao atualizar a agenda de arquivamento.  <br/> |
|AdminArchiveScheduleFailed = 28018  <br/> |A agenda de arquivamento falhou.  <br/> |
|AdminReadArchivedProjectsListFailed = 28019  <br/> |Falha ao ler a lista de projetos arquivados.  <br/> |
|AdminReadArchiveScheduleFailed = 28020  <br/> |Falha ao ler a agenda de arquivamento.  <br/> |
|AdminUserAccountNameNull = 28021  <br/> |O nome da conta do usuário é nulo.  <br/> |
|AdminIsWindowsUserNull = 28022  <br/> |A conta do usuário do Windows (NTLM) parece ser nula.  <br/> |
|AdminInvalidTimePeriodState = 28023  <br/> |O estado timeperiod não é válido.  <br/> |
|AdminGlobalUpdateFailed = 28024  <br/> |A atualização global da empresa falhou durante a chamada a **SetServerCurrency**.  <br/> |
|AdminGlobalCheckedOut = 28025  <br/> |Já foi feito o check-out do modelo global da empresa durante a chamada a **SetServerCurrency**.  <br/> |
|AdminInvalidDatabaseTimeout = 28026  <br/> |Tempo limite atingido devido a um banco de dados que não é válido.  <br/> |
|AdminInvalidDatabaseTimeoutType = 28027  <br/> |Tempo limite atingido devido a um tipo de banco de dados que não é válido.  <br/> |
|AdminInvalidEntityType = 28028  <br/> |O tipo de entidade não é válido. Consulte [EntityCollection](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.aspx) .  <br/> |
|AdminInvalidCompatibilityModeChange = 28029  <br/> |A alteração no modo de compatibilidade não é válida.  <br/> |
|AdminInvalidCompatibilityMode = 28030  <br/> |O modo de compatibilidade não é válido.  <br/> |
|AdminInvalidProjectProfessionalVersions = 28031  <br/> |O conjunto de versões do Project Professional não é válido.  <br/> |
|AdminInvalidProjectProfessionalVersion = 28032  <br/> |A versão do Project Professional não é válida.  <br/> |
|AdminTooManyProjectProfessionalVersions = 28033  <br/> |Muitas versões do Project Professional foram especificadas.  <br/> |
|AdminDuplicateProjectProfessionalMajorVersions = 28034  <br/> |Há duplicatas nas versões principais do Project Professional. Você só poderá especificar uma versão para cada lançamento principal, começando pelo Project Professional 2007.  <br/> |
|AdminInvalidServerFlags = 28035  <br/> |Um ou mais sinalizadores nas configurações do Project Server não são válidos.  <br/> |
|AdminNullProjectProfessionalVersions = 28036  <br/> |Uma ou mais versões do Project Professional são nulas.  <br/> |

<a name="pj15_ErrorCodes_Archive"></a>

## <a name="table-7-archive-web-service"></a>Tabela 7. Serviço da web de arquivo morto

|Arquivar o código de erro do web service (backup e restauração)|Descrição|
|:-----|:-----|
|ArchiveProjectFailure = 25000  <br/> |A operação de arquivamento do projeto falhou.  <br/> |
|ArchiveProjectsFailed = 25001  <br/> |Não é possível salvar nenhum dos projetos no banco de dados Arquivo Morto.  <br/> |
|ArchiveProjectFailed = 25002  <br/> |Não é possível salvar o arquivo morto do projeto.  <br/> |
|RestoreProjectFailed = 25003  <br/> |Não é possível restaurar o projeto.  <br/> |
|ArchiveResourcesFailed = 25007  <br/> |Não é possível salvar o arquivo morto de recursos.  <br/> |
|ArchiveCustomFieldsFailed = 25008  <br/> |Não é possível salvar o arquivo morto de campos personalizados.  <br/> |
|RestoreCustomFieldsFailed = 25009  <br/> |Não é possível restaurar os campos personalizados.  <br/> |
|ArchiveSystemSettingsFailed = 25010  <br/> |Não é possível salvar o arquivo morto de configurações do sistema.  <br/> |
|RestoreSystemSettingsFailed = 25011  <br/> |Não é possível restaurar as configurações do sistema.  <br/> |
|ArchiveCategoriesFailed = 25012  <br/> |Não é possível salvar o arquivo morto de categorias de segurança.  <br/> |
|RestoreCategoriesFailed = 25013  <br/> |Não é possível restaurar as categorias de segurança.  <br/> |
|ArchiveViewsFailed = 25014  <br/> |Não é possível salvar o arquivo morto de modos de exibição.  <br/> |
|RestoreViewsFailed = 25015  <br/> |Não é possível restaurar os modos de exibição.  <br/> |
|ArchiveGlobalProjectFailed = 25016  <br/> |Não é possível salvar o arquivo morto global da empresa.  <br/> |
|RestoreGlobalProjectFailed = 25017  <br/> |Não é possível restaurar o modelo global da empresa.  <br/> |
|ArchiveInvalidRetentionPolicyValue = 25018  <br/> |O valor da política de retenção do arquivo morto não é válido.  <br/> |
|ArchiveCustomFieldsFailure = 25019  <br/> |Não é possível ler o arquivo morto de campos personalizados.  <br/> |
|ArchiveGlobalProjectFailure = 25020  <br/> |Não é possível ler o arquivo morto global da empresa.  <br/> |
|ArchiveResourcesFailure = 25021  <br/> |Não é possível ler o arquivo morto de recursos.  <br/> |
|ArchiveSystemSettingsFailure = 25022  <br/> |Não é possível ler o arquivo morto de configurações do sistema.  <br/> |
|ArchiveViewsFailure = 25023  <br/> |Não é possível ler o arquivo morto de modos de exibição.  <br/> |
|ArchiveCategoriesFailure = 25024  <br/> |Não é possível ler o arquivo morto de categorias de segurança.  <br/> |
|ResourcePlanPublishFailure = 25025  <br/> |Não é possível publicar o plano de recursos.  <br/> |
|RestoreCategoriesFailure = 25026  <br/> |Não é possível restaurar as categorias de segurança do arquivo morto.  <br/> |
|RestoreCustomFieldsFailure = 25027  <br/> |Não é possível restaurar os campos personalizados do arquivo morto.  <br/> |
|RestoreGlobalProjectFailure = 25028  <br/> |Não é possível restaurar o modelo global da empresa do arquivo morto.  <br/> |
|RestoreProjectFailure = 25029  <br/> |Não é possível restaurar o projeto do arquivo morto.  <br/> |
|RestoreResourcesFailure = 25030  <br/> |Não é possível restaurar os recursos do arquivo morto.  <br/> |
|RestoreSystemSettingsFailure = 25031  <br/> |Não é possível restaurar as configurações do sistema do arquivo morto.  <br/> |
|RestoreViewsFailure = 25032  <br/> |Não é possível restaurar os modos de exibição do arquivo morto.  <br/> |
|ArchiveReadProjectArchiveRetentionSettingFailed = 25033  <br/> |Falha ao ler as configurações de retenção do arquivo morto do projeto.  <br/> |
|RestoreResourcesFailed = 29021  <br/> |Não é possível restaurar os recursos.  <br/> |

<a name="pj15_ErrorCodes_Assignments"></a>

## <a name="table-8-assignment"></a>Tabela 8. Assignment

|Código de erro de atribuição|Descrição|
|:-----|:-----|
|AssignmentNotFound = 120  <br/> |Atribuição não encontrada.  <br/> |
|AssignmentWrongTrackingMethod = 122  <br/> |A atribuição tem o método de rastreamento incorreto.  <br/> |
|AssignmentWorkTypeInvalid = 127  <br/> |O tipo de trabalho de atribuição não é válido.  <br/> |
|AssignmentRateTableInvalid = 130  <br/> |A tabela de taxas para a atribuição não é válida.  <br/> |
|AssignmentAlreadyExists = 131  <br/> |A atribuição já existe.  <br/> |
|AssignmentDuplicateSpecified = 132  <br/> |Há uma atribuição duplicada.  <br/> |
|AssignmentUidInvalid = 133  <br/> |O GUID da atribuição não é válido.  <br/> |
|AssignmentDelayInvalid = 134  <br/> |O atraso da atribuição não é válido.  <br/> |
|AssignmentCannotEditSummaryTask = 135  <br/> |Uma tarefa de resumo não pode ser editada para atribuições.  <br/> |
|AssignmentInvalid = 136  <br/> |A atribuição não é válida.  <br/> |
|AssignmentFieldsInvalidForBudget = 137  <br/> |Os campos da atribuição não são válidos para o orçamento.  <br/> |
|AssignmentAlreadyAssignedToResource = 138  <br/> |O recurso já tinha a atribuição.  <br/> |
|AssignmentInvalidOwner = 139  <br/> |O proprietário da atribuição não é válido.  <br/> |

<a name="pj15_ErrorCodes_Calendar"></a>

## <a name="table-9-calendar"></a>Tabela 9. Calendário

|Código de erro de calendário|Descrição|
|:-----|:-----|
|CalendarUidInvalid = 77  <br/> |O GUID do calendário não é válido.  <br/> |
|CalendarOnlyOneShiftIsNull = 13000  <br/> |Somente um turno é nulo.  <br/> |
|CalendarRecurrenceDaysShouldBeNull = 13001  <br/> |Os dias de recorrência devem ser nulos.  <br/> |
|CalendarRecurrenceMonthDayShouldBeNull = 13002  <br/> |O mês e o dia de recorrência devem ser nulos.  <br/> |
|CalendarRecurrenceMonthShouldBeNull = 13003  <br/> |O mês de recorrência deve ser nulo.  <br/> |
|CalendarRecurrenceMonthShouldNotBeNull = 13004  <br/> |O mês de recorrência não deve ser nulo.  <br/> |
|CalendarRecurrencePositionShouldBeNull = 13005  <br/> |A posição de recorrência deve ser nula.  <br/> |
|CalendarRecurrencePositionShouldNotBeNull = 13006  <br/> |A posição de recorrência não deve ser nula.  <br/> |
|CalendarRecurrenceDaysShouldNotBeNull = 13007  <br/> |Os dias de recorrência não devem ser nulos.  <br/> |
|CalendarInvalidRecurrenceFrequency = 13008  <br/> |A frequência de recorrência não é válida.  <br/> |
|CalendarInvalidRecurrenceType = 13009  <br/> |O tipo de recorrência não é válido.  <br/> |
|CalendarInvalidRecurrenceDays = 13010  <br/> |Os dias de recorrência não são válidos.  <br/> |
|CalendarInvalidCombinationOfMonthDayAndPosition = 13011  <br/> |A combinação de mês, dia e posição não é válida.  <br/> |
|CalendarInvalidRecurrencePosition = 13012  <br/> |A posição de recorrência não é válida.  <br/> |
|CalendarCannotModifyExceptionsForCalendarBeingDeleted = 13013  <br/> |As exceções de calendário não poderão ser modificadas quando um calendário estiver sendo excluído.  <br/> |
|CalendarExceptionConflict = 13014  <br/> |Há um conflito nas exceções do calendário.  <br/> |
|CalendarBadDateValue = 13015  <br/> |A data não é válida.  <br/> |
|CalendarNotFound = 13021  <br/> |O calendário não foi encontrado.  <br/> |
|CalendarAlreadyExists = 13022  <br/> |O calendário já existe.  <br/> |
|CalendarNameShouldNotBeNull = 13023  <br/> |O nome do calendário é nulo.  <br/> |
|CalendarInternalError = 13025  <br/> |Há um erro interno na operação do calendário.  <br/> |
|CalendarNameTooLong = 13027  <br/> |O nome do calendário é muito longo.  <br/> |
|CalendarInvalidCalendarName = 13028  <br/> |O nome do calendário não é válido.  <br/> |
|CalendarStandardCalendarNotFound = 13031  <br/> |O calendário padrão não foi encontrado.  <br/> |
|CalendarInvalidShifts = 13032  <br/> |Os turnos não são válidos.  <br/> |
|CalendarCannotDeleteCalendarUsedByProject = 13033  <br/> |Não é possível excluir um calendário que esteja sendo usado em um projeto.  <br/> |
|CalCalendarUniqueIdToDuplicateShouldBeNull = 13035  <br/> |O GUID deve ser nulo para duplicar um calendário.  <br/> |
|CalendarInvalidBaseCalendarUniqueId = 13037  <br/> |O GUID do calendário base não é válido.  <br/> |
|CalendarInvalidUniqueIdToDuplicate = 13038  <br/> |O GUID não é válido para duplicar um calendário  <br/> |
|CalendarUnusedCalendarException = 13039  <br/> |A exceção do calendário não tem um calendário correspondente. Ocorre ao usar o método **UpdateResources** se houver uma entrada na tabela **ResourceDataSet.CalendarExceptions**, mas nenhuma **BaseCalendarUniqueId** para o recurso na tabela **Resources**.<br/> |
|CalendarCannotDeleteStandardCalendar = 13040  <br/> |O calendário padrão não pode ser excluído.  <br/> |
|CalendarCannotRenameStandardCalendar = 13041  <br/> |O calendário padrão não pode ser renomeado.  <br/> |
|CalendarCannotDeleteCalendarUsedByEnterpriseResource = 13042  <br/> |O calendário está sendo usado por um recurso da empresa e não pode ser excluído.  <br/> |
|CalendarFilterInvalid = 13043  <br/> |O filtro não é válido para um calendário.  <br/> |

<a name="pj15_ErrorCodes_CBS"></a>

## <a name="table-10-cubeadmin-and-cube-build-service"></a>Tabela 10. CubeAdmin e Cube Build Service

|Código de erro CubeAdmin e Cube Build Service (CBS)|Descrição|
|:-----|:-----|
|CBSGeneralFailure = 17001  <br/> |Falha no Serviço de Criação do Cubo (CBS). É um código de erro geral que poderia ser resultado de várias causas diferentes.  <br/> |
|CBSDsoNotInstalled = 17002  <br/> |O CBS precisa do componente DSO (Decision Support Objects) instalado para o Analysis Services.  <br/> |
|CBSASConnectionFailure = 17003  <br/> |O CBS falhou ao conectar ao servidor do Analysis Services.  <br/> |
|CBSOlapProcessingFailure = 17004  <br/> |O processamento do cubo OLAP falhou.  <br/> |
|CBSMetadataProcessingFailure = 17005  <br/> |O processamento dos metadados do cubo falhou.  <br/> |
|CBSASServerLockTimeOut = 17006  <br/> |O bloqueio do servidor do Analysis Services atingiu o tempo limite.  <br/> |
|CBSOlapDatabaseSetupFailure = 17007  <br/> |A configuração do banco de dados do cubo OLAP falhou.  <br/> |
|CBSASEntityLimitation = 17008  <br/> |Foi excedido o número de entidades que o Analysis Services pode usar.  <br/> |
|CBSRequestInvalidArguments = 17009  <br/> |Um ou mais argumentos na solicitação do CBS não são válidos.  <br/> |
|CBSQueueingRequestFailed = 17010  <br/> |O CBS falhou ao enviar o trabalho para a fila.  <br/> |
|CBSUpdateCubeCalculatedMeasureDefintionError = 17011  <br/> |Há um erro em um membro calculado do cubo.  <br/> |
|CBSAttemptToOverwrite = 17013  <br/> |Não é possível substituir dados no cubo.  <br/> |
|CBSCustomFieldCannotBeAddedAsDimension = 17014  <br/> |O campo personalizado não pode ser uma dimensão do cubo.  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimension = 17015  <br/> |Falha ao adicionar o campo personalizado como uma dimensão do cubo.  <br/> |
|CBSCustomFieldCannotBeAddedAsMeasure = 17016  <br/> |O campo personalizado não pode ser uma medida do cubo.  <br/> |
|CBSCustomFieldFailedToBeAddedAsMeasure = 17017  <br/> |Falha ao adicionar o campo personalizado como uma medida do cubo.  <br/> |
|CBSDsoTranslatorNotFound = 17018  <br/> |O tradutor de Decision Support Objects não foi encontrado.  <br/> |
|CBSUpdateOlapDBOperationFailure = 17019  <br/> |Falha ao atualizar o banco de dados OLAP.  <br/> |
|CBSOlapDBInvalidArguments = 17020  <br/> |Um ou mais argumentos para o banco de dados OLAP não são válidos.  <br/> |
|CBSOlapDatabaseReadSettingListFailed = 17021  <br/> |Falha ao ler a lista de configurações do banco de dados OLAP.  <br/> |
|CBSOlapDatabaseReadSettingFailed = 17022  <br/> |Falha ao ler a configuração do banco de dados OLAP.  <br/> |
|CBSDeleteOlapDatabaseSetting = 17023  <br/> |Erro ao excluir a configuração do banco de dados OLAP.  <br/> |
|CBSSetDefaultOlapDatabase = 17024  <br/> |Erro ao configurar o banco de dados OLAP padrão.  <br/> |
|CBSSetOlapDatabaseEnabled = 17025  <br/> |Erro ao habilitar o banco de dados OLAP.  <br/> |
|CBSGetDefaultOlapDatabase = 17026  <br/> |Erro ao obter o banco de dados OLAP padrão.  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimensionOrMeasure = 17027  <br/> |Não é possível adicionar um campo personalizado como uma dimensão ou uma medida.  <br/> |
|CBSOlapDatabaseAssocFieldsSettings = 17028  <br/> |Erro nas configurações de campos associados de banco de dados OLAP.  <br/> |
|CBSUpdateOlapDBOperationDuplicateOrFailure = 17029  <br/> |Falha ou duplicação de operação de atualização de banco de dados OLAP.  <br/> |
|CBSErrorReadingDefaultDatabase = 17030  <br/> |Erro ao ler o banco de dados OLAP padrão.  <br/> |
|CBSCreateOlapDBOperationFailure = 17031  <br/> |Falha ao criar a operação de banco de dados OLAP.  <br/> |
|CBSSetCubeFieldsSettingsFromListForGroupMeasureFailed = 17032  <br/> |Falha ao definir a lista para configurações de medida de grupo dos campos do cubo.  <br/> |
|CBSErrorReadingCubeDepartments = 17033  <br/> |Erro ao ler departamentos no cubo OLAP.  <br/> |
|CBSErrorMaxOlapDatabaseCountReached = 17034  <br/> |A contagem máxima de bancos de dados OLAP foi atingida.  <br/> |
|CBSErrorReadingCubeFieldsSettings = 17035  <br/> |Erro ao ler configurações de campos de cubo.  <br/> |

<a name="pj15_ErrorCodes_CICO"></a>

## <a name="table-11-check-in-and-check-out"></a>A tabela 11. Fazer check-in e check-out

|Código de erro de check-in e de check-out|Descrição|
|:-----|:-----|
|CICOCheckedOutToOtherUser = 10100  <br/> |Check-out para outro usuário.  <br/> |
|CICOAlreadyCheckedOutToYou = 10101  <br/> |Já foi feito o check-out para você.  <br/> |
|CICONotCheckedOut = 10102  <br/> |Não foi feito o check-out.  <br/> |
|CICOCheckedOutInOtherSession = 10103  <br/> |Foi feito o check-out em outra sessão.  <br/> |
|CICOInvalidSessionGuid = 10104  <br/> |O GUID da sessão não é válido.  <br/> |
|CICOAlreadyCheckedOutInSameSession = 10105  <br/> |Já foi feito o check-out na mesma sessão.  <br/> |
|CICOCannotCheckOutVisibilityModeProjectWithMppInDocLib = 10106  <br/> |Não é possível fazer check-out do projeto de modo de visibilidade com um arquivo mpp na biblioteca de documentos.  <br/> |

<a name="pj15_ErrorCodes_CustomFields"></a>

## <a name="table-12-custom-field"></a>A tabela 12. Campo personalizado

|Código de erro de campo personalizado|Descrição|
|:-----|:-----|
|CustomFieldInvalidPropertyType = 11500  <br/> |O tipo de propriedade não é válido.  <br/> |
|CustomFieldInvalidScope = 11503  <br/> |O escopo do campo personalizado não é válido.  <br/> |
|CustomFieldScopesMustBeIdentical = 11504  <br/> |Os escopos devem ser idênticos.  <br/> |
|CustomFieldInvalidEntityUID = 11505  <br/> |O GUID da entidade de campo personalizado não é válido.  <br/> |
|CustomFieldHasInvalidPropertiesForNonLookupTableCF = 11506  <br/> |As propriedades não são válidas para um campo personalizado sem tabela de pesquisa.  <br/> |
|CustomFieldNonExistentWeightsTableUID = 11507  <br/> |O GUID da tabela de pesos não existe.  <br/> |
|CustomFieldInvalidName = 11508  <br/> |O nome do campo personalizado não é válido.  <br/> |
|CustomFieldInvalidDefault = 11510  <br/> |O valor padrão para o campo personalizado não é válido.  <br/> |
|CustomFieldInvalidLookupTableUID = 11511  <br/> |O GUID da tabela de pesquisa não é válido.  <br/> |
|CustomFieldTypeDoesNotMatchLookupTableMask = 11512  <br/> |O tipo de campo personalizado não corresponde à máscara da tabela de pesquisa.  <br/> |
|CustomFieldCannotHaveNonLeafNodeDefault = 11513  <br/> |O valor padrão do campo personalizado deve ser um nó de folha.  <br/> |
|CustomFieldMatchingOnlyAvailableForResources = 11514  <br/> |O campo personalizado correspondente só está disponível para recursos.  <br/> |
|CustomFieldUIDCannotMatchLookupTableUID = 11516  <br/> |O GUID não corresponde a um GUID da tabela de pesquisa.  <br/> |
|CustomFieldUIDAlreadyExists = 11517  <br/> |O GUID do campo personalizado já existe.  <br/> |
|CustomFieldIDAlreadyExists = 11518  <br/> |O número de identificação do campo personalizado já existe.  <br/> |
|CustomFieldNameAlreadyExists = 11519  <br/> |O nome do campo personalizado já existe.  <br/> |
|CustomFieldInvalidEntity = 11520  <br/> |A entidade não é válida para o campo personalizado.  <br/> |
|CustomFieldMaskDoesNotMatchEntityType = 11521  <br/> |A máscara de código não corresponde ao tipo de entidade.  <br/> |
|CustomFieldLowerOrderBitsOutOfRange = 11522  <br/> |Os bits de ordem inferior estão fora de alcance.  <br/> |
|CustomFieldInvalidMaxValues = 11523  <br/> |Um ou mais valores máximos não são válidos.  <br/> |
|CustomFieldCannotModifyCertainValuesOnceDefined = 11524  <br/> |Determinados valores não podem ser modificados depois de definidos.  <br/> |
|CustomFieldNonExistentPID = 11526  <br/> |O número de identificação da propriedade do campo personalizado não existe.  <br/> |
|CustomFieldCannotChangeBuiltInFields = 11527  <br/> |Não é possível alterar os campos internos do Project Server, como Tipo de Custo, Estado e RBS.  <br/> |
|CustomFieldSecondaryUidCannotEqualUid = 11528  <br/> |O GUID secundário não pode ser igual ao GUID principal.  <br/> |
|CustomFieldCannotHaveSecondaryUIDorIDForThisEntityType = 11529  <br/> |O campo personalizado não pode ter um GUID secundário ou um GUID para esse tipo de entidade.  <br/> |
|CustomFieldNameMatchesIntrinsicField = 11530  <br/> |O nome do campo personalizado corresponde a um campo intrínseco.  <br/> |
|CustomFieldInvalidAggregationType = 11531  <br/> |O tipo de agregação não é válido.  <br/> |
|CustomFieldProjectFormulaFieldsMustUseFormulaAggregation = 11532  <br/> |Os campos de fórmula do projeto devem usar agregação de fórmula.  <br/> |
|CustomFieldMustSpecifyEitherIDorUID = 11700  <br/> |Deve especificar o número de identificação do campo personalizado ou GUID.  <br/> |
|CustomFieldInvalidID = 11701  <br/> |O número de identificação do campo personalizado não é válido.  <br/> |
|CustomFieldInvalidUID = 11702  <br/> |O GUID do campo personalizado não é válido.  <br/> |
|CustomFieldInvalidType = 11703  <br/> |O tipo de campo personalizado não é válido.  <br/> |
|CustomFieldInvalidTypeColumnFilledIn = 11704  <br/> |O valor de coluna de tipo de campo personalizado não é válido. Consulte o exemplo no [Exemplo de código de erro para WCF](#pj15_ErrorCodes_WCFExample).  <br/> |
|CustomFieldCodeValueDoesNotMatchLookupTable = 11706  <br/> |O valor do código não corresponde à tabela de pesquisa.  <br/> |
|CustomFieldCodeValueIsNotLeafNode = 11707  <br/> |O valor do código não é um nó de folha da tabela de pesquisa.  <br/> |
|CustomFieldRowAlreadyExists = 11708  <br/> |A linha do campo personalizado já existe.  <br/> |
|CustomFieldRowDoesNotMatchCorrespondingDefinitionInDB = 11710  <br/> |A linha do campo personalizado não corresponde à definição do banco de dados.  <br/> |
|CustomFieldCodeValueAlreadyUsed = 11711  <br/> |O valor do código já foi usado.  <br/> |
|CustomFieldMaxValuesExceeded = 11712  <br/> |Os valores máximos do campo personalizado foram excedidos.  <br/> |
|CustomFieldRequiredValueNotProvided = 11713  <br/> |Um valor de campo personalizado obrigatório não for fornecido. Consulte o exemplo no [Exemplo de código de erro para WCF](#pj15_ErrorCodes_WCFExample).  <br/> |
|CustomFieldCannotChangeLookupTable = 11715  <br/> |Não é possível alterar a tabela de pesquisa do campo personalizado.  <br/> |
|CustomFieldFilterInvalid = 11716  <br/> |O filtro do campo personalizado não é válido.  <br/> |
|CustomFieldRolldownInvalidOnFormulaFields = 11717  <br/> |Não é possível rolar para baixo em um campo personalizado de fórmula.  <br/> |
|CustomFieldFormulaFieldCannotBeRequired = 11718  <br/> |O campo de fórmula não pode ser obrigatório.  <br/> |
|CustomFieldFormulaFieldCannotBeWorkflowControlled = 11719  <br/> |O campo de fórmula não pode ser controlado por um fluxo de trabalho.  <br/> |
|CustomFieldCannotSetValueOnFormulaFields = 11720  <br/> |Não é possível definir valor em campos de fórmula.  <br/> |
|CustomFieldNewPerRequestLimitExcedeed = 11721  <br/> |Excedeu o limite de solicitação para novos campos personalizados. O limite é [NEW_CF_PER_REQUEST_LIMIT](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.CustomField.NEW_CF_PER_REQUEST_LIMIT.aspx) em uma solicitação.  <br/> |
|CustomFieldNameIsReservedName = 11722  <br/> |Um nome do campo personalizado não pode ser um nome reservado.  <br/> |
|CustomFieldNameInvalidForOlapMeasure = 11723  <br/> |O nome do campo personalizado não é válido para uma medida de cubo OLAP.  <br/> |
|CustomFieldNameInvalidForOlapDimension = 11724  <br/> |O nome do campo personalizado não é válido para uma dimensão de cubo OLAP.  <br/> |
|CustomFieldSettingsInvalidForOlapMeasure = 11725  <br/> |As configurações do campo personalizado não são válidas para uma medida de cubo OLAP.  <br/> |
|CustomFieldSettingsInvalidForOlapDimension = 11726  <br/> |As configurações do campo personalizado não são válidas para uma dimensão de cubo OLAP.  <br/> |
|CustomFieldCannotAddRelativeImportanceField = 11727  <br/> |Não é possível adicionar um campo de importância relativa.  <br/> |
|CustomFieldCannotAddProjectImpactField = 11728  <br/> |Não é possível adicionar um campo de impacto no projeto.  <br/> |
|CustomFieldInvalidDepartmentUid = 11731  <br/> |O GUID do departamento no campo personalizado não é válido.  <br/> |
|CustomFieldCannotModifyDepartmentUidOnBuiltinFields = 11732  <br/> |O GUID do departamento não pode ser modificado em campos personalizados internos.  <br/> |
|CustomFieldCannotHaveBothLookupTableAndMultilineText = 11733  <br/> |Um campo personalizado não pode incluir uma tabela de pesquisa e um texto multilinha.  <br/> |
|CustomFieldCannotHaveBothFormulaAndMultilineText = 11734  <br/> |Um campo personalizado não pode incluir uma forma e um texto multilinha.  <br/> |
|CustomFieldDescriptionExceedsLimit = 11735  <br/> |A descrição do campo personalizado é muito longa. O comprimento máximo da propriedade **MD_PROP_DESCRIPTION** é de 1000 caracteres.<br/> |
|CustomFieldOnlyTextFieldsCanHaveMultilineText = 11736  <br/> |Somente os campos personalizados de texto podem ter texto multilinha.  <br/> |
|CustomFieldOnlyProjectFieldsCanHaveMultilineText = 11737  <br/> |Somente os campos personalizados do projeto podem ter texto multilinha.  <br/> |
|CustomFieldCannotChangeWorkflowControlledBehaviorForNonProjectCustomFields = 11738  <br/> |Um campo personalizado não pode alterar o comportamento de campos personalizados de não projeto controlados por um fluxo de trabalho.  <br/> |
|CustomFieldIsWorkflowControlledAndCannotBeChanged = 11739  <br/> |O campo personalizado é controlado por um fluxo de trabalho e não pode ser alterado.  <br/> |
|CustomFieldCannotHaveRequiredFlagWhenWorkflowControlledFlagIsSet = 11740  <br/> |O campo personalizado não poderá ser obrigatório quando for controlado por um fluxo de trabalho.  <br/> |
|CustomFieldFormulaCreatesCircularReference = 11742  <br/> |A fórmula do campo personalizado cria uma referência circular.  <br/> |
|CustomFieldFormulaContainsInvalidFieldReference = 11743  <br/> |A fórmula do campo personalizado contém uma referência de campo que não é válida.  <br/> |
|CustomFieldFormulaContainsErrors = 11744  <br/> |A fórmula do campo personalizado contém um ou mais erros.  <br/> |
|CustomFieldLocalCustomFieldNotDefined = 11745  <br/> |O campo personalizado local não foi definida.  <br/> |
|CustomFieldGraphicalIndicatorContainsErrors = 11746  <br/> |O indicador gráfico do campo personalizado contém erros.  <br/> |
|CustomFieldGraphicalIndicatorContainsInvalidFieldReference = 11747  <br/> |O indicador gráfico do campo personalizado contém uma referência de campo que não é válido.  <br/> |
|CustomFieldGraphicalIndicatorTypeMismatch = 11748  <br/> |Há uma incompatibilidade de tipos para o indicador gráfico do campo personalizado.  <br/> |
|CustomFieldFormulaFieldCannotReferenceWorkflowControlledField = 11749  <br/> |Um campo na fórmula não pode referenciar um campo controlado por um fluxo de trabalho.  <br/> |
|CustomFieldWorkflowCustomFieldBeingReferencedByFormula = 11750  <br/> |Uma fórmula está tentando referenciar um campo personalizado de fluxo de trabalho.  <br/> |

<a name="pj15_ErrorCodes_LookupTables"></a>

## <a name="table-13-lookup-table"></a>A tabela 13. Tabela de pesquisa

|Código de erro de tabela de pesquisa|Descrição|
|:-----|:-----|
|LookupTableMaskNotDefined = 11000  <br/> |A máscara de código da tabela de pesquisa não foi definida.  <br/> |
|LookupTableMaskHasTooManyValues = 11001  <br/> |A máscara de código da tabela de pesquisa tem valores em excesso.  <br/> |
|LookupTableMaskHasGaps = 11002  <br/> |A máscara de código da tabela de pesquisa tem lacunas.  <br/> |
|LookupTableMaskSequenceTypeLimitedToOneLevelDeep = 11003  <br/> |O tipo de sequência da máscara de código está limitado a um nível.  <br/> |
|LookupTableMaskSequenceTypeInvalid = 11004  <br/> |O tipo de sequência da máscara de código não é válido.  <br/> |
|LookupTableMaskSequenceRequiresAnyLength = 11005  <br/> |A sequência de máscara de código requer um comprimento de _qualquer_.  <br/> |
|LookupTableMaskSeparatorTooLong = 11006  <br/> |O separador da máscara de código tem caracteres em excesso.  <br/> |
|LookupTableMaskLevelMustBeBlankAcrossLCIDs = 11007  <br/> |O nível da máscara de código deve ficar em branco nos identificadores de localidade (IDs de idioma).  <br/> |
|LookupTableMaskSeparatorInvalid = 11008  <br/> |Um caractere separador da máscara de código não é válido.  <br/> |
|LookupTableMaskBlankSeparatorInvalidAfterAnyLengthSequence = 11009  <br/> |Um caractere separador em branco não é válido após um período de sequência de _qualquer_.  <br/> |
|LookupTableMaskSequenceLengthInvalid = 11010  <br/> |O comprimento de sequência da máscara de código não é válido.  <br/> |
|LookupTableMaskLevelMustBeOneOrMore = 11011  <br/> |A máscara de código deve ser de nível 1 ou superior.  <br/> |
|LookupTableItemDoesNotFitMask = 11050  <br/> |O item da tabela de pesquisa não se ajusta à definição da máscara de código.  <br/> |
|LookupTableItemContainsSeparator = 11051  <br/> |O item da tabela de pesquisa contém um caractere separador.  <br/> |
|LookupTableItemFullValueTooLong = 11052  <br/> |O valor completo do item da tabela de pesquisa é muito longo.  <br/> |
|LookupTableDuplicateSiblingsDisallowed = 11053  <br/> |Não são permitidos irmãos duplicados na tabela de pesquisa.  <br/> |
|LookupTableSortOrderIndexInvalid = 11054  <br/> |O índice de ordem de classificação da tabela de pesquisa não é válido.  <br/> |
|LookupTableSortOrderIndexDuplicate = 11055  <br/> |Índice de ordem de classificação da tabela de pesquisa duplicado.  <br/> |
|LookupTableSortOrderTypeInvalid = 11056  <br/> |O tipo de ordem de classificação da tabela de pesquisa não é válido.  <br/> |
|LookupTableSortOrderMustComeAfterParentSortOrder = 11057  <br/> |A ordem de classificação deve vir após a ordem de classificação pai.  <br/> |
|LookupTableSortOrderMustComeBeforeParentNextSiblingSortOrder = 11058  <br/> |A ordem de classificação deve vir antes do pai na próxima ordem de classificação irmã.  <br/> |
|LookupTableInvalidCookieLength = 11060  <br/> |O comprimento do cookie para uma tabela de pesquisa não é válido.  <br/> |
|LookupTableMustHaveValuesForPrimaryLCIDorJustOneValue = 11061  <br/> |A tabela de pesquisa deve ter valores para o identificador de localidade principal (ID do idioma) ou somente um valor. Quando você criar uma tabela de pesquisa multilíngue, por exemplo, adicione somente um valor de máscara para cada nível ou primeiro adicione o valor para o LCID principal.  <br/> |
|LookupTableLCIDNotSupportedInLookupTableLanguages = 11062  <br/> |O identificador de localidade (ID do idioma) não está incluído nos idiomas da tabela de pesquisa.  <br/> |
|LookupTableInvalidDescriptionLength = 11063  <br/> |O comprimento da descrição de um item da tabela de pesquisa não é válido.  <br/> |
|LookupTableCannotChangeBuiltInTables = 11064  <br/> |Não é possível alterar as tabelas de pesquisa internas.  <br/> |
|LookupTableCannotChangeTypeOnceCreated = 11065  <br/> |Não é possível alterar o tipo de tabela de pesquisa após a criação da tabela de pesquisa.  <br/> |
|LookupTableCannotDeleteLTWithDependantCustomField = 11066  <br/> |Não é possível excluir uma tabela de pesquisa usada em um campo personalizado.  <br/> |
|LookupTableAllLevelsNotFilled = 11067  <br/> |Todos os níveis da tabela de pesquisa devem ser preenchidos.  <br/> |
|LookupTableDuplicateName = 11068  <br/> |Os nomes da tabela de pesquisa devem ser exclusivos.  <br/> |
|LookupTableInvalidName = 11069  <br/> |O nome da tabela de pesquisa não é válido.  <br/> |
|LookupTableDuplicateSiblingPhoneticsDisallowed = 11071  <br/> |Não é possível ter fonética irmã duplicada em uma tabela de pesquisa.  <br/> |
|LookupTableItemInvalidLookupTable = 11073  <br/> |Um item da tabela de pesquisa não é válido.  <br/> |
|LookupTableInvalidPhoneticsLength = 11074  <br/> |O comprimento do campo de fonética não é válido.  <br/> |
|LookupTableAlreadyExists = 11076  <br/> |A tabela de pesquisa já existe.  <br/> |
|LookupTableInvalidUID = 11078  <br/> |O GUID da tabela de pesquisa não é válido.  <br/> |
|LookupTableFilterInvalid = 11079  <br/> |O filtro da tabela de pesquisa não é válido.  <br/> |
|LookupTableLanguageParameterInvalidWithXmlFilter = 11080  <br/> |Um parâmetro de idioma não é válido com um parâmetro de _xmlFilter_ de tabela de pesquisa.  <br/> |
|LookupTableInvalidParentStructUid = 11081  <br/> |O GUID de uma estrutura pai da tabela de pesquisa não é válido.  <br/> |
|LookupTableItemContainsListSeparator = 11082  <br/> |O item da tabela de pesquisa contém um separador de lista.  <br/> |
   
Códigos de erro na tabela 14 incluem itens para páginas de detalhes do projeto (PDPs), sincronização do Exchange, o cronograma do Project Web App e os erros de banco de dados. Muitos dos códigos de erro miscellaneous na tabela 14 são usados internamente.
  
> [!NOTE]
> Os códigos de erro de auditoria não são usados no Project Server 2013. 

<a name="pj15_ErrorCodes_Miscellaneous"></a>

## <a name="table-14-miscellaneous-error-codes"></a>Tabela 14. Códigos de erro diversos

|Código de erro Miscellaneous|Descrição|
|:-----|:-----|
|AuditingUpdateFailure = 31000  <br/> |Não usado.  <br/> |
|AuditingCannotDeleteFeature = 31001  <br/> |Não usado.  <br/> |
|AuditingCannotAddFeature = 31002  <br/> |Não usado.  <br/> |
|AuditingFeatureIsNoLongerAudited = 31003  <br/> |Não usado.  <br/> |
|AuditingItemIsNotYetAvailable = 31004  <br/> |Não usado.  <br/> |
|AuditingInvalidFeatureUid = 31005  <br/> |Não usado.  <br/> |
|AuditingInvalidStoreForSelectedFeature = 31006  <br/> |Não usado.  <br/> |
|AuditingInvalidStore = 31007  <br/> |Não usado.  <br/> |
|AuditingVersionNameTooLong = 31008  <br/> |Não usado.  <br/> |
|AuditingBeginVersionFailure = 31009  <br/> |Não usado.  <br/> |
|AuditingEndVersionFailure = 31010  <br/> |Não usado.  <br/> |
|ProjectDetailPagesStrategicImpactRatingRequired = 32000  <br/> |Uma classificação de impacto estratégico é obrigatória para a página de detalhes do projeto.  <br/> |
|ProjectDetailPagesMissingPDPLinks = 32001  <br/> |Links ausentes para as páginas de detalhes do projeto.  <br/> |
|ProjectDetailPagesUnavailableWorker = 32002  <br/> |Falha na carga de busca detalhada do projeto. Nenhum trabalhador disponível.  <br/> |
|ProjectDetailPagesFailedToLoadProjectInWorker = 32003  <br/> |O trabalhador falhou ao carregar.  <br/> |
|AppPermissionInvalidAppPermissionId = 32300  <br/> |Há um problema com a id da permissão do aplicativo.  <br/> |
|InvariantValidationPSIFailed = 40000  <br/> |Retornado por métodos **PWA** caso algum método privado retorne **ValidationMethodFailed**. Uso interno.<br/> |
|ValidationMethodFailed = 40001  <br/> |Retornado por métodos privados do **PWA** quando eles detectam inconsistências de banco de dados. Uso interno.<br/> |
|GeneralExchangeSyncError = 40500  <br/> |Erro geral na sincronização do Microsoft Exchange. Uso interno.  <br/> |
|ExchangeSyncRootFolderCreationFailed = 40501  <br/> |Falha ao criar a pasta raiz na sincronização do Microsoft Exchange.  <br/> |
|ExchangeSyncTaskFolderCreationFailed = 40502  <br/> |Falha ao criar a pasta da tarefa.  <br/> |
|ExchangeSyncCouldNotGetRootFolder = 40503  <br/> |Não foi possível obter a pasta raiz.  <br/> |
|ExchangeSyncCouldNotLoadTaskObject = 40504  <br/> |Não foi possível carregar o objeto da tarefa.  <br/> |
|ExchangeSyncNewExchangeTaskCreationFailed = 40505  <br/> |A criação de uma nova tarefa falhou na sincronização do Exchange.  <br/> |
|ExchangeSyncFailedToUpdateCacheForUser = 40506  <br/> |Falha ao atualizar o cache de sincronização do Exchange para o usuário.  <br/> |
|ExchangeSyncFailedToUpdateExchangeTask = 40507  <br/> |Falha ao atualizar a tarefa no Microsoft Exchange.  <br/> |
|ExchangeSyncSubscriptionUpdateFailed = 40508  <br/> |Falha ao atualizar a assinatura de sincronização do Exchange.  <br/> |
|ExchangeSyncEWSUrlFailed = 40509  <br/> |A URL do serviço Web do Microsoft Exchange falhou.  <br/> |
|ExchangeSyncExchangeUrlRefreshFailed = 40510  <br/> |Falha ao atualizar a URL do Exchange.  <br/> |
|ExchangeSyncExchangeSubscriptionUpdateForUserFailed = 40511  <br/> |Falha ao atualizar a assinatura do Exchange para o usuário.  <br/> |
|ExchangeSyncGeneralProcessingFailure = 40512  <br/> |Falha de processamento geral na sincronização do Microsoft Exchange.  <br/> |
|ExchangeSyncDeletionOfTasksInExchangeFailure = 40513  <br/> |Falha ao excluir tarefas na sincronização do Exchange.  <br/> |
|ExchangeSyncAttemptedSyncOfInvalidConfiguredResource = 40514  <br/> |Tentativa de sincronizar um recurso com uma configuração que não é válida.  <br/> |
|ExchangeSyncRetrievalOfEWSUrlCausedException = 40515  <br/> |Ocorreu uma exceção durante a recuperação do serviço Web do Exchange.  <br/> |
|TimelineViewDataDoesNotExist = 42000  <br/> |Dados não existir para o modo de exibição linha do tempo no Project Web App.  <br/> |
|DatabaseUndefinedError = 50000  <br/> |O banco de dados não foi definido.  <br/> |
|DatabaseCannotInsertDuplicateKeyError = 50001  <br/> |O banco de dados não pode inserir uma chave duplicada.  <br/> |

<a name="pj15_ErrorCodes_Notifications"></a>

## <a name="table-15-notification"></a>A tabela 15. Notification

|Código de erro de notificação|Descrição|
|:-----|:-----|
|NotificationReminderUnknown = 16050  <br/> |Notificação de lembrete desconhecida.  <br/> |
|NotificationReminderParentNotSubscribed = 16051  <br/> |Não há assinatura para o pai da notificação de lembrete.  <br/> |
|NotificationReminderParentNotFound = 16052  <br/> |O pai da notificação de lembrete não foi encontrado.  <br/> |
|NotificationReminderChildStillSubscribed = 16053  <br/> |Ainda há uma assinatura para o filho do lembrete de notificação.  <br/> |
|NotificationReminderChildNotFound = 16054  <br/> |O filho da notificação de lembrete não foi encontrado.  <br/> |
|NotificationEMailDeliveryFailed = 16080  <br/> |A entrega da mensagem de email de notificação falhou.  <br/> |
|NotificationQueueMessageFailed = 16082  <br/> |A mensagem de fila de notificação falhou.  <br/> |
|NotificationXSLTTransformationError = 16084  <br/> |Erro na transformação XSLT de notificação.  <br/> |
   
Todos os códigos de erro da Tabela 16 estão relacionados ao Otimizador, que é um componente usado na análise de portfólio de projeto.

<a name="pj15_ErrorCodes_Optimizer"></a>

## <a name="table-16-optimizer-project-portfolio-analysis"></a>A tabela 16. Otimizador (análise de portfólio do project)

|Código de erro do Otimizador|Descrição|
|:-----|:-----|
|OptimizerDepInvalidDepType = 29000  <br/> |O valor **DEPENDENCY_TYPE** no [OptimizerDependencyDataSet.OptimizerDependenciesRow](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependenciesRow.aspx) otimizador não é válido. Consulte [Optimizer.DependencyTypes](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Optimizer.DependencyTypes.aspx) .  <br/> |
|OptimizerDepInvalidEntityType = 29001  <br/> |O tipo de entidade não é válido. Consulte a propriedade de [entidades](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.Entities.aspx) .  <br/> |
|OptimizerDepInvalidPosition = 29003  <br/> |O valor de [posição](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsRow.POSITION.aspx) não é válido.  <br/> |
|OptimizerDepDuplicateDependentProjects = 29004  <br/> |Existem projetos duplicados no [OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable.aspx) .  <br/> |
|OptimizerDepInvalidDependency = 29005  <br/> |A dependência do Otimizador não é válida.  <br/> |
|OptimizerDepCircularDependency = 29006  <br/> |Há uma dependência circular.  <br/> |
|OptimizerCannotDeleteDependency = 29007  <br/> |A dependência não pode ser excluída.  <br/> |
|OptimizerCannotCreateDependency = 29008  <br/> |A dependência não pode ser criada.  <br/> |
|OptimizerCannotUpdateDependency = 29009  <br/> |A dependência não pode ser atualizado.  <br/> |
|OptimizerCannotCreateMultipleDependencies = 29010  <br/> |Não é possível criar várias dependências.  <br/> |
|OptimizerCannotUpdateMultipleDependencies = 29011  <br/> |Não é possível atualizar várias dependências.  <br/> |
|OptimizerEngineMatrixNotFilled = 29100  <br/> |O Otimizador não tem dados suficientes para cálculo.  <br/> |
|OptimizerEngineCustomFieldIsNotAConstraint = 29101  <br/> |O campo personalizado não é uma restrição para o Otimizador.  <br/> |
|OptimizerCouldNotCalculatePrioritiesFromCustomFields = 29102  <br/> |Não é possível calcular prioridades dos campos personalizados especificados.  <br/> |
|OptimizerEngineBinaryInfeasibleSolution = 29103  <br/> |O cálculo do Otimizador resulta em uma solução inviável.  <br/> |
|OptimizerEngineBinaryNumericalError = 29104  <br/> |Há um erro numérico no cálculo do Otimizador.  <br/> |
|OptimizerEngineBinaryTimedOut = 29105  <br/> |O cálculo do Otimizador atingiu o tempo limite.  <br/> |
|OptimizerEngineBinaryMaxedIterations = 29106  <br/> |O cálculo do Otimizador atingiu o número máximo de iterações.  <br/> |
|OptimizerEngineBinarySubOptimal = 29107  <br/> |Os resultados do cálculo do Otimizador não são ideais.  <br/> |
|OptimizerEngineBinaryInternalError = 29108  <br/> |Há um erro interno no cálculo do Otimizador.  <br/> |
|OptimizerInvalidRange = 29200  <br/> |O intervalo de datas para o otimizador não é válido.  <br/> |
|OptimizerNonNormalizedWeights = 29201  <br/> |Valores de **Peso** no [AnalysisDataSet.AnalysisPriorityDataDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisPriorityDataDataTable.aspx) não são normalizados.  <br/> |
|OptimizerCannotEditPrioritization = 29300  <br/> |Não é possível editar a priorização do fator comercial.  <br/> |
|OptimizerCannotDeletePrioritization = 29301  <br/> |Não é possível excluir a priorização do fator comercial.  <br/> |
|OptimizerCannotCreatePrioritization = 29302  <br/> |Não é possível criar a priorização do fator comercial.  <br/> |
|OptimizerCannotUpdatePrioritization = 29303  <br/> |Não é possível atualizar a priorização do fator comercial.  <br/> |
|OptimizerCannotCalculateDriverPriorities = 29304  <br/> |Não é possível calcular as prioridades do fator comercial.  <br/> |
|OptimizerCannotCreateMultiplePrioritizations = 29305  <br/> |Não é possível criar várias priorizações de fatores comerciais.  <br/> |
|OptimizerCannotUpdateMultiplePrioritizations = 29306  <br/> |Não é possível atualizar várias priorizações de fator comercial.  <br/> |
|OptimizerDriverRelationsNotFilled = 29307  <br/> |Os dados DriverRelationsRow não foi concluídos.  <br/> |
|OptimizerDriversNotFilled = 29308  <br/> |Não há informações suficientes nos fatores comerciais do projeto para uma solução.  <br/> |
|OptimizerDriverRelationsInvalidInversedValue = 29309  <br/> |Há valores inversas no [DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx) .  <br/> |
|OptimizerCannotCreatePrioritizationUsingInactiveDrivers = 29310  <br/> |Não há um driver inativo especificado no [DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx) . Verifique as propriedades **DRIVER1_UID** e **DRIVER2_UID** .  <br/> |
|OptimizerCannotChangePrioritizationType = 29311  <br/> |Não é possível alterar o tipo de priorização.  <br/> |
|OptimizerCannotSpecifyPriorityValuesForCalculatedPrioritizations = 29312  <br/> |Se uma prioridade for calculada, você não poderá especificar o valor da prioridade.  <br/> |
|OptimizerCannotNormalizePriorityValues = 29313  <br/> |Os valores de prioridade não podem ser normalizados.  <br/> |
|OptimizerTooManyDriversInPrioritization = 29314  <br/> |Há fatores comerciais em excesso na priorização.  <br/> |
|OptimizerInvalidProjectImpactValue = 29400  <br/> |O valor de impacto do projeto não é válido.  <br/> |
|OptimizerCannotDeleteDriver = 29401  <br/> |O fator comercial do projeto não pode ser excluído.  <br/> |
|OptimizerCannotCreateDriver = 29402  <br/> |O fator comercial do projeto não pode ser criado.  <br/> |
|OptimizerCannotUpdateDriver = 29403  <br/> |O fator comercial do projeto não pode ser atualizado.  <br/> |
|OptimizerCannotEditDriver = 29404  <br/> |O fator comercial do projeto não pode ser editado.  <br/> |
|OptimizerCannotCreateMultipleDrivers = 29405  <br/> |Não é possível criar vários fatores comerciais.  <br/> |
|OptimizerCannotUpdateMultipleDrivers = 29406  <br/> |Não é possível atualizar vários fatores comerciais.  <br/> |
|OptimizerInvalidRelativeImportanceValue = 29407  <br/> |O valor de importância relativa não é válido.  <br/> |
|OptimizerInvalidDriverUid = 29500  <br/> |O GUID do fator comercial não é válido.  <br/> |
|OptimizerInvalidEntityType = 29501  <br/> |O tipo de entidade não é válido para o Otimizador.  <br/> |
|OptimizerInvalidProjectUid = 29502  <br/> |O GUID do projeto não é válido.  <br/> |
|OptimizerInvalidCustomFieldUid = 29503  <br/> |O GUID do campo personalizado não é válido para o Otimizador.  <br/> |
|OptimizerInvalidHardConstraintUid = 29504  <br/> |O GUID da restrição inflexível não é válido.  <br/> |
|OptimizerInvalidAnalysisUid = 29505  <br/> |O GUID da análise não é válido.  <br/> |
|OptimizerDriverFilterInvalid = 29506  <br/> |O filtro de fator comercial não é válido.  <br/> |
|OptimizerPrioritizationFilterInvalid = 29507  <br/> |O filtro de priorização não é válido.  <br/> |
|OptimizerCannotLoadOptimizationEngine = 29508  <br/> |O mecanismo de cálculo do Otimizador não pode ser carregado.  <br/> |
|OptimizerAnalysisFilterInvalid = 29509  <br/> |O filtro de análise não é válido.  <br/> |
|OptimizerSolutionFilterInvalid = 29510  <br/> |O filtro de solução para o Otimizador não é válido.  <br/> |
|OptimizerDependenciesFilterInvalid = 29511  <br/> |O filtro de dependências para o Otimizador não é válido.  <br/> |
|OptimizerInvalidSolutionUid = 29512  <br/> |O GUID da solução para o Otimizador não é válido.  <br/> |
|OptimizerInvalidViewUid = 29513  <br/> |O GUID de execução para o Otimizador não é válido.  <br/> |
|OptimizerInvalidAnalysisType = 29600  <br/> |O tipo de análise de portfólio não é válido.  <br/> |
|OptimizerInvalidPrioritizationType = 29601  <br/> |O tipo de priorização para o Otimizador não é válido.  <br/> |
|OptimizerCannotDeleteAnalysis = 29602  <br/> |Não é possível excluir a análise de portfólio.  <br/> |
|OptimizerCannotCreateAnalysis = 29603  <br/> |Não é possível criar a análise de portfólio.  <br/> |
|OptimizerCannotUpdateAnalysis = 29604  <br/> |Não é possível atualizar a análise de portfólio.  <br/> |
|OptimizerInvalidPrioritizationUid = 29607  <br/> |O GUID da priorização não é válido.  <br/> |
|OptimizerCannotCreateMultipleAnalyses = 29608  <br/> |Não é possível criar várias análises de portfólio.  <br/> |
|OptimizerCannotUpdateMultipleAnalyses = 29609  <br/> |Não é possível atualizar várias análises de portfólio.  <br/> |
|OptimizerCannotCalculateProjectPriorities = 29610  <br/> |O Otimizador não pode calcular prioridades de projeto.  <br/> |
|OptimizerCannotDeleteAnalysisProjectImpact = 29611  <br/> |Não é possível excluir o impacto do projeto na análise de portfólio.  <br/> |
|OptimizerCannotChangeAnalysisProjects = 29612  <br/> |Não é possível alterar projetos na análise de portfólio.  <br/> |
|OptimizerCannotChangePriorityData = 29613  <br/> |Não é possível alterar dados de prioridade.  <br/> |
|OptimizerCannotEditAnalysis = 29614  <br/> |Não é possível editar a análise de portfólio.  <br/> |
|OptimizerInvalidPlannerData = 29615  <br/> |Os dados do Planejador não são válidos para o Otimizador.  <br/> |
|OptimizerCannotChangeImpactData = 29616  <br/> |Não é possível alterar os dados de impacto do projeto.  <br/> |
|OptimizerInvalidProjectsNumber = 29617  <br/> |O número de projetos não é válido.  <br/> |
|OptimizerCannotAddImpactCFUIDToCFAnalysis = 29618  <br/> |Não é possível adicionar o projeto impacto campo personalizado GUID ([PROJECT_IMPACT_CF_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.PROJECT_IMPACT_CF_UID.aspx) ) para análise de portfólio.  <br/> |
|OptimizerInvalidDepartmentUid = 29619  <br/> |O [DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.DEPARTMENT_UID.aspx) não é válida.  <br/> |
|OptimizerTooManyProjectsInAnalysis = 29620  <br/> |Há projetos em excesso na análise.  <br/> |
|QueueAnalysisCannotDeleteAnalysis = 29680  <br/> |O método [QueueDeleteAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteAnalyses.aspx) não é possível excluir a análise.  <br/> |
|QueueAnalysisCannotCreateAnalysis = 29681  <br/> |O método [QueueCreateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateAnalysis.aspx) não é possível criar a análise.  <br/> |
|QueueAnalysisCannotUpdateAnalysis = 29682  <br/> |O método [QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx) não é possível atualizar a análise.  <br/> |
|AnalysisMismatchedJobList = 29690  <br/> |A lista de trabalhos de análise é incompatível.  <br/> |
|OptimizerInvalidForceInLookupTableUid = 29691  <br/> |O GUID da tabela de pesquisa não pode ser forçado na entrada.  <br/> |
|OptimizerInvalidForceOutLookupTableUid = 29692  <br/> |O GUID da tabela de pesquisa não pode ser forçado na saída.  <br/> |
|OptimizerDuplicateForceLookupTableUids = 29693  <br/> |Há GUIDs de tabela de pesquisa forçados duplicados.  <br/> |
|OptimizerInvalidDecisionResult = 29701  <br/> |O resultado da decisão não é válido.  <br/> |
|OptimizerInvalidForcedStatus = 29702  <br/> |O status forçado não é válido.  <br/> |
|OptimizerCannotDeleteSolution = 29703  <br/> |O método [QueueDeleteOptimizerSolutions](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteOptimizerSolutions.aspx) não é possível excluir a solução do otimizador.  <br/> |
|OptimizerCannotCreateSolution = 29704  <br/> |O método [QueueCreateOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateOptimizerSolution.aspx) não é possível criar uma solução otimizador.  <br/> |
|OptimizerCannotUpdateSolution = 29705  <br/> |O método [QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx) não é possível atualizar a solução do otimizador.  <br/> |
|OptimizerCannotCalculateSolutionStrategicAlignment = 29706  <br/> |O Otimizador não pode calcular a solução para alinhamento estratégico.  <br/> |
|OptimizerCannotCreateMultipleSolutions = 29707  <br/> |O Otimizador não pode criar várias soluções.  <br/> |
|OptimizerCannotUpdateMultipleSolutions = 29708  <br/> |O Otimizador não pode atualizar várias soluções.  <br/> |
|OptimizerCannotAddPrioritizationToCFAnalysis = 29709  <br/> |O Otimizador não pode adicionar uma priorização a um campo personalizado para a análise.  <br/> |
|OptimizerTableIsReadOnly = 29710  <br/> |A tabela do Otimizador é somente leitura.  <br/> |
|OptimizerSolutionCreateMessageFailed = 29711  <br/> |O Otimizador falhou ao criar uma mensagem "solução criada".  <br/> |
|OptimizerSolutionDeleteMessageFailed = 29712  <br/> |O Otimizador falhou ao criar uma mensagem "solução excluída".  <br/> |
|OptimizerCannotCalculateEfficientFrontier = 29714  <br/> |O Otimizador não pode calcular a fronteira eficiente para a análise.  <br/> |
|OptimizerCannotUpdateSolutionProperties = 29715  <br/> |Não é possível atualizar as propriedades da solução.  <br/> |
|OptimizerInvalidConstraintPosition = 29716  <br/> |A posição da restrição no Otimizador não é válida.  <br/> |
|OptimizerInvalidHardConstraintPosition = 29717  <br/> |A posição da restrição inflexível no Otimizador não é válida.  <br/> |
|OptimizerInvalidConstraintLimit = 29718  <br/> |O limite da restrição no Otimizador não é válido.  <br/> |
|OptimizerInvalidConstraintValue = 29719  <br/> |O valor da restrição não é válido.  <br/> |
|OptimizerInvalidSolutionProjectsSet = 29720  <br/> |O conjunto de projetos na solução não é válido.  <br/> |
|OptimizerCannotCommitSolution = 29721  <br/> |O método [CommitOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.CommitOptimizerSolution.aspx) não é possível confirmar a solução.  <br/> |
|OptimizerInvalidInputData = 29723  <br/> |Os dados de entrada para o Otimizador não são válidos.  <br/> |
|OptimizerInvalidConstraintSet = 29724  <br/> |O conjunto de restrições para o Otimizador não é válido.  <br/> |
|OptimizerCannotUpdateAnalysisMetrics = 29725  <br/> |Não é possível atualizar a métrica da análise.  <br/> |
|OptimizerSolutionMismatchedJobList = 29726  <br/> |A lista de trabalhos da solução é incompatível.  <br/> |
|OptimizerInvalidForceLookupTableValue = 29727  <br/> |O valor da tabela de pesquisa forçada não é válido.  <br/> |
|OptimizerCannotCreateSolutionWhileAnalysisUpdateIsPending = 29728  <br/> |Não é possível criar uma solução do Otimizador enquanto uma atualização de análise estiver pendente.  <br/> |
|OptimizerProjectSelectorAtLeastOne = 29800  <br/> |Deve haver pelo menos um projeto selecionado para o Otimizador.  <br/> |
   
Os códigos de erro da Tabela 17 estão relacionados ao Planejador, que é um componente usado na análise de portfólio de projeto.

<a name="pj15_ErrorCodes_Planner"></a>

## <a name="table-17-planner-project-portfolio-analysis"></a>A tabela 17. Planejador (análise de portfólio do project)

|Código de erro do Planejador|Descrição|
|:-----|:-----|
|PlannerSolutionMessageDeleteFailed = 28000  <br/> |Erro de fila: a mensagem para excluir a solução do planejador falhou.  <br/> |
|PlannerSolutionMessageCreateFailed = 28001  <br/> |Erro de fila: a mensagem para criar a solução do planejador falhou.  <br/> |
|PlannerInvalidRBSValueUid = 28002  <br/> |O GUID para um valor de estrutura de divisão de recurso não é válido nos dados do Planejador.  <br/> |
|PlannerInvalidCustomFieldUid = 28003  <br/> |O GUID para um campo personalizado não é válido.  <br/> |
|PlannerHorizonInvalid = 28004  <br/> |O horizonte de tempo do Planejador não é válido. Um horizonte de tempo é o período especificado para o planejamento de capacidade.  <br/> |
|PlannerHorizonTooBig = 28005  <br/> |O horizonte de tempo está muito avançado no futuro.  <br/> |
|PlannerInvalidBookingType = 28006  <br/> |O tipo de reserva de recurso não é válido.  <br/> |
|PlannerInvalidTimeScale = 28007  <br/> |A escala de tempo não é válida.  <br/> |
|PlannerInvalidProjectSNET = 28008  <br/> |A data "não iniciar antes de" do projeto não é válida.  <br/> |
|PlannerInvalidProjectFNLT = 28009  <br/> |A data "não terminar depois de" do projeto não é válida.  <br/> |
|PlannerInvalidAnalysisStartDate = 28010  <br/> |[Data_inicial](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectRequirementsByRoleRow.START_DATE.aspx) para o projeto não é válida.  <br/> |
|PlannerInvalidAnalysisDuration = 28011  <br/> |A [duração](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectsRow.DURATION.aspx) não é válida para análise de portfólio.  <br/> |
|PlannerInvalidHorizonStartDate = 28012  <br/> |A data de início do horizonte de tempo não é válida.  <br/> |
|PlannerInvalidHorizonEndDate = 28013  <br/> |A data de término do horizonte de tempo não é válida.  <br/> |
|PlannerInvalidHorizonTimeScale = 28014  <br/> |A escala de tempo do horizonte de tempo não é válido.  <br/> |
|PlannerInvalidAnalysisType = 28015  <br/> |O tipo de análise de portfólio não é válido.  <br/> |
|PlannerHorizonStartDateDoesNotMatchTimeScale = 28016  <br/> |A data de início do horizonte de tempo não corresponde à escala de tempo.  <br/> |
|PlannerHorizonEndDateDoesNotMatchTimeScale = 28017  <br/> |A data de término do horizonte de tempo não corresponde à escala de tempo.  <br/> |
|PlannerAnalysisNoCapacityData = 28037  <br/> |Não há dados de capacidade de recurso para a análise de portfólio.  <br/> |
|PlannerInvalidSolutionUid = 28100  <br/> |O GUID da solução de análise não é válido.  <br/> |
|PlannerInvalidOptimizerSolutionUid = 28101  <br/> |O GUID da solução do Otimizador não é válido.  <br/> |
|PlannerInvalidLookupTableValueUid = 28102  <br/> |O GUID do valor da tabela de pesquisa não é válido.  <br/> |
|PlannerInvalidEfficientFrontierUid = 28103  <br/> |O [FRONTIER_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionEfficientFrontierRow.FRONTIER_UID.aspx) não é válida.  <br/> |
|PlannerInvalidProjectUid = 28104  <br/> |O GUID do projeto não é válido.  <br/> |
|PlannerInvalidAllocationThreshold = 28105  <br/> |O limite de alocação não é válido.  <br/> |
|PlannerInvalidHiringType = 28109  <br/> |O [HIRING_TYPE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.HIRING_TYPE.aspx) não é válida. Consulte [Planner.PlannerHiringType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.PlannerHiringType.aspx) .  <br/> |
|PlannerInvalidConstraintType = 28110  <br/> |O [Tipo_Restrição](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_TYPE.aspx) não é válida. Consulte [Planner.ConstraintType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.ConstraintType.aspx) .  <br/> |
|PlannerInvalidConstraintValue = 28111  <br/> |O [CONSTRAINT_VALUE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_VALUE.aspx) não é válida.  <br/> |
|PlannerInvalidRateTable = 28112  <br/> |O [RATE_TABLE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.RATE_TABLE.aspx) não é válida.  <br/> |
|PlannerInvalidSolutionForConstraint = 28113  <br/> |A solução do Planejador não é válida para a restrição. Projetos em excesso são forçados na entrada durante a primeira passagem do planejador.  <br/> |
|PlannerInvalidSolutionForDependencies = 28114  <br/> |A solução do Planejador não é válida porque há projetos em excesso para considerar dependências ou conflitos comerciais. Este erro ocorre na segunda passagem.  <br/> |
|PlannerInvalidSolutionForScheduling = 28115  <br/> |A solução do Planejador não é válida para agendamento porque há dependências circulares.  <br/> |
|PlannerInvalidAnalysisUid = 28116  <br/> |O [ANALYSIS_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.ANALYSIS_UID.aspx) não é válida.  <br/> |
|PlannerInvalidProjectStartDate = 28200  <br/> |A data de início do projeto não é válida.  <br/> |
|PlannerInvalidProjectEndDate = 28201  <br/> |A data de término do projeto não é válida.  <br/> |
|PlannerInvalidProjectDuration = 28202  <br/> |A duração do projeto não é válida.  <br/> |
|PlannerInvalidProjectFNLTDate = 28203  <br/> |A data "não terminar depois de" do projeto não é válida.  <br/> |
|PlannerInvalidProjectSNETDate = 28204  <br/> |A data "não iniciar antes de" do projeto não é válida.  <br/> |
|PlannerCannotCreateSolution = 28900  <br/> |O Planejador não pode criar uma solução.  <br/> |
|PlannerCannotUpdateSolution = 28901  <br/> |O Planejador não pode atualizar uma solução.  <br/> |
|PlannerCannotDeleteSolution = 28902  <br/> |O Planejador não pode excluir uma solução.  <br/> |
|PlannerCannotCreateMultipleSolutions = 28903  <br/> |O Planejador não pode criar várias soluções.  <br/> |
|PlannerCannotUpdateMultipleSolutions = 28904  <br/> |O Planejador não pode atualizar várias soluções.  <br/> |
|PlannerTableIsReadOnly = 28907  <br/> |A **DataTable** é somente leitura.  <br/> |
|PlannerCannotCommitSolution = 28908  <br/> |O Planejador não pode confirmar a solução no banco de dados.  <br/> |
|PlannerFieldIsReadOnly = 28909  <br/> |O campo é somente leitura.  <br/> |
|PlannerProjectNotInParentSolution = 28910  <br/> |O projeto não está na solução pai.  <br/> |
|PlannerProjectNotSelectedInParentSolution = 28911  <br/> |O projeto não está selecionado na solução pai.  <br/> |
|PlannerProjectNotInParentAnalysis = 28912  <br/> |O projeto não está na análise de portfólio pai.  <br/> |
|PlannerProjectBeyondHorizon = 28913  <br/> |O projeto se estende para além do horizonte de tempo.  <br/> |
|PlannerResourceAllocationInternalError = 28915  <br/> |Há um erro interno na alocação do recurso.  <br/> |
|PlannerResourceAllocationInfeasibleSolution = 28916  <br/> |A locação do recurso é uma solução inviável.  <br/> |
|PlannerProjectEndDateViolatesDependency = 28917  <br/> |A data de término do projeto viola uma dependência.  <br/> |
|PlannerInvalidProjectsSet = 28919  <br/> |O conjunto de projetos não é válido.  <br/> |
|PlannerInvalidInputData = 28920  <br/> |O Planejador tem dados de entrada não é válido.  <br/> |
|PlannerDecimalOverflowError = 28921  <br/> |Há um erro de sobrecarga decimal no Planejador.  <br/> |
|PlannerSolutionMismatchedJobList = 28922  <br/> |A solução tem uma lista de trabalhos incompatíveis.  <br/> |
|PlannerInvalidForceLookupTableValue = 28923  <br/> |O valor forçado de uma tabela de pesquisa não é válido.  <br/> |
|PlannerNoHiredResource = 28924  <br/> |Não há um recurso contratado para a proposta.  <br/> |

<a name="pj15_ErrorCodes_Projects"></a>

## <a name="table-18-project"></a>A tabela 18. Project

|Código de erro de projeto|Descrição|
|:-----|:-----|
|ProjectGlobalNotFound = 100  <br/> |Não é possível localizar o modelo global da empresa.  <br/> |
|ProjectGlobalCannotBeDeleted = 101  <br/> |Não é possível excluir o modelo global da empresa.  <br/> |
|ProjectNotFound = 1000  <br/> |Projeto não encontrado.  <br/> |
|ProjectAlreadyExists = 1001  <br/> |O projeto já existe.  <br/> |
|ProjectCheckedoutToOtherUser = 1002  <br/> |Foi feito o check-out do projeto para outro usuário.  <br/> |
|ProjectTypeInvalidForCreate = 1003  <br/> |O tipo de projeto para a operação de criação não é válido.  <br/> |
|ProjectParametersInvalid = 1004  <br/> |Um ou mais parâmetros do projeto não são válidos.  <br/> |
|ProjectNotCheckedoutToUser = 1006  <br/> |Outro usuário não fez check-out do projeto.  <br/> |
|ProjectCheckedout = 1007  <br/> |Foi feito o check-out do projeto.  <br/> |
|ProjectTypeInvalid = 1008  <br/> |O tipo de projeto não é válido.  <br/> |
|ProjectIDInvalid = 1009  <br/> |O número de identificação do projeto não é válido.  <br/> |
|ProjectNameTooLong = 1014  <br/> |O nome do projeto é muito longo.  <br/> |
|ProjectManagerNameTooLong = 1015  <br/> |O nome do gerente de projeto é muito longo.  <br/> |
|ProjectNameInvalid = 1016  <br/> |O nome do projeto não é válido.  <br/> |
|ProjectStartDateMissing = 1025  <br/> |A data de início do projeto está ausente.  <br/> |
|ProjectNameMissing = 1026  <br/> |O nome do projeto está ausente.  <br/> |
|ProjectVersionMissing = 1027  <br/> |A versão do projeto está ausente.  <br/> |
|ProjectDoesNotExist = 1028  <br/> |O projeto não existe.  <br/> |
|ProjectMultipleProjectsInvalid = 1029  <br/> |Vários projetos não são válidos.  <br/> |
|ProjectHasWriteLock = 1030  <br/> |O projeto tem um bloqueio de gravação no banco de dados.  <br/> |
|ProjectHasPendingWriteLock = 1031  <br/> |O projeto tem um bloqueio de gravação pendente.  <br/> |
|ProjectHasNoReadLock = 1032  <br/> |O projeto não tem um bloqueio de leitura.  <br/> |
|ProjectHasReadLock = 1033  <br/> |O projeto tem um bloqueio de leitura.  <br/> |
|ProjectNameAlreadyExists = 1034  <br/> |O nome do projeto já existe.  <br/> |
|ProjectOptCriticalSlackLimitInvalid = 1035  <br/> |O limite de desperdício crítico opcional não é válido.  <br/> |
|ProjectOptCurrencyPositionInvalid = 1036  <br/> |A posição de moeda opcional não é válida.  <br/> |
|ProjectOptCurrencyDigitsInvalid = 1037  <br/> |Os dígitos de moeda opcionais não são válidos.  <br/> |
|ProjectOptCurrencySymbolTooLong = 1038  <br/> |O símbolo de moeda opcional é muito longo.  <br/> |
|ProjectCannotDelete = 1039  <br/> |Não é possível excluir o projeto. Somente projetos do lado servidor de modelo ou regular podem ser excluídos.  <br/> |
|ProjectCannotAdd = 1040  <br/> |Não é possível use o método **AddToProject** no projeto do lado servidor.  <br/> |
|ProjectOptCurrencySymbolInvalid = 1041  <br/> |O símbolo de moeda opcional não é válido.  <br/> |
|ProjectHasNoWriteLock = 1042  <br/> |O projeto não tem um bloqueio de gravação.  <br/> |
|ProjectFilterInvalid = 1043  <br/> |O filtro do projeto não é válido.  <br/> |
|ProjectTooLarge = 1044  <br/> |A proposta de projeto é muito grande.  <br/> |
|ProjectOptCurrencyCodeNot3Chars = 1045  <br/> |O código de moeda opcional não tem três caracteres.  <br/> |
|ProjectOptCurrencyCodeInvalid = 1046  <br/> |O código de moeda não é válido nas opções de projeto.  <br/> |
|ProjectActualsAreProtected = 1047  <br/> |Os dados reais do projeto estão protegidos.  <br/> |
|ProjectTemplateNotFound = 1048  <br/> |Modelo de projeto não encontrado.  <br/> |
|ProjectCurrencyCodeInvalid = 1049  <br/> |O código de moeda não é válido.  <br/> |
|ProjectCannotEditCostResource = 1050  <br/> |Não é possível editar o recurso de custo.  <br/> |
|ProjectIsNotPublished = 1051  <br/> |Projeto não publicado.  <br/> |
|ProjectExceededLWPTaskLimit = 1052  <br/> |O limite da tarefa foi excedido para a proposta de projeto (um projeto leve).  <br/> |
|ProjectOptFinishDateInvalid = 1053  <br/> |A data de término nas opções do projeto não é válida.  <br/> |
|ProjectExceededItemsLimit = 1054  <br/> |Foi excedido o limite de itens para processamento. O aplicativo de serviço do Project Server não pode usar **ProjectDataSet** para adicionar ou atualizar mais de 1000 no total em todas as tabelas. Para processar mais de 1000 itens, use várias chamadas, por exemplo, para **QueueUpdateProject**.<br/> |
|ProjectColumnNotReadOnly = 1055  <br/> |The column is not read-only.  <br/> |
|ProjectInvalidOwner = 1056  <br/> |O proprietário do projeto não é válido.  <br/> |
|ProjectCantEditPctWrkCompForNonWrkRscs = 1057  <br/> |Não é possível editar **PctWorkComplete** para uma tarefa que não tenha atribuições de trabalho reais.  <br/> |
|ProjectCannotEditMaterialResource = 1058  <br/> |Não é possível editar o recurso de material.  <br/> |
|ProjectCannotEditFieldWhenTaskHasNoWorkAssignment = 1059  <br/> |Não é possível editar o campo porque a tarefa não tem atribuição de trabalho.  <br/> |
|ProjectSubProjectNotFound = 1070  <br/> |. Nenhum subprojeto foi encontrado.  <br/> |
|ProjectResourceNotFound = 1100  <br/> |Recurso não encontrado.  <br/> |
|ProjectResourceAlreadyExists = 1101  <br/> |O recurso já existe.  <br/> |
|ProjectCannotReplaceResourceWithSelf = 1106  <br/> |Não é possível substituir o recurso pelo mesmo objeto.  <br/> |
|ProjectCannotChangeLockedTrackingMethod = 1107  <br/> |Não é possível alterar porque o método de rastreamento está bloqueado.  <br/> |
|ProjectInvalidColumnForCompatibilityMode = 1108  <br/> |A coluna para o modo de compatibilidade não é válida.  <br/> |
|ProjectUpdateInvalidUpdateSequenceNumber = 1151  <br/> |O número de sequência na atualização do projeto não é válido.  <br/> |
|ProjectUpdateDuplicateUpdateSequenceNumber = 1152  <br/> |Número de sequência duplicado na atualização do projeto.  <br/> |
|ProjectUpdateNullUpdateSequenceNumber = 1153  <br/> |Número de sequência nulo na atualização do projeto.  <br/> |
|ProjectUpdateNullUpdateColumnNames = 1154  <br/> |Nomes de coluna nulos na atualização do projeto.  <br/> |
|ProjectUpdateInvalidProjectUID = 1155  <br/> |O GUID do projeto não é válido na atualização do projeto.  <br/> |
|ProjectUpdateInvalidColumnForUpdate = 1156  <br/> |A coluna não é válida para a atualização do projeto.  <br/> |
|ProjectUpdateCannotEditColumn = 1157  <br/> |Não é possível editar a coluna na atualização do projeto.  <br/> |
|ProjectUpdateNoChangesToValidateAndSchedule = 1158  <br/> |A atualização do projeto não contém alterações que possam ser validadas e agendadas.  <br/> |
|LinkNotFound = 1159  <br/> |O link não foi encontrado.  <br/> |
|ProjectUpdateInvalidColumnValue = 1160  <br/> |O valor da coluna não é válido na atualização do projeto.  <br/> |
|ProjectCannotDeleteItem = 1161  <br/> |Não é possível excluir o item de projeto.  <br/> |
|ProjectUpdateCannotComputeOptIndex = 1162  <br/> |Não é possível calcular o índice de otimização na atualização do projeto.  <br/> |
|ProjectCannotUpdateDueToVisibilityMode = 1163  <br/> |Não é possível atualizar porque o projeto está em modo de visibilidade.  <br/> |
|ProjectNodeConsistencyException = 9132  <br/> |Exceção: o nó não está consistente.  <br/> |
|ProjectSchedulingEngineException = 9133  <br/> |Exceção no mecanismo de agendamento.  <br/> |
|ProjectFormulaCalculationException = 9134  <br/> |Exceção em cálculo de fórmula.  <br/> |
|ProjectUpdateDatabaseException = 9135  <br/> |Exceção em atualização de banco de dados.  <br/> |
|ProjectDeleteException = 9136  <br/> |Exceção em exclusão de projeto.  <br/> |
|ProjectOperationException = 9137  <br/> |Exceção em operação de projeto.  <br/> |
|ProjectCannotComunicateWithPCS = 9138  <br/> |Falha na comunicação com o trabalhador PCS.  <br/> |
|ProjectPCSSessionInvalid = 9139  <br/> |O projeto na sessão de mecanismo falhou ao abrir.  <br/> |
|ProjectPublishFailure = 23000  <br/> |Falha na fila durante publicação de projeto.  <br/> |
|ProjectCurrencyConflict = 23001  <br/> |Há um conflito na moeda especificada.  <br/> |
|ProjectPublishFailed = 23002  <br/> |A publicação do projeto falhou ao ser enfileirada.  <br/> |
|ProjectReversePublishFailed = 23003  <br/> |A operação de publicação do projeto falhou quando estava sendo enfileirada.  <br/> |
|ProjectReversePublishFailure = 23004  <br/> |A reversão da publicação do projeto falhou durante o processamento da fila.  <br/> |
|ProjectArchiveRetentionDeleteFailure = 23005  <br/> |Falha na exclusão do projeto devido a retenção de arquivo morto.  <br/> |
|ProjectDeleteFailure = 23006  <br/> |Falha ao excluir projeto.  <br/> |
|ProjectPublishEnqueueFailure = 23007  <br/> |Falha na publicação do projeto durante enfileiramento.  <br/> |
|ProjectCheckinFailure = 23008  <br/> |O check-in do projeto falhou durante o processamento da fila.  <br/> |
|ProjectCheckinFailed = 23009  <br/> |O check-in do projeto falhou ao ser enfileirado.  <br/> |
|ProjectCheckoutFailed = 23010  <br/> |O usuário não tem permissão para fazer check-out do projeto.  <br/> |
|ProjectPublishSummaryEnqueueFailure = 23011  <br/> |Falha ao publicar resumo ao ser enfileirado.  <br/> |
|ProjectPublishSummaryFailed = 23012  <br/> |Falha ao publicar resumo.  <br/> |
|ProjectUpdateScheduledProjectFailure = 26026  <br/> |Falha de atualização de agendamento de projeto durante processamento de fila.  <br/> |
|ProjectSyncProjectEnterpriseEntitiesFailure = 26033  <br/> |Falha ao sincronizar entidades corporativas de projeto durante o processamento da fila.  <br/> |
|GeneralDalDatabaseIsReadOnly = 26034  <br/> |O carregamento de detalhamento do projeto falhou. O banco de dados é somente leitura.  <br/> |
|GeneralDatabaseCommunicationError = 26035  <br/> |Pode haver diversas causas diferentes, como problemas de rede ou de autenticação.  <br/> |

<a name="pj15_ErrorCodes_RDS"></a>

## <a name="table-19-reporting-data-service-rds"></a>19 de tabela. Serviço de relatório de dados (RDS)

|Código de erro do RDS|Descrição|
|:-----|:-----|
|ReportingAttributeCubeSettingsChangedMessageFailed = 24000  <br/> |A mensagem de alteração do RDS falhou para um atributo de configurações de cubo.  <br/> |
|ReportingBaseCalendarChangeMessageFailed = 24001  <br/> |A mensagem de alteração do RDS falhou para um calendário base.  <br/> |
|ReportingCustomFieldMetadataChangeMessageFailed = 24002  <br/> |A mensagem de alteração do RDS falhou para metadados do campo personalizado.  <br/> |
|ReportingEntityUserViewChangedMessageFailed = 24003  <br/> |A mensagem de alteração do RDS falhou para um modo de exibição de usuário de entidade.  <br/> |
|ReportingFiscalPeriodChangeMessageFailed = 24004  <br/> |A mensagem de alteração do RDS falhou para um período fiscal.  <br/> |
|ReportingLookupTableChangeMessageFailed = 24005  <br/> |A mensagem de alteração do RDS falhou para uma tabela de pesquisa.  <br/> |
|ReportingProjectChangeMessageFailed = 24006  <br/> |A mensagem de alteração do RDS falhou para um projeto.  <br/> |
|ReportingResourceCapacityUpdateMessageFailed = 24007  <br/> |A mensagem de atualização do RDS falhou para capacidade de recurso.  <br/> |
|ReportingResourceChangeMessageFailed = 24008  <br/> |A mensagem de alteração do RDS falhou para um recurso.  <br/> |
|ReportingTimesheetAdjustMessageFailed = 24009  <br/> |A mensagem de ajuste do RDS falhou para um quadro de horários.  <br/> |
|ReportingTimesheetClassCreateMessageFailed = 24010  <br/> |A mensagem de criação do RDS falhou para uma classe de quadro de horários.  <br/> |
|ReportingTimesheetDeleteMessageFailed = 24011  <br/> |A mensagem de exclusão do RDS falhou para um quadro de horários.  <br/> |
|ReportingTimesheetPeriodDeleteMessageFailed = 24012  <br/> |A mensagem de exclusão do RDS falhou para um período de quadro de horários.  <br/> |
|ReportingTimesheetPeriodMessageFailed = 24013  <br/> |A mensagem do RDS falhou para um período de quadro de horários.  <br/> |
|ReportingTimesheetSaveMessageFailed = 24014  <br/> |A mensagem de salvamento do RDS falhou para um quadro de horários.  <br/> |
|ReportingTimesheetStatusChangeMessageFailed = 24015  <br/> |A mensagem de alteração do RDS falhou para o status de quadro de horários.  <br/> |
|ReportingWSSSyncMessageFailed = 24016  <br/> |A mensagem do RDS falhou para a sincronização do SharePoint.  <br/> |
|ReportingGetSPWebFailed = 24017  <br/> |O RDS falhou ao obter o valor do site do SharePoint.  <br/> |
|ReportingWssSyncListFailed = 24018  <br/> |O RDS falhou ao sincronizar com a lista do SharePoint.  <br/> |
|ReportingWssTransferLinksFailed = 24019  <br/> |O RDS falhou ao transferir links do SharePoint.  <br/> |
|ReportingQueueMessageSubmitFailed = 24020  <br/> |O RDS falhou ao enviar uma mensagem para a fila.  <br/> |
|ReportingWssSyncHRefFailed = 24021  <br/> |O RDS falhou ao sincronizar com o valor HRef do SharePoint.  <br/> |
|ReportingSyncGlobalDataMessageFailed = 24022  <br/> |A mensagem do RDS a ser sincronizada com os dados globais da empresa falhou.  <br/> |
|ReportingRDBRefreshMessageFailed = 24023  <br/> |A mensagem do RDS para atualizar o RDB falhou.  <br/> |
|ReportingAttributeCubeDepartmentsChangedMessageFailed = 24024  <br/> |A mensagem do RDS falhou ao alterar o atributo de departamento para o cubo OLAP.  <br/> |
|ReportingTimesheetProjectAggregationMessageFailed = 24025  <br/> |A mensagem do RDS falhou ao agregar projetos para tabelas de quadro de horários no RDB.  <br/> |
|ReportingRdbBulkDataSyncMessageFailed = 24026  <br/> |A mensagem do RDS falhou para sincronização de dados em massa no RDB.  <br/> |
|ReportingWorkflowMetadataSyncMessageFailed = 24027  <br/> |A mensagem do RDS falhou ao sincronizar metadados de fluxo de trabalho.  <br/> |
|ReportingProjectWorkflowInformationSyncMessageFailed = 24028  <br/> |A mensagem RDS falhou ao sincronizar informações do fluxo de trabalho do projeto.  <br/> |
|ReportingEptSyncMessageFailed = 24029  <br/> |A mensagem do RDS falhou ao sincronizar o modelo de projeto da empresa.  <br/> |
|ReportingSummaryProjectPublishMessageFailed = 24030  <br/> |a mensagem do RDS falhou ao publicar o projeto de resumo.  <br/> |
|ReportingSolutionCommitedDecisionChangedMessageFailed = 24031  <br/> |A mensagem do RDS falhou ao alterar a decisão confirmada para a solução.  <br/> |
|ReportingDelayedUpgradeFailed = 24032  <br/> |a atualização atrasada do RDB falhou.  <br/> |

<a name="pj15_ErrorCodes_Resources"></a>

## <a name="table-20-resource"></a>20 de tabela. Recurso

|Código de erro de recurso|Descrição|
|:-----|:-----|
|ResourceNotFound = 2000  <br/> |Recurso não encontrado.  <br/> |
|ResourceAlreadyExists = 2001  <br/> |O recurso já existe.  <br/> |
|ResourceCheckedoutToOtherUser = 2002  <br/> |Foi feito o check-out do recurso para outro usuário.  <br/> |
|ResourceUIDInvalid = 2011  <br/> |O GUID do recurso não é válido.  <br/> |
|ResourceNameInvalid = 2016  <br/> |O nome do recurso não é válido.  <br/> |
|ResourceNameTooLong = 2017  <br/> |O nome do recurso é muito longo.  <br/> |
|ResourceInitialsTooLong = 2018  <br/> |As iniciais do recurso são muito longas.  <br/> |
|ResourceCheckedout = 2025  <br/> |Foi feito o check-out do recurso.  <br/> |
|ResourceNTAccountInvalid = 2026  <br/> |A conta do Windows (NTLM) do recurso não é válida.  <br/> |
|ResourceNameAlreadyInUse = 2027  <br/> |Nome de recurso já usado. Os nomes devem ser exclusivos.  <br/> |
|ResourceNTAccountAlreadyInUse = 2028  <br/> |A conta NTLM do recurso já foi usada.  <br/> |
|ResourceAdGuidAlreadyInUse = 2029  <br/> |O GUID do recurso já foi usado.  <br/> |
|ResourceHasActuals = 2031  <br/> |O recurso tem dados reais.  <br/> |
|ResourceNTAccountTooLong = 2035  <br/> |A conta NTLM é muito longa.  <br/> |
|ResourceEMailAddressTooLong = 2036  <br/> |O endereço de email do recurso é muito longo.  <br/> |
|ResourceCodeTooLong = 2037  <br/> |O código do recurso é muito longo.  <br/> |
|ResourceGroupTooLong = 2038  <br/> |O grupo do recurso é muito longo.  <br/> |
|ResourceWorkGroupInvalid = 2039  <br/> |O grupo de trabalho do recurso não é válido.  <br/> |
|ResourceTypeInvalid = 2040  <br/> |O tipo de recurso não é válido.  <br/> |
|ResourceNonWorkResourceWithEMailInvalid = 2044  <br/> |Um recurso que não esteja trabalhando não pode ter um endereço de trabalho.  <br/> |
|rsResourceNameHasTrailingOrLeadingWhitespace = 2046  <br/> |O nome do recurso tem um espaço em branco inicial ou final.  <br/> |
|ResourceCannotDeleteCallingUserAccount = 2047  <br/> |O usuário não pode excluir sua própria conta.  <br/> |
|ResourceInitialsInvalid = 2048  <br/> |As iniciais do recurso não são válidas.  <br/> |
|ResourceAccrueAtInvalid = 2049  <br/> |O valor para acumulação não é válido.  <br/> |
|ResourceNonMaterialResourceCannotHaveMaterialLabel = 2050  <br/> |Um recurso não material não pode ter um rótulo de material.  <br/> |
|ResourceMaterialResourceCannotHaveCertainFields = 2051  <br/> |Um recurso de material não pode ter determinados campos.  <br/> |
|ResourceAvailFromAvailToOverlap = 2052  <br/> |Sobreposição de datas iniciais e finais disponíveis.  <br/> |
|ResourceInvalidEmailLanguage = 2053  <br/> |O idioma do email não é válido.  <br/> |
|ResourceBookingTypeInvalid = 2055  <br/> |O tipo de reserva não é válido.  <br/> |
|ResourceCannotReplaceMaterialResourceWithNonMaterialResource = 2056  <br/> |Não é possível substituir o recurso de material por um recurso de não material.  <br/> |
|ResourceCannotUpdateEnterpriseResource = 2057  <br/> |Não é possível atualizar o recurso da empresa.  <br/> |
|rsResourceCannotAddLocalWithSameNameAsEnterprise = 2058  <br/> |Não é possível adicionar um recurso local com um nome igual a um recurso da empresa.  <br/> |
|ResourceCannotSetRateOnCostResource = 2059  <br/> |Não é possível definir uma taxa em um recurso de custo.  <br/> |
|ResourceCannotSetRateOnMaterialResource = 2060  <br/> |Não é possível definir uma taxa em um recurso de material.  <br/> |
|ResourceCannotSetCanLevelOnNonWorkResource = 2061  <br/> |Não é possível definir o nível de um recurso de folga.  <br/> |
|ResourceCannotDeleteThisUser = 2062  <br/> |Não é possível excluir este usuário.  <br/> |
|ResourceCannotDeactivateSelf = 2063  <br/> |Um recurso não pode desativar a si mesmo.  <br/> |
|ResourceAvailabilityDateRangesOverlap = 2064  <br/> |Os intervalos de datas de disponibilidade de recurso estão sobrepostos.  <br/> |
|ResourceAvailabilityOutsideTheHireAndTerminationDateRange = 2065  <br/> |A data de disponibilidade do recurso está fora do intervalo de datas de contração e de demissão.  <br/> |
|ResourceFilterInvalid = 2066  <br/> |O filtro para um recurso não é válido.  <br/> |
|ResourceSegmentWithThisEffectiveDateDoesNotExist = 2067  <br/> |Não é possível excluir uma taxa de recurso que ainda não foi salva.  <br/> |
|ResourceSegmentWithThisEffectiveDateAlready = 2068  <br/> |Já existe um segmento com esta data de efetivação.  <br/> |
|ResourceUserHasItemCheckedOutToItStill = 2069  <br/> |O usuário tem um item ainda com check-out.  <br/> |
|ResourceInvalidHireDate = 2070  <br/> |A data de contratação não é válida.  <br/> |
|ResourceInvalidTerminationDate = 2071  <br/> |A data de demissão não é válida.  <br/> |
|ResourceCannotChangeExistingResourceType = 2072  <br/> |Não é possível alterar um tipo de recurso.  <br/> |
|ResourceCannotSetTimesheetManagerOnSpecifiedResource = 2073  <br/> |Não é possível definir o gerente de quadro de horários no recurso especificado.  <br/> |
|ResourceInvalidTimesheetManager = 2074  <br/> |O gerente de quadro de horários não é válido.  <br/> |
|ResourceInvalidAssignmentOwner = 2075  <br/> |O proprietário da atribuição não é válido.  <br/> |
|ResourceCannotCreateCostResource = 2076  <br/> |Não é possível criar o recurso de custo.  <br/> |
|ResourceInvalidRbsValue = 2077  <br/> |O valor do RBS não é válido.  <br/> |
|ResourceCannotSetAssignmentOwnerOnSpecifiedResource = 2078  <br/> |Não é possível definir o proprietário da atribuição no recurso especificado.  <br/> |
|ResourceFieldsInvalidForBudget = 2079  <br/> |Um ou mais campos para o orçamento não são válidos.  <br/> |
|ResourceHyperlinkInvalid = 2080  <br/> |O hiperlink do recurso não é válido.  <br/> |
|ResourceAuthorizationValidOnlyOnWorkResources = 2081  <br/> |A autorização é válida somente em recursos de trabalho.  <br/> |
|ResourceIsProjectOwner = 2082  <br/> |Não é possível excluir o recurso porque o recurso é o proprietário do projeto.  <br/> |
|ResourceIsTimesheetManager = 2083  <br/> |Não é possível excluir o recurso porque o recurso é o gerente de quadro de horários.  <br/> |
|ResourceIsDefaultAssignmentOwner = 2084  <br/> |Não é possível excluir o recurso porque o recurso é o proprietário da atribuição padrão.  <br/> |
|ResourceIsAssignmentOwner = 2085  <br/> |Não é possível excluir o recurso porque o recurso é o proprietário da atribuição.  <br/> |
|ResourceIsUsedInResourcePlan = 2086  <br/> |Não é possível excluir o recurso porque o recurso é usado no plano de recursos.  <br/> |
|ResourceCannotDeleteEnterpriseResource = 2087  <br/> |Não é possível excluir o recurso da empresa por um motivo desconhecido.  <br/> |
|ResourceSetResourceAuthorizationFailed = 2088  <br/> |Falha ao definir a autorização do recurso.  <br/> |
|ResourceTooManyResourcesSpecifiedToDelete = 2089  <br/> |Não é possível excluir o número de recursos especificados.  <br/> |
|ResourceTooManyResourcesReturned = 2090  <br/> |O método não pode lidar com esta quantidade de recursos.  <br/> |
|ResourceCannotDeleteWorkflowProxyUser = 2091  <br/> |O usuário de proxy de fluxo de trabalho não pode ser excluído.  <br/> |
|ResourceInvalidEmailWithExchangeSync = 2092  <br/> |O email não é válido para sincronização com o Microsoft Exchange Server.  <br/> |
|ResourceInvalidResourceTypeWithExchangeSync = 2093  <br/> |O tipo de recurso não é válido para sincronização com o Exchange Server.  <br/> |
|ResourceInvalidPrincipalNameWithExchangeSync = 2094  <br/> |O nome da entidade de segurança do recurso não é válido para sincronização com o Exchange Server.  <br/> |
|ResourceInvalidAuthenticationTypeWithExchangeSync = 2095  <br/> |O tipo de autenticação de recurso não é válido para sincronização com o Exchange Server.  <br/> |
|ResourceExchangeSyncFlagAndPrincipalNameMismatch = 2096  <br/> |Incompatibilidade entre o sinalizador de sincronização do Exchange Server e o nome da entidade de segurança para o recurso.  <br/> |
|ResourceUnsupportedUserUpdateInSharePointSecurityMode = 2097  <br/> |A criação do usuário não tem suporte no Modo de Segurança do SharePoint.  <br/> |

<a name="pj15_ErrorCodes_ResourcePlans"></a>

## <a name="table-21-resource-plan"></a>21 de tabela. Planejamento de recursos

|Código de erro de plano de recursos|Descrição|
|:-----|:-----|
|ResourcePlanProjectPublishIncomplete = 30000  <br/> |A publicação do projeto para o plano de recursos não foi concluída.  <br/> |
|ResourcePlanInvalidResourceType = 30001  <br/> |O tipo de recurso no plano de recursos não é válido.  <br/> |
|ResourcePlanInactiveResourcesDisallowed = 30002  <br/> |Os recursos inativos não são permitidos em um plano de recursos.  <br/> |
|ResourcePlanFilterInvalid = 30003  <br/> |O filtro de plano de recursos não é válido.  <br/> |
|ResourcePlanSaveFailure = 30004  <br/> |Falha ao salvar o plano de recursos.  <br/> |
|ResourcePlanCheckinFailure = 30005  <br/> |Falha ao fazer check-in no plano de recursos.  <br/> |
|ResourcePlanDeleteFailure = 30006  <br/> |Falha ao excluir o plano de recursos.  <br/> |
|ResourcePlanInvalidUtilizationType = 30007  <br/> |O tipo de utilização do plano de recursos não é válido.  <br/> |
|ResourcePlanInvalidTimescale = 30008  <br/> |A escala de tempo do plano de recursos não é válida.  <br/> |
|ResourcePlanMismatchedJobList = 30009  <br/> |Incompatibilidade em uma lista de trabalhos de plano de recursos.  <br/> |
|ResourcePlanAlreadyExists = 30010  <br/> |O plano de recursos já existe.  <br/> |
|ResourcePlanInvalidProjectUID = 30011  <br/> |O GUID do projeto para o plano de recursos não é válido.  <br/> |
|ResourcePlanResourceAlreadyExists = 30012  <br/> |O recurso já existe no plano de recursos.  <br/> |
   
Os códigos de erro da Tabela 22 estão relacionados aos métodos **Rules** no serviço Web do **PWA**. Eles são usados internamente. 

<a name="pj15_ErrorCodes_Rules"></a>

## <a name="table-22-rules"></a>A tabela 22. Rules

|Código de erro de regras|Descrição|
|:-----|:-----|
|RulesNameTooLong = 21001  <br/> |O nome da regra de aprovação é muito longo. Para uso interno somente no Project Web App.  <br/> |
|RulesDescriptionTooLong = 21002  <br/> |A descrição da regra é muito longa. Para uso interno somente no Project Web App.  <br/> |
|RulesInvalidRuleType = 21003  <br/> |O tipo de regra não é válido. Para uso interno somente no Project Web App.  <br/> |
|RulesInvalidConditionType = 21004  <br/> |O tipo de condição para uma regra não é válido. Para uso interno somente no Project Web App.  <br/> |
|RulesInvalidOperatorType = 21005  <br/> |O tipo de operador para uma regra não é válido. Para uso interno somente no Project Web App.  <br/> |
|RulesInvalidListItemType = 21007  <br/> |O tipo de item de lista para uma regra não é válido. Para uso interno somente no Project Web App.  <br/> |
|RulesNameInvalidCharacters = 21008  <br/> |Há um ou mais caracteres no nome da regra que não são válidos. Para uso interno somente no Project Web App.  <br/> |
|RulesDescriptionInvalidCharacters = 21009  <br/> |Há um ou mais caracteres na descrição da regra que não são válidos. Para uso interno somente no Project Web App.  <br/> |
|RulesInvalidValueType = 21010  <br/> |O tipo de valor na regra não é válido. Para uso interno somente no Project Web App.  <br/> |

<a name="pj15_ErrorCodes_Security"></a>

## <a name="table-23-security"></a>A tabela 23. Security

|Código de erro de segurança|Descrição|
|:-----|:-----|
|SecurityGroupCouldNotBeCreated = 19001  <br/> |Não é possível criar um grupo de segurança.  <br/> |
|SecurityFieldAccessIDInvalid = 19003  <br/> |O número de identificação do código de acesso ao campo de segurança não é válido.  <br/> |
|SecurityCannotUpdateFacForNonExistentCategory = 19004  <br/> |A categoria de segurança não existe; não é possível atualizar o código de acesso ao campo.  <br/> |
|SecurityDuplicateCategoryUid = 19005  <br/> |GUID da categoria de segurança duplicado.  <br/> |
|SecurityDuplicateGroupUid = 19006  <br/> |GUID do grupo de segurança duplicado.  <br/> |
|SecurityDuplicateTemplateUid = 19007  <br/> |GUID do modelo de segurança duplicado.  <br/> |
|SecurityInvalidTemplateUidRef = 19008  <br/> |O GUID do modelo de segurança não é válido.  <br/> |
|SecurityInvalidGlobalPermission = 19009  <br/> |A permissão de segurança global não é válida.  <br/> |
|SecurityInvalidCategoryPermission = 19010  <br/> |A permissão da categoria de segurança não é válida.  <br/> |
|SecurityUpdatedGroupNotFound = 19013  <br/> |Grupo de segurança atualizado não encontrado.  <br/> |
|SecurityUpdatedCategoryNotFound = 19014  <br/> |Categoria de segurança atualizada não encontrada.  <br/> |
|SecurityUpdatedTemplateNotFound = 19015  <br/> |Modelo de segurança atualizado não encontrado.  <br/> |
|SecurityGroupMemberNotFound = 19016  <br/> |Membro do grupo de segurança não encontrado.  <br/> |
|SecurityUserNotFound = 19018  <br/> |Usuário do Project Server não encontrado.  <br/> |
|SecurityNoCategoryRelationForPermission = 19019  <br/> |Relação de categoria de segurança não encontrada para a permissão.  <br/> |
|SecurityCannotDeleteDefaultGroup = 19020  <br/> |Não é possível excluir o grupo de segurança padrão.  <br/> |
|SecurityCannotDeleteDefaultCategory = 19021  <br/> |Não é possível excluir a categoria de segurança padrão.  <br/> |
|SecurityCategoryCouldNotBeCreated = 19022  <br/> |Não é possível criar a categoria de segurança.  <br/> |
|SecurityNoCategoryForPermission = 19023  <br/> |Categoria de segurança não encontrada para a permissão.  <br/> |
|SecurityNoCategoryForObject = 19024  <br/> |Categoria de segurança não encontrada para o objeto.  <br/> |
|SecurityNoCategoryForRule = 19025  <br/> |Categoria de segurança não encontrada para a regra.  <br/> |
|SecurityNoGroupForPermission = 19026  <br/> |Grupo de segurança não encontrado para a permissão.  <br/> |
|SecurityCannotSetPermissionForFieldGroup = 19027  <br/> |Não é possível definir uma permissão para o campo de grupo de segurança.  <br/> |
|SecurityInvalidFieldGroup = 19028  <br/> |O campo do grupo de segurança não é válido.  <br/> |
|SecurityCannotSetOrgPermission = 19029  <br/> |Não é possível definir a permissão da organização de segurança.  <br/> |
|SecurityInvalidOrgPermission = 19030  <br/> |A permissão da organização de segurança não é válida.  <br/> |
|SecurityInvalidSecurityRule = 19031  <br/> |A regra de segurança não é válida.  <br/> |
|SecurityTemplateNotFound = 19034  <br/> |Modelo de segurança não encontrado.  <br/> |
|SecurityInvalidObjectType = 19035  <br/> |O tipo de objeto de segurança não é válido.  <br/> |
|SecurityDuplicateUid = 19036  <br/> |O GUID do objeto de segurança está duplicado.  <br/> |
|SecurityObjectNotFound = 19037  <br/> |O objeto de segurança não foi encontrado.  <br/> |
|SecurityInvalidCategoryUidRef = 19080  <br/> |O GUID da categoria de segurança não é válido.  <br/> |
|SecurityInvalidProjectUidRef = 19081  <br/> |O GUID do projeto para o objeto de segurança não é válido.  <br/> |
|SecurityInvalidGroupUidRef = 19082  <br/> |O GUID do grupo de segurança não é válido.  <br/> |
|SecurityInvalidUserUidRef = 19083  <br/> |O GUID do usuário para o objeto de segurança não é válido.  <br/> |
|SecurityInvalidCategoryPermissionUidRef = 19084  <br/> |O GUID da permissão para a categoria de segurança não é válido.  <br/> |
|SecurityInvalidGlobalPermissionUidRef = 19085  <br/> |O GUID da permissão global de segurança não é válido.  <br/> |
|SecurityInvalidResourceUidRef = 19086  <br/> |O GUID do recurso para o objeto de segurança não é válido.  <br/> |
|SecurityDeleteNotSupportedBySetMethod = 19087  <br/> |O método não pode excluir o objeto de segurança.  <br/> |
|SecurityInvalidProjectCategoryPermissionUidRef = 19088  <br/> |O GUID da permissão da categoria de projeto não é válido.  <br/> |
|SecurityCannotModifyCoreProjectCategoryDataInUpdate = 19089  <br/> |O método de atualização de segurança não pode modificar os dados da categoria de projeto principal.  <br/> |
|SecurityProjectCategoryEntitiesDoNotAllowInPlaceChanges = 19090  <br/> |As entidades da categoria de segurança não podem ser alteradas em uma atualização.  <br/> |
|SecurityCategoryCannotAddRelationForDeletedCategory = 19091  <br/> |Não é possível adicionar uma relação para uma categoria de segurança excluída.  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedCategory = 19092  <br/> |Não é possível adicionar uma permissão para uma categoria de segurança excluída.  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedRelation = 19093  <br/> |Não é possível adicionar uma permissão para uma relação de categoria de segurança excluída.  <br/> |
|SecurityCategoryCannotDeleteRelationForNewlyAddedCategory = 19094  <br/> |Não é possível excluir a relação para uma categoria de segurança recém-adicionada.  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedCategory = 19095  <br/> |Não é possível excluir a permissão para uma categoria de segurança recém-adicionada.  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedRelation = 19096  <br/> |Não é possível excluir a permissão para uma relação recém-adicionada a uma categoria de segurança.  <br/> |
|SecurityCategoryCannotHaveDuplicateUserOrGroupUidsForRelation = 19097  <br/> |Não é possível ter UIDs de usuário ou de grupo duplicadas para uma relação de categoria de segurança.  <br/> |
|SecurityCategoryPermissionMustHaveMatchingRelation = 19098  <br/> |Uma permissão de categoria deve ter uma relação de categoria de segurança correspondente.  <br/> |
|SecurityCategoryProjectAlreadyHasSecurityProjectCategory = 19099  <br/> |A lista de categorias selecionadas já tem uma categoria de segurança de projeto.  <br/> |

<a name="pj15_ErrorCodes_Events"></a>

## <a name="table-24-project-server-event"></a>Tabela 24. Evento do Project Server

|Código de erro de eventos do Project Server|Descrição|
|:-----|:-----|
|ServerEventInvalidEventId = 19033  <br/> |O número de identificação de evento do Project Server não é válido.  <br/> |
|ServerEventServiceNotFound = 22003  <br/> |O serviço Eventos do Project Server não foi encontrado. Este erro não é usado no código do Project Server, mas é mapeado para um evento bruto do ULS (Serviço de Log Unificado).  <br/> |
|ServerEventRemoteCouldNotReachProxy = 22005  <br/> |O computador remoto Project Web App não pôde acessar o proxy do Gerenciador de eventos do Project Server. Esse erro não é usado no código do Project Server, mas ele é mapeado para um evento bruto do ULS.  <br/> |
|ServerEventManagerCouldNotReachRemote = 22006  <br/> |O Gerenciador de eventos do Project Server não pôde acessar o Project Web App remoto. Esse erro não é usado no código do Project Server, mas ele é mapeado para um evento bruto do ULS.  <br/> |
|ServerEventHandlerNotSigned = 22007  <br/> |O manipulador de eventos do Project Server não está assinado.  <br/> |
|ServerEventHandlerMalformedAssemblyName = 22008  <br/> |O nome do assembly para o manipulador de eventos do Project Server não é válido.  <br/> |
|ServerEventHandlerOrderInvalid = 22009  <br/> |A ordem para o manipulador de eventos do Project Server não é válida.  <br/> |
|ServerEventHandlerDuplicateEntry = 22010  <br/> |Entrada duplicada para o manipulador de eventos do Project Server.  <br/> |
|ServerEventHandlerNotFound = 22011  <br/> |Manipulador de eventos do Project Server não encontrado.  <br/> |
|ServerEventHandlerDuplicateName = 22012  <br/> |Nome duplicado para o manipulador de eventos do Project Server .  <br/> |
|ServerEventHandlerNullAssemblyNameAndEndpointUrl = 22013  <br/> |Valide se há uma URL do ponto de extremidade ou um nome de assembly.  <br/> |

<a name="pj15_ErrorCodes_Statusing"></a>

## <a name="table-25-statusing-web-service"></a>Tabela 25. Serviço web de status 

|Código de erro de serviço de web de status|Descrição|
|:-----|:-----|
|StatusingInvalidEntity = 3102  <br/> |A entidade para **Statusing** não é válida.  <br/> |
|StatusingGetDataForTaskFailed = 3103  <br/> |Falha ao obter dados para o status da tarefa.  <br/> |
|StatusingGetTaskOrAssnCntrFailed = 3104  <br/> |Falha ao obter tarefa ou o Centro de Atribuição para status.  <br/> |
|StatusingInvalidPIDForProjCntr = 3105  <br/> |O número de identificação da propriedade **Statusing** para o Centro de Projeto não é válido.  <br/> |
|StatusingDeleteAssnFailed = 3106  <br/> |Falha ao excluir atribuição do processo **Statusing**.  <br/> |
|StatusingAssnSaveFailed = 3107  <br/> |Falha ao salvar atribuição no processo **Statusing**.  <br/> |
|StatusingTaskSaveFailed = 3108  <br/> |Falha ao salvar tarefa no processo **Statusing**.  <br/> |
|StatusingInvalidPID = 3109  <br/> |O número de identificação da propriedade **Statusing** não é válido.  <br/> |
|StatusingSetDataValueInvalid = 3111  <br/> |O valor de dados do **Statusing** não é válido.  <br/> |
|StatusingSetDataFailed = 3112  <br/> |Falha ao definir o valor de dados de **Statusing**.  <br/> |
|StatusingInvalidDelegationStart = 3113  <br/> |A hora de início para uma atribuição no método **DelegateAssignments** não é válido.  <br/> |
|StatusingApprovalUpdateFailed = 3114  <br/> |Falha ao atualizar a aprovação de status.  <br/> |
|StatusingInvalidApprovalType = 3115  <br/> |O tipo de aprovação de status não é válido.  <br/> |
|StatusingInternalError = 3116  <br/> |Erro de processamento interno em um método **Statusing**.  <br/> |
|StatusingInvalidUpdateData = 3117  <br/> |Os dados de atualização em um método **Statusing** não é válido.  <br/> |
|StatusingProjectUpdateFailed = 3118  <br/> |A atualização de **Statusing** do projeto falhou.  <br/> |
|StatusingInvalidPreviewData = 3119  <br/> |Os dados de visualização de **Statusing** não são válidos.  <br/> |
|StatusingInvalidTransaction = 3120  <br/> |A transação **Statusing** não é válida.  <br/> |
|StatusingTooManyResults = 3121  <br/> |Resultados em excesso. Mais de 5000 linhas seriam retornadas ao ler dados de status de divisão ao longo do tempo.  <br/> |
|StatusingInvalidInterval = 3122  <br/> |O intervalo em um método **Statusing** não é válido. O intervalo deve estar em minutos e deve ser maior do que zero.<br/> |
|StatusingApplyUpdatesFailed = 3123  <br/> |Falha ao aplicar atualizações de **Statusing** ao enfileirar a solicitação.  <br/> |
|StatusingApplyUpdatesFailure = 3124  <br/> |Falha ao aplicar atualizações de **Statusing** durante o processamento da fila.  <br/> |
|StatusingInvalidWorkData = 3125  <br/> |Os dados de trabalho para **Statusing** não são válidos.  <br/> |
|StatusingMissingNameAttribute = 3126  <br/> |Atributo de nome ausente para **Statusing**.  <br/> |
|StatusingInvalidNameAttribute = 3127  <br/> |O atributo de nome para **Statusing** não é válido.  <br/> |
|StatusingInvalidData = 3128  <br/> |The **Statusing** data não é válido.  <br/> |
|StatusingInvalidChangelist = 3130  <br/> |Os dados XML não são válidos no parâmetro _changexml_ do método **UpdateStatus** .  <br/> |
|StatusingInsufficientAssignmentRights = 3131  <br/> |**SetAssignmentWorkData** não pode atualizar uma atribuição porque o usuário não tem permissão.  <br/> |
|StatusingInvalidChangeNumber = 3132  <br/> |O número da alteração de **Statusing** não é válido.  <br/> |
|StatusingPidNotEditable = 3133  <br/> |O número de identificação da propriedade **Statusing** não é editável.  <br/> |
|StatusingCannotSetTimephasedDataInManualTasks = 3134  <br/> |Não é possível definir dados de divisão ao longo do tempo em tarefas manuais para **Statusing**.  <br/> |
|StatusingCannotChangeTaskMode = 3135  <br/> |Não é possível alterar o modo de tarefa para **Statusing**.  <br/> |
   
Os códigos de erro na tabela 26 são para **StatusReports** métodos no serviço da web do **PWA** . Eles são usados internamente no Project Web App. 

<a name="pj15_ErrorCodes_StatusReports"></a>

## <a name="table-26-statusreports"></a>Tabela 26. StatusReports 

|Código de erro do relatório de status|Descrição|
|:-----|:-----|
|StatusReportsUnknownError = 12100  <br/> |Erro desconhecido em **StatusReports**.  <br/> |
|StatusReportsPeriodUnmatched = 12101  <br/> |Não é possível corresponder o período de relatório de status.  <br/> |
|StatusReportsPeriodUnavailable = 12102  <br/> |O período do relatório de status está indisponível.  <br/> |
|StatusReportsInvalidFormInput = 12103  <br/> |Os dados no relatório de status não são válidos.  <br/> |

<a name="pj15_ErrorCodes_Tasks"></a>

## <a name="table-27-task"></a>Tabela 27. Task 

|Código de erro da tarefa|Descrição|
|:-----|:-----|
|TaskIDInvalid = 7001  <br/> |O GUID da tarefa não é válido.  <br/> |
|TaskNameTooLong = 7003  <br/> |Nome de tarefa muito longo.  <br/> |
|TaskTypeInvalid = 7005  <br/> |O tipo de tarefa não é válido.  <br/> |
|TaskPriorityInvalid = 7006  <br/> |A prioridade da tarefa não é válida.  <br/> |
|TaskConstraintTypeInvalid = 7007  <br/> |O tipo de restrição de tarefa não é válido.  <br/> |
|TaskNameInvalid = 7008  <br/> |O nome da tarefa não é válido.  <br/> |
|TaskConstraintTypeRequiresConstraint = 7010  <br/> |A tarefa exige um tipo de restrição.  <br/> |
|TaskConstraintTypeCannotHaveConstraintDate = 7011  <br/> |Não é possível ter uma data de restrição para o tipo de restrição.  <br/> |
|TaskSummaryTaskCannotBeMilestone = 7013  <br/> |A tarefa de resumo não pode ser um marco.  <br/> |
|TaskFixedCostAccrualInvalid = 7014  <br/> |A acumulação de custo fixo para uma tarefa não é válida.  <br/> |
|TaskPercentCompleteInvalid = 7015  <br/> |O valor de percentual concluído da tarefa não é válido.  <br/> |
|TaskWorkPercentCompleteInvalid = 7016  <br/> |O valor de percentual concluído do trabalho da tarefa não é válido.  <br/> |
|TaskPhysicalPercentCompleteInvalid = 7017  <br/> |O valor de conclusão de percentual físico de tarefa não é válido.  <br/> |
|TaskLinkTypeInvalid = 7018  <br/> |O tipo de link da tarefa não é válido.  <br/> |
|TaskAlreadyExists = 7019  <br/> |A tarefa já existe.  <br/> |
|TaskLinkAlreadyExists = 7020  <br/> |O link da tarefa já existe.  <br/> |
|TaskNotFound = 7021  <br/> |Tarefa não encontrada.  <br/> |
|TaskLinkNotFound = 7022  <br/> |Link de tarefa não encontrado.  <br/> |
|TaskLinkLagInvalid = 7023  <br/> |O tempo de retardo em um link de tarefa não é válido.  <br/> |
|TaskUnableToInsert = 7025  <br/> |Não é possível inserir uma tarefa.  <br/> |
|TaskAddPositionInvalid = 7026  <br/> |A posição de adição para uma tarefa não é válida.  <br/> |
|TaskOutlineLevelInvalid = 7027  <br/> |O nível de estrutura da tarefa não é válido.  <br/> |
|TaskDurationFormatInvalid = 7028  <br/> |O formato de duração da tarefa não é válido.  <br/> |
|TaskCannotAddWhereSpecified = 7029  <br/> |Não é possível adicionar a tarefa ao local especificado.  <br/> |
|TaskEarnedValueMethodInvalid = 7030  <br/> |O método para o valor agregado da tarefa não é válido.  <br/> |
|TaskCannotModifyProjectSummary = 7031  <br/> |Não é possível modificar a tarefa de resumo do projeto.  <br/> |
|TaskCannotDeleteProjectSummary = 7032  <br/> |Não é possível excluir a tarefa de resumo do projeto.  <br/> |
|TaskCannotSetActualCost = 7033  <br/> |Não é possível definir o custo real para a tarefa.  <br/> |
|TaskLevelingDelayInvalid = 7034  <br/> |O atraso de nivelamento para a tarefa não é válido.  <br/> |
|TaskCannotEditSummary = 7035  <br/> |Não é possível editar a tarefa de resumo.  <br/> |
|TaskCannotCreateSubTasksUnderTasksWithAssignments = 7036  <br/> |Não é possível criar subtarefas sob uma tarefa com atribuições.  <br/> |
|TaskCannotDeleteSubProject = 7037  <br/> |Não é possível excluir subprojeto para a tarefa.  <br/> |
|TaskCannotEditExternal = 7038  <br/> |Não é possível editar a tarefa externa.  <br/> |
|TaskCannotDeleteExternal = 7039  <br/> |Não é possível excluir uma tarefa externa.  <br/> |
|TaskLinkCannotDeleteExternal = 7040  <br/> |Não é possível excluir um link para uma tarefa externa.  <br/> |
|TaskCannotModifyNullTask = 7041  <br/> |Não é possível modificar uma tarefa nula.  <br/> |
|TaskCannotModifyLeafTaskWithNoAssignment = 7042  <br/> |Não é possível modificar uma tarefa folha que não tenha atribuição.  <br/> |
|TaskCannotModifyExternalTask = 7043  <br/> |Não é possível modificar uma tarefa externa.  <br/> |
|TaskStatusManagerInvalid = 7044  <br/> |O gerenciador de status da tarefa não é válido.  <br/> |
|TaskLinkCyclicDependency = 7045  <br/> |O link da tarefa tem uma dependência cíclica.  <br/> |
|TaskCannotCreateOrModifySubTasksUnderTasksWithAssignments = 7046  <br/> |Não é possível criar ou modificar subtarefas sob uma tarefa de resumo que tenha atribuições.  <br/> |
|TaskLinkCannotEditExternal = 7047  <br/> |Não é possível editar o link para uma tarefa externa.  <br/> |

<a name="pj15_ErrorCodes_Timesheets"></a>

## <a name="table-28-timesheet"></a>Tabela 28. Quadro de horários 

|Código de erro de quadro de horários|Descrição|
|:-----|:-----|
|TimesheetMaxHourPerDayExceeded = 3201  <br/> |Foi excedido o máximo de horas por dia para o quadro de horários.  <br/> |
|TimesheetHoursPerTSLimitExceeded = 3202  <br/> |Foi excedido o limite do número de horas em um quadro de horários.  <br/> |
|TimesheetUnverifiedTSLineNotAllowed = 3203  <br/> |Uma linha de quadro de horários não verificada não é permitida neste caso.  <br/> |
|TimesheetIncorrectMode = 3204  <br/> |O modo de quadro de horários não é válido.  <br/> |
|TimesheetInvalidApprover = 3205  <br/> |O aprovador do quadro de horários não é válido.  <br/> |
|TimesheetFutureReportingNotAllowed = 3206  <br/> |Relatórios de itens futuro não são permitidos para quadro de horários.  <br/> |
|TimesheetIncorrectPeriod = 3208  <br/> |O período do quadro de horários não é válido.  <br/> |
|TimesheetPeriodClosed = 3209  <br/> |Período do quadro de horários fechado.  <br/> |
|TimesheetPendingLines = 3210  <br/> |As linhas do quadro de horários estão pendentes.  <br/> |
|TimesheetInvalidDateRange = 3211  <br/> |O intervalo de datas do quadro de horários não é válido.  <br/> |
|TimesheetLineClassDisabled = 3212  <br/> |A classe de linha de quadro de horários está desabilitada.  <br/> |
|TimesheetLineHasNonExistentItem = 3213  <br/> |A linha de quadro de horários inclui um item que não existe.  <br/> |
|TimesheetLineInvalidStatus = 3214  <br/> |O status da linha do quadro de horários não é válido.  <br/> |

<a name="pj15_ErrorCodes_UserDelegation"></a>

## <a name="table-29-user-delegation"></a>Tabela 29. Delegação de usuário 

|Código de erro de delegação de usuário|Descrição|
|:-----|:-----|
|UserDelegationExpired = 43000  <br/> |A delegação de usuário expirou.  <br/> |
|UserDelegationCannotSelfDelegate = 43001  <br/> |Um usuário não pode delegar para ele mesmo.  <br/> |
|UserDelegationInvalidDelegate = 43002  <br/> |O representante do usuário não é válido.  <br/> |
|UserDelegationInvalidUser = 43003  <br/> |O usuário não é válido para delegação.  <br/> |
|UserDelegationInvalidDates = 43004  <br/> |As datas de delegação de usuário não são válidas.  <br/> |
|UserDelegationCannotDoubleDelegate = 43005  <br/> |Não é possível criar dois delegados.  <br/> |
|UserDelegationDelegateCannotLogon = 43006  <br/> |O representante do usuário não pode fazer logon no Project Server.  <br/> |
|UserDelegationDelegateIsInactive = 43007  <br/> |O representante do usuário está inativo.  <br/> |
|UserDelegationInvalidFilter = 43008  <br/> |O filtro do representante do usuário não é válido.  <br/> |
|UserDelegationUserCannotLogon = 43010  <br/> |O usuário não pode fazer logon no Project Server.  <br/> |
|UserDelegationUserIsInactive = 43011  <br/> |O representante do usuário está inativo.  <br/> |

<a name="pj15_ErrorCodes_Workflow"></a>

## <a name="table-30-workflow"></a>30 de tabela. Fluxo de trabalho 

|Código de erro de fluxo de trabalho|Descrição|
|:-----|:-----|
|WorkflowPhasesCannotCreatePhase = 35000  <br/> |Não é possível criar a fase do fluxo de trabalho.  <br/> |
|WorkflowPhasesCannotUpdatePhase = 35001  <br/> |Não é possível atualizar a fase do fluxo de trabalho.  <br/> |
|WorkflowPhasesCannotDeletePhase = 35002  <br/> |Não é possível excluir a fase do fluxo de trabalho.  <br/> |
|WorkflowPhaseNameIsRequired = 35003  <br/> |O fluxo de trabalho [PHASE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_NAME.aspx) é necessário.  <br/> |
|WorkflowStagesCannotCreateStage = 35004  <br/> |Não é possível criar o estágio do fluxo de trabalho.  <br/> |
|WorkflowStagesCannotUpdateStage = 35005  <br/> |Não é possível atualizar o estágio do fluxo de trabalho.  <br/> |
|WorkflowStagesCannotDeleteStage = 35006  <br/> |Não é possível excluir o estágio do fluxo de trabalho.  <br/> |
|WorkflowStagesProjectsInStage = 35007  <br/> |Há projetos no estágio do fluxo de trabalho.  <br/> |
|WorkflowCannotAccessPDPLibrary = 35008  <br/> |Não é possível acessar a biblioteca de páginas de detalhes do projeto.  <br/> |
|WorkflowInvalidPDPUid = 35009  <br/> |O GUID da página de detalhes do projeto não é válido.  <br/> |
|WorkflowInvalidCustomFieldUid = 35010  <br/> |O GUID do campo personalizado não é válido.  <br/> |
|WorkflowCustomFieldNotWorkflowControlled = 35011  <br/> |O campo personalizado não é controlado por um fluxo de trabalho.  <br/> |
|WorkflowCustomFieldCannotBeRequiredAndReadOnly = 35012  <br/> |O campo personalizado do fluxo de trabalho não pode ser obrigatório e somente leitura.  <br/> |
|WorkflowInvalidWorkflowPhaseUid = 35013  <br/> |O fluxo de trabalho [PHASE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_UID.aspx) não é válido.  <br/> |
|WorkflowInsertWorkflowPhaseNotAllowed = 35014  <br/> |Não é possível inserir uma fase de fluxo de trabalho.  <br/> |
|WorkflowInvalidWorkflowStageUid = 35015  <br/> |O fluxo de trabalho [STAGE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_UID.aspx) não é válido.  <br/> |
|WorkflowPhaseHasStages = 35016  <br/> |A fase do fluxo de trabalho tem estágios.  <br/> |
|WorkflowStageNameIsRequired = 35020  <br/> |O fluxo de trabalho [STAGE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_NAME.aspx) é necessário.  <br/> |
|WorkflowStageAtLeastOnePDPIsRequired = 35021  <br/> |Pelo menos uma página de detalhes do projeto é necessária para o estágio do fluxo de trabalho.  <br/> |
|WorkflowCannotStartWorkflow = 35100  <br/> |Não é possível iniciar o fluxo de trabalho.  <br/> |
|WorkflowStatusCannotUpdateStatus = 35101  <br/> |Não é possível atualizar o fluxo de trabalho.  <br/> |
|WorkflowOnlyProjectsHaveWorkflow = 35102  <br/> |Somente projetos podem ter um fluxo de trabalho.  <br/> |
|WorkflowNoWorkflowsDefined = 35103  <br/> |Nenhum fluxo de trabalho foi definido.  <br/> |
|WorkflowInvalidStageForProject = 35104  <br/> |O estágio de fluxo de trabalho para o projeto não é válido.  <br/> |
|WorkflowNoWorkflowForProject = 35105  <br/> |O projeto não tem um fluxo de trabalho.  <br/> |
|WorkflowCheckinRequiredAndProjectNotCheckedin = 35106  <br/> |Deve ser feito o check-in do projeto para que o fluxo de trabalho funcione.  <br/> |
|WorkflowWaitingForRequiredData = 35107  <br/> |O fluxo de trabalho está aguardando os dados necessários.  <br/> |
|WorkflowFlagCustomFieldsCannotBeRequired = 35108  <br/> |Um campo personalizado de sinalizador não pode ser obtido em um fluxo de trabalho.  <br/> |
|WorkflowCannotChangeWorkflow = 35109  <br/> |Não é possível alterar o fluxo de trabalho.  <br/> |
|WorkflowWorkflowStatusPDPNotAllowed = 35110  <br/> |Não é permitida uma página de detalhes do projeto para o status do fluxo de trabalho.  <br/> |
|WorkflowInvalidWorkflowStatusPDPUid = 35111  <br/> |O GUID da página de detalhes do projeto de status de fluxo de trabalho não é válido.  <br/> |
|WorkflowInvalidStageStatusValue = 35112  <br/> |O valor do status do estágio do fluxo de trabalho não é válido. Quando você definir o status do estágio do fluxo de trabalho, apenas os valores **InProgressRequestSent**, **InProgressRunning**ou **InProgressWaiting** no [Workflow.StageStatus](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Workflow.StageStatus.aspx) são permitidos.  <br/> |
|WorkflowCannotCheckinNotify = 35113  <br/> |Não é possível notificar o fluxo de trabalho de que foi feito o check-in do projeto.  <br/> |
|WorkflowCannotCommitNotify = 35114  <br/> |Não é possível notificar o fluxo de trabalho de que o projeto foi confirmado no Planejador ou no Otimizador.  <br/> |
|WorkflowExceptionStartingWorkflow = 35115  <br/> |Há um erro ao iniciar o fluxo de trabalho.  <br/> |
|WorkflowStatusPDPMustBeSupplied = 35116  <br/> |Uma página de detalhes do projeto para o status do fluxo de trabalho é necessária.  <br/> |
|WorkflowWorkflowProxyAccountNotFound = 35117  <br/> |A conta de proxy de fluxo de trabalho não foi encontrada.  <br/> |
|WorkflowInvalidCurrentStage = 35118  <br/> |O estágio atual do fluxo de trabalho não é válido.  <br/> |
|WorkflowMultipleStagesInProgress = 35119  <br/> |Há vários estágios em andamento no fluxo de trabalho.  <br/> |
|WorkflowActivityInvalidArgument = 35120  <br/> |A mensagem recebida caso uma atividade do fluxo de trabalho receba um argumento inválido.  <br/> |
|WorkflowMTWConfigurationError = 35121  <br/> |Erro de configuração do fluxo de trabalho do Microsoft Azure.  <br/> |
|EnterpriseProjectTypeInvalidEnterpriseProjectTypeUid = 35200  <br/> |O **ENTERPRISE_PROJECT_TYPE_UID** não é válido.  <br/> |
|EnterpriseProjectTypeCannotCreateEnterpriseProjectType = 35201  <br/> |Não é possível criar o tipo de projeto da empresa.  <br/> |
|EnterpriseProjectTypeCannotUpdateEnterpriseProjectType = 35202  <br/> |Não é possível atualizar o tipo de projeto da empresa.  <br/> |
|EnterpriseProjectTypeCannotDeleteEnterpriseProjectType = 35203  <br/> |Não é possível excluir o tipo de projeto da empresa.  <br/> |
|EnterpriseProjectTypeCannotCreateMultipleEnterpriseProjectTypes = 35204  <br/> |Não é possível criar vários tipos de projeto da empresa.  <br/> |
|EnterpriseProjectTypeCannotUpdateMultipleEnterpriseProjectTypes = 35205  <br/> |Não é possível atualizar vários tipos de projeto da empresa.  <br/> |
|EnterpriseProjectTypeInvalidCreatePDPUid = 35206  <br/> |Um modelo de projeto empresarial (EPT) requer uma página de detalhes do projeto associado (PDP) para criar um projeto usando o EPT. Se o EPT for para um fluxo de trabalho, este erro ocorre durante a validação de EPT quando a página de detalhes do projeto (PDP) não é do tipo de *criar* . Outros tipos PDP são *Normal* para a edição de um projeto e o *Status do fluxo de trabalho* para mostrando detalhes de um projeto relacionadas ao fluxo de trabalho.  <br/> |
|EnterpriseProjectTypeInvalidProjectPlanTemplateUid = 35207  <br/> |O [ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID.aspx) não é válida.  <br/> |
|EnterpriseProjectTypeInvalidWorkspaceTemplateName = 35208  <br/> |O [ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME.aspx) não é válida.  <br/> |
|EnterpriseProjectTypeInvalidWorkflowAssociationUid = 35209  <br/> |O [WORKFLOW_ASSOCIATION_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.WORKFLOW_ASSOCIATION_UID.aspx) não é válida.  <br/> |
|EnterpriseProjectTypeCannotReadWssSettings = 35210  <br/> |Não é possível ler as configurações do SharePoint.  <br/> |
|EnterpriseProjectTypeCannotReadWssLanguagesAndTemplates = 35211  <br/> |Não é possível ler as linguagens do SharePoint e os modelos de site.  <br/> |
|EnterpriseProjectTypeInvalidDepartmentUid = 35212  <br/> |O [DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.DEPARTMENT_UID.aspx) não é válida.  <br/> |
|EnterpriseProjectTypeInvalidUri = 35213  <br/> |O [ENTERPRISE_PROJECT_TYPE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.ENTERPRISE_PROJECT_TYPE_UID.aspx) não é válido.  <br/> |
|EnterpriseProjectTypeUriRequiresHttp = 35214  <br/> |O URI do tipo de projeto da empresa exige o protocolo HTTP.  <br/> |
|EnterpriseProjectTypeCannotDeleteDefault = 35215  <br/> |Não é possível excluir o tipo de projeto da empresa padrão.  <br/> |
|EnterpriseProjectTypeCannotChangeDefault = 35216  <br/> |Não é possível alterar o tipo de projeto da empresa padrão.  <br/> |
|EnterpriseProjectTypeHasProjectsCannotDelete = 35217  <br/> |Não é possível excluir um tipo de projeto da empresa que tenha projetos.  <br/> |
|EnterpriseProjectTypeCreatePDPIsRequired = 35218  <br/> |Um modelo de projeto empresarial (EPT) para um fluxo de trabalho requer uma associado página de detalhes do projeto de tipo *criar* (PDP) para criar um projeto usando o EPT. Este erro ocorre quando o PDP não está incluído na definição de EPT. Outros tipos PDP são *Normal* para a edição de um projeto e o *Status do fluxo de trabalho* para mostrando detalhes de um projeto relacionadas ao fluxo de trabalho.  <br/> |
|EnterpriseProjectTypeOnlyOneCreatePDPAllowed = 35219  <br/> |A definição de EPT permite que apenas uma página de detalhes do projeto tipo de *criar* .  <br/> |
|EnterpriseProjectTypeHasWorkflowOnlyCreatePDPAllowed = 35220  <br/> |Um modelo de projeto empresarial (EPT) para um fluxo de trabalho requer uma associado página de detalhes do projeto de tipo *criar* (PDP) para criar um projeto usando o EPT. Este erro ocorre quando o PDP definição EPT do fluxo de trabalho é de outro tipo. Outros tipos PDP são *Normal* para a edição de um projeto e o *Status do fluxo de trabalho* para mostrando detalhes de um projeto relacionadas ao fluxo de trabalho.  <br/> |
|EnterpriseProjectTypeInvalidData = 35221  <br/> |O **WorkflowDataSet** para o tipo de projeto da empresa tem dados que não são válidos.  <br/> |
|EnterpriseProjectNoDefaultEnterpriseProjectTypeDefined = 35222  <br/> |Nenhum tipo de projeto da empresa foi definido.  <br/> |
|EnterpriseProjectTypeAtLeastOnePDPIsRequired = 35223  <br/> |Pelo menos uma página de detalhes do projeto é necessária para o tipo de projeto da empresa.  <br/> |
|EnterpriseProjectTypeWorkflowStatusPDPNotAllowed = 35224  <br/> |Uma página de detalhes do projeto para o status do fluxo de trabalho não é permitida para o tipo de projeto da empresa.  <br/> |
|EnterpriseProjectTypeCannotChangeWorkflowAssociation = 35225  <br/> |O projeto já tem um EPT (tipo de projeto da empresa); você não pode alterar o EPT para o projeto;  <br/> |

<a name="pj15_ErrorCodes_WSS"></a>

## <a name="table-31-wssinterop-and-objectlinkprovider-sharepoint-integration"></a>Tabela 31. WssInterop e ObjectLinkProvider (integração do SharePoint)

|Código de erro de integração do SharePoint|Descrição|
|:-----|:-----|
|WSSCreateSiteFailure = 16400  <br/> |Falha ao criar o site do SharePoint para o espaço de trabalho do projeto.  <br/> |
|WSSCannotCreateWebWithBlankName = 16401  <br/> |Não é possível criar um site do SharePoint com um nome em branco.  <br/> |
|WSSWebAlreadyExists = 16402  <br/> |O site do SharePoint já existe.  <br/> |
|WSSInvalidProjectUID = 16403  <br/> |O GUID do projeto não é válido para o espaço de trabalho do projeto do SharePoint.  <br/> |
|WSSProjectAlreadyHasSpWeb = 16404  <br/> |O projeto já tem um site de espaço de trabalho do SharePoint.  <br/> |
|WSSWebDoesNotExist = 16405  <br/> |O site do SharePoint não existe.  <br/> |
|WSSSpWebAlreadyLinkedToProject = 16406  <br/> |O site do SharePoint já está vinculado ao projeto.  <br/> |
|WSSWebHierarchyDoesNotExist = 16407  <br/> |A hierarquia da Web do SharePoint não existe.  <br/> |
|WSSSPWebHasChildren = 16408  <br/> |O site do SharePoint tem sites filhos.  <br/> |
|WSSURIInvalidFormat = 16409  <br/> |O formato para um URI do site do SharePoint não é válido.  <br/> |
|WSSSyncReportingDataFailed = 16410  <br/> |Falha ao sincronizar dados de relatório para o SharePoint.  <br/> |
|WSSWorkspaceUrlPathTooLong = 16411  <br/> |Caminho da URL de espaço de trabalho de projeto do SharePoint muito longa.  <br/> |
|WSSWorkspaceNameContainsIllegalChars = 16412  <br/> |Um ou mais caracteres em um nome de site de projeto do SharePoint não são válidos. Os seguintes caracteres não são válidos em um nome de projeto: / ": \<\> | , . ' ? \* #  <br/> |
|WSSInvalidWssServerUid = 16413  <br/> |O GUID do servidor do SharePoint não é válido.  <br/> |
|WSSSyncUsersFailed = 16414  <br/> |Falha ao sincronizar usuários do Project Server com o SharePoint.  <br/> |
|WSSWrongWebTemplateLCID = 16415  <br/> |O identificador de localidade (ID do idioma) do modelo da Web do SharePoint não é válido.  <br/> |
|WSSWrongWebTemplate = 16416  <br/> |O modelo da Web do SharePoint não é válido.  <br/> |
|WSSWebIsNotProjectWorkspace = 16417  <br/> |O site do SharePoint não é um espaço de trabalho do projeto.  <br/> |
|WSSWebCannotStartOrEndOnPeriod = 16418  <br/> |Um nome da Web do SharePoint não pode começar ou terminar com um ponto.  <br/> |
|WSSCannotDeleteSiteCollection = 16419  <br/> |Não é possível excluir o conjunto de sites.  <br/> |
|WSSListUidInvalid = 16420  <br/> |O GUID da lista do SharePoint não é válido.  <br/> |
|WSSSyncDataSetListUidMismatch = 16421  <br/> |O GUID da lista do SharePoint não corresponde ao GUID da lista no **DataSet** que está sendo sincronizado.  <br/> |
|WSSSyncDataSetMissingProjectSettingsRow = 16422  <br/> |O **DataSet** para sincronização com o SharePoint está ausente da linha de configurações do projeto.  <br/> |
|WSSSyncDataSetTaskMappingsNotAllowed = 16423  <br/> |Os mapeamentos de tarefa não são permitidos no **DataSet** para sincronização com o SharePoint.  <br/> |
|WSSSyncDataSetWssListUidEmpty = 16424  <br/> |O GUID da lista do SharePoint está vazio no **DataSet** para sincronização com o SharePoint.  <br/> |
|WSSSyncDataNotFound = 16425  <br/> |Há dados ausentes na sincronização com o SharePoint.  <br/> |
|WSSSyncCriticalDataValidationError = 16426  <br/> |Há um erro de validação de dados críticos na sincronização com o SharePoint.  <br/> |
|WSSSyncSharePointListNotAccessibleError = 16427  <br/> |A lista do SharePoint está inacessível.  <br/> |
|WSSSyncInvalidEntityUids = 16428  <br/> |Os GUIDs da entidade não são válidos para sincronização com o SharePoint.  <br/> |
|WSSSyncInvalidSyncData = 16429  <br/> |A sincronização do SharePoint tem dados que não são válidos.  <br/> |
|WSSSyncSPSummaryTaskAssignedToResourceError = 16430  <br/> |A sincronização do SharePoint tem uma tarefa de resumo atribuída a um recurso.  <br/> |
|WSSSyncInsufficientPermissionsToCreateWinUser = 16431  <br/> |As permissões não são suficientes para criar um usuário do Windows ao sincronizar com o SharePoint.  <br/> |
|WSSSyncNoDefaultValueForCustomField = 16432  <br/> |Um campo personalizado não tem um valor padrão na sincronização do SharePoint.  <br/> |
|WSSOLPCreateLinkFailure = 18000  <br/> |Falha ao criar link para o provedor de links de objeto do SharePoint.  <br/> |
|WSSOLPDeleteWebObjectLinkError = 18001  <br/> |Erro ao excluir um link de objeto da Web no provedor de links de objeto do SharePoint.  <br/> |
|WSSInvalidPermissionsToWssList = 18002  <br/> |As permissões não são válidas para a lista do SharePoint.  <br/> |
|WSSWebIsNotUnderDefaultCollection = 18003  <br/> |O site do SharePoint não está no conjunto padrão.  <br/> |
|WSSWorkspaceUrlIsNotUnderPrimaryCollection = 18004  <br/> |Espaço de trabalho especificado url não está no conjunto de sites associado a essa instância do project server. Isso é necessário para o modo de permissão atual.  <br/> |
|WSSWorkspacesMustBeRestrictedToDefaultCollection = 18005  <br/> |Os espaços de trabalho devem ficar restritos ao conjunto de sites padrão no modo de permissão atual.  <br/> |

<a name="pj15_ErrorCodes_ASMXExample"> </a>

## <a name="error-code-example-for-asmx"></a>Exemplo de código de erro para ASMX

Para obter uma lista de erros se você receber uma exceção quando você chama um método PSI, passe o objeto **SoapException** ao construtor da classe [Microsoft.Office.Project.Server.Library.PSClientError](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.aspx) . Em seguida, você pode usar [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx) para armazenar as informações de erro em uma matriz de **PSErrorInfo** e enumerar os erros, como no exemplo a seguir. 
  
> [!NOTE]
> O objeto **PSErrorInfo** não inclui todas as informações que você possa precisar. Por exemplo, se você usar **Resource.CheckOutResources** onde um dos recursos já está check-out, **PSErrorInfo** mostra o motivo da falha para cada recurso que não é possível fazer check-out, mas não inclui o nome do recurso ou o GUID. Para obter uma forma obter mais informações em um aplicativo baseado em ASMX, consulte [CheckOutResources](https://msdn.microsoft.com/library/WebSvcResource.Resource.CheckOutResources.aspx) . 
  
```cs
using System;
using System.Collections.Generic;
using System.Text;
using System.Web.Services.Protocols;
using System.Windows.Forms;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch (SoapException ex)
{
    string errAttributeName;
    string errAttribute;
    string errMess = "".PadRight(30, '=') + "\r\n" + "Error: " + "\r\n";
    PSLibrary.PSClientError error = new PSLibrary.PSClientError(ex);
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\n" + ex.Message.ToString() + "\r\n";
        errMess += "".PadRight(30, '=') + "\r\nPSCLientError Output:\r\n \r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName +
                       ": " + errAttribute;
        }
        errMess += "\r\n".PadRight(30, '=');
    }
    MessageBox.Show(errMess, "Error", MessageBoxButtons.OK,
        MessageBoxIcon.Error);
}
```

<a name="pj15_ErrorCodes_WCFExample"> </a>

## <a name="error-code-example-for-wcf"></a>Exemplo de código de erro para WCF

Para obter uma lista de erros se você receber um **System.ServiceModel.FaultException** quando você chama um método PSI em um aplicativo baseado em WCF, você pode extrair um objeto **PSClientError** do objeto **FaultException** . Em seguida, você pode usar [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx) para armazenar as informações de erro em uma matriz de **PSErrorInfo** e enumerar os erros, como no exemplo anterior de ASMX. 
  
```cs
using System;
using System.Text;
using System.ServiceModel;
using System.Xml;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch(FaultException fault)
{
    // Use the WCF FaultException, because the ASMX SoapException does not 
    // exist in a WCF-based application.
    WriteFaultOutput(fault);
}
// Get a PSClientError object from the WCF FaultException object, and
// then display the exception details and each error in the PSClientError stack.
private static void WriteFaultOutput(FaultException fault)
{
    string errAttributeName;
    string errAttribute;
    string errOut;
    string errMess = "".PadRight(30, '=') + "\r\n"
        + "Error details: " + "\r\n";
    PSLibrary.PSClientError error = GetPSClientError(fault, out errOut);
    errMess += errOut;
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\r\n".PadRight(30, '=') + "\r\nPSClientError output:\r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName
                + ": " + errAttribute;
        }
    }
    Console.ForegroundColor = ConsoleColor.Red;
    Console.WriteLine(errMess);
    Console.ResetColor();
}
/// <summary>
/// Extract a PSClientError object from the ServiceModel.FaultException,
/// for use in output of the GetPSClientError stack of errors.
/// </summary>
/// <param name="e"></param>
/// <param name="errOut">Shows that FaultException has more information 
/// about the errors than PSClientError has. FaultException can also contain 
/// other types of errors, such as failure to connect to the server.</param>
/// <returns>PSClientError object, for enumerating errors.</returns>
public static PSLibrary.PSClientError GetPSClientError(FaultException e, 
                                                        out string errOut)
{
    const string PREFIX = "GetPSClientError() returns null: ";
    errOut = string.Empty;
    PSLibrary.PSClientError psClientError = null;
    if (e == null)
    {
        errOut = PREFIX + "Null parameter (FaultException e) passed in.";
        psClientError = null;
    }
    else
    {
        // Get a ServiceModel.MessageFault object.
        var messageFault = e.CreateMessageFault();
        if (messageFault.HasDetail)
        {
            using (var xmlReader = messageFault.GetReaderAtDetailContents())
            {
                var xml = new XmlDocument();
                xml.Load(xmlReader);
                var serverExecutionFault = xml["ServerExecutionFault"];
                if (serverExecutionFault != null)
                {
                    var exceptionDetails = serverExecutionFault["ExceptionDetails"];
                    if (exceptionDetails != null)
                    {
                        try
                        {
                            errOut = exceptionDetails.InnerXml + "\r\n";
                            psClientError = 
                                new PSLibrary.PSClientError(exceptionDetails.InnerXml);
                        }
                        catch (InvalidOperationException ex)
                        {
                            errOut = PREFIX + "Unable to convert fault exception info ";
                            errOut += "a valid Project Server error message. Message: \n\t";
                            errOut += ex.Message;
                            psClientError = null;
                        }
                    }
                    else
                    {
                        errOut = PREFIX + "The FaultException e is a ServerExecutionFault, "
                            + "but does not have ExceptionDetails.";
                    }
                }
                else
                {
                    errOut = PREFIX + "The FaultException e is not a ServerExecutionFault.";
                }
            }
        }
        else // No detail in the MessageFault.
        {
            errOut = PREFIX + "The FaultException e does not have any detail.";
        }
    }
    errOut += "\r\n" + e.ToString() + "\r\n";
    return psClientError;
}

```

<br/>

Além dos dados no objeto **PSClientError** , o objeto **FaultException** pode incluir outros tipos de erros, como falha para se conectar ao Project Server. O parâmetro _errOut_ do método **GetPSClientError** no exemplo anterior mostra informações adicionais. Por exemplo, o exemplo de código **CreateProject4Department** no método [QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) inclui comentários que mostram como criar erros durante a configuração de propriedades da tabela **ProjectCustomFields** . Quando o aplicativo é executado, o parâmetro _errOut_ inclui o elemento **errinfo** e outros dados (aqui formatados da saída do console). 
  
```XML
==============================
Error details:
<errinfo xmlns="">
  <dataset name="ProjectDataSet">
    <table name="ProjectCustomFields">
      <row CUSTOM_FIELD_UID="976d3bd9-95ff-40a2-a938-960c410b0341">
        <error id="11704" name="CustomFieldInvalidTypeColumnFilledIn" 
               uid="aa8a2fab-9262-422f-b022-ca1cb12bc75f"></error>
        <error id="11713" name="CustomFieldRequiredValueNotProvided" 
               uid="dc2e2156-86e9-4aac-bede-d07dc44dfedc"></error>
      </row>
    </table>
  </dataset>
</errinfo>
System.ServiceModel.FaultException`1[SvcProject.ServerExecutionFault]: 
ProjectServerError(s) LastError=CustomFieldRequiredValueNotProvided Instructions: 
Pass this into PSClientError constructor to access all error information 
(Fault Detail is equal to SvcProject.ServerExecutionFault).
============================
PSClientError output:
CustomFieldInvalidTypeColumnFilledIn
============================
PSClientError output:
CustomFieldRequiredValueNotProvided
```

<a name="pj15_ErrorCodes_AR"> </a>

## <a name="see-also"></a>Confira também

- [Artigos de conceituais e instruções do Project](project-conceptual-and-how-to-articles.md)
- [SQL Server Profiler](https://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx)
- [Project Server 2010: O que esperar quando você obtiver a inesperada](https://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx)
- [Visualizador do ULS](https://www.codeproject.com/Articles/458052/ULS-Log-Viewer)
    

