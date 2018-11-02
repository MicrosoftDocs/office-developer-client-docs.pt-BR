---
title: Método Recordset.CancelUpdate (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c75b98de62738e479b0bbb1608097f0f920cf60c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926483"
---
# <a name="recordsetcancelupdate-method-dao"></a><span data-ttu-id="d2285-102">Método Recordset.CancelUpdate (DAO)</span><span class="sxs-lookup"><span data-stu-id="d2285-102">Recordset.CancelUpdate method (DAO)</span></span>


<span data-ttu-id="d2285-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2285-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2285-104">Cancela quaisquer atualizações pendentes para um objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="d2285-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2285-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2285-105">Syntax</span></span>

<span data-ttu-id="d2285-106">*expressão* . CancelUpdate (***UpdateType***)</span><span class="sxs-lookup"><span data-stu-id="d2285-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="d2285-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d2285-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="d2285-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2285-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2285-109">Nome</span><span class="sxs-lookup"><span data-stu-id="d2285-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d2285-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="d2285-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="d2285-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d2285-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="d2285-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2285-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2285-113">UpdateType</span><span class="sxs-lookup"><span data-stu-id="d2285-113">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="d2285-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="d2285-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="d2285-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="d2285-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="d2285-116">Defina como um dos valores <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="d2285-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="d2285-117">Os valores <EM>dbUpdateRegular</EM> e <EM>dbUpdateBatch</EM> são válidos somente se a atualização em lotes está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d2285-117">The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></P>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d2285-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2285-118">Remarks</span></span>

<span data-ttu-id="d2285-p101">Você pode usar o método **CancelUpdate** para cancelar atualizações pendentes que resultam de uma operação **[Edit](recordset-edit-method-dao.md)** ou **[AddNew](recordset-addnew-method-dao.md)**. Por exemplo, se um usuário invocar o método **Edit** ou **AddNew** e não tiver invocado ainda o método **Update**, **CancelUpdate** cancela quaisquer alterações feitas depois que **Edit** ou **AddNew** tiver sido invocado.</span><span class="sxs-lookup"><span data-stu-id="d2285-p101">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** operation. For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="d2285-121">Verifique a propriedade **[EditMode](recordset-editmode-property-dao.md)** do **Recordset** para determinar se existe uma operação pendente que possa ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="d2285-121">Check the **[EditMode](recordset-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d2285-122">[!OBSERVAçãO] Usar o método <STRONG>CancelUpdate</STRONG> tem o mesmo efeito de mover para outro registro sem usar o método <STRONG><A href="recordset-update-method-dao.md">Update</A></STRONG>, exceto pelo fato de que o registro atual não muda e várias propriedades, como <STRONG><A href="recordset-bof-property-dao.md">BOF</A></STRONG> e <STRONG><A href="recordset-eof-property-dao.md">EOF</A></STRONG>, não são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="d2285-122">Using the <STRONG>CancelUpdate</STRONG> method has the same effect as moving to another record without using the <STRONG><A href="recordset-update-method-dao.md">Update</A></STRONG> method, except that the current record doesn't change, and various properties, such as <STRONG><A href="recordset-bof-property-dao.md">BOF</A></STRONG> and <STRONG><A href="recordset-eof-property-dao.md">EOF</A></STRONG>, aren't updated.</span></span></P>



## <a name="example"></a><span data-ttu-id="d2285-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d2285-123">Example</span></span>

<span data-ttu-id="d2285-124">Este exemplo mostra como o método **CancelUpdate** é usado com o método **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="d2285-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
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

<span data-ttu-id="d2285-125">Este exemplo mostra como o método **CancelUpdate** é usado com o método **Edit**.</span><span class="sxs-lookup"><span data-stu-id="d2285-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

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

