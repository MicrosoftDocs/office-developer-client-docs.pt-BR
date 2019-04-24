---
title: Propriedade Campo2. Size (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f1467414729f4ea82bc2779eeb2bd162465b5ccd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292682"
---
# <a name="field2size-property-dao"></a><span data-ttu-id="de817-102">Propriedade Campo2. Size (DAO)</span><span class="sxs-lookup"><span data-stu-id="de817-102">Field2.Size property (DAO)</span></span>


<span data-ttu-id="de817-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de817-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="de817-104">Define ou retorna um valor que indica o tamanho máximo, em bytes, de um objeto **Field2**.</span><span class="sxs-lookup"><span data-stu-id="de817-104">Sets or returns a value that indicates the maximum size, in bytes, of a **Field2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="de817-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de817-105">Syntax</span></span>

<span data-ttu-id="de817-106">*expressão* . Porte</span><span class="sxs-lookup"><span data-stu-id="de817-106">*expression* .Size</span></span>

<span data-ttu-id="de817-107">*expressão* Uma variável que representa um objeto **campo2** .</span><span class="sxs-lookup"><span data-stu-id="de817-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="de817-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="de817-108">Remarks</span></span>

<span data-ttu-id="de817-109">Para um objeto ainda não acrescentado à coleção **[Fields](fields-collection-dao.md)**, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="de817-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="de817-p101">Para campos (diferentes dos campos tipo Memorando) que contêm dados de caractere, a propriedade **Size** indica o número máximo de caracteres que o campo pode ter. Para campos numéricos, a propriedade **Size** indica quantos bytes de repositório são necessários.</span><span class="sxs-lookup"><span data-stu-id="de817-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="de817-112">O uso da propriedade **Size** depende do objeto que contém a coleção **Fields** à qual o objeto **Field2** está acrescentado, como mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="de817-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de817-113">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="de817-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="de817-114">Uso</span><span class="sxs-lookup"><span data-stu-id="de817-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de817-115"><strong>Índice</strong></span><span class="sxs-lookup"><span data-stu-id="de817-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="de817-116">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="de817-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de817-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="de817-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="de817-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de817-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de817-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="de817-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="de817-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de817-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de817-121"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="de817-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="de817-122">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="de817-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de817-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="de817-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="de817-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de817-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="de817-p102">Quando você cria um objeto **Field2** com um tipo de dados diferente de Text, a configuração da propriedade **Type** automaticamente determina a configuração da propriedade **Size**; não é necessário defini-la. Para um objeto **Field2** com o tipo de dados Text, contudo, você pode definir **Size** para qualquer número inteiro até o tamanho máximo permito (255 para bancos de dados do mecanismo de bancos de dados do Microsoft Access). Se você não definir o tamanho, o campo será tão grande quanto o banco de dados permitir.</span><span class="sxs-lookup"><span data-stu-id="de817-p102">When you create a **Field2** object with a data type other than Text, the **Type** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field2** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access database engine databases). If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="de817-p103">Para objetos **Field2** Long Binary e Memo, **Size** é sempre definido como 0. Use a propriedade **FieldSize** do objeto **Field2** para determinar o tamanho dos dados em um registro específico. O tamanho máximo de um campo Long Binary ou Memo é limitado apenas pelos recursos do sistema ou pelo tamanho máximo permitido pelo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="de817-p103">For Long Binary and Memo **Field2** objects, **Size** is always set to 0. Use the **FieldSize** property of the **Field2** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="de817-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="de817-131">Example</span></span>

<span data-ttu-id="de817-132">Este exemplo demonstra a propriedade **Size** enumerando os nomes e os tamanhos dos objetos **Field2** na tabela Funcionários.</span><span class="sxs-lookup"><span data-stu-id="de817-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field2** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
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
