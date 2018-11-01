---
title: Método Fields.Append (DAO)
TOCTitle: Append Method
ms:assetid: a0e553ba-6a57-09af-3436-4f6ca3cbe561
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820791(v=office.15)
ms:contentKeyID: 48546719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44d7b6c8c9c44b51f7771dd731b50848f1cbf175
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884818"
---
# <a name="fieldsappend-method-dao"></a><span data-ttu-id="7ab9d-102">Método Fields.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="7ab9d-102">Fields.Append Method (DAO)</span></span>


<span data-ttu-id="7ab9d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ab9d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="7ab9d-104">Adiciona um novo objeto **[Field](field-object-dao.md)** à coleção **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="7ab9d-104">Adds a new **[Field](field-object-dao.md)** to the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ab9d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ab9d-105">Syntax</span></span>

<span data-ttu-id="7ab9d-106">*expressão* . Acrescentar (***objeto***)</span><span class="sxs-lookup"><span data-stu-id="7ab9d-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="7ab9d-107">*expressão* Uma variável que representa um objeto **Fields** .</span><span class="sxs-lookup"><span data-stu-id="7ab9d-107">*expression* A variable that represents a **Fields** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="7ab9d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ab9d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ab9d-109">Nome</span><span class="sxs-lookup"><span data-stu-id="7ab9d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7ab9d-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="7ab9d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="7ab9d-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7ab9d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="7ab9d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ab9d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ab9d-113">Objeto</span><span class="sxs-lookup"><span data-stu-id="7ab9d-113">Object</span></span></p></td>
<td><p><span data-ttu-id="7ab9d-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7ab9d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7ab9d-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="7ab9d-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="7ab9d-116">Uma variável de objeto que representa o campo sendo acrescentado à coleção.</span><span class="sxs-lookup"><span data-stu-id="7ab9d-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7ab9d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ab9d-117">Remarks</span></span>

<span data-ttu-id="7ab9d-118">Você pode usar o método **Append** para adicionar uma nova tabela ao banco de dados, um campo a uma tabela ou um campo a um índice.</span><span class="sxs-lookup"><span data-stu-id="7ab9d-118">You can use the **Append** method to add a new table to a database, add a field to a table, and add a field to an index.</span></span>

<span data-ttu-id="7ab9d-119">O objeto acrescentado torna-se um objeto persistente, armazenado em disco, até que seja excluído utilizando o método **Delete**.</span><span class="sxs-lookup"><span data-stu-id="7ab9d-119">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="7ab9d-120">A adição de um novo objeto ocorre imediatamente, mas você deve usar o método **Refresh** em qualquer outra coleção que possa ser afetada pelas alterações na estrutura do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7ab9d-120">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="7ab9d-121">Se o objeto que você está acrescentando não estiver completo (como quando você não acrescentou um objeto **Field** a uma coleção **Fields** de um objeto **Index** antes de ele ser acrescentado a uma coleção **Indexes**) ou se as propriedades definidas em um ou mais objetos subordinados estiverem incorretas, a utilização do método **Append** causará um erro.</span><span class="sxs-lookup"><span data-stu-id="7ab9d-121">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="7ab9d-122">Por exemplo, se você ainda não tiver especificado um tipo de campo e, então, tenta acrescentar o objeto **Field** à coleção **Fields** em um objeto **TableDef** , usar o método **Append** dispara um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7ab9d-122">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="7ab9d-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7ab9d-123">Example</span></span>

<span data-ttu-id="7ab9d-p102">Este exemplo usa o método **Append** ou **Delete** para modificar a coleção **Fields** de um **TableDef**. O procedimento AppendDeleteField é necessário para que esse procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="7ab9d-p102">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**. The AppendDeleteField procedure is required for this procedure to run.</span></span>

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
