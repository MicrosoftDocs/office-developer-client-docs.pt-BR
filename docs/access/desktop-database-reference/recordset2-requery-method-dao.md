---
title: Método Recordset2.Requery (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44f573d179c26677fc801dac82e0deecc3874fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307207"
---
# <a name="recordset2requery-method-dao"></a>Método Recordset2.Requery (DAO)

**Aplica-se a:** Access 2013, Office 2013

Atualiza os dados no objeto **[Recordset](recordset-object-dao.md)** reexecutando a consulta na qual o objeto é baseado.

## <a name="syntax"></a>Sintaxe

*expression* .Requery(***NewQueryDef***)

*expressão* Uma variável que representa **um objeto Recordset2** .

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
<th><p>Necessária/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>NewQueryDef</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Representa o valor da propriedade <strong>Name</strong> de um objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use este método para garantir que um **Recordset** contenha os dados mais recentes. Esse método preenche novamente o **Recordset** atual utilizando parâmetros de consulta atuais ou (em um espaço de trabalho do Microsoft Access) os novos parâmetros fornecidos pelo argumento newquerydef.

Se você não especificar um argumento newquerydef, o **Recordset** será preenchido novamente com base na mesma definição de consulta e nos parâmetros utilizados para preencher originalmente o **Recordset**. Qualquer alteração nos dados de base será refletida durante esse repreenchimento. Se você não usou **QueryDef** para criar o **Recordset**, o **Recordset** é recriado do zero.

Se você especificar o **QueryDef** original no argumento newquerydef, o **Recordset** é consultado novamente utilizando os parâmetros especificados pelo **QueryDef**. As alterações feitas nos dados subjacentes serão refletidas durante esse novo preenchimento. Para refletir qualquer alteração nos valores de parâmetro da consulta no **Recordset**, forneça o argumento newquerydef.

Se você especificar um **QueryDef** diferente do originalmente utilizado para criar o **Recordset**, o **Recordset** será recriado do zero.

Quando você usa **Requery**, o primeiro registro no **Recordset** torna-se o registro atual.

Você não pode usar o método **Requery** nos objetos **Recordset** do tipo dynaset ou instantâneo cuja propriedade **[Restartable](recordset2-restartable-property-dao.md)** está definida como **False**. Entretanto, se você fornecer o argumento newquerydef opcional, a propriedade **Restartable** será ignorada.

Se as configurações das propriedades **[BOF](recordset2-bof-property-dao.md)** e **[EOF](recordset2-eof-property-dao.md)** do objeto **Recordset** forem **True** após a utilização do método **Requery**, a consulta não retornará nenhum registro, e o **Recordset** não conterá nenhum dado.

## <a name="example"></a>Exemplo

Este exemplo mostra como o método **Requery** pode ser usado para atualizar uma consulta após dados subjacentes serem alterados.

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
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
 Dim rstView As Recordset2 
 
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

