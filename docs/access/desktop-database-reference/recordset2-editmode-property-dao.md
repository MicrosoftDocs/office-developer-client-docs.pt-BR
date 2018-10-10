---
title: Propriedade Recordset2.EditMode (DAO)
TOCTitle: EditMode Property
ms:assetid: fd61ea2b-e7d7-195f-4114-87e54eba2451
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837240(v=office.15)
ms:contentKeyID: 48548914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053080
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7b8ff4fa104dd153faf6eb1a50d2e922e5e5021d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462174"
---
# <a name="recordset2editmode-property-dao"></a>Propriedade Recordset2.EditMode (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Retorna um valor que indica o estado da edição para o registro atual.

## <a name="syntax"></a>Sintaxe

*expressão* . EditMode

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

O valor de retorno é **Long** que indica o estado da edição. O valor pode ser uma das constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.

A propriedade **EditMode** é útil quando um processo de edição é interrompido, por exemplo, por um erro durante a validação. Você pode usar o valor da propriedade **EditMode** para determinar se você deve usar o método **[Update](recordset2-update-method-dao.md)** ou **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.

Você também pode verificar se a configuração da propriedade **[LockEdits](recordset2-lockedits-property-dao.md)** é **True** e se a configuração de propriedade **EditMode** é **dbEditInProgress** para determinar se a página atual está bloqueada.

## <a name="example"></a>Exemplo

Este exemplo mostra o valor da propriedade **EditMode** sob diversas condições. A função EditModeOutput é exigida para que esse procedimento seja executado.

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
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
