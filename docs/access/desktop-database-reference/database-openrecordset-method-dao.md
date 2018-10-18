---
title: Método Database.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0dd33e24914d7e45d8678379df5825a42ef0b6fd
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605832"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="1cd19-102">Método Database.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="1cd19-102">Database.OpenRecordset Method (DAO)</span></span>

<span data-ttu-id="1cd19-103">**Aplica-se a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cd19-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="1cd19-104">Cria e anexa um novo objeto **[Recordset](recordset-object-dao.md)** à coleção **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="1cd19-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd19-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cd19-105">Syntax</span></span>

<span data-ttu-id="1cd19-106">*expressão* . OpenRecordset (_**nome**_, _**tipo**_, _**Opções**_, _**LockEdit**_)</span><span class="sxs-lookup"><span data-stu-id="1cd19-106">*expression* .OpenRecordset(_**Name**_, _**Type**_, _**Options**_, _**LockEdit**_)</span></span>

<span data-ttu-id="1cd19-107">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="1cd19-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="1cd19-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cd19-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1cd19-109">Nome</span><span class="sxs-lookup"><span data-stu-id="1cd19-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1cd19-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="1cd19-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="1cd19-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1cd19-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="1cd19-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="1cd19-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cd19-113">Name</span><span class="sxs-lookup"><span data-stu-id="1cd19-113">Name</span></span></p></td>
<td><p><span data-ttu-id="1cd19-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1cd19-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1cd19-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1cd19-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1cd19-p101">A origem dos registros para o novo <strong>Recordset</strong>. A origem pode ser um nome de tabela, um nome de consulta ou uma instrução SQL que retorna registros. Para objetos de <strong>Recordset</strong> do tipo tabela nos mecanismos de banco de dados do Microsoft Access, a origem pode ser apenas um nome de tabela.  </span><span class="sxs-lookup"><span data-stu-id="1cd19-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cd19-119">Type</span><span class="sxs-lookup"><span data-stu-id="1cd19-119">Type</span></span></p></td>
<td><p><span data-ttu-id="1cd19-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="1cd19-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="1cd19-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1cd19-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1cd19-122">Uma constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica que tipo de <strong>Recordset</strong> abrir.</span><span class="sxs-lookup"><span data-stu-id="1cd19-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <span data-ttu-id="1cd19-p102">Se você abrir um **Recordset** em um espaço de trabalho do Microsoft Access se especificar um tipo, o método **OpenRecordset** criará um **Recordset** do tipo tabela, se possível. Se você especificar uma consulta ou tabela vinculada, o método **OpenRecordset** criará um **Recordset** do tipo dynaset.</span><span class="sxs-lookup"><span data-stu-id="1cd19-p102">If you open a **Recordset** in a Microsoft Access workspace and you don't specify a type, **OpenRecordset** creates a table-type **Recordset**, if possible. If you specify a linked table or query, **OpenRecordset** creates a dynaset-type **Recordset**.</span></span>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cd19-125">Opções</span><span class="sxs-lookup"><span data-stu-id="1cd19-125">Options</span></span></p></td>
<td><p><span data-ttu-id="1cd19-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="1cd19-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="1cd19-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1cd19-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1cd19-128">Uma combinação de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica as características do novo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="1cd19-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="1cd19-p103">As constantes **dbConsistent** e **dbInconsistent** são mutuamente exclusivos, e o uso de ambos pode causar erros. Fornecer um argumento.LockEdit quando Options usa o a constante **dbReadOnly** também causa erros.</span><span class="sxs-lookup"><span data-stu-id="1cd19-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive, and using both causes an error. Supplying a LockEdit argument when Options uses the **dbReadOnly** constant also causes an error.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cd19-131">LockEdit</span><span class="sxs-lookup"><span data-stu-id="1cd19-131">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="1cd19-132">Opcional</span><span class="sxs-lookup"><span data-stu-id="1cd19-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="1cd19-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1cd19-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1cd19-134">Uma constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina o bloqueio do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="1cd19-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="1cd19-p104">Você pode usar a constante **dbReadOnly** tanto no argumento Options quanto no LockedEdit, mas não em ambos. Se você usá-lo em ambos os argumentos, ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="1cd19-p104">You can use **dbReadOnly** in either the Options argument or the LockedEdit argument, but not both. If you use it for both arguments, a run-time error occurs.</span></span>


