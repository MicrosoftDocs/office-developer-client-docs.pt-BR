---
title: Método Database.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 06/04/2019
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b13abd7f3f2c856a0f1a1288717d6f8affb81252
ms.sourcegitcommit: 4a570873914c58dd4cdbe97b5d9ec41866dc797c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2019
ms.locfileid: "34675740"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="842f2-102">Método Database.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="842f2-102">Database.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="842f2-103">**Se aplica ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="842f2-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="842f2-104">Cria um novo objeto **[Conjunto de registros](recordset-object-dao.md)** e o acrescenta à coleção **Conjuntos de registros**.</span><span class="sxs-lookup"><span data-stu-id="842f2-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="842f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="842f2-105">Syntax</span></span>

<span data-ttu-id="842f2-106">*expressão*.**OpenRecordset** (_Nome_, _Tipo_, _Opções_, _LockEdit_)</span><span class="sxs-lookup"><span data-stu-id="842f2-106">*expression*.**OpenRecordset** (_Name_, _Type_, _Options_, _LockEdit_)</span></span>

<span data-ttu-id="842f2-107">*expressão* Uma variável que representa um objeto do **Banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="842f2-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="842f2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="842f2-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="842f2-109">Nome</span><span class="sxs-lookup"><span data-stu-id="842f2-109">Name</span></span></p></th>
<th><p><span data-ttu-id="842f2-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="842f2-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="842f2-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="842f2-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="842f2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="842f2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="842f2-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="842f2-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="842f2-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="842f2-114">Required</span></span></p></td>
<td><p><span data-ttu-id="842f2-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="842f2-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="842f2-p101">A origem dos registros para o novo <strong>Recordset</strong>. A origem pode ser um nome de tabela, um nome de consulta ou uma instrução SQL que retorna registros. Para objetos de <strong>Recordset</strong> do tipo tabela nos mecanismos de banco de dados do Microsoft Access, a origem pode ser apenas um nome de tabela.</span><span class="sxs-lookup"><span data-stu-id="842f2-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="842f2-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="842f2-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="842f2-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="842f2-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="842f2-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="842f2-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="842f2-122">Uma constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica que tipo de <strong>Recordset</strong> abrir.</span><span class="sxs-lookup"><span data-stu-id="842f2-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="842f2-123"><strong>OBSERVAÇÃO</strong>: Se você abrir um <strong>Conjunto de Registros</strong> em um espaço de trabalho do Microsoft Access e não especificar um tipo, o <strong>OpenRecordset</strong> criará uma tabela do tipo <strong>Conjunto de Registros</strong>, se possível.</span><span class="sxs-lookup"><span data-stu-id="842f2-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="842f2-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="842f2-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="842f2-125"><em>Opções</em></span><span class="sxs-lookup"><span data-stu-id="842f2-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="842f2-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="842f2-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="842f2-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="842f2-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="842f2-128">Uma combinação de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica as características do novo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="842f2-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="842f2-129"><strong>Observação</strong>: As constantes <strong>dbConsistent</strong> e <strong>dbInconsistent</strong> são mutuamente exclusivas e usar ambas causará um erro.</span><span class="sxs-lookup"><span data-stu-id="842f2-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="842f2-130">Fornecer um argumento LockEdit quando Opções usa a constante <strong>dbReadOnly</strong> também causará um erro.</span><span class="sxs-lookup"><span data-stu-id="842f2-130">Supplying a LockEdit argument when Options uses the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="842f2-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="842f2-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="842f2-132">Opcional</span><span class="sxs-lookup"><span data-stu-id="842f2-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="842f2-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="842f2-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="842f2-134">Uma constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina o bloqueio do <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="842f2-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="842f2-135"><strong>Observação</strong>: É possível usar <strong>dbReadOnly</strong> tanto no argumento Opções ou quanto no LockedEdit, mas não em ambos.</span><span class="sxs-lookup"><span data-stu-id="842f2-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the Options argument or the LockedEdit argument, but not both.</span></span> <span data-ttu-id="842f2-136">Se usá-la para ambos argumentos, ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="842f2-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="842f2-137">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="842f2-137">Return value</span></span>

