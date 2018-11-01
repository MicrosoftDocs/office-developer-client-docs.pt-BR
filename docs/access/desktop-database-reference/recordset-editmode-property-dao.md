---
title: Propriedade Recordset.EditMode (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7445538d1e9aaa27f9cefcd17f085e2e0f26ec23
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871350"
---
# <a name="recordseteditmode-property-dao"></a>Propriedade Recordset.EditMode (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna um valor que indica o estado da edição para o registro atual.

## <a name="syntax"></a>Sintaxe

*expressão* . EditMode

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

O valor de retorno é **Long** que indica o estado da edição. O valor pode ser uma das constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.

A propriedade **EditMode** é útil quando um processo de edição é interrompido, por exemplo, por um erro durante a validação. Você pode usar o valor da propriedade **EditMode** para determinar se você deve usar o método **[Update](recordset-update-method-dao.md)** ou **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.

Você também pode verificar se a configuração da propriedade **[LockEdits](recordset-lockedits-property-dao.md)** é **True** e se a configuração de propriedade **EditMode** é **dbEditInProgress** para determinar se a página atual está bloqueada.

## <a name="example"></a>Exemplo

Este exemplo mostra o valor da propriedade **EditMode** sob diversas condições. A função EditModeOutput é exigida para que esse procedimento seja executado.

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
