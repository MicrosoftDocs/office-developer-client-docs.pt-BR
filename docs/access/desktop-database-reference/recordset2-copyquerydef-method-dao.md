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
# <a name="recordset2copyquerydef-method-dao"></a>Método Recordset2. CopyQueryDef (DAO)


**Aplica-se ao:** Access 2013, Office 2013 

Retorna um objeto **[QueryDef](querydef-object-dao.md)** que é uma cópia do **QueryDef** usado para criar o objeto **[Recordset](recordset-object-dao.md)** representado pelo espaço reservado Recordset (apenas espaços de trabalho do Microsoft Access). .

## <a name="syntax"></a>Sintaxe

*expressão* . CopyQueryDef

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="return-value"></a>Valor de retorno

QueryDef

## <a name="remarks"></a>Comentários

Você pode usar o método **CopyQueryDef** para criar um novo **QueryDef** que é uma duplicata do **QueryDef** utilizado para criar o **Recordset**.

Ocorre um erro se um **QueryDef** não foi usado para criar esse **Recordset**. Você deve primeiro abrir um **Recordset** com o método **OpenRecordset** antes de usar o método **CopyQueryDef**.

Esse método é útil quando você cria um objeto **Recordset** de um **QueryDef** e transmite o **Recordset** para uma função, e a função deve recriar o equivalente SQL da consulta, por exemplo, para modificá-la de alguma forma.

## <a name="example"></a>Exemplo

Este exemplo usa o método **CopyQueryDef** para criar uma cópia de um **QueryDef** a partir de um **Recordset** existente e modifica a cópia adicionando uma cláusula à propriedade SQL. Quando você cria um **QueryDef** permanente, espaços, ponto-e-vírgulas ou preenchimentos de linha podem ser adicionados à propriedade SQL; esses caracteres extra devem ser removidos antes de uma nova cláusula ser acrescentada à instrução SQL.

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

Este exemplo mostra um uso possível de CopyQueryNew().

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