</td>
</tr>
</tbody>
</table>


<span data-ttu-id="1cd19-137"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="1cd19-137"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="1cd19-138">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1cd19-138">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="1cd19-139">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1cd19-139">Return value</span></span>
>>>>>>> <span data-ttu-id="1cd19-140">mestre</span><span class="sxs-lookup"><span data-stu-id="1cd19-140">master</span></span>

<span data-ttu-id="1cd19-141">Recordset</span><span class="sxs-lookup"><span data-stu-id="1cd19-141">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="1cd19-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cd19-142">Remarks</span></span>

<span data-ttu-id="1cd19-p105">Normalmente, se o usuário obtém esse erro ao atualizar um registro, seu código deve atualizar o conteúdo dos campos e recuperar os valores modificados recentemente. Se o erro ocorrer ao excluir um registro, seu código poderá exibir os dados do novo registro para o usuário e uma mensagem indicando que os dados foram alterados recentemente. Nesse momento, seu código pode solicitar uma confirmação de que o usuário ainda deseja excluir o registro.</span><span class="sxs-lookup"><span data-stu-id="1cd19-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="1cd19-146">Você também deverá usar a constante **dbSeeChanges** se abrir um **Recordset** em um espaço de trabalho ODBC conectado ao mecanismo de banco de dados do Microsoft Access em uma tabela do Microsoft SQL Server 6.0 (ou posterior), que tenha uma coluna IDENTITY; caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="1cd19-146">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="1cd19-p106">Abrir mais de um **Recordset** em uma fonte de dados ODBC pode falhar porque a conexão está ocupada com uma chamada **OpenRecordset** anterior. Uma forma de contornar essa situação é preencher totalmente o **Recordset** usando o método **MoveLast** assim que o **Recordset** for aberto.</span><span class="sxs-lookup"><span data-stu-id="1cd19-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="1cd19-149">Fechar um **Recordset** com o método **[Close](connection-close-method-dao.md)** o exclui automaticamente da coleção **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="1cd19-149">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="1cd19-150">Se a *fonte* refere-se a uma instrução SQL composto por uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strSQL = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar abrir o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1cd19-150">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="1cd19-151">Isso ocorre porque durante a concatenação, o número é convertido para uma sequência utilizando o caractere decimal padrão do seu sistema, e o SQL aceita apenas caracteres decimais EUA.</span><span class="sxs-lookup"><span data-stu-id="1cd19-151">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="1cd19-152">**Link fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="1cd19-152">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="1cd19-153">UtterAccess é o fórum principal de wiki e a Ajuda do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1cd19-153">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="1cd19-154">Transferência de dados do Access para o Excel</span><span class="sxs-lookup"><span data-stu-id="1cd19-154">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="1cd19-155">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1cd19-155">Example</span></span>

<span data-ttu-id="1cd19-156">O exemplo a seguir mostra como abrir um Recordset baseado em uma consulta de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1cd19-156">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="1cd19-157">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="1cd19-157">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

<span data-ttu-id="1cd19-158">O exemplo a seguir mostra como abrir um Recordset baseado em uma tabela ou uma consulta.</span><span class="sxs-lookup"><span data-stu-id="1cd19-158">The following example shows how to open a Recordset based on a table or a query.</span></span>

```vb 
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

<span data-ttu-id="1cd19-159">O exemplo a seguir mostra como abrir um Recordset baseado em uma instrução SQL (Structured Query Language).</span><span class="sxs-lookup"><span data-stu-id="1cd19-159">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

<span data-ttu-id="1cd19-160">O exemplo a seguir mostra como abrir uma propriedade Filter para determinar que registros incluir em um Recordset aberto subsequentemente.</span><span class="sxs-lookup"><span data-stu-id="1cd19-160">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```



