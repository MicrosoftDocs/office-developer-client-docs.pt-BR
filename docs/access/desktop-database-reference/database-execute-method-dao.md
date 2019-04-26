---
title: Método Database.Execute (DAO)
TOCTitle: Execute method
ms:assetid: 9294d530-f70f-e1ed-3990-ce128de4378b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197654(v=office.15)
ms:contentKeyID: 48546378
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 5a2ebbb549e309349695d93618f4522a2dbf7a7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294957"
---
# <a name="databaseexecute-method-dao"></a><span data-ttu-id="0c5fa-102">Método Database.Execute (DAO)</span><span class="sxs-lookup"><span data-stu-id="0c5fa-102">Database.Execute Method (DAO)</span></span>

<span data-ttu-id="0c5fa-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c5fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c5fa-104">Executa uma consulta de ação ou executa uma instrução SQL no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="0c5fa-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c5fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c5fa-105">Syntax</span></span>

<span data-ttu-id="0c5fa-106">*expression* .Execute(***Query***, ***Options***)</span><span class="sxs-lookup"><span data-stu-id="0c5fa-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="0c5fa-107">*expressão* Uma variável que representa um objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="0c5fa-107">*expression*  A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c5fa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c5fa-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0c5fa-109">Nome</span><span class="sxs-lookup"><span data-stu-id="0c5fa-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0c5fa-110">Necessário/opcional</span><span class="sxs-lookup"><span data-stu-id="0c5fa-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0c5fa-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0c5fa-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="0c5fa-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c5fa-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c5fa-113"><em>Query</em></span><span class="sxs-lookup"><span data-stu-id="0c5fa-113"><em>Query</em></span></span></p></td>
<td><p><span data-ttu-id="0c5fa-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0c5fa-114">Required</span></span></p></td>
<td><p><span data-ttu-id="0c5fa-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="0c5fa-115"><strong>String</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c5fa-116"><em>Opções</em></span><span class="sxs-lookup"><span data-stu-id="0c5fa-116"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="0c5fa-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="0c5fa-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="0c5fa-118"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0c5fa-118"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0c5fa-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c5fa-119">Remarks</span></span>

