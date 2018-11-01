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
# <a name="recordset2seek-method-dao"></a>Método Recordset2.Seek (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Localiza o registro em um objeto **Recordset** do tipo tabela indexada que satisfaz os critérios especificados para o índice atual e torna esse registro o registro atual (somente espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . Seek (***comparação***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)

*expressão* Uma variável que representa um objeto **Recordset2** .

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
<td><p>comparison</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Uma das seguintes expressões de cadeia de caracteres: &lt;, &lt;=, =, &gt;= ou &gt;.</p></td>
</tr>
<tr class="even">
<td><p>Key1, Key2...Key13</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um ou mais valores correspondentes a campos no índice atual do objeto <strong>Recordset</strong>, como especificado pela configuração de sua propriedade <strong>Index</strong>. Você pode usar até 13 argumentos principais.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você deve definir o índice atual com a propriedade **Index** antes de usar **Seek**. Se o índice identificar um campo de chave não exclusiva, **Seek** localiza o primeiro registro que satisfaz os critérios.

O método **Seek** pesquisa por meio de campos de chave especificados e localiza o primeiro registro que satisfaz os critérios especificados por comparação e key1. Uma vez encontrado, ele transformará o registro em atual e definirá a propriedade **NoMatch** como **False**. Se o método **Seek** falhar em localizar uma correspondência, a propriedade **NoMatch** será definida como **True** e o registro atual ficará indefinido.

Se a comparação é igual (=), maior ou igual (\>=), ou maior que (\>), **Seek** começará no início do índice e encaminham pesquisas.

Se a comparação é menor que (\<) ou menor ou igual (\<=), **Seek** começará no final do índice e procura para trás. No entanto, se houver entradas de índice duplicadas no final do índice, **Seek** começará em uma entrada arbitrária entre as duplicadas e então pesquisará de trás para frente.

Você deve especificar valores para todos os campos definidos no índice. Se você usar **Seek** com um índice de várias colunas e se não especificar um valor de comparação para todos os campos do índice, então não poderá usar o operador igual a (=) na comparação. Isso acontece porque alguns dos campos critérios (key2 key3 e assim por diante) serão definido como nulo, o que provavelmente não corresponderá. Dessa forma, o operador igual a só funcionará corretamente se você tiver um registro que seja todo **null**, exceto a chave que você esteja procurando. É recomendável que você use o maior ou igual (\>=) operador em vez disso.

O argumento key1 deve ser do mesmo tipo de dados de campo do campo correspondente no índice atual. Por exemplo, se o índice atual se refere a um campo numérico (por exemplo, Employee ID), key1 deve ser numérico. Da mesma forma, se o índice atual se refere a um campo de texto (por exemplo, o sobrenome), key1 deve ser uma cadeia de caracteres.

Não precisa ser um registro atual quando você usar **Seek**.

Você pode usar a coleção **[Indexes](indexes-collection-dao.md)** para enumerar os índices existentes.

Para localizar um registro em um **Recordset** do tipo dynaset ou instantâneo que satisfaça uma condição específica que não seja convertida por índices existentes, use os métodos **[Find](recordset2-findfirst-method-dao.md)**. Para incluir todos os registros, e não apenas aqueles que satisfaçam a uma condição específica, use os métodos **[Move](recordset-movefirst-method-dao.md)** para se mover de registro em registro.

Você não pode usar o método **Seek** em uma tabela vinculada porque não pode abrir tabelas vinculadas como objetos **Recordset** do tipo tabela. No entanto, se você usar o método **[OpenDatabase](dbengine-opendatabase-method-dao.md)** para abrir diretamente um banco de dados ISAM (não ODBC) não instalado, poderá usar **Seek** em tabelas naquele banco de dados.

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

Este exemplo usa a propriedade **NoMatch** para determinar se **Seek** e **FindFirst** foram bem-sucedidos e, se não foram, fornece os comentários adequados. Os procedimentos SeekMatch e FindMatch são necessários para executar esse procedimento.

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
