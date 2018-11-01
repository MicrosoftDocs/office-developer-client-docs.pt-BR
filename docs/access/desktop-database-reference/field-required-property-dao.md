---
title: Propriedade Field.Required (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 77214fcad0f5b2cafe794282782df4446d37fcf6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887156"
---
# <a name="fieldrequired-property-dao"></a>Propriedade Field.Required (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que indica se um objeto **[Field](field-object-dao.md)** requer um valor não Null.

## <a name="syntax"></a>Sintaxe

*expressão* . Necessário

*expressão* Uma variável que representa um objeto **Field** .

## <a name="remarks"></a>Comentários

Para um **Field** ainda não acrescentado à coleção **Fields**, essa propriedade é de leitura/gravação.

A disponibilidade da propriedade **Required** depende do objeto que contém a coleção [Fields](fields-collection-dao.md), como exibido na tabela a seguir.

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
<td><p>							Objeto <strong>Index</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td><p>Objeto <strong>QueryDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p>Objeto <strong>Recordset</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p>Objeto <strong>Relation</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p>Objeto <strong>TableDef</strong></p></td>
<td><p>Leitura/gravação</p></td>
</tr>
</tbody>
</table>


Use a propriedade **Required** junto com a propriedade **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** ou a propriedade **[ValidationRule](field-validationrule-property-dao.md)** para determinar a validade da definição da propriedade **[Value](field-value-property-dao.md)** desse objeto **Field**. Se a propriedade **Required** for definida como **False**, o campo pode conter os valores **null** assim como os valores que atendem as condições especificadas pelas definições das propriedades **AllowZeroLength** e **ValidationRule**.


> [!NOTE]
> <P>[!OBSERVAçãO] Quando definir essa propriedade para um objeto <STRONG>Index</STRONG> ou um objeto <STRONG>Field</STRONG>, defina-a para o objeto <STRONG>Field</STRONG>. A validade da definição da propriedade para um objeto <STRONG>Field</STRONG> é verificada antes da validade do objeto <STRONG>Index</STRONG>.</P>



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
 
 Dim fldLoop As Field 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

