---
title: Método Database.CreateTableDef (DAO)
TOCTitle: CreateTableDef Method
ms:assetid: d919b44e-ffae-dc4a-f1cc-d01df49987a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835094(v=office.15)
ms:contentKeyID: 48548046
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052968
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e85c9f22ecfa6efa11a3d916e0bb374948df6104
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463216"
---
# <a name="databasecreatetabledef-method-dao"></a><span data-ttu-id="edcc2-102">Método Database.CreateTableDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="edcc2-102">Database.CreateTableDef Method (DAO)</span></span>

<span data-ttu-id="edcc2-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="edcc2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="edcc2-p101">Cria um novo objeto **[TableDef](tabledef-object-dao.md)** (apenas espaços de trabalho do Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="edcc2-p101">Creates a new **[TableDef](tabledef-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="edcc2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edcc2-106">Syntax</span></span>

<span data-ttu-id="edcc2-107">*expressão* . CreateTableDef (***nome***, ***atributos***, ***SourceTableName***, ***Conecte-se***)</span><span class="sxs-lookup"><span data-stu-id="edcc2-107">*expression* .CreateTableDef(***Name***, ***Attributes***, ***SourceTableName***, ***Connect***)</span></span>

<span data-ttu-id="edcc2-108">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="edcc2-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="edcc2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edcc2-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="edcc2-110">Nome</span><span class="sxs-lookup"><span data-stu-id="edcc2-110">Name</span></span></p></th>
<th><p><span data-ttu-id="edcc2-111">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="edcc2-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="edcc2-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="edcc2-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="edcc2-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="edcc2-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edcc2-114">Name</span><span class="sxs-lookup"><span data-stu-id="edcc2-114">Name</span></span></p></td>
<td><p><span data-ttu-id="edcc2-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="edcc2-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="edcc2-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="edcc2-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="edcc2-p102">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que denomina exclusivamente o novo objeto <strong>TableDef</strong>. Consulte a propriedade <strong><a href="tabledef-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes válidos de <strong>TableDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="edcc2-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>TableDef</strong> object. See the <strong><a href="tabledef-name-property-dao.md">Name</a></strong> property for details on valid <strong>TableDef</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edcc2-119">Atributos</span><span class="sxs-lookup"><span data-stu-id="edcc2-119">Attributes</span></span></p></td>
<td><p><span data-ttu-id="edcc2-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="edcc2-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="edcc2-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="edcc2-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="edcc2-p103">Uma constante ou combinação de constantes que indica uma ou mais características do novo objeto <strong>TableDef</strong>. Consulte a propriedade <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="edcc2-p103">A constant or combination of constants that indicates one or more characteristics of the new <strong>TableDef</strong> object. See the <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edcc2-124">SourceTableName</span><span class="sxs-lookup"><span data-stu-id="edcc2-124">SourceTableName</span></span></p></td>
<td><p><span data-ttu-id="edcc2-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="edcc2-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="edcc2-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="edcc2-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="edcc2-p104">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que contém o nome de uma tabela em um banco de dados externo, que é a fonte original dos dados. A cadeia de caracteres source torna-se a configuração de propriedade <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> do novo objeto <strong>TableDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="edcc2-p104">A <strong>Variant</strong> (<strong>String</strong> subtype) containing the name of a table in an external database that is the original source of the data. The source string becomes the <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> property setting of the new <strong>TableDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edcc2-129">Connect</span><span class="sxs-lookup"><span data-stu-id="edcc2-129">Connect</span></span></p></td>
<td><p><span data-ttu-id="edcc2-130">Opcional</span><span class="sxs-lookup"><span data-stu-id="edcc2-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="edcc2-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="edcc2-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="edcc2-p105">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que contém informações sobre a fonte de um banco de dados aberto, um banco de dados usando em uma consulta passagem ou uma tabela vinculada. Consulte a propriedade <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> para obter mais informações sobre cadeias de caracteres de conexão válidas.</span><span class="sxs-lookup"><span data-stu-id="edcc2-p105">A <strong>Variant</strong> (<strong>String</strong> subtype) containing information about the source of an open database, a database used in a pass-through query, or a linked table. See the <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> property for more information about valid connection strings.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="edcc2-134">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="edcc2-134">Return Value</span></span>

<span data-ttu-id="edcc2-135">TableDef</span><span class="sxs-lookup"><span data-stu-id="edcc2-135">TableDef</span></span>

## <a name="remarks"></a><span data-ttu-id="edcc2-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="edcc2-136">Remarks</span></span>

<span data-ttu-id="edcc2-p106">Se omitir uma ou mais dessas partes opcionais quando usar o método **CreateTableDef**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o objeto, você poderá alterar algumas, mas não todas as suas propriedades. Consulte os tópicos de propriedade individuais para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="edcc2-p106">If you omit one or more of the optional parts when you use the **CreateTableDef** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its properties. See the individual property topics for more details.</span></span>

<span data-ttu-id="edcc2-140">Se name fizer referência a um objeto que já é um membro da coleção ou se você especificar uma propriedade inválida no objeto **TableDef** ou **[campo](field-object-dao.md)** que você está anexando, ocorrerá um erro de tempo de execução quando você usa o método **[Append](tabledefs-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="edcc2-140">If name refers to an object that is already a member of the collection, or you specify an invalid property in the **TableDef** or **[Field](field-object-dao.md)** object you're appending, a run-time error occurs when you use the **[Append](tabledefs-append-method-dao.md)** method.</span></span> <span data-ttu-id="edcc2-141">Além disso, não é possível acrescentar um objeto **TableDef** à coleção **TableDefs** até que se defina ao menos um **Field** para o objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="edcc2-141">Also, you can't append a **TableDef** object to the **TableDefs** collection until you define at least one **Field** for the **TableDef** object.</span></span>

<span data-ttu-id="edcc2-142">Para remover um objeto **TableDef** da coleção **[TableDefs](tabledefs-collection-dao.md)**, use o método **[Delete](tabledefs-delete-method-dao.md)** na coleção.</span><span class="sxs-lookup"><span data-stu-id="edcc2-142">To remove a **TableDef** object from the **[TableDefs](tabledefs-collection-dao.md)** collection, use the **[Delete](tabledefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="edcc2-143">Exemplo</span><span class="sxs-lookup"><span data-stu-id="edcc2-143">Example</span></span>

<span data-ttu-id="edcc2-144">Este exemplo cria um novo objeto **TableDef** no banco de dados Northwind.</span><span class="sxs-lookup"><span data-stu-id="edcc2-144">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb
    Sub CreateTableDefX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create a new TableDef object. 
     Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
     
     With tdfNew 
     ' Create fields and append them to the new TableDef 
     ' object. This must be done before appending the 
     ' TableDef object to the TableDefs collection of the 
     ' Northwind database. 
     .Fields.Append .CreateField("FirstName", dbText) 
     .Fields.Append .CreateField("LastName", dbText) 
     .Fields.Append .CreateField("Phone", dbText) 
     .Fields.Append .CreateField("Notes", dbMemo) 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "before appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     ' Append the new TableDef object to the Northwind 
     ' database. 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "after appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     ' Delete new TableDef object since this is a 
     ' demonstration. 
     dbsNorthwind.TableDefs.Delete "Contacts" 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="edcc2-p108">Este exemplo usa os métodos **CreateTableDef** e **FillCache** e as propriedades **CacheSize**, **CacheStart** e **SourceTableName** para enumerar os registros em uma tabela vinculada duas vezes. Em seguida, enumeram-se os registros duas vezes com um cache de 50 registros. O exemplo exibe então as estatísticas de desempenho das execuções sem cache e com cache por meio da tabela vinculada.</span><span class="sxs-lookup"><span data-stu-id="edcc2-p108">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset 
     Dim sngStart As Single 
     Dim sngEnd As Single 
     Dim sngNoCache As Single 
     Dim sngCache As Single 
     Dim intLoop As Integer 
     Dim strTemp As String 
     Dim intRecords As Integer 
     
     ' Open a database to which a linked table can be 
     ' appended. 
     Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
     ' Create a linked table that connects to a Microsoft SQL 
     ' Server database. 
     Set tdfRoyalties = _ 
     dbsCurrent.CreateTableDef("Royalties") 
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     tdfRoyalties.Connect = _ 
     "ODBC;DATABASE=pubs;DSN=Publishers" 
     tdfRoyalties.SourceTableName = "roysched" 
     dbsCurrent.TableDefs.Append tdfRoyalties 
     Set rstRemote = _ 
     dbsCurrent.OpenRecordset("Royalties") 
     
     With rstRemote 
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     sngStart = Timer 
     
     For intLoop = 1 To 2 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     .MoveNext 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngNoCache = sngEnd - sngStart 
     
     ' Cache the first 50 records. 
     .MoveFirst 
     .CacheSize = 50 
     .FillCache 
     sngStart = Timer 
     
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     For intLoop = 1 To 2 
     intRecords = 0 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     ' Count the records. If the end of the 
     ' cache is reached, reset the cache to the 
     ' next 50 records. 
     intRecords = intRecords + 1 
     .MoveNext 
     If intRecords Mod 50 = 0 Then 
     .CacheStart = .Bookmark 
     .FillCache 
     End If 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngCache = sngEnd - sngStart 
     
     ' Display performance results. 
     MsgBox "Caching Performance Results:" & vbCr & _ 
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
