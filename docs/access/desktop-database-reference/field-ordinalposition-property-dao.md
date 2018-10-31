---
title: Propriedade Field.OrdinalPosition (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 07f2344e-2a72-33d8-be47-b37d76ecca47
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845002(v=office.15)
ms:contentKeyID: 48543088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1218dd1cc6b1b309c5513a9b0f67a66d06d9c499
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863624"
---
# <a name="fieldordinalposition-property-dao"></a><span data-ttu-id="a3636-102">Propriedade Field.OrdinalPosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="a3636-102">Field.OrdinalPosition Property (DAO)</span></span>


<span data-ttu-id="a3636-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3636-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a3636-p101">Define ou retorna a posição relativa de um objeto **[Field](field-object-dao.md)** em uma coleção **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="a3636-p101">Sets or returns the relative position of a **[Field](field-object-dao.md)** object within a **[Fields](fields-collection-dao.md)** collection. .</span></span>

## <a name="syntax"></a><span data-ttu-id="a3636-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3636-106">Syntax</span></span>

<span data-ttu-id="a3636-107">*expressão* . OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="a3636-107">*expression* .OrdinalPosition</span></span>

<span data-ttu-id="a3636-108">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="a3636-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3636-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3636-109">Remarks</span></span>

<span data-ttu-id="a3636-110">Para um objeto ainda não acrescentado à coleção **Fields**, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a3636-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="a3636-111">O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a3636-111">The default is 0.</span></span>

<span data-ttu-id="a3636-112">A disponibilidade da propriedade **OrdinalPosition** depende do objeto que contém a coleção **Fields**, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3636-112">The availability of the **OrdinalPosition** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3636-113">Se a coleção Fields pertencer a um</span><span class="sxs-lookup"><span data-stu-id="a3636-113">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="a3636-114">
OrdinalPosition será</span><span class="sxs-lookup"><span data-stu-id="a3636-114">Then OrdinalPosition is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3636-115">Objeto <strong>index</strong></span><span class="sxs-lookup"><span data-stu-id="a3636-115"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a3636-116">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="a3636-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3636-117">Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a3636-117"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a3636-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3636-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3636-119">Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="a3636-119"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a3636-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3636-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3636-121">Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="a3636-121"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a3636-122">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="a3636-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3636-123">Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a3636-123"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a3636-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a3636-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a3636-p102">Em geral, a posição ordinal de um objeto que você acrescenta a uma coleção depende da ordem na qual ele é acrescentado. O primeiro objeto acrescentado está na primeira posição (0), o segundo está na segunda posição (1) e assim por diante. O último objeto acrescentado está na posição ordinal count – 1, em que count é o número de objetos na coleção como especificado pela configuração da propriedade **[Count](containers-count-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="a3636-p102">Generally, the ordinal position of an object that you append to a collection depends on the order in which you append the object. The first appended object is in the first position (0), the second appended object is in the second position (1), and so on. The last appended object is in ordinal position count – 1, where count is the number of objects in the collection as specified by the **[Count](containers-count-property-dao.md)** property setting.</span></span>

<span data-ttu-id="a3636-128">Use a propriedade **OrdinalPosition** para especificar a posição ordinal dos novos objetos **Field** que é diferente da ordem na qual foram acrescentados à uma coleção.</span><span class="sxs-lookup"><span data-stu-id="a3636-128">You can use the **OrdinalPosition** property to specify an ordinal position for new **Field** objects that differs from the order in which you append those objects to a collection.</span></span> <span data-ttu-id="a3636-129">Isso permite especificar a ordem dos campos para tabelas, consultas e recordsets quando você usá-los em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3636-129">This enables you to specify a field order for your tables, queries, and recordsets when you use them in an application.</span></span> <span data-ttu-id="a3636-130">Por exemplo, a ordem na qual os campos são retornados em uma selecionar \* consulta é determinada pelos valores de propriedade **OrdinalPosition** atuais.</span><span class="sxs-lookup"><span data-stu-id="a3636-130">For example, the order in which fields are returned in a SELECT \* query is determined by the current **OrdinalPosition** property values.</span></span>

<span data-ttu-id="a3636-131">Redefina, de forma permanente, a ordem na qual os campos são retornados nos recordsets pela definição da propriedade **OrdinalPosition** para qualquer número inteiro positivo.</span><span class="sxs-lookup"><span data-stu-id="a3636-131">You can permanently reset the order in which fields are returned in recordsets by setting the **OrdinalPosition** property to any positive integer.</span></span>

<span data-ttu-id="a3636-p104">Dois ou mais objetos **Field** na mesma coleção podem ter o mesmo valor da propriedade **OrdinalPosition** e, nesse caso, serão colocados em ordem alfabética. Por exemplo, se você tem um campo denominado Idade definido como 4 e definir um segundo campo denominado Peso como 4, Peso será retornado depois de Idade.</span><span class="sxs-lookup"><span data-stu-id="a3636-p104">Two or more **Field** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically. For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.</span></span>

<span data-ttu-id="a3636-p105">Especifique um número maior que o número de campos menos 1. O campo será retornado em uma ordem relativa ao maior número. Por exemplo, se você definir a propriedade **OrdinalPosition** do campo como 20 (e existirem somente cinco campos) e já tiver definido a propriedade **OrdinalPosition** para outros dois campos como 10 e 30, respectivamente, o campo definido como 20 será retornado entre os campos definidos como 10 e 30.</span><span class="sxs-lookup"><span data-stu-id="a3636-p105">You can specify a number that is greater than the number of fields minus 1. The field will be returned in an order relative to the largest number. For example, if you set a field's **OrdinalPosition** property to 20 (and there are only 5 fields) and you've set the **OrdinalPosition** property for two other fields to 10 and 30, respectively, the field set to 20 is returned between the fields set to 10 and 30.</span></span>

> [!NOTE]
> <span data-ttu-id="a3636-p106">[!OBSERVAçãO] Mesmo se a coleção **Fields** de um [TableDef](tabledef-object-dao.md) não tiver sido atualizado, a ordem do campo em um [Recordset](recordset-object-dao.md) aberto a partir de **TableDef** refletirá os dados de **OrdinalPosition** do objeto **TableDef**. Um **Recordset** tipo tabela terá os mesmos dados de **OrdinalPosition** que a tabela base, mas nenhum outro tipo de **Recordset** terá novos dados **OrdinalPosition** (começando com 0) que seguirão a ordem determinada pelos dados **OrdinalPosition** de **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="a3636-p106">Even if the **Fields** collection of a [TableDef](tabledef-object-dao.md) has not been refreshed, the field order in a [Recordset](recordset-object-dao.md) opened from the **TableDef** will reflect the **OrdinalPosition** data of the **TableDef** object. A table-type **Recordset** will have the same **OrdinalPosition** data as the underlying table, but any other type of **Recordset** will have new **OrdinalPosition** data (starting with 0) that follow the order determined by the **OrdinalPosition** data of the **TableDef**.</span></span>

## <a name="example"></a><span data-ttu-id="a3636-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a3636-139">Example</span></span>

<span data-ttu-id="a3636-p107">Este exemplo altera os valores da propriedade **OrdinalPosition** no **TableDef** Funcionários para controlar a ordem **Field** em um **Recordset** resultante. Pela definição de **OrdinalPosition** de todos os **Fields** como 1, qualquer **Recordset** resultante colocará os **Fields** em ordem alfabética. Observe que os valores **OrdinalPosition** em **Recordset** não correspondem aos valores de **TableDef**, mas refletem apenas o resultado final das alterações de **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="a3636-p107">This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field** order in a resulting **Recordset**. By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically. Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.</span></span>

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     
     With tdfEmployees 
     ' Display and store original OrdinalPosition data. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldTemp In .Fields 
     fldTemp.OrdinalPosition = 1 
     Next fldTemp 
     
     ' Open new Recordset object to show how the 
     ' OrdinalPosition data has affected the record order. 
     Debug.Print _ 
     "OrdinalPosition data from resulting Recordset." 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT * FROM Employees") 
     For Each fldTemp In rstEmployees.Fields 
     Debug.Print , fldTemp.OrdinalPosition, fldTemp.Name 
     Next fldTemp 
     rstEmployees.Close 
     
     ' Restore original OrdinalPosition data because this is 
     ' a demonstration. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
