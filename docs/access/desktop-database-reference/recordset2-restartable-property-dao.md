---
title: Propriedade Recordset2. restartable (DAO)
TOCTitle: Restartable Property
ms:assetid: 9b1c40f8-5a33-2527-a7b6-bef4cb991d7e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198019(v=office.15)
ms:contentKeyID: 48546560
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 873911ff8475a0b37f3f67d9cb2c01afc577487d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309055"
---
# <a name="recordset2restartable-property-dao"></a>Propriedade Recordset2. restartable (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Retorna um valor que indica se um objeto **[Recordset](recordset-object-dao.md)** oferece suporte ao método **[Requery](recordset2-requery-method-dao.md)**, que reexecuta a consulta na qual está baseado o objeto **Recordset**.

## <a name="syntax"></a>Sintaxe

*expressão* . Restartable

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Os objetos **Recordset** do tipo tabela sempre retornam **False**.

Verifique a propriedade **Restartable** antes de usar o método **Requery** em um objeto **Recordset**. Se a propriedade **Restartable** do objeto estiver definida como **False**, use o método **[OpenRecordset](connection-openrecordset-method-dao.md)** no objeto **[QueryDef](querydef-object-dao.md)** base para reexecutar a consulta.

## <a name="example"></a>Exemplo

Este exemplo demonstra a propriedade **Restartable** com objetos **Recordset** diferentes.

```vb
    Sub RestartableX()
    
       Dim dbsNorthwind As Database
       Dim rstTemp As Recordset2
    
       Set dbsNorthwind = OpenDatabase("Northwind.mdb")
    
       With dbsNorthwind
          ' Open a table-type Recordset and print its 
          ' Restartable property.
          Set rstTemp = .OpenRecordset("Employees", dbOpenTable)
          Debug.Print _
             "Table-type recordset from Employees table"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          ' Open a Recordset from an SQL statement and print its 
          ' Restartable property.
          Set rstTemp = _
             .OpenRecordset("SELECT * FROM Employees")
          Debug.Print "Recordset based on SQL statement"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          ' Open a Recordset from a saved QueryDef object and 
          ' print its Restartable property.
          Set rstTemp = .OpenRecordset("Current Product List")
          Debug.Print _
             "Recordset based on permanent QueryDef (" & _
             rstTemp.Name & ")"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          .Close
       End With
    
    End Sub
```