<span data-ttu-id="0c5fa-120">Você pode usar as seguintes constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** para options.</span><span class="sxs-lookup"><span data-stu-id="0c5fa-120">You can use the following  RecordsetOptionEnum  constants for  options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0c5fa-121">Constante</span><span class="sxs-lookup"><span data-stu-id="0c5fa-121">Constant</span></span></p></th>
<th><p><span data-ttu-id="0c5fa-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c5fa-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c5fa-123"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="0c5fa-123"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="0c5fa-124">Nega a permissão de gravação para outros usuários (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0c5fa-124">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c5fa-125"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="0c5fa-125"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="0c5fa-126">(Padrão) Executa atualizações inconsistentes (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0c5fa-126">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c5fa-127"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="0c5fa-127"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="0c5fa-128">Executa atualizações consistentes (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0c5fa-128">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c5fa-129"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="0c5fa-129"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="0c5fa-p101">Executa uma consulta de passagem SQL. A configuração dessa opção passa a instrução SQL para um banco de dados ODBC para processamento (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0c5fa-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c5fa-132"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="0c5fa-132"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="0c5fa-133">Reverte atualizações se ocorrer erro (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0c5fa-133">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c5fa-134"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="0c5fa-134"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="0c5fa-135">Gera um erro de tempo de execução caso outro usuário esteja alterando dados que você esteja editando (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0c5fa-135">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c5fa-136"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="0c5fa-136"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="0c5fa-137">Executa a consulta de forma assíncrona (somente objetos ODBCDirect Connection e QueryDef).</span><span class="sxs-lookup"><span data-stu-id="0c5fa-137">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c5fa-138"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="0c5fa-138"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="0c5fa-139">Executa a instrução sem chamar primeiro a função SQLPrepare ODBC API (somente objetos ODBCDirect Connection e QueryDef).</span><span class="sxs-lookup"><span data-stu-id="0c5fa-139">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="0c5fa-p102">O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0c5fa-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="0c5fa-p103">As constantes **dbConsistent** e **dbInconsistent** são mutuamente exclusivas. Você pode usar uma ou outra, as não ambas em uma determinada instância de **OpenRecordset**. Usar **dbConsistent** e **dbInconsistent** causará um erro.</span><span class="sxs-lookup"><span data-stu-id="0c5fa-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="0c5fa-p104">O método **Execute** só será válido para consultas de ação. Se você usar **Execute** com outro tipo de consulta, ocorrerá um erro. Como uma consulta de ação não retorna registros, **Execute** não retorna um **Recordset** (a execução de uma consulta de passagem SQL em um espaço de trabalho ODBCDirect não retornará um erro se um **Recordset** não for retornado).</span><span class="sxs-lookup"><span data-stu-id="0c5fa-p104">The **Execute** method is valid only for action queries. If you use **Execute** with another type of query, an error occurs. Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**. (Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="0c5fa-p105">Use a propriedade **RecordsAffected** do objeto **Connection**, **Database** ou **QueryDef** para determinar o número de registros afetados pelo método **Execute** mais recente. Por exemplo, **RecordsAffected** contém o número de registros excluídos, atualizados ou inseridos na execução de uma consulta de ação. Quando você usar o método **Execute** para executar uma consulta, a propriedade **RecordsAffected** do objeto **QueryDef** é definida como o número de registros afetados.</span><span class="sxs-lookup"><span data-stu-id="0c5fa-p105">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="0c5fa-p106">Em um espaço de trabalho do Microsoft Access, se você fornecer uma instrução SQL sintaticamente correta e tiver as permissões apropriadas, o método **Execute** não falhará  mesmo que uma única linha possa ser modificada ou excluída. Portanto, sempre use a opção **dbFailOnError** quando empregar o método **Execute** para executar uma consulta atualização ou exclusão. Essa opção gera um erro em tempo de execução e devolve todas as alterações bem-sucedidas se qualquer um dos registros afetados estiver protegido e não puder ser atualizado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="0c5fa-p106">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="0c5fa-p107">Em versões anteriores do mecanismo de banco de dados do Microsoft Jet, instruções SQL foram automaticamente incorporadas a transações implícitas. Se parte de uma instrução executada com o **dbFailOnError** tiver falhado, a instrução inteira será devolvida. Para melhorar o desempenho, essas transações implícitas foram removidas a partir da versão 3.5. Se estiver atualizando código DAO antigo, considere o uso de transações explícitas envolvendo instruções **Execute**.</span><span class="sxs-lookup"><span data-stu-id="0c5fa-p107">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="0c5fa-p108">Para obter o melhor desempenho em um espaço de trabalho do Microsoft Access, especialmente em um ambiente multiusuário, aninhe o método **Execute** em uma transação. Use o método **BeginTrans** no objeto **Espaço de Trabalho** atual, então use o método **Execute** e conclua a transação usando o método **CommitTrans** no **Espaço de Trabalho**. Isso salva alterações no disco e libera qualquer bloqueio gerado durante a execução da consulta.</span><span class="sxs-lookup"><span data-stu-id="0c5fa-p108">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="0c5fa-162">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0c5fa-162">Example</span></span>

<span data-ttu-id="0c5fa-p109">Este exemplo demonstra o método **Execute** quando executado de um objeto **QueryDef** e de um objeto **Banco de Dados**. Os procedimentos ExecuteQueryDef e PrintOutput são necessários para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="0c5fa-p109">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object. The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span></span>

```vb
    Sub ExecuteX() 
     
     Dim dbsNorthwind As Database 
     Dim strSQLChange As String 
     Dim strSQLRestore As String 
     Dim qdfChange As QueryDef 
     Dim rstEmployees As Recordset 
     Dim errLoop As Error 
     
     ' Define two SQL statements for action queries. 
     strSQLChange = "UPDATE Employees SET Country = " & _ 
     "'United States' WHERE Country = 'USA'" 
     strSQLRestore = "UPDATE Employees SET Country = " & _ 
     "'USA' WHERE Country = 'United States'" 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Create temporary QueryDef object. 
     Set qdfChange = dbsNorthwind.CreateQueryDef("", _ 
     strSQLChange) 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT LastName, Country FROM Employees", _ 
     dbOpenForwardOnly) 
     
     ' Print report of original data. 
     Debug.Print _ 
     "Data in Employees table before executing the query" 
     PrintOutput rstEmployees 
     
     ' Run temporary QueryDef. 
     ExecuteQueryDef qdfChange, rstEmployees 
     
     ' Print report of new data. 
     Debug.Print _ 
     "Data in Employees table after executing the query" 
     PrintOutput rstEmployees 
     
     ' Run action query to restore data. Trap for errors, 
     ' checking the Errors collection if necessary. 
     On Error GoTo Err_Execute 
     dbsNorthwind.Execute strSQLRestore, dbFailOnError 
     On Error GoTo 0 
     
     ' Retrieve the current data by requerying the recordset. 
     rstEmployees.Requery 
     
     ' Print report of restored data. 
     Debug.Print "Data after executing the query " & _ 
     "to restore the original information" 
     PrintOutput rstEmployees 
     
     rstEmployees.Close 
     
     Exit Sub 
     
    Err_Execute: 
     
     ' Notify user of any errors that result from 
     ' executing the query. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
     
    Sub ExecuteQueryDef(qdfTemp As QueryDef, _ 
     rstTemp As Recordset) 
     
     Dim errLoop As Error 
     
     ' Run the specified QueryDef object. Trap for errors, 
     ' checking the Errors collection if necessary. 
     On Error GoTo Err_Execute 
     qdfTemp.Execute dbFailOnError 
     On Error GoTo 0 
     
     ' Retrieve the current data by requerying the recordset. 
     rstTemp.Requery 
     
     Exit Sub 
     
    Err_Execute: 
     
     ' Notify user of any errors that result from 
     ' executing the query. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
     
    Sub PrintOutput(rstTemp As Recordset) 
     
     ' Enumerate Recordset. 
     Do While Not rstTemp.EOF 
     Debug.Print " " & rstTemp!LastName & _ 
     ", " & rstTemp!Country 
     rstTemp.MoveNext 
     Loop 
     
    End Sub
```