<span data-ttu-id="842f2-138">Conjunto de Registros</span><span class="sxs-lookup"><span data-stu-id="842f2-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="842f2-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="842f2-139">Remarks</span></span>

<span data-ttu-id="842f2-p105">Normalmente, se o usuário receber este erro durante a atualização de um registro, seu código deverá atualizar o conteúdo dos campos e recuperar os valores modificados recentemente. Se o erro ocorrer durante a exclusão de um registro, o código poderá exibir os novos dados de registro para o usuário e uma mensagem indicando que os dados foram alterados recentemente. Nesse momento, seu código pode solicitar uma confirmação de que o usuário ainda deseja excluir o registro.</span><span class="sxs-lookup"><span data-stu-id="842f2-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="842f2-143">Você também deve usar a constante **dbSeeChanges** se for abrir um **Recordset** em um espaço de trabalho ODBC conectado ao mecanismo do banco de dados do Microsoft Access versus uma tabela do Microsoft SQL Server 6.0 (ou posterior) com uma coluna IDENTIDADE, caso contrário pode resultar em um erro.</span><span class="sxs-lookup"><span data-stu-id="842f2-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="842f2-p106">Abrir mais de um  **Recordset** em uma origem de dados ODBC pode falhar porque a conexão está ocupada com uma chamada **OpenRecordset** anterior. Uma maneira de evitar isso é preenchendo completamente o **Recordset** usando o método **MoveLast** assim que o **Recordset** for aberto.</span><span class="sxs-lookup"><span data-stu-id="842f2-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="842f2-146">Fechar o **Recordset** com o método **[Close](connection-close-method-dao.md)** o exclui automaticamente da coleção de **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="842f2-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="842f2-147">Se a *fonte* se referir a uma instrução SQL composta por uma sequência concatenada e com um valor não inteiro, e se os parâmetros do sistema especificarem um caractere decimal não-EUA, como uma vírgula (por exemplo, strSQL = "PRICE &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar abrir o **Conjunto de Registros**.</span><span class="sxs-lookup"><span data-stu-id="842f2-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="842f2-148">Isso se deve ao fato de que, durante a concatenação, o número é convertido em uma cadeia de caracteres usando o caractere decimal padrão do seu sistema, e o SQL aceita apenas caracteres decimais americanos.</span><span class="sxs-lookup"><span data-stu-id="842f2-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="842f2-149">**Link fornecido pela** comunidade [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="842f2-149">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="842f2-150">UtterAccess é o fórum wiki e ajuda principal do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="842f2-150">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="842f2-151">Transferir os dados do Access para Excel</span><span class="sxs-lookup"><span data-stu-id="842f2-151">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="842f2-152">Exemplo</span><span class="sxs-lookup"><span data-stu-id="842f2-152">Example</span></span>

<span data-ttu-id="842f2-153">O exemplo a seguir mostra como abrir um Conjunto de Registros baseado em uma consulta de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="842f2-153">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="842f2-154">**Código de exemplo fornecido pela** [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="842f2-154">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="842f2-155">O exemplo a seguir mostra como abrir um Conjunto de Registros baseado em uma tabela ou uma consulta.</span><span class="sxs-lookup"><span data-stu-id="842f2-155">The following example shows how to open a Recordset based on a table or a query.</span></span>

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

<span data-ttu-id="842f2-156">O exemplo a seguir mostra como abrir um Conjunto de Registros baseado em uma instrução de linguagem SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="842f2-156">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

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

<span data-ttu-id="842f2-157">O exemplo a seguir mostra como usar a propriedade do Filtro para determinar que registros incluir em um Recordset aberto subsequentemente.</span><span class="sxs-lookup"><span data-stu-id="842f2-157">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rst = dbs.OpenRecordset(_ 
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



