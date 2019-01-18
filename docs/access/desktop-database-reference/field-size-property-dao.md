---
title: Propriedade Field.Size (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 16ce8a9e63c18ded2738035f23e9a1baeff4cc8c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708337"
---
# <a name="fieldsize-property-dao"></a><span data-ttu-id="f3a03-102">Propriedade Field.Size (DAO)</span><span class="sxs-lookup"><span data-stu-id="f3a03-102">Field.Size property (DAO)</span></span>


<span data-ttu-id="f3a03-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3a03-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f3a03-104">Define ou retorna um valor que indica o tamanho máximo, em bytes, de um objeto **[Field](field-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="f3a03-104">Sets or returns a value that indicates the maximum size, in bytes, of a **[Field](field-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a03-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3a03-105">Syntax</span></span>

<span data-ttu-id="f3a03-106">*expressão* . Tamanho</span><span class="sxs-lookup"><span data-stu-id="f3a03-106">*expression* .Size</span></span>

<span data-ttu-id="f3a03-107">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="f3a03-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a03-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3a03-108">Remarks</span></span>

<span data-ttu-id="f3a03-109">Para um objeto ainda não acrescentado à coleção **[Fields](fields-collection-dao.md)**, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f3a03-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="f3a03-p101">Para os campos (diferentes dos campos de tipo Memorando) que contêm dados do caractere, a propriedade **Size** indica o número máximo de caracteres que o campo pode manter. Para os campos numéricos, a propriedade **Size** indica quantos bytes de repositório serão necessários.</span><span class="sxs-lookup"><span data-stu-id="f3a03-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="f3a03-112">O uso da propriedade **Size** depende do objeto que contém a coleção **Fields** à qual o objeto **Field** foi acrescentado, conforme mostra a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f3a03-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3a03-113">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="f3a03-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="f3a03-114">Uso</span><span class="sxs-lookup"><span data-stu-id="f3a03-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3a03-115"><strong>Índice</strong></span><span class="sxs-lookup"><span data-stu-id="f3a03-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="f3a03-116">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="f3a03-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3a03-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="f3a03-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="f3a03-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f3a03-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3a03-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="f3a03-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="f3a03-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f3a03-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3a03-121"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="f3a03-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="f3a03-122">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="f3a03-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3a03-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="f3a03-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="f3a03-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f3a03-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f3a03-p102">Quando você criar um objeto **Field** com um tipo de dados diferente de Texto, a definição da propriedade **[Type](field-type-property-dao.md)** determinará automaticamente a definição da propriedade **Size**; não será necessário defini-la. Para um objeto **Field** com o tipo de dados Texto, no entanto, você deve definir **Size** como um número inteiro até o tamanho de texto máximo (255 para o banco de dados do Microsoft Access). Se você não definir o tamanho, o campo será tão grande quanto o banco de dados permitir.</span><span class="sxs-lookup"><span data-stu-id="f3a03-p102">When you create a **Field** object with a data type other than Text, the **[Type](field-type-property-dao.md)** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access databases). If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="f3a03-p103">Para objetos Long Binary e Memo **Field**, **Size** será sempre definido como 0. Use a propriedade **[FieldSize](field-fieldsize-property-dao.md)** do objeto **Field** para determinar o tamanho dos dados em um registro específico. O tamanho máximo de um campo Long Binary ou Memo estará limitado apenas pelos recursos do sistema ou pelo tamanho máximo que o banco de dados permitir.</span><span class="sxs-lookup"><span data-stu-id="f3a03-p103">For Long Binary and Memo **Field** objects, **Size** is always set to 0. Use the **[FieldSize](field-fieldsize-property-dao.md)** property of the **Field** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="f3a03-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f3a03-131">Example</span></span>

<span data-ttu-id="f3a03-132">Este exemplo demonstra a propriedade **Size** pela enumeração dos nomes e dos tamanhos dos objetos **Field** na tabela Funcionários.</span><span class="sxs-lookup"><span data-stu-id="f3a03-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
