---
title: Método Recordset.Seek (DAO)
TOCTitle: Seek Method
ms:assetid: ef83d909-c962-b016-7d33-36eacdc25c2c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836416(v=office.15)
ms:contentKeyID: 48548585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053061
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: db2c90d42feacee58af9eea30a2d99439cb4ddaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307599"
---
# <a name="recordsetseek-method-dao"></a><span data-ttu-id="4ed4e-102">Método Recordset.Seek (DAO)</span><span class="sxs-lookup"><span data-stu-id="4ed4e-102">Recordset.Seek Method (DAO)</span></span>

<span data-ttu-id="4ed4e-103">**Aplica-se a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ed4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ed4e-104">Localiza o registro em um objeto **Recordset** do tipo tabela indexada que satisfaz os critérios especificados para o índice atual e torna esse registro o registro atual (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4ed4e-104">Locates the record in an indexed table-type **Recordset** object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ed4e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ed4e-105">Syntax</span></span>

<span data-ttu-id="4ed4e-106">*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span><span class="sxs-lookup"><span data-stu-id="4ed4e-106">Seek(\*\*\*\*Comparison\*\*\*\*, \*\*\*\*\*\*Key1\*\*\*\*\*\*, \*\*\*\*\*\*Key2\*\*\*\*\*\*, \*\*\*\*\*\*Key3\*\*\*\*\*\*, \*\*\*\*\*\*Key4\*\*\*\*\*\*, \*\*\*\*\*\*Key5\*\*\*\*\*\*, \*\*\*\*\*\*Key6\*\*\*\*\*\*, ***Key7, Key8, Key9, Key10, Key11, Key12, Key13***)</span></span>

<span data-ttu-id="4ed4e-107">*expression* Uma variável que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ed4e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ed4e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ed4e-109">Nome</span><span class="sxs-lookup"><span data-stu-id="4ed4e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4ed4e-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="4ed4e-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="4ed4e-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4ed4e-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="4ed4e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ed4e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ed4e-113"><em>Comparação</em></span><span class="sxs-lookup"><span data-stu-id="4ed4e-113"><em>Comparison</em></span></span></p></td>
<td><p><span data-ttu-id="4ed4e-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4ed4e-114">Required</span></span></p></td>
<td><p><span data-ttu-id="4ed4e-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="4ed4e-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="4ed4e-116">Uma das seguintes expressões de cadeia de caracteres: &lt;, &lt;=, =, &gt;= ou &gt;.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-116">One of the following string expressions: &lt;, &lt;=, =, &gt;=, or &gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ed4e-117"><em>Key1, Key2...Key13</em></span><span class="sxs-lookup"><span data-stu-id="4ed4e-117"><em>Key1, Key2...Key13</em></span></span></p></td>
<td><p><span data-ttu-id="4ed4e-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4ed4e-118">Required</span></span></p></td>
<td><p><span data-ttu-id="4ed4e-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4ed4e-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4ed4e-120">Um ou mais valores correspondentes a campos no índice atual do objeto <strong>Recordset</strong>, como especificado pela configuração de sua propriedade <strong>Index</strong>.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-120">One or more values corresponding to fields in the <strong>Recordset</strong> object's current index, as specified by its <strong>Index</strong> property setting.</span></span> <span data-ttu-id="4ed4e-121">Você pode usar até 13 argumentos de chave.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-121">You can use up to 13 key arguments.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4ed4e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ed4e-122">Remarks</span></span>

<span data-ttu-id="4ed4e-p102">Você deve definir o índice atual com a propriedade **Index** antes de usar **Seek**. Se o índice identificar um campo de chave não exclusiva, **Seek** localiza o primeiro registro que satisfaz os critérios.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-p102">You must set the current index with the **Index** property before you use **Seek**. If the index identifies a nonunique key field, **Seek** locates the first record that satisfies the criteria.</span></span>

