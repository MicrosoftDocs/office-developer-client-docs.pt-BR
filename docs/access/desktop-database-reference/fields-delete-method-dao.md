---
title: Método Fields. (DAO)
TOCTitle: Delete Method
ms:assetid: a8e249e7-7526-3eff-a5cf-70cab2081970
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821417(v=office.15)
ms:contentKeyID: 48546913
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052868
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ffeb9594dda7a041758659fd1a88ee6adfa02403
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997599"
---
# <a name="fieldsdelete-method-dao"></a><span data-ttu-id="7ea82-102">Método Fields. (DAO)</span><span class="sxs-lookup"><span data-stu-id="7ea82-102">Fields.Delete method (DAO)</span></span>

<span data-ttu-id="7ea82-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ea82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ea82-104">Exclui um objeto **[Field](field-object-dao.md)** da coleção **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="7ea82-104">Deletes a **[Field](field-object-dao.md)** from the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ea82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ea82-105">Syntax</span></span>

<span data-ttu-id="7ea82-106">*expressão* . Excluir (***nome***)</span><span class="sxs-lookup"><span data-stu-id="7ea82-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="7ea82-107">*expressão* Uma variável que representa um objeto **Fields** .</span><span class="sxs-lookup"><span data-stu-id="7ea82-107">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ea82-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ea82-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ea82-109">Nome</span><span class="sxs-lookup"><span data-stu-id="7ea82-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7ea82-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="7ea82-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7ea82-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7ea82-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7ea82-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ea82-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ea82-113"><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="7ea82-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="7ea82-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7ea82-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7ea82-115"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="7ea82-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7ea82-116">O campo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7ea82-116">The field to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7ea82-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ea82-117">Remarks</span></span>

<span data-ttu-id="7ea82-118">A exclusão de um objeto armazenado ocorre imediatamente, mas você deve usar o método **Refresh** em qualquer outra coleção que possa ser afetada pelas alterações na estrutura do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7ea82-118">The deletion of a stored object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

## <a name="example"></a><span data-ttu-id="7ea82-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7ea82-119">Example</span></span>

<span data-ttu-id="7ea82-p101">Este exemplo usa o método **Append** ou **Delete** para modificar a coleção **Fields** de um **TableDef**. O procedimento AppendDeleteField é necessário para que esse procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="7ea82-p101">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**. The AppendDeleteField procedure is required for this procedure to run.</span></span>

```vb
    Sub AppendX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Add three new fields. 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "E-mail", dbText, 50 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Http", dbText, 80 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Quota", dbInteger, 5 
     
     Debug.Print "Fields after Append" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show the new fields. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     ' Delete the newly added fields. 
     AppendDeleteField tdfEmployees, "DELETE", "E-mail" 
     AppendDeleteField tdfEmployees, "DELETE", "Http" 
     AppendDeleteField tdfEmployees, "DELETE", "Quota" 
     
     Debug.Print "Fields after Delete" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show that the new 
     ' fields have been deleted. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub AppendDeleteField(tdfTemp As TableDef, _ 
     strCommand As String, strName As String, _ 
     Optional varType, Optional varSize) 
     
     With tdfTemp 
     
     ' Check first to see if the TableDef object is 
     ' updatable. If it isn't, control is passed back to 
     ' the calling procedure. 
     If .Updatable = False Then 
     MsgBox "TableDef not Updatable! " & _ 
     "Unable to complete task." 
     Exit Sub 
     End If 
     
     ' Depending on the passed data, append or delete a 
     ' field to the Fields collection of the specified 
     ' TableDef object. 
     If strCommand = "APPEND" Then 
     .Fields.Append .CreateField(strName, _ 
     varType, varSize) 
     Else 
     If strCommand = "DELETE" Then .Fields.Delete _ 
     strName 
     End If 
     
     End With 
     
    End Sub
```
