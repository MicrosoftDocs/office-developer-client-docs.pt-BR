---
title: Método Execute (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 488fca77f09ae683232ccbd3e88a5b42d1faa1c3
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998564"
---
# <a name="connectionexecute-method-dao"></a><span data-ttu-id="13178-102">Método Execute (DAO)</span><span class="sxs-lookup"><span data-stu-id="13178-102">Connection.Execute method (DAO)</span></span>

<span data-ttu-id="13178-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="13178-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13178-104">Executa uma consulta de ação ou executa uma instrução SQL no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="13178-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="13178-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13178-105">Syntax</span></span>

<span data-ttu-id="13178-106">*expressão* . Executar (***consulta***, ***Opções***)</span><span class="sxs-lookup"><span data-stu-id="13178-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="13178-107">*expressão* Uma variável que representa um objeto de **Conexão** .</span><span class="sxs-lookup"><span data-stu-id="13178-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="13178-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13178-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13178-109">Nome</span><span class="sxs-lookup"><span data-stu-id="13178-109">Name</span></span></p></th>
<th><p><span data-ttu-id="13178-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="13178-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="13178-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="13178-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="13178-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="13178-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13178-113"><em>Query</em></span><span class="sxs-lookup"><span data-stu-id="13178-113"><em>Query</em></span></span></p></td>
<td><p><span data-ttu-id="13178-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="13178-114">Required</span></span></p></td>
<td><p><span data-ttu-id="13178-115"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="13178-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="13178-116">Uma <strong>String</strong> que é uma instrução SQL ou o valor da propriedade <strong>Name</strong> de um objeto <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="13178-116">A <strong>String</strong> that is an SQL statement or the <strong>Name</strong> property value of a <strong>QueryDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13178-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="13178-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="13178-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="13178-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="13178-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="13178-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="13178-120">Uma constante ou combinação de constantes que determina as características de integridade dos dados da consulta, conforme especificado em Configurações.</span><span class="sxs-lookup"><span data-stu-id="13178-120">A constant or combination of constants that determines the data integrity characteristics of the query, as specified in Settings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="13178-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="13178-121">Remarks</span></span>

<span data-ttu-id="13178-122">Você pode usar as seguintes constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** para opções.</span><span class="sxs-lookup"><span data-stu-id="13178-122">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13178-123">Constant</span><span class="sxs-lookup"><span data-stu-id="13178-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="13178-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="13178-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13178-125"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="13178-125"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="13178-126">Nega a permissão de gravação para outros usuários (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="13178-126">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13178-127"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="13178-127"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="13178-128">(Padrão) Executa atualizações inconsistentes (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="13178-128">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13178-129"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="13178-129"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="13178-130">Executa atualizações consistentes (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="13178-130">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13178-131"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="13178-131"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="13178-p101">Executa uma consulta de passagem SQL. A configuração dessa opção passa a instrução SQL para um banco de dados ODBC para processamento (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="13178-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13178-134"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="13178-134"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="13178-135">Reverte atualizações se ocorrer erro (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="13178-135">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13178-136"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="13178-136"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="13178-137">Gera um erro de tempo de execução caso outro usuário esteja alterando dados que você esteja editando (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="13178-137">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13178-138"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="13178-138"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="13178-139">Executa a consulta de forma assíncrona (somente objetos ODBCDirect Connection e QueryDef).</span><span class="sxs-lookup"><span data-stu-id="13178-139">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13178-140"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="13178-140"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="13178-141">Executa a instrução sem chamar primeiro a função SQLPrepare ODBC API (somente objetos ODBCDirect Connection e QueryDef).</span><span class="sxs-lookup"><span data-stu-id="13178-141">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="13178-p102">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="13178-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="13178-p103">[!OBSERVAçãO] As constantes **dbConsistent** e **dbInconsistent** são mutuamente exclusivas. Você pode usar uma ou outra, as não ambas em uma determinada instância de **OpenRecordset**. Usar **dbConsistent** e **dbInconsistent** causará um erro.</span><span class="sxs-lookup"><span data-stu-id="13178-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="13178-p104">O método **Execute** só será válido para consultas de ação. Se você usar **Execute** com outro tipo de consulta, ocorrerá um erro. Como uma consulta de ação não retorna registros, **Execute** não retorna um **Recordset** (a execução de uma consulta de passagem SQL em um espaço de trabalho ODBCDirect não retornará um erro se um **Recordset** não for retornado).</span><span class="sxs-lookup"><span data-stu-id="13178-p104">The **Execute** method is valid only for action queries. If you use **Execute** with another type of query, an error occurs. Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**. (Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="13178-p105">Use a propriedade **RecordsAffected** do objeto **Connection**, **Database** ou **QueryDef** para determinar o número de registros afetados pelo método **Execute** mais recente. Por exemplo, **RecordsAffected** contém o número de registros excluídos, atualizados ou inseridos na execução de uma consulta de ação. Quando você usar o método **Execute** para executar uma consulta, a propriedade **RecordsAffected** do objeto **QueryDef** é definida como o número de registros afetados.</span><span class="sxs-lookup"><span data-stu-id="13178-p105">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="13178-p106">Em um espaço de trabalho do Microsoft Access, se você fornecer uma instrução SQL sintaticamente correta e se tiver as permissões apropriadas, o método **Execute** não falhará  mesmo se nem uma única linha puder ser modificada ou excluída. Dessa forma, sempre use a opção **dbFailOnError** ao utilizar o método **Execute** para executar uma consulta de atualização ou de exclusão. Essa opção gera um erro de tempo de execução e reverte todas as alterações bem-sucedidas caso qualquer um dos registros afetados esteja bloqueado ou não possa ser atualizado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="13178-p106">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="13178-p107">Em versões anteriores do mecanismo de banco de dados Microsoft Jet, as instruções SQL foram automaticamente inseridas em transações implícitas. Se parte de uma instrução executada com **dbFailOnError** tiver falhado, a instrução inteira é revertida. Para aprimorar o desempenho, essas transações implícitas foram removidas a partir da versão 3.5. Se você estiver atualizando um código DAO mais antigo, considere o uso de transações explícitas em torno de instruções **Execute**.</span><span class="sxs-lookup"><span data-stu-id="13178-p107">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="13178-p108">Para obter melhor desempenho em um espaço de trabalho do Microsoft Access, especialmente em um ambiente multiusuário, aninhe o método **Execute** em uma transação. Use o método **BeginTrans** no atual objeto **Workspace**, em seguida use o método **Execute** e conclua a transação usando o método **CommitTrans** no **Workspace**. Isso salvará as alterações em disco e liberará quaisquer proteções durante a execução da consulta.</span><span class="sxs-lookup"><span data-stu-id="13178-p108">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

