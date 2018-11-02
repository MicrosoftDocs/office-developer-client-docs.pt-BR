---
title: Propriedade Recordset2.Sort (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d9d154bb7506ca75862006a889c84906e43bc2a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925419"
---
# <a name="recordset2sort-property-dao"></a><span data-ttu-id="9f511-102">Propriedade Recordset2.Sort (DAO)</span><span class="sxs-lookup"><span data-stu-id="9f511-102">Recordset2.Sort property (DAO)</span></span>


<span data-ttu-id="9f511-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f511-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="9f511-104">Define ou retorna a ordem de classificação para registros em um objeto **[Recordset](recordset-object-dao.md)** (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9f511-104">Sets or returns the sort order for records in a **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f511-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f511-105">Syntax</span></span>

<span data-ttu-id="9f511-106">*expressão* . Classificar</span><span class="sxs-lookup"><span data-stu-id="9f511-106">*expression* .Sort</span></span>

<span data-ttu-id="9f511-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="9f511-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f511-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f511-108">Remarks</span></span>

<span data-ttu-id="9f511-109">Você pode usar a propriedade **Sort** com dynaset e instantâneo – objetos **Recordset** do tipo.</span><span class="sxs-lookup"><span data-stu-id="9f511-109">You can use the **Sort** property with dynaset– and snapshot–type **Recordset** objects.</span></span>

<span data-ttu-id="9f511-p101">Quando você definir essa propriedade para um objeto, ocorrerá a classificação durante a criação de um objeto **Recordset** subsequente para esse objeto. A definição da propriedade **Sort** substituirá qualquer ordem de classificação especificada para um objeto **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9f511-p101">When you set this property for an object, sorting occurs when a subsequent **Recordset** object is created from that object. The **Sort** property setting overrides any sort order specified for a **[QueryDef](querydef-object-dao.md)** object.</span></span>

<span data-ttu-id="9f511-112">A ordem de classificação padrão é a ascendente (A a Z ou 0 a 100).</span><span class="sxs-lookup"><span data-stu-id="9f511-112">The default sort order is ascending (A to Z or 0 to 100).</span></span>

<span data-ttu-id="9f511-113">A propriedade **Sort** não se aplica à tabela – ou – tipo forward only objetos **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="9f511-113">The **Sort** property doesn't apply to table– or forward–only–type **Recordset** objects.</span></span> <span data-ttu-id="9f511-114">Para classificar um objeto **Recordset** do tipo tabela, use a propriedade **[Index](recordset2-index-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="9f511-114">To sort a table–type **Recordset** object, use the **[Index](recordset2-index-property-dao.md)** property.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9f511-115">[!OBSERVAçãO] Em muitos casos, é mais rápido abrir um novo objeto <STRONG>Recordset</STRONG> usando uma instrução SQL que inclui os critérios de classificação.</span><span class="sxs-lookup"><span data-stu-id="9f511-115">In many cases, it's faster to open a new <STRONG>Recordset</STRONG> object by using an SQL statement that includes the sorting criteria.</span></span></P>



## <a name="example"></a><span data-ttu-id="9f511-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9f511-116">Example</span></span>

<span data-ttu-id="9f511-p103">Este exemplo demonstra a propriedade **Sort** pela alteração do seu valor e a criação de um novo **Recordset**. A função SortOutput será necessária para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="9f511-p103">This example demonstrates the **Sort** property by changing its value and creating a new **Recordset**. The SortOutput function is required for this procedure to run.</span></span>

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim rstSortEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

<span data-ttu-id="9f511-p104">Quando você conhecer os dados a serem selecionados, geralmente, será mais eficiente criar um **Recordset** com uma instrução SQL. Este exemplo mostra como você pode criar apenas um **Recordset** e obter os mesmos resultados de um exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="9f511-p104">When you know the data you want to select, it's usually more efficient to create a **Recordset** with an SQL statement. This example shows how you can create just one **Recordset** and obtain the same results as in the preceding example.</span></span>

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```
