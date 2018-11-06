---
title: Método QueryDef (DAO)
TOCTitle: Execute Method
ms:assetid: ad9e859e-c6fe-496c-a1f2-a000cf4bebcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821728(v=office.15)
ms:contentKeyID: 48547043
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052884
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 55a3f8a345ffa6669ef721395be4cb1286f2696b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997389"
---
# <a name="querydefexecute-method-dao"></a><span data-ttu-id="9b134-102">Método QueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="9b134-102">QueryDef.Execute method (DAO)</span></span>

<span data-ttu-id="9b134-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b134-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b134-104">Executa uma instrução SQL no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="9b134-104">Executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b134-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b134-105">Syntax</span></span>

<span data-ttu-id="9b134-106">*expressão* . Executar (***Opções***)</span><span class="sxs-lookup"><span data-stu-id="9b134-106">*expression* .Execute(***Options***)</span></span>

<span data-ttu-id="9b134-107">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="9b134-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b134-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b134-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b134-109">Nome</span><span class="sxs-lookup"><span data-stu-id="9b134-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9b134-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="9b134-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9b134-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9b134-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="9b134-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b134-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b134-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="9b134-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="9b134-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="9b134-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="9b134-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9b134-115"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9b134-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b134-116">Remarks</span></span>

<span data-ttu-id="9b134-117">Você pode usar as seguintes constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** para opções.</span><span class="sxs-lookup"><span data-stu-id="9b134-117">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for Options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b134-118">Constant</span><span class="sxs-lookup"><span data-stu-id="9b134-118">Constant</span></span></p></th>
<th><p><span data-ttu-id="9b134-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b134-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b134-120"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="9b134-120"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="9b134-121">Nega a permissão de gravação para outros usuários (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9b134-121">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b134-122"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="9b134-122"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="9b134-123">(Padrão) Executa atualizações inconsistentes (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9b134-123">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b134-124"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="9b134-124"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="9b134-125">Executa atualizações consistentes (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9b134-125">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b134-126"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="9b134-126"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="9b134-p101">Executa uma consulta de passagem SQL. A configuração dessa opção passa a instrução SQL para um banco de dados ODBC para processamento (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9b134-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b134-129"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="9b134-129"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="9b134-130">Reverte atualizações se ocorrer erro (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9b134-130">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b134-131"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="9b134-131"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="9b134-132">Gera um erro de tempo de execução caso outro usuário esteja alterando dados que você esteja editando (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9b134-132">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b134-133"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="9b134-133"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="9b134-134">Executa a consulta de forma assíncrona (somente objetos ODBCDirect Connection e QueryDef).</span><span class="sxs-lookup"><span data-stu-id="9b134-134">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b134-135"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="9b134-135"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="9b134-136">Executa a instrução sem chamar primeiro a função SQLPrepare ODBC API (somente objetos ODBCDirect Connection e QueryDef).</span><span class="sxs-lookup"><span data-stu-id="9b134-136">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="9b134-p102">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9b134-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="9b134-p103">[!OBSERVAçãO] As constantes **dbConsistent** e **dbInconsistent** são mutuamente exclusivas. Você pode usar uma ou outra, as não ambas em uma determinada instância de **OpenRecordset**. Usar **dbConsistent** e **dbInconsistent** causará um erro.</span><span class="sxs-lookup"><span data-stu-id="9b134-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="9b134-p104">Use a propriedade **[RecordsAffected](querydef-recordsaffected-property-dao.md)** do objeto **[Connection](connection-object-dao.md)**, **[Database](database-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)** para determinar o número de registros afetados pelo método **[Execute](querydef-execute-method-dao.md)** mais recente. Por exemplo, **RecordsAffected** contém o número de registros excluídos, atualizados ou inseridos ao executar uma consulta ação. Quando você usa o método **Execute** para executar uma consulta, a propriedade **RecordsAffected** do objeto **QueryDef** é definida como o número de registros afetados.</span><span class="sxs-lookup"><span data-stu-id="9b134-p104">Use the **[RecordsAffected](querydef-recordsaffected-property-dao.md)** property of the **[Connection](connection-object-dao.md)**, **[Database](database-object-dao.md)**, or **[QueryDef](querydef-object-dao.md)** object to determine the number of records affected by the most recent **[Execute](querydef-execute-method-dao.md)** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="9b134-p105">Em um espaço de trabalho do Microsoft Access, se você fornecer uma instrução SQL sintaticamente correta e tiver as permissões apropriadas, o método **Execute** não falhará  mesmo que uma única linha possa ser modificada ou excluída. Portanto, sempre use a opção **dbFailOnError** quando empregar o método **Execute** para executar uma consulta atualização ou exclusão. Essa opção gera um erro em tempo de execução e devolve todas as alterações bem-sucedidas se qualquer um dos registros afetados estiver protegido e não puder ser atualizado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="9b134-p105">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="9b134-p106">Em versões anteriores do mecanismo de banco de dados do Microsoft Jet, instruções SQL foram automaticamente incorporadas a transações implícitas. Se parte de uma instrução executada com o **dbFailOnError** tiver falhado, a instrução inteira será devolvida. Para melhorar o desempenho, essas transações implícitas foram removidas a partir da versão 3.5. Se estiver atualizando código DAO antigo, considere o uso de transações explícitas envolvendo instruções **Execute**.</span><span class="sxs-lookup"><span data-stu-id="9b134-p106">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="9b134-p107">Para obter melhor desempenho em um espaço de trabalho do Microsoft Access, especialmente em um ambiente multiusuário, aninhe o método **Execute** em uma transação. Use o método **[BeginTrans](workspace-begintrans-method-dao.md)** no objeto **[Workspace](workspace-object-dao.md)** atual e use o método **Execute** e conclua a transação usando o método **[CommitTrans](workspace-committrans-method-dao.md)** no **Workspace**. Isso salva as alterações em disco e libera todas as proteções colocadas durante a execução da consulta.</span><span class="sxs-lookup"><span data-stu-id="9b134-p107">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **[BeginTrans](workspace-begintrans-method-dao.md)** method on the current **[Workspace](workspace-object-dao.md)** object, then use the **Execute** method, and complete the transaction by using the **[CommitTrans](workspace-committrans-method-dao.md)** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="9b134-155">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9b134-155">Example</span></span>

<span data-ttu-id="9b134-p108">Este exemplo demonstra o método **Execute** quando executado de um objeto **QueryDef** e de um objeto **Banco de Dados**. Os procedimentos ExecuteQueryDef e PrintOutput são necessários para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="9b134-p108">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object. The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span></span>

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
          Debug.Print "  " & rstTemp!LastName & _ 
             ", " & rstTemp!Country 
          rstTemp.MoveNext 
       Loop 
     
    End Sub 
```

<br/>

<span data-ttu-id="9b134-158">O exemplo a seguir mostra como executar uma consulta de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9b134-158">The following example shows how to execute a parameter query.</span></span> <span data-ttu-id="9b134-159">A coleção Parameters é usada para definir o parâmetro Organization da consulta myActionQuery antes que a consulta é executada.</span><span class="sxs-lookup"><span data-stu-id="9b134-159">The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="9b134-160">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="9b134-160">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```
