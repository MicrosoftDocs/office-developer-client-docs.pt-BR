---
title: Propriedade Field2.Required (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6b1950c8a864fbf23bee26be89e07e49357840b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292717"
---
# <a name="field2required-property-dao"></a>Propriedade Field2.Required (DAO)


**Aplica-se ao:** Access 2013, Office 2013


Define ou retorna um valor que indica se o objeto **Field2** requer ou não um valor não-Nulo .

## <a name="syntax"></a>Sintaxe

*expressão* . Obrigatório

*expressão* Uma variável que representa um objeto **Field2**.

## <a name="remarks"></a>Comentários

Para um objeto **Field2** ainda não acrescentado à coleção **Fields**, essa propriedade é de leitura/gravação.

A disponibilidade da propriedade **Required** depende do objeto que contém a coleção **[Fields](fields-collection-dao.md)**, conforme mostrado na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Se a coleção Fields pertencer a um</p></th>
<th><p>Então Required será</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>
						Objeto <strong>Index</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td><p>
						Objeto <strong>QueryDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p>
						Objeto <strong>Recordset</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p>
						Objeto <strong>Relation</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p>
						Objeto <strong>TableDef</strong></p></td>
<td><p>Leitura/gravação</p></td>
</tr>
</tbody>
</table>


Você pode usar a propriedade **Required** junto com as propriedades **AllowZeroLength**, **ValidateOnSet** ou **ValidationRule** para determinar a validade da configuração da propriedade **Value** para aquele objeto **Field2**. Se a propriedade **Required** for definida como **False**, o campo conterá valores **null** e valores que atendam às condições especificadas pelas configurações das propriedades **AllowZeroLength** e **ValidationRule**.


> [!NOTE]
> [!OBSERVAçãO] Quando for possível definir essa propriedade para um objeto **Index** ou para um objeto **Field2**, defina-a para o objeto **Field2**. A validade da configuração da propriedade para um objeto **Field2** é verificada antes da configuração para um objeto **Index**.



## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **Required** para relatar quais campos de três tabelas diferentes devem conter dados para que um novo registro possa ser adicionado. O procedimento RequiredOutput é necessário para que este procedimento seja executado.

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field2 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

