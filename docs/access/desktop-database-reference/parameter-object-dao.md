---
title: Objeto Parameter (DAO)
TOCTitle: Parameter Object
ms:assetid: 194efd23-6086-13ac-beb9-c2aec101d6fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845640(v=office.15)
ms:contentKeyID: 48543495
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5df04b1ee06a2224db9e21f67e9c68a3ee5740bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288081"
---
# <a name="parameter-object-dao"></a>Objeto Parameter (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Um objeto **Parameter** representa um valor fornecido para uma consulta. O parâmetro está associado ao objeto **QueryDef** criado a partir de uma consulta parâmetro.

## <a name="remarks"></a>Comentários

Os objetos **Parameter** permitem alterar os argumentos em um objeto **QueryDef** executado frequentemente, sem ter que recompilar a consulta.

Utilizando as propriedades de um objeto **Parameter**, você pode definir uma consulta parâmetro que pode ser alterada antes da execução da consulta. Você pode:

  - Usar a propriedade **Name** para retornar o nome de um parâmetro.

  - Usar a propriedade **Value** para definir ou retornar os valores de parâmetro a serem utilizados na consulta.

  - Usar a propriedade **Type** para retornar o tipo de dados do objetos **Parameter**.

  - Usar a propriedade **Direction** para definir ou retornar se o parâmetro é de entrada, de saída ou ambos.

## <a name="example"></a>Exemplo

Este exemplo demonstra objetos **Parameter** e a coleção **Parameters** criando uma **QueryDef** temporária e recuperando dados com base em alterações feitas aos objetos **Parameters** do objeto **QueryDef**. O procedimento ParametersChange é exigido para a execução deste procedimento.

```vb
    Sub ParameterX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfReport As QueryDef 
     Dim prmBegin As Parameter 
     Dim prmEnd As Parameter 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create temporary QueryDef object with two 
     ' parameters. 
     Set qdfReport = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS dteBegin DateTime, dteEnd DateTime; " & _ 
     "SELECT EmployeeID, COUNT(OrderID) AS NumOrders " & _ 
     "FROM Orders WHERE ShippedDate BETWEEN " & _ 
     "[dteBegin] AND [dteEnd] GROUP BY EmployeeID " & _ 
     "ORDER BY EmployeeID") 
     Set prmBegin = qdfReport.Parameters!dteBegin 
     Set prmEnd = qdfReport.Parameters!dteEnd 
     
     ' Print report using specified parameter values. 
     ParametersChange qdfReport, prmBegin, #1/1/95#, _ 
     prmEnd, #6/30/95# 
     ParametersChange qdfReport, prmBegin, #7/1/95#, _ 
     prmEnd, #12/31/95# 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub ParametersChange(qdfTemp As QueryDef, _ 
     prmFirst As Parameter, dteFirst As Date, _ 
     prmLast As Parameter, dteLast As Date) 
     ' Report function for ParameterX. 
     
     Dim rstTemp As Recordset 
     Dim fldLoop As Field 
     
     ' Set parameter values and open recordset from 
     ' temporary QueryDef object. 
     prmFirst = dteFirst 
     prmLast = dteLast 
     Set rstTemp = _ 
     qdfTemp.OpenRecordset(dbOpenForwardOnly) 
     Debug.Print "Period " & dteFirst & " to " & dteLast 
     
     ' Enumerate recordset. 
     Do While Not rstTemp.EOF 
     
     ' Enumerate Fields collection of recordset. 
     For Each fldLoop In rstTemp.Fields 
     Debug.Print " - " & fldLoop.Name & " = " & fldLoop; 
     Next fldLoop 
     
     Debug.Print 
     rstTemp.MoveNext 
     Loop 
     
     rstTemp.Close 
     
    End Sub
```
