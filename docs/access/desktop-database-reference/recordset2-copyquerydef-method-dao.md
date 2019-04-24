---
title: Método Recordset2. CopyQueryDef (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: 36689ac0-f8a6-1f3e-4170-799141373777
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192474(v=office.15)
ms:contentKeyID: 48544170
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053073
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 8a643dae0b67cf4f2a2a0148619d9a8f4df7e6f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307361"
---
# <a name="recordset2copyquerydef-method-dao"></a><span data-ttu-id="6ced0-102">Método Recordset2. CopyQueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="6ced0-102">Recordset2.CopyQueryDef method (DAO)</span></span>


<span data-ttu-id="6ced0-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ced0-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="6ced0-104">Retorna um objeto **[QueryDef](querydef-object-dao.md)** que é uma cópia do **QueryDef** usado para criar o objeto **[Recordset](recordset-object-dao.md)** representado pelo espaço reservado Recordset (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6ced0-104">Returns a **[QueryDef](querydef-object-dao.md)** object that is a copy of the **QueryDef** used to create the **[Recordset](recordset-object-dao.md)** object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6ced0-105">.</span><span class="sxs-lookup"><span data-stu-id="6ced0-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="6ced0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ced0-106">Syntax</span></span>

<span data-ttu-id="6ced0-107">*expressão* . CopyQueryDef</span><span class="sxs-lookup"><span data-stu-id="6ced0-107">*expression* .CopyQueryDef</span></span>

<span data-ttu-id="6ced0-108">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="6ced0-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ced0-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6ced0-109">Return value</span></span>

<span data-ttu-id="6ced0-110">QueryDef</span><span class="sxs-lookup"><span data-stu-id="6ced0-110">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="6ced0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ced0-111">Remarks</span></span>

<span data-ttu-id="6ced0-112">Você pode usar o método **CopyQueryDef** para criar um novo **QueryDef** que é uma duplicata do **QueryDef** utilizado para criar o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6ced0-112">You can use the **CopyQueryDef** method to create a new **QueryDef** that is a duplicate of the **QueryDef** used to create the **Recordset**.</span></span>

<span data-ttu-id="6ced0-p102">Ocorre um erro se um **QueryDef** não foi usado para criar esse **Recordset**. Você deve primeiro abrir um **Recordset** com o método **OpenRecordset** antes de usar o método **CopyQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="6ced0-p102">If a **QueryDef** wasn't used to create this **Recordset**, an error occurs. You must first open a **Recordset** with the **OpenRecordset** method before using the **CopyQueryDef** method.</span></span>

<span data-ttu-id="6ced0-115">Esse método é útil quando você cria um objeto **Recordset** de um **QueryDef** e transmite o **Recordset** para uma função, e a função deve recriar o equivalente SQL da consulta, por exemplo, para modificá-la de alguma forma.</span><span class="sxs-lookup"><span data-stu-id="6ced0-115">This method is useful when you create a **Recordset** object from a **QueryDef**, and pass the **Recordset** to a function, and the function must re-create the SQL equivalent of the query, for example, to modify it in some way.</span></span>

## <a name="example"></a><span data-ttu-id="6ced0-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6ced0-116">Example</span></span>

<span data-ttu-id="6ced0-p103">Este exemplo usa o método **CopyQueryDef** para criar uma cópia de um **QueryDef** a partir de um **Recordset** existente e modifica a cópia adicionando uma cláusula à propriedade SQL. Quando você cria um **QueryDef** permanente, espaços, ponto-e-vírgulas ou preenchimentos de linha podem ser adicionados à propriedade SQL; esses caracteres extra devem ser removidos antes de uma nova cláusula ser acrescentada à instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="6ced0-p103">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the SQL property. When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the SQL property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
     strAdd As String) As QueryDef 
     
     Dim strSQL As String 
     Dim strRightSQL As String 
     
     Set CopyQueryNew = rstTemp.CopyQueryDef 
     With CopyQueryNew 
     ' Strip extra characters. 
     strSQL = .SQL 
     strRightSQL = Right(strSQL, 1) 
     Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
     strRightSQL = Chr(10) Or strRightSQL = vbCr 
     strSQL = Left(strSQL, Len(strSQL) - 1) 
     strRightSQL = Right(strSQL, 1) 
     Loop 
     .SQL = strSQL & strAdd 
     End With 
     
    End Function 
```     

<br/>

<span data-ttu-id="6ced0-119">Este exemplo mostra um uso possível de CopyQueryNew().</span><span class="sxs-lookup"><span data-stu-id="6ced0-119">This example shows a possible use of CopyQueryNew().</span></span>

```vb
Sub CopyQueryDefX() 
 
 Dim dbsNorthwind As Database 
 Dim qdfEmployees As QueryDef 
 Dim rstEmployees As Recordset2 
 Dim intCommand As Integer 
 Dim strOrderBy As String 
 Dim qdfCopy As QueryDef 
 Dim rstCopy As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
 "NewQueryDef", "SELECT FirstName, LastName, " & _ 
 "BirthDate FROM Employees") 
 Set rstEmployees = qdfEmployees.OpenRecordset( _ 
 dbOpenForwardOnly) 
 
 Do While True 
 intCommand = Val(InputBox( _ 
 "Choose field on which to order a new " & _ 
 "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
 "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
 "[Cancel - exit]")) 
 Select Case intCommand 
 Case 1 
 strOrderBy = " ORDER BY FirstName" 
 Case 2 
 strOrderBy = " ORDER BY LastName" 
 Case 3 
 strOrderBy = " ORDER BY BirthDate" 
 Case Else 
 Exit Do 
 End Select 
 Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
 Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
 dbForwardOnly) 
 With rstCopy 
 Do While Not .EOF 
 Debug.Print !LastName & ", " & !FirstName & _ 
 " - " & !BirthDate 
 .MoveNext 
 Loop 
 .Close 
 End With 
 Exit Do 
 Loop 
 
 rstEmployees.Close 
 ' Delete new QueryDef because this is a demonstration. 
 dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

