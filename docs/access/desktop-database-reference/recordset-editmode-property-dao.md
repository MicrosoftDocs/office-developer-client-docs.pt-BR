---
title: Propriedade Recordset.EditMode (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 326f23f95f9ccf8763f76b21df8955c39198a88c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307645"
---
# <a name="recordseteditmode-property-dao"></a>Propriedade Recordset.EditMode (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Retorna um valor que indica o estado da edição do registro atual.

## <a name="syntax"></a>Sintaxe

*expressão* . EditMode

*expression* Uma variável que representa um objeto **Recordset**.

## <a name="remarks"></a>Comentários

O valor de retorno é um **Long** que indica o estado da edição. O valor pode ser uma das constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.

A propriedade **EditMode** será útil quando um processo de edição for interrompido, por exemplo, por um erro durante a validação. Use o valor da propriedade **EditMode** para determinar se você deverá usar o método **[Update](recordset-update-method-dao.md)** ou **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.

Você também pode verificar se a definição da propriedade **[LockEdits](recordset-lockedits-property-dao.md)** será **True** e a definição da propriedade **EditMode** será **dbEditInProgress** para determinar se a página será bloqueada.

## <a name="example"></a>Exemplo

Este exemplo mostra o valor da propriedade **EditMode** em várias condições. A função EditModeOutput é necessária para esse procedimento ser executado.

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Show the EditMode property under different editing 
     ' states. 
     With rstEmployees 
     EditModeOutput "Before any Edit or AddNew:", .EditMode 
     .Edit 
     EditModeOutput "After Edit:", .EditMode 
     .Update 
     EditModeOutput "After Update:", .EditMode 
     .AddNew 
     EditModeOutput "After AddNew:", .EditMode 
     .CancelUpdate 
     EditModeOutput "After CancelUpdate:", .EditMode 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function EditModeOutput(strTemp As String, _ 
     intEditMode As Integer) 
     
     ' Print report based on the value of the EditMode 
     ' property. 
     Debug.Print strTemp 
     Debug.Print " EditMode = "; 
     
     Select Case intEditMode 
     Case dbEditNone 
     Debug.Print "dbEditNone" 
     Case dbEditInProgress 
     Debug.Print "dbEditInProgress" 
     Case dbEditAdd 
     Debug.Print "dbEditAdd" 
     End Select 
     
    End Function
```
