---
title: Método Database.Execute (DAO)
TOCTitle: Execute Method
ms:assetid: 9294d530-f70f-e1ed-3990-ce128de4378b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197654(v=office.15)
ms:contentKeyID: 48546378
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e72de1f266b1dc24267b1c7f3c43be489d92fb5e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889592"
---
# <a name="databaseexecute-method-dao"></a>Método Database.Execute (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Executa uma consulta de ação ou executa uma instrução SQL no objeto especificado.

## <a name="syntax"></a>Sintaxe

*expressão* . Executar (***consulta***, ***Opções***)

*expressão* Uma variável que representa um objeto de **banco de dados** .

### <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Query</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Cadeia de caracteres</strong></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Opções</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar as seguintes constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** para opções.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDenyWrite</strong></p></td>
<td><p>Nega a permissão de gravação para outros usuários (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(Padrão) Executa atualizações inconsistentes (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>Executa atualizações consistentes (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>Executa uma consulta de passagem SQL. A configuração dessa opção passa a instrução SQL para um banco de dados ODBC para processamento (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>Reverte atualizações se ocorrer erro (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>Gera um erro de tempo de execução caso outro usuário esteja alterando dados que você esteja editando (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Executa a consulta de forma assíncrona (somente objetos ODBCDirect Connection e QueryDef).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>Executa a instrução sem chamar primeiro a função SQLPrepare ODBC API (somente objetos ODBCDirect Connection e QueryDef).</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> [!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.

> [!NOTE]
> [!OBSERVAçãO] As constantes **dbConsistent** e **dbInconsistent** são mutuamente exclusivas. Você pode usar uma ou outra, as não ambas em uma determinada instância de **OpenRecordset**. Usar **dbConsistent** e **dbInconsistent** causará um erro.

O método **Execute** só será válido para consultas de ação. Se você usar **Execute** com outro tipo de consulta, ocorrerá um erro. Como uma consulta de ação não retorna registros, **Execute** não retorna um **Recordset** (a execução de uma consulta de passagem SQL em um espaço de trabalho ODBCDirect não retornará um erro se um **Recordset** não for retornado).

Use a propriedade **RecordsAffected** do objeto **Connection**, **Database** ou **QueryDef** para determinar o número de registros afetados pelo método **Execute** mais recente. Por exemplo, **RecordsAffected** contém o número de registros excluídos, atualizados ou inseridos na execução de uma consulta de ação. Quando você usar o método **Execute** para executar uma consulta, a propriedade **RecordsAffected** do objeto **QueryDef** é definida como o número de registros afetados.

Em um espaço de trabalho do Microsoft Access, se você fornecer uma instrução SQL sintaticamente correta e se tiver as permissões apropriadas, o método **Execute** não falhará  mesmo se nem uma única linha puder ser modificada ou excluída. Dessa forma, sempre use a opção **dbFailOnError** ao utilizar o método **Execute** para executar uma consulta de atualização ou de exclusão. Essa opção gera um erro de tempo de execução e reverte todas as alterações bem-sucedidas caso qualquer um dos registros afetados esteja bloqueado ou não possa ser atualizado ou excluído.

Em versões anteriores do mecanismo de banco de dados Microsoft Jet, as instruções SQL foram automaticamente inseridas em transações implícitas. Se parte de uma instrução executada com **dbFailOnError** tiver falhado, a instrução inteira é revertida. Para aprimorar o desempenho, essas transações implícitas foram removidas a partir da versão 3.5. Se você estiver atualizando um código DAO mais antigo, considere o uso de transações explícitas em torno de instruções **Execute**.

Para obter o melhor desempenho em um espaço de trabalho do Microsoft Access, especialmente em um ambiente multiusuário, aninhe o método **Execute** em uma transação. Use o método **BeginTrans** no objeto **Espaço de Trabalho** atual, então use o método **Execute** e conclua a transação usando o método **CommitTrans** no **Espaço de Trabalho**. Isso salva alterações no disco e libera qualquer bloqueio gerado durante a execução da consulta.

## <a name="example"></a>Exemplo

Este exemplo demonstra o método **Execute** quando executado de um objeto **QueryDef** e de um objeto **Banco de Dados**. Os procedimentos ExecuteQueryDef e PrintOutput são necessários para a execução deste procedimento.

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