<span data-ttu-id="4ed4e-125">O método **Seek** faz buscas nos campos de chave especificados e localiza o primeiro registro que atenda ao critério especificado por comparison e key1.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-125">The Seek method searches through the specified key fields and locates the first record that satisfies the criteria specified by  comparison and  key1.</span></span> <span data-ttu-id="4ed4e-126">Depois de encontrado, ela torna atual aquele registro e define a propriedade **NoMatch** como **False**.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-126">Once found, it makes that record current and sets the **NoMatch** property to **False**.</span></span> <span data-ttu-id="4ed4e-127">Se o método **Seek** falhar ao localizar uma correspondência, a propriedade **NoMatch** será definida como **True**, e o registro atual será indefinido.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-127">If the **Seek** method fails to locate a match, the **NoMatch** property is set to **True**, and the current record is undefined.</span></span>

<span data-ttu-id="4ed4e-128">Se comparison for igual a (=), maior ou igual a (\>=) ou maior que (\>), **Seek** começará no início do índice e pesquisará adiante.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-128">If  comparison is equal (=), greater than or equal (>=), or greater than (>), Seek starts at the beginning of the index and searches forward.</span></span>

<span data-ttu-id="4ed4e-129">Se comparison for menor que (\<) ou menor ou igual a (\<=), **Seek** começará no final do índice e pesquisará para trás.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-129">If comparison is less than (<) or less than or equal (<=), Seek starts at the end of the index and searches backward.</span></span> <span data-ttu-id="4ed4e-130">Entretanto, se houver entradas de índice duplicadas no final do índice, **Seek** começará em uma entrada arbitrária entre as duplicatas e pesquisará para trás.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-130">However, if there are duplicate index entries at the end of the index, **Seek** starts at an arbitrary entry among the duplicates and then searches backward.</span></span>

<span data-ttu-id="4ed4e-131">Você deve especificar valores para todos os campos definidos no índice.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-131">You must specify values for all fields defined in the index.</span></span> <span data-ttu-id="4ed4e-132">Se você utilizar **Seek** com um índice de várias colunas e não especificar um valor de comparação para cada campo no índice, não será possível usar o operador igual (=) na comparação.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-132">If you use **Seek** with a multiple-column index, and you don't specify a comparison value for every field in the index, then you cannot use the equal (=) operator in the comparison.</span></span> <span data-ttu-id="4ed4e-133">Isso ocorre porque alguns dos campos de critérios (key2, key3 e assim por diante) serão padronizados como Null, o que provavelmente não terá uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-133">That's because some of the criteria fields (key2, key3, and so on) will default to Null, which will probably not match.</span></span> <span data-ttu-id="4ed4e-134">Portanto, o operador igual só funcionará corretamente se você tiver um registro que seja todo **null**, exceto a chave que você estiver procurando.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-134">Therefore, the equal operator will work correctly only if you have a record which is all **null** except the key you're looking for.</span></span> <span data-ttu-id="4ed4e-135">Recomenda-se utilizar o operador maior ou igual a (\>=) no lugar dele.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-135">It's recommended that you use the greater than or equal (>=) operator instead.</span></span>

<span data-ttu-id="4ed4e-136">O argumento key1 deve ter o mesmo tipo de dados de campo que o campo correspondente no índice atual.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-136">The  key1 argument must be of the same field data type as the corresponding field in the current index.</span></span> <span data-ttu-id="4ed4e-137">Por exemplo, se o índice atual se referir a um campo de número (como ID de Funcionário), key1 deverá ser numérico.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-137">For example, if the current index refers to a number field (such as Employee ID),  key1 must be numeric.</span></span> <span data-ttu-id="4ed4e-138">De forma semelhante, se o índice atual se referir a um campo de texto (como Sobrenome), key1 deverá ser uma sequência.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-138">Similarly, if the current index refers to a Text field (such as Last Name),  key1 must be a string.</span></span>

<span data-ttu-id="4ed4e-139">Não precisa ser um registro atual quando você usar **Seek**.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-139">There doesn't have to be a current record when you use **Seek**.</span></span>

