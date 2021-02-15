---
title: Propriedade Recordset2.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: 77852966-11e9-1773-6e58-53927b84c03b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196071(v=office.15)
ms:contentKeyID: 48545728
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052890
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c23de433f26b5a54b3fee5cc69f67a07b53f8a3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309149"
---
# <a name="recordset2recordcount-property-dao"></a>Propriedade Recordset2.RecordCount (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Retorna o número de registros acessados em um objeto **[Recordset](recordset-object-dao.md)** ou o número total de registros em um objeto **Recordset** do tipo tabela ou do objeto **[TableDef](tabledef-object-dao.md)**. **Long** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* .RecordCount

*expressão* Uma variável que representa **um objeto Recordset2** .

## <a name="remarks"></a>Comentários

Use a propriedade **RecordCount** para descobrir quantos registros de um objeto **Recordset** ou **TableDef** foram acessados. A propriedade **RecordCount** não indica quantos registros foram contidos em um objeto **Recordset** do tipo dynaset, instantâneo ou somente encaminhamento até que todos os registros tenham sido acessados. Assim que o último registro tiver sido acessado, a propriedade **RecordCount** indicará o número total de registros não excluídos no objeto **Recordset** ou **TableDef**. Para forçar o acesso ao último registro, use o método **[MoveLast](recordset2-movelast-method-dao.md)** no objeto **Recordset**. Além disso, é possível usar a função **Count** SQL para determinar o número de registros aproximado que a consulta retornará.

> [!NOTE]
> O uso do método **MoveLast** para preencher um **Recordset** aberto recentemente causará impacto negativo no desempenho. A não ser que seja necessário ter um **RecordCount** preciso assim que você abrir um **Recordset**, é melhor aguardar até que o **Recordset** seja preenchido com outras partes do código antes de verificar a propriedade **RecordCount**.

À medida que o aplicativo excluir os registros de um objeto **Recordset** do tipo dynaset, diminuirá o valor da propriedade **RecordCount**. No entanto, os registros excluídos por outros usuários não serão refletidos pela propriedade **RecordCount** até que o registro atual seja posicionado em um registro excluído. Se você executar uma transação que afeta a definição da propriedade **RecordCount** e reduzir posteriormente o preço da transação, a propriedade **RecordCount** não refletirá o número real de registros restantes.

A propriedade **RecordCount** de um objeto **Recordset** do tipo instantâneo ou somente encaminhamento não é afetado por alterações nas tabelas subjacentes.

Um objeto **Recordset** ou **TableDef** sem registros tem a propriedade **RecordCount** configurada como 0.

O uso do método **[Requery](recordset2-requery-method-dao.md)** em um objeto **Recordset** redefine a propriedade **RecordCount** exatamente como se a consulta tivesse sido reexecutada.

## <a name="example"></a>Exemplo

Este exemplo demonstra a propriedade **RecordCount** com tipos diferentes de **Recordsets** antes e depois de preenchidos.

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```
