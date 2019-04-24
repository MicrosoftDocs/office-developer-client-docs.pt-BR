---
title: Propriedade Recordset. restartable (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 5142d0d47be37ca8c2e1c6b89462c05b7d41d302
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307571"
---
# <a name="recordsetrestartable-property-dao"></a>Propriedade Recordset. restartable (DAO)


**Aplica-se ao:** Access 2013, Office 2013

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