<span data-ttu-id="4ed4e-140">Você pode usar a coleção **[Indexes](indexes-collection-dao.md)** para enumerar os índices existentes.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-140">You can use the **[Indexes](indexes-collection-dao.md)** collection to enumerate the existing indexes.</span></span>

<span data-ttu-id="4ed4e-p107">Para localizar um registro em um **Recordset** do tipo dynaset ou instantâneo que satisfaça uma condição específica que não seja convertida por índices existentes, use os métodos **[Find](recordset-findfirst-method-dao.md)**. Para incluir todos os registros, e não apenas aqueles que satisfaçam a uma condição específica, use os métodos **[Move](recordset-movefirst-method-dao.md)** para se mover de registro em registro.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-p107">To locate a record in a dynaset- or snapshot-type **Recordset** that satisfies a specific condition that is not covered by existing indexes, use the **[Find](recordset-findfirst-method-dao.md)** methods. To include all records, not just those that satisfy a specific condition, use the **[Move](recordset-movefirst-method-dao.md)** methods to move from record to record.</span></span>

<span data-ttu-id="4ed4e-p108">Você não pode usar o método **Seek** em uma tabela vinculada porque não pode abrir tabelas vinculadas como objetos **Recordset** do tipo tabela. No entanto, se você usar o método **[OpenDatabase](dbengine-opendatabase-method-dao.md)** para abrir diretamente um banco de dados ISAM (não ODBC) não instalado, poderá usar **Seek** em tabelas naquele banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-p108">You can't use the **Seek** method on a linked table because you can't open linked tables as table-type **Recordset** objects. However, if you use the **[OpenDatabase](dbengine-opendatabase-method-dao.md)** method to directly open an installable ISAM (non-ODBC) database, you can use **Seek** on tables in that database.</span></span>

## <a name="example"></a><span data-ttu-id="4ed4e-145">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4ed4e-145">Example</span></span>

<span data-ttu-id="4ed4e-146">Este exemplo demonstra o método **Seek** ao permitir que o usuário procure um produto com base em um número de ID.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-146">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="4ed4e-p109">Este exemplo usa a propriedade **NoMatch** para determinar se um **Seek** e um **FindFirst** foram bem-sucedidos e, em caso negativo, para fornecer os comentários apropriados. Os procedimentos SeekMatch e FindMatch são exigidos para que esse procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-p109">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim rstCustomers As Recordset 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim strCountry As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Default is dbOpenTable; required if Index property will  
       ' be used. 
       Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
       With rstProducts 
          .Index = "PrimaryKey" 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with Seek method" & vbCr & _ 
                "Product ID: " & !ProductID & vbCr & _ 
                "Product Name: " & !ProductName & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter a product ID." 
             strSeek = InputBox(strMessage) 
             If strSeek = "" Then Exit Do 
     
             ' Call procedure that seeks for a record based on  
             ' the ID number supplied by the user. 
             SeekMatch rstProducts, Val(strSeek) 
          Loop 
     
          .Close 
       End With 
     
       Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
          "SELECT CompanyName, Country FROM Customers " & _ 
          "ORDER BY CompanyName", dbOpenSnapshot) 
     
       With rstCustomers 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with FindFirst method" & _ 
                vbCr & "Customer Name: " & !CompanyName & _ 
                vbCr & "Country: " & !Country & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter country on which to search." 
             strCountry = Trim(InputBox(strMessage)) 
             If strCountry = "" Then Exit Do 
     
             ' Call procedure that finds a record based on  
             ' the country name supplied by the user. 
             FindMatch rstCustomers, _ 
                "Country = '" & strCountry & "'" 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
       intSeek As Integer) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .Seek "=", intSeek 
     
          ' If Seek method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
       strFind As String) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .FindFirst strFind 
     
          ' If Find method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="4ed4e-149">O exemplo a seguir mostra como usar o método Seek para localizar um registro em uma tabela vinculada.</span><span class="sxs-lookup"><span data-stu-id="4ed4e-149">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="4ed4e-150">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4ed4e-150">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
