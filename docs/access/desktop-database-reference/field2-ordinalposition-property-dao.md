---
title: Propriedade Field2.OrdinalPosition (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 55d89611-ad07-990d-fc33-f81d59472430
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194179(v=office.15)
ms:contentKeyID: 48544937
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052899
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 451f2d1045b900460a24533ca49579bd9252f456
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881507"
---
# <a name="field2ordinalposition-property-dao"></a><span data-ttu-id="c950e-102">Propriedade Field2.OrdinalPosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="c950e-102">Field2.OrdinalPosition Property (DAO)</span></span>


<span data-ttu-id="c950e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c950e-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c950e-p101">Define ou retorna a posição relativa de um objeto **Field2** dentro de uma coleção **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="c950e-p101">Sets or returns the relative position of a **Field2** object within a **[Fields](fields-collection-dao.md)** collection. .</span></span>

## <a name="syntax"></a><span data-ttu-id="c950e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c950e-106">Syntax</span></span>

<span data-ttu-id="c950e-107">*expressão* . OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="c950e-107">*expression* .OrdinalPosition</span></span>

<span data-ttu-id="c950e-108">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="c950e-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c950e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c950e-109">Remarks</span></span>

<span data-ttu-id="c950e-110">Para um objeto ainda não acrescentado à coleção **Fields**, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c950e-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="c950e-111">O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="c950e-111">The default is 0.</span></span>

<span data-ttu-id="c950e-112">A disponibilidade da propriedade **OrdinalPosition** depende do objeto que contém a coleção **Fields**, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c950e-112">The availability of the **OrdinalPosition** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c950e-113">Se a coleção Fields pertencer a um</span><span class="sxs-lookup"><span data-stu-id="c950e-113">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="c950e-114">
OrdinalPosition será</span><span class="sxs-lookup"><span data-stu-id="c950e-114">Then OrdinalPosition is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c950e-115">Objeto <strong>index</strong></span><span class="sxs-lookup"><span data-stu-id="c950e-115"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c950e-116">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="c950e-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c950e-117">Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="c950e-117"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c950e-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c950e-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c950e-119">Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="c950e-119"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c950e-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c950e-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c950e-121">Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="c950e-121"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c950e-122">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="c950e-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c950e-123">Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="c950e-123"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c950e-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c950e-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c950e-p102">Em geral, a posição ordinal de um objeto que você acrescenta a uma coleção depende da ordem na qual ele é acrescentado. O primeiro objeto acrescentado está na primeira posição (0), o segundo está na segunda posição (1) e assim por diante. O último objeto acrescentado está na posição ordinal count – 1, em que count é o número de objetos na coleção como especificado pela configuração da propriedade **[Count](containers-count-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="c950e-p102">Generally, the ordinal position of an object that you append to a collection depends on the order in which you append the object. The first appended object is in the first position (0), the second appended object is in the second position (1), and so on. The last appended object is in ordinal position count – 1, where count is the number of objects in the collection as specified by the **[Count](containers-count-property-dao.md)** property setting.</span></span>

<span data-ttu-id="c950e-128">Você pode usar a propriedade **OrdinalPosition** para especificar uma posição ordinal para os novos objetos **Field2** que se difere da ordem na qual você acrescenta aqueles objetos a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="c950e-128">You can use the **OrdinalPosition** property to specify an ordinal position for new **Field2** objects that differs from the order in which you append those objects to a collection.</span></span> <span data-ttu-id="c950e-129">Isso permite que você especifique uma ordem de campo para suas tabelas, consultas e recordsets quando usá-los em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c950e-129">This enables you to specify a field order for your tables, queries, and recordsets when you use them in an application.</span></span> <span data-ttu-id="c950e-130">Por exemplo, a ordem na qual os campos são retornados em uma selecionar \* consulta é determinada pelos valores de propriedade **OrdinalPosition** atuais.</span><span class="sxs-lookup"><span data-stu-id="c950e-130">For example, the order in which fields are returned in a SELECT \* query is determined by the current **OrdinalPosition** property values.</span></span>

<span data-ttu-id="c950e-131">Você pode redefinir de modo permanente a ordem na qual os campos serão retornados em recordsets, configurando a propriedade **OrdinalPosition** para qualquer inteiro positivo.</span><span class="sxs-lookup"><span data-stu-id="c950e-131">You can permanently reset the order in which fields are returned in recordsets by setting the **OrdinalPosition** property to any positive integer.</span></span>

<span data-ttu-id="c950e-p104">Dois ou mais objetos **Field2** na mesma coleção podem ter o mesmo valor da propriedade **OrdinalPosition**, caso em que eles serão ordenados alfabeticamente. Por exemplo, se você tiver um campo chamado Idade definido como 4 e definir um segundo campo chamado Peso como 4, Peso será retornado depois de Idade.</span><span class="sxs-lookup"><span data-stu-id="c950e-p104">Two or more **Field2** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically. For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.</span></span>

<span data-ttu-id="c950e-p105">É possível especificar um número maior que o número de campos menos 1. O campo será retornado em uma ordem relativa ao maior número. Por exemplo, se você definir a propriedade **OrdinalPosition** de um campo como 20 (e se houver apenas 5 campos) e definir a propriedade **OrdinalPosition** de dois outros campos como 10 e 30 respectivamente, o campo definido como 20 será retornado entre os campos definidos como 10 e 30.</span><span class="sxs-lookup"><span data-stu-id="c950e-p105">You can specify a number that is greater than the number of fields minus 1. The field will be returned in an order relative to the largest number. For example, if you set a field's **OrdinalPosition** property to 20 (and there are only 5 fields) and you've set the **OrdinalPosition** property for two other fields to 10 and 30, respectively, the field set to 20 is returned between the fields set to 10 and 30.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c950e-p106">[!OBSERVAçãO] Mesmo se a coleção <STRONG>Fields</STRONG> de um <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> não tiver sido atualizado, a ordem do campo em um <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> aberto a partir de <STRONG>TableDef</STRONG> refletirá os dados de <STRONG>OrdinalPosition</STRONG> do objeto <STRONG>TableDef</STRONG>. Um <STRONG>Recordset</STRONG> tipo tabela terá os mesmos dados de <STRONG>OrdinalPosition</STRONG> que a tabela base, mas nenhum outro tipo de <STRONG>Recordset</STRONG> terá novos dados <STRONG>OrdinalPosition</STRONG> (começando com 0) que seguirão a ordem determinada pelos dados <STRONG>OrdinalPosition</STRONG> de <STRONG>TableDef</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c950e-p106">Even if the <STRONG>Fields</STRONG> collection of a <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> has not been refreshed, the field order in a <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> opened from the <STRONG>TableDef</STRONG> will reflect the <STRONG>OrdinalPosition</STRONG> data of the <STRONG>TableDef</STRONG> object. A table-type <STRONG>Recordset</STRONG> will have the same <STRONG>OrdinalPosition</STRONG> data as the underlying table, but any other type of <STRONG>Recordset</STRONG> will have new <STRONG>OrdinalPosition</STRONG> data (starting with 0) that follow the order determined by the <STRONG>OrdinalPosition</STRONG> data of the <STRONG>TableDef</STRONG>.</span></span></P>



## <a name="example"></a><span data-ttu-id="c950e-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c950e-139">Example</span></span>

<span data-ttu-id="c950e-p107">Este exemplo altera os valores da propriedade **OrdinalPosition** em **TableDef** de Funcionário para controlar a ordem de **Field2** em um **Recordset** resultante. Configurando a **OrdinalPosition** de todos os **Fields** para 1, qualquer **Recordset** resultante ordenará **Fields** alfabeticamente. Observe que os valores de **OrdinalPosition** no **Recordset** não correspondem aos valores na **TableDef**, mas simplesmente refletem o resultado final das alterações de **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="c950e-p107">This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field2** order in a resulting **Recordset**. By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically. Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.</span></span>

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field2 
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
