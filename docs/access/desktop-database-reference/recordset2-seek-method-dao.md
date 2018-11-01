---
title: Método Recordset2.Seek (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9a1c89bb060eb7d282db5ad5f64db9d887868486
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873653"
---
# <a name="recordset2seek-method-dao"></a><span data-ttu-id="7f621-102">Método Recordset2.Seek (DAO)</span><span class="sxs-lookup"><span data-stu-id="7f621-102">Recordset2.Seek Method (DAO)</span></span>


<span data-ttu-id="7f621-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f621-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f621-104">Localiza o registro em um objeto **Recordset** do tipo tabela indexada que satisfaz os critérios especificados para o índice atual e torna esse registro o registro atual (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="7f621-104">Locates the record in an indexed table-type **Recordset** object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f621-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f621-105">Syntax</span></span>

<span data-ttu-id="7f621-106">*expressão* . Seek (***comparação***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span><span class="sxs-lookup"><span data-stu-id="7f621-106">*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span></span>

<span data-ttu-id="7f621-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="7f621-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="7f621-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f621-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f621-109">Nome</span><span class="sxs-lookup"><span data-stu-id="7f621-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7f621-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="7f621-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="7f621-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7f621-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="7f621-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f621-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f621-113">comparison</span><span class="sxs-lookup"><span data-stu-id="7f621-113">Comparison</span></span></p></td>
<td><p><span data-ttu-id="7f621-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7f621-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7f621-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7f621-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7f621-116">Uma das seguintes expressões de cadeia de caracteres: &lt;, &lt;=, =, &gt;= ou &gt;.</span><span class="sxs-lookup"><span data-stu-id="7f621-116">One of the following string expressions: &lt;, &lt;=, =, &gt;=, or &gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f621-117">Key1, Key2...Key13</span><span class="sxs-lookup"><span data-stu-id="7f621-117">Key1, Key2...Key13</span></span></p></td>
<td><p><span data-ttu-id="7f621-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7f621-118">Required</span></span></p></td>
<td><p><span data-ttu-id="7f621-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7f621-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7f621-120">Um ou mais valores correspondentes a campos no índice atual do objeto <strong>Recordset</strong>, como especificado pela configuração de sua propriedade <strong>Index</strong>.</span><span class="sxs-lookup"><span data-stu-id="7f621-120">One or more values corresponding to fields in the <strong>Recordset</strong> object's current index, as specified by its <strong>Index</strong> property setting.</span></span> <span data-ttu-id="7f621-121">Você pode usar até 13 argumentos principais.</span><span class="sxs-lookup"><span data-stu-id="7f621-121">You can use up to 13 key arguments.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7f621-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f621-122">Remarks</span></span>

<span data-ttu-id="7f621-p102">Você deve definir o índice atual com a propriedade **Index** antes de usar **Seek**. Se o índice identificar um campo de chave não exclusiva, **Seek** localiza o primeiro registro que satisfaz os critérios.</span><span class="sxs-lookup"><span data-stu-id="7f621-p102">You must set the current index with the **Index** property before you use **Seek**. If the index identifies a nonunique key field, **Seek** locates the first record that satisfies the criteria.</span></span>

<span data-ttu-id="7f621-125">O método **Seek** pesquisa por meio de campos de chave especificados e localiza o primeiro registro que satisfaz os critérios especificados por comparação e key1.</span><span class="sxs-lookup"><span data-stu-id="7f621-125">The **Seek** method searches through the specified key fields and locates the first record that satisfies the criteria specified by comparison and key1.</span></span> <span data-ttu-id="7f621-126">Uma vez encontrado, ele transformará o registro em atual e definirá a propriedade **NoMatch** como **False**.</span><span class="sxs-lookup"><span data-stu-id="7f621-126">Once found, it makes that record current and sets the **NoMatch** property to **False**.</span></span> <span data-ttu-id="7f621-127">Se o método **Seek** falhar em localizar uma correspondência, a propriedade **NoMatch** será definida como **True** e o registro atual ficará indefinido.</span><span class="sxs-lookup"><span data-stu-id="7f621-127">If the **Seek** method fails to locate a match, the **NoMatch** property is set to **True**, and the current record is undefined.</span></span>

<span data-ttu-id="7f621-128">Se a comparação é igual (=), maior ou igual (\>=), ou maior que (\>), **Seek** começará no início do índice e encaminham pesquisas.</span><span class="sxs-lookup"><span data-stu-id="7f621-128">If comparison is equal (=), greater than or equal (\>=), or greater than (\>), **Seek** starts at the beginning of the index and searches forward.</span></span>

<span data-ttu-id="7f621-129">Se a comparação é menor que (\<) ou menor ou igual (\<=), **Seek** começará no final do índice e procura para trás.</span><span class="sxs-lookup"><span data-stu-id="7f621-129">If comparison is less than (\<) or less than or equal (\<=), **Seek** starts at the end of the index and searches backward.</span></span> <span data-ttu-id="7f621-130">No entanto, se houver entradas de índice duplicadas no final do índice, **Seek** começará em uma entrada arbitrária entre as duplicadas e então pesquisará de trás para frente.</span><span class="sxs-lookup"><span data-stu-id="7f621-130">However, if there are duplicate index entries at the end of the index, **Seek** starts at an arbitrary entry among the duplicates and then searches backward.</span></span>

<span data-ttu-id="7f621-131">Você deve especificar valores para todos os campos definidos no índice.</span><span class="sxs-lookup"><span data-stu-id="7f621-131">You must specify values for all fields defined in the index.</span></span> <span data-ttu-id="7f621-132">Se você usar **Seek** com um índice de várias colunas e se não especificar um valor de comparação para todos os campos do índice, então não poderá usar o operador igual a (=) na comparação.</span><span class="sxs-lookup"><span data-stu-id="7f621-132">If you use **Seek** with a multiple-column index, and you don't specify a comparison value for every field in the index, then you cannot use the equal (=) operator in the comparison.</span></span> <span data-ttu-id="7f621-133">Isso acontece porque alguns dos campos critérios (key2 key3 e assim por diante) serão definido como nulo, o que provavelmente não corresponderá.</span><span class="sxs-lookup"><span data-stu-id="7f621-133">That's because some of the criteria fields (key2, key3, and so on) will default to Null, which will probably not match.</span></span> <span data-ttu-id="7f621-134">Dessa forma, o operador igual a só funcionará corretamente se você tiver um registro que seja todo **null**, exceto a chave que você esteja procurando.</span><span class="sxs-lookup"><span data-stu-id="7f621-134">Therefore, the equal operator will work correctly only if you have a record which is all **null** except the key you're looking for.</span></span> <span data-ttu-id="7f621-135">É recomendável que você use o maior ou igual (\>=) operador em vez disso.</span><span class="sxs-lookup"><span data-stu-id="7f621-135">It's recommended that you use the greater than or equal (\>=) operator instead.</span></span>

<span data-ttu-id="7f621-136">O argumento key1 deve ser do mesmo tipo de dados de campo do campo correspondente no índice atual.</span><span class="sxs-lookup"><span data-stu-id="7f621-136">The key1 argument must be of the same field data type as the corresponding field in the current index.</span></span> <span data-ttu-id="7f621-137">Por exemplo, se o índice atual se refere a um campo numérico (por exemplo, Employee ID), key1 deve ser numérico.</span><span class="sxs-lookup"><span data-stu-id="7f621-137">For example, if the current index refers to a number field (such as Employee ID), key1 must be numeric.</span></span> <span data-ttu-id="7f621-138">Da mesma forma, se o índice atual se refere a um campo de texto (por exemplo, o sobrenome), key1 deve ser uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7f621-138">Similarly, if the current index refers to a Text field (such as Last Name), key1 must be a string.</span></span>

<span data-ttu-id="7f621-139">Não precisa ser um registro atual quando você usar **Seek**.</span><span class="sxs-lookup"><span data-stu-id="7f621-139">There doesn't have to be a current record when you use **Seek**.</span></span>

<span data-ttu-id="7f621-140">Você pode usar a coleção **[Indexes](indexes-collection-dao.md)** para enumerar os índices existentes.</span><span class="sxs-lookup"><span data-stu-id="7f621-140">You can use the **[Indexes](indexes-collection-dao.md)** collection to enumerate the existing indexes.</span></span>

<span data-ttu-id="7f621-p107">Para localizar um registro em um **Recordset** do tipo dynaset ou instantâneo que satisfaça uma condição específica que não seja convertida por índices existentes, use os métodos **[Find](recordset2-findfirst-method-dao.md)**. Para incluir todos os registros, e não apenas aqueles que satisfaçam a uma condição específica, use os métodos **[Move](recordset-movefirst-method-dao.md)** para se mover de registro em registro.</span><span class="sxs-lookup"><span data-stu-id="7f621-p107">To locate a record in a dynaset- or snapshot-type **Recordset** that satisfies a specific condition that is not covered by existing indexes, use the **[Find](recordset2-findfirst-method-dao.md)** methods. To include all records, not just those that satisfy a specific condition, use the **[Move](recordset-movefirst-method-dao.md)** methods to move from record to record.</span></span>

<span data-ttu-id="7f621-p108">Você não pode usar o método **Seek** em uma tabela vinculada porque não pode abrir tabelas vinculadas como objetos **Recordset** do tipo tabela. No entanto, se você usar o método **[OpenDatabase](dbengine-opendatabase-method-dao.md)** para abrir diretamente um banco de dados ISAM (não ODBC) não instalado, poderá usar **Seek** em tabelas naquele banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7f621-p108">You can't use the **Seek** method on a linked table because you can't open linked tables as table-type **Recordset** objects. However, if you use the **[OpenDatabase](dbengine-opendatabase-method-dao.md)** method to directly open an installable ISAM (non-ODBC) database, you can use **Seek** on tables in that database.</span></span>

## <a name="example"></a><span data-ttu-id="7f621-145">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7f621-145">Example</span></span>

<span data-ttu-id="7f621-146">Este exemplo demonstra o método **Seek** ao permitir que o usuário procure um produto com base em um número de ID.</span><span class="sxs-lookup"><span data-stu-id="7f621-146">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
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

<span data-ttu-id="7f621-p109">Este exemplo usa a propriedade **NoMatch** para determinar se **Seek** e **FindFirst** foram bem-sucedidos e, se não foram, fornece os comentários adequados. Os procedimentos SeekMatch e FindMatch são necessários para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="7f621-p109">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
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
