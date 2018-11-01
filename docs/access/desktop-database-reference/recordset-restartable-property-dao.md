---
title: Propriedade Recordset.Restartable (DAO)
TOCTitle: Restartable Property
ms:assetid: 00def49d-ea7e-6cd5-2f4a-914a1ddcdd51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844737(v=office.15)
ms:contentKeyID: 48542919
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052926
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 782008e1fcad427a8d47a143dab0a54bc3b9e041
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874640"
---
# <a name="recordsetrestartable-property-dao"></a>Propriedade Recordset.Restartable (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna um valor que indica se um objeto **[Recordset](recordset-object-dao.md)** oferece suporte ao método **[Requery](recordset-requery-method-dao.md)**, que reexecuta a consulta na qual está baseado o objeto **Recordset**.

## <a name="syntax"></a>Sintaxe

*expressão* . Restartable

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Os objetos **Recordset** do tipo tabela sempre retornam **False**.

Verifique a propriedade **Restartable** antes de usar o método **Requery** em um objeto **Recordset**. Se a propriedade **Restartable** do objeto estiver definida como **False**, use o método **[OpenRecordset](connection-openrecordset-method-dao.md)** no objeto **[QueryDef](querydef-object-dao.md)** base para reexecutar a consulta.

## <a name="example"></a>Exemplo

Este exemplo demonstra a propriedade **Restartable** com objetos **Recordset** diferentes.

```vb
    Sub RestartableX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTemp As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open a table-type Recordset and print its 
     ' Restartable property. 
     Set rstTemp = .OpenRecordset("Employees", dbOpenTable) 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from an SQL statement and print its 
     ' Restartable property. 
     Set rstTemp = _ 
     .OpenRecordset("SELECT * FROM Employees") 
     Debug.Print "Recordset based on SQL statement" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from a saved QueryDef object and 
     ' print its Restartable property. 
     Set rstTemp = .OpenRecordset("Current Product List") 
     Debug.Print _ 
     "Recordset based on permanent QueryDef (" & _ 
     rstTemp.Name & ")" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     .Close 
     End With 
     
    End Sub
```
