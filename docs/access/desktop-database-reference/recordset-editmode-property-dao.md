---
title: Propriedade Recordset.EditMode (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c111193f7cfb90eb593788381e839839f29ba784
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926441"
---
# <a name="recordseteditmode-property-dao"></a><span data-ttu-id="1269c-102">Propriedade Recordset.EditMode (DAO)</span><span class="sxs-lookup"><span data-stu-id="1269c-102">Recordset.EditMode property (DAO)</span></span>


<span data-ttu-id="1269c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1269c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1269c-104">Retorna um valor que indica o estado da edição para o registro atual.</span><span class="sxs-lookup"><span data-stu-id="1269c-104">Returns a value that indicates the state of editing for the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="1269c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1269c-105">Syntax</span></span>

<span data-ttu-id="1269c-106">*expressão* . EditMode</span><span class="sxs-lookup"><span data-stu-id="1269c-106">*expression* .EditMode</span></span>

<span data-ttu-id="1269c-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1269c-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1269c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1269c-108">Remarks</span></span>

<span data-ttu-id="1269c-p101">O valor de retorno é **Long** que indica o estado da edição. O valor pode ser uma das constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1269c-p101">The return value is a **Long** that indicates the state of editing. The value can be one of the **[EditModeEnum](editmodeenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="1269c-p102">A propriedade **EditMode** é útil quando um processo de edição é interrompido, por exemplo, por um erro durante a validação. Você pode usar o valor da propriedade **EditMode** para determinar se você deve usar o método **[Update](recordset-update-method-dao.md)** ou **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1269c-p102">The **EditMode** property is useful when an editing process is interrupted, for example, by an error during validation. You can use the value of the **EditMode** property to determine whether you should use the **[Update](recordset-update-method-dao.md)** or **[CancelUpdate](recordset-cancelupdate-method-dao.md)** method.</span></span>

<span data-ttu-id="1269c-113">Você também pode verificar se a configuração da propriedade **[LockEdits](recordset-lockedits-property-dao.md)** é **True** e se a configuração de propriedade **EditMode** é **dbEditInProgress** para determinar se a página atual está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="1269c-113">You can also check to see if the **[LockEdits](recordset-lockedits-property-dao.md)** property setting is **True** and the **EditMode** property setting is **dbEditInProgress** to determine whether the current page is locked.</span></span>

## <a name="example"></a><span data-ttu-id="1269c-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1269c-114">Example</span></span>

<span data-ttu-id="1269c-p103">Este exemplo mostra o valor da propriedade **EditMode** sob diversas condições. A função EditModeOutput é exigida para que esse procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="1269c-p103">This example shows the value of the **EditMode** property under various conditions. The EditModeOutput function is required for this procedure to run.</span></span>

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
