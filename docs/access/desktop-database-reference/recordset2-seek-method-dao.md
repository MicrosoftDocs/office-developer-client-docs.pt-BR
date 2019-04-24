---
title: Método Recordset2. Seek (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9510faab9035f2b2cbcccae0a8ddefa484a95cb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307186"
---
# <a name="recordset2seek-method-dao"></a>Método Recordset2. Seek (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Localiza o registro em um objeto **Recordset** do tipo tabela indexada que satisfaz os critérios especificados para o índice atual e torna esse registro o registro atual (somente espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . Seek (***comparação***, ***key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="parameters"></a>Parâmetros

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
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Comparison</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Uma das seguintes expressões de cadeia de caracteres: &lt;, &lt;=, =, &gt;= ou &gt;.</p></td>
</tr>
<tr class="even">
<td><p><em>Key1, Key2...Key13</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um ou mais valores correspondentes a campos no índice atual do objeto <strong>Recordset</strong>, como especificado pela configuração de sua propriedade <strong>Index</strong>. Você pode usar até 13 argumentos key.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você deve definir o índice atual com a propriedade **Index** antes de usar **Seek**. Se o índice identificar um campo de chave não exclusiva, **Seek** localiza o primeiro registro que satisfaz os critérios.

O método **Seek** pesquisa os campos de chave especificados e localiza o primeiro registro que satisfaz os critérios especificados por Comparison e key1. Depois de encontrado, ela torna atual aquele registro e define a propriedade **NoMatch** como **False**. Se o método **Seek** falhar ao localizar uma correspondência, a propriedade **NoMatch** será definida como **True**, e o registro atual será indefinido.

Se Comparison for igual a (=), maior ou igual a\>(=) ou maior que (\>), **Seek** começará no início do índice e pesquisará para frente.

Se Comparison for menor que (\<) ou menor que ou igual a\<(=), **Seek** começará no final do índice e pesquisará para trás. Entretanto, se houver entradas de índice duplicadas no final do índice, **Seek** começará em uma entrada arbitrária entre as duplicatas e pesquisará para trás.

Você deve especificar valores para todos os campos definidos no índice. Se você utilizar **Seek** com um índice de várias colunas e não especificar um valor de comparação para cada campo no índice, não será possível usar o operador igual (=) na comparação. Isso acontece porque alguns dos campos de critério (key2, key3 e assim por diante) terão como padrão Null, que provavelmente não terá correspondência. Portanto, o operador igual funcionará de modo correto somente se você tiver um registro que seja todo **null**, exceto a chave que você está procurando. É recomendável que você use o operador maior que ou igual\>a (=) em vez disso.

O argumento key1 deve ter o mesmo tipo de dados de campo que o campo correspondente no índice atual. Por exemplo, se o índice atual se referir a um campo número (como o código do funcionário), key1 deverá ser numérico. Da mesma forma, se o índice atual se referir a um campo de texto (como sobrenome), key1 deverá ser uma cadeia de caracteres.

Não deve haver um registro atual quando você utilizar **Seek**.

Você pode usar a coleção **[Indexes](indexes-collection-dao.md)** para enumerar os índices existentes.

Para localizar um registro em um **Recordset** do tipo dynaset ou instantâneo que atenda a uma condição específica não coberta por índices existentes, use os métodos **[Find](recordset2-findfirst-method-dao.md)**. Para incluir todos os registros, não apenas aqueles que atendem a uma condição específica, use os métodos **[Move](recordset-movefirst-method-dao.md)** para mover de um registro para outro.

Você não pode usar o método **Seek** em uma tabela vinculada porque não é possível abrir tabelas vinculadas como objetos **Recordset** do tipo tabela. Contudo, se você utilizar o método **[OpenDatabase](dbengine-opendatabase-method-dao.md)** para abrir diretamente um banco de dados (não-ODBC) ISAM instalável, poderá usar **Seek** nas tabelas naquele banco de dados.

## <a name="example"></a>Exemplo

Este exemplo demonstra o método **Seek** ao permitir que o usuário procure um produto com base em um número de ID.

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

Este exemplo usa a propriedade **NoMatch** para determinar se um **Seek** e um **FindFirst** foram bem-sucedidos e, em caso negativo, para fornecer os comentários apropriados. Os procedimentos SeekMatch e FindMatch são exigidos para que esse procedimento seja executado.

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
