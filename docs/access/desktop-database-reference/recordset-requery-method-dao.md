---
title: Método Requery (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d5c98eeb94e49693cf13d358987307f61f15069c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998333"
---
# <a name="recordsetrequery-method-dao"></a>Método Requery (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Atualiza os dados em um objeto **[Recordset](recordset-object-dao.md)** executando novamente a consulta na qual o objeto se baseia.

## <a name="syntax"></a>Sintaxe

*expressão* . Requery (***novadefiniçãodaconsulta***)

*expressão* Uma variável que representa um objeto **Recordset** .

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
<td><p><em>Novadefiniçãodaconsulta</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Representa o valor da propriedade <strong>Name</strong> de um objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use esse método para verificar se um **Recordset** contém os dados mais recentes. Esse método preenche novamente o **Recordset** atual usando os parâmetros consulta atual ou (em um espaço de trabalho do Microsoft Access) os novos parâmetros fornecidos pelo argumento novadefiniçãodaconsulta.

Se você não especificar um argumento novadefiniçãodaconsulta, o **Recordset** será preenchido novamente com base na mesma definição de consulta e os parâmetros usados para preencher originalmente o **Recordset**. Qualquer alteração nos dados de base será refletida durante esse repreenchimento. Se você não usou **QueryDef** para criar o **Recordset**, o **Recordset** é recriado do zero.

Se você especificar um **QueryDef** original no argumento novadefiniçãodaconsulta, em seguida, o **Recordset** é consultado novamente usando os parâmetros especificados por **QueryDef**. Qualquer alteração nos dados de base será refletida durante esse repreenchimento. Para refletir as alterações para os valores de parâmetro de consulta no **Recordset**, você deve fornecer o argumento novadefiniçãodaconsulta.

Se você especificar um **QueryDef** diferente do originalmente utilizado para criar o **Recordset**, o **Recordset** será recriado do zero.

Quando você usa **Requery**, o primeiro registro no **Recordset** torna-se o registro atual.

Você não pode usar o método **Requery** nos objetos **Recordset** do tipo dynaset ou instantâneo cuja propriedade **[Restartable](recordset-restartable-property-dao.md)** está definida como **False**. No entanto, se você fornecer o argumento opcional novadefiniçãodaconsulta, a propriedade **Restartable** será ignorada.

Se as configurações das propriedades **[BOF](recordset-bof-property-dao.md)** e **[EOF](recordset-eof-property-dao.md)** do objeto **Recordset** forem **True** após a utilização do método **Requery**, a consulta não retornará nenhum registro, e o **Recordset** não conterá nenhum dado.

## <a name="example"></a>Exemplo

Este exemplo mostra como o método **Requery** pode ser utilizado para atualizar uma consulta após a alteração dos dados de base.

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset 
     Dim rstChange As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Este exemplo mostra como o método **Requery** pode ser utilizado para atualizar uma consulta após a alteração dos parâmetros de consulta.

```vb 
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```

