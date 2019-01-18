---
title: Método Recordset2.CancelUpdate (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 90378dc61d12485a290bbd7857d026a46cd9da96
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721370"
---
# <a name="recordset2cancelupdate-method-dao"></a><span data-ttu-id="5908c-102">Método Recordset2.CancelUpdate (DAO)</span><span class="sxs-lookup"><span data-stu-id="5908c-102">Recordset2.CancelUpdate method (DAO)</span></span>

<span data-ttu-id="5908c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5908c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5908c-104">Cancela quaisquer atualizações pendentes para um objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="5908c-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5908c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5908c-105">Syntax</span></span>

<span data-ttu-id="5908c-106">*expressão* . CancelUpdate (***UpdateType***)</span><span class="sxs-lookup"><span data-stu-id="5908c-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="5908c-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="5908c-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5908c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5908c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5908c-109">Nome</span><span class="sxs-lookup"><span data-stu-id="5908c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5908c-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="5908c-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="5908c-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5908c-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="5908c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5908c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5908c-113"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="5908c-113"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="5908c-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="5908c-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="5908c-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="5908c-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="5908c-116">Defina como um dos valores <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="5908c-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p><p><span data-ttu-id="5908c-117"><strong>Observação</strong>: os valores de <EM>dbUpdateRegular</EM> e <EM>dbUpdateBatch</EM> são válidos somente se a atualização em lotes está habilitado.</span><span class="sxs-lookup"><span data-stu-id="5908c-117"><strong>NOTE</strong>: The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5908c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5908c-118">Remarks</span></span>

<span data-ttu-id="5908c-p101">Você pode usar o método **CancelUpdate** para cancelar atualizações pendentes que resultam de uma operação **[Edit](recordset2-edit-method-dao.md)** ou **[AddNew](recordset2-addnew-method-dao.md)**. Por exemplo, se um usuário invocar o método **Edit** ou **AddNew** e não tiver invocado ainda o método **Update**, **CancelUpdate** cancela quaisquer alterações feitas depois que **Edit** ou **AddNew** tiver sido invocado.</span><span class="sxs-lookup"><span data-stu-id="5908c-p101">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset2-addnew-method-dao.md)** operation. For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="5908c-121">Verifique a propriedade **[EditMode](recordset2-editmode-property-dao.md)** do **Recordset** para determinar se existe uma operação pendente que possa ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="5908c-121">Check the **[EditMode](recordset2-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="5908c-122">[!OBSERVAçãO] Usar o método **CancelUpdate** tem o mesmo efeito de mover para outro registro sem usar o método **[Update](recordset2-update-method-dao.md)**, exceto pelo fato de que o registro atual não muda e várias propriedades, como **[BOF](recordset2-bof-property-dao.md)** e **[EOF](recordset2-eof-property-dao.md)**, não são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="5908c-122">Using the **CancelUpdate** method has the same effect as moving to another record without using the **[Update](recordset2-update-method-dao.md)** method, except that the current record doesn't change, and various properties, such as **[BOF](recordset2-bof-property-dao.md)** and **[EOF](recordset2-eof-property-dao.md)**, aren't updated.</span></span>

## <a name="example"></a><span data-ttu-id="5908c-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5908c-123">Example</span></span>

<span data-ttu-id="5908c-124">Este exemplo mostra como o método **CancelUpdate** é usado com o método **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="5908c-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="5908c-125">Este exemplo mostra como o método **CancelUpdate** é usado com o método **Edit**.</span><span class="sxs-lookup"><span data-stu-id="5908c-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

