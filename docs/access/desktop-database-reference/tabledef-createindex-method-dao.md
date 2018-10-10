---
title: Método TableDef.CreateIndex (DAO)
TOCTitle: CreateIndex Method
ms:assetid: 857b25c1-01fa-b926-0c74-7105e71b7505
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196791(v=office.15)
ms:contentKeyID: 48546062
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052970
f1_categories:
- Office.Version=v15
ms.openlocfilehash: eee732709c4c10c8e6399d34afafd1b27bf827c1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464048"
---
# <a name="tabledefcreateindex-method-dao"></a>Método TableDef.CreateIndex (DAO)


**Aplica-se a**: Access 2013 | Office 2013 

Cria um novo objeto **[Index](index-object-dao.md)** (apenas espaços de trabalho do Microsoft Access). .

## <a name="syntax"></a>Sintaxe

*expressão* . CreateIndex (***nome***)

*expressão* Uma variável que representa um objeto **TableDef** .

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
<td><p>Name</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Index</strong>. Consulte a propriedade <strong>Name</strong> para obter detalhes sobre nomes válidos de <strong>Index</strong>.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor retornado

Index

## <a name="remarks"></a>Comentários

Você pode usar o método **CreateIndex** para criar um novo objeto **Index** para um objeto **TableDef**. Se você omitir a parte do nome opcional quando você usa **CreateIndex**, você pode usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade **Name** , antes de você acrescentar o novo objeto a uma coleção. Depois de acrescentar o objeto, você pode ou não conseguir definir sua propriedade **Name**, dependendo do tipo de objeto que contém a coleção **Indexes**. Consulte o tópico da propriedade **Name** para obter mais detalhes.

Se name fizer referência a um objeto que já é um membro da coleção, ocorrerá um erro de tempo de execução quando você usa o método **[Append](fields-append-method-dao.md)** .

Para remover um objeto **Index** de uma coleção, use o método **[Delete](fields-delete-method-dao.md)** na coleção.

## <a name="example"></a>Exemplo

Este exemplo usa o método **CreateIndex** para criar dois novos objetos **Index** e, em seguida, acrescenta-os à coleção **Indexes** do objeto **TableDef** Employees. Em seguida, é enumerada a coleção Indexes do objeto **TableDef**, a coleção **Fields** dos novos objetos **Index** e a coleção Properties dos novos objetos **Index**. A função CreateIndexOutput é exigida para a execução deste procedimento.

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
