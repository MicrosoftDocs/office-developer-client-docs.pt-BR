---
title: Objeto Parameter (DAO)
TOCTitle: Parameter Object
ms:assetid: 194efd23-6086-13ac-beb9-c2aec101d6fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845640(v=office.15)
ms:contentKeyID: 48543495
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 69388834d5469c9fa66d70d397d63be4376db218
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465153"
---
# <a name="parameter-object-dao"></a><span data-ttu-id="63340-102">Objeto Parameter (DAO)</span><span class="sxs-lookup"><span data-stu-id="63340-102">Parameter Object (DAO)</span></span>


<span data-ttu-id="63340-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="63340-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="63340-p101">Um objeto **Parameter** representa um valor fornecido para uma consulta. O parâmetro está associado ao objeto **QueryDef** criado a partir de uma consulta parâmetro.</span><span class="sxs-lookup"><span data-stu-id="63340-p101">A **Parameter** object represents a value supplied to a query. The parameter is associated with a **QueryDef** object created from a parameter query.</span></span>

## <a name="remarks"></a><span data-ttu-id="63340-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="63340-106">Remarks</span></span>

<span data-ttu-id="63340-107">Os objetos **Parameter** permitem alterar os argumentos em um objeto **QueryDef** executado frequentemente, sem ter que recompilar a consulta.</span><span class="sxs-lookup"><span data-stu-id="63340-107">**Parameter** objects allow you to change the arguments in a frequently run **QueryDef** object without having to recompile the query.</span></span>

<span data-ttu-id="63340-p102">Utilizando as propriedades de um objeto **Parameter**, você pode definir uma consulta parâmetro que pode ser alterada antes da execução da consulta. Você pode:</span><span class="sxs-lookup"><span data-stu-id="63340-p102">Using the properties of a **Parameter** object, you can set a query parameter that can be changed before the query is run. You can:</span></span>

  - <span data-ttu-id="63340-110">Usar a propriedade **Name** para retornar o nome de um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="63340-110">Use the **Name** property to return the name of a parameter.</span></span>

  - <span data-ttu-id="63340-111">Usar a propriedade **Value** para definir ou retornar os valores de parâmetro a serem utilizados na consulta.</span><span class="sxs-lookup"><span data-stu-id="63340-111">Use the **Value** property to set or return the parameter values to be used in the query.</span></span>

  - <span data-ttu-id="63340-112">Usar a propriedade **Type** para retornar o tipo de dados do objetos **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="63340-112">Use the **Type** property to return the data type of the **Parameter** object.</span></span>

  - <span data-ttu-id="63340-113">Usar a propriedade **Direction** para definir ou retornar se o parâmetro é de entrada, de saída ou ambos.</span><span class="sxs-lookup"><span data-stu-id="63340-113">Use the **Direction** property to set or return whether the parameter is an input parameter, an output parameter, or both.</span></span>

## <a name="example"></a><span data-ttu-id="63340-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="63340-114">Example</span></span>

<span data-ttu-id="63340-p103">Este exemplo demonstra os objetos **Parameter** e a coleção **Parameters**, criando um **QueryDef** temporário e recuperando dados com base nas alterações feitas em **Parameters** do objeto **QueryDef**. O procedimento ParametersChange é exigido para que este procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="63340-p103">This example demonstrates **Parameter** objects and the **Parameters** collection by creating a temporary **QueryDef** and retrieving data based on changes made to the **QueryDef** object's **Parameters**. The ParametersChange procedure is required for this procedure to run.</span></span>

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
