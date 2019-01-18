---
title: Método Recordset.CopyQueryDef (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: fee8c2fe-500e-dfb3-21ce-211e54ff334b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837296(v=office.15)
ms:contentKeyID: 48548950
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa6c5aab5f357eef8c62c63c6fca873e64031411
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713643"
---
# <a name="recordsetcopyquerydef-method-dao"></a>Método Recordset.CopyQueryDef (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna um objeto **[QueryDef](querydef-object-dao.md)** que é uma cópia do **QueryDef** usado para criar o objeto **[Recordset](recordset-object-dao.md)** representado por um espaço reservado recordset (somente espaços de trabalho do Microsoft Access). .

## <a name="syntax"></a>Sintaxe

*expressão* . CopyQueryDef

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="return-value"></a>Valor de retorno

QueryDef

## <a name="remarks"></a>Comentários

Você pode usar o método **CopyQueryDef** para criar um novo **QueryDef** que seja uma duplicata do **QueryDef** usado para criar o **Recordset**.

Se não foi usado um **QueryDef** para criar esse **Recordset**, ocorrerá um erro. Você deve primeiramente abrir um **Recordset** com o método **OpenRecordset** antes de usar o método **CopyQueryDef**.

Esse método é útil quando você cria um objeto **Recordset** a partir de um **QueryDef** e passa o **Recordset** para uma função, e a função deve recriar o equivalente SQL da consulta, por exemplo, para modificá-lo de alguma maneira.

## <a name="example"></a>Exemplo

Este exemplo usa o método **CopyQueryDef** para criar uma cópia de um **QueryDef** a partir de um **Recordset** existente e modifica a cópia adicionando uma cláusula à propriedade SQL. Quando você cria um **QueryDef** permanente, espaços, ponto-e-vírgulas ou alimentações de linha podem ser adicionados à propriedade SQL; esses caracteres adicionais devem ser removidos antes da adição de qualquer cláusula à instrução SQL.

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

Este exemplo mostra um possível uso do CopyQueryNew().

```vb 
Sub CopyQueryDefX() 
 
 Dim dbsNorthwind As Database 
 Dim qdfEmployees As QueryDef 
 Dim rstEmployees As Recordset 
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

