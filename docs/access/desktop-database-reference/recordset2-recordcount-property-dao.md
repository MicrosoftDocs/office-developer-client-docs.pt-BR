---
title: Propriedade Recordset2. RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: 77852966-11e9-1773-6e58-53927b84c03b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196071(v=office.15)
ms:contentKeyID: 48545728
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052890
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c23de433f26b5a54b3fee5cc69f67a07b53f8a3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309149"
---
# <a name="recordset2recordcount-property-dao"></a><span data-ttu-id="3d0c1-102">Propriedade Recordset2. RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="3d0c1-102">Recordset2.RecordCount property (DAO)</span></span>

<span data-ttu-id="3d0c1-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d0c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d0c1-p101">Retorna o número de registros acessados em um objeto **[Recordset](recordset-object-dao.md)** ou o número total de registros em um objeto **Recordset** do tipo tabela ou do objeto **[TableDef](tabledef-object-dao.md)**. **Long** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-p101">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d0c1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d0c1-107">Syntax</span></span>

<span data-ttu-id="3d0c1-108">*expressão* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="3d0c1-108">*expression* .RecordCount</span></span>

<span data-ttu-id="3d0c1-109">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3d0c1-109">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d0c1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d0c1-110">Remarks</span></span>

<span data-ttu-id="3d0c1-111">Use a propriedade **RecordCount** para descobrir quantos registros de um objeto **Recordset** ou **TableDef** foram acessados.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="3d0c1-112">A propriedade **RecordCount** não indica quantos registros foram contidos em um objeto **Recordset** do tipo dynaset, instantâneo ou somente encaminhamento até que todos os registros tenham sido acessados.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="3d0c1-113">Assim que o último registro tiver sido acessado, a propriedade **RecordCount** indicará o número total de registros não excluídos no objeto **Recordset** ou **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="3d0c1-114">Para forçar o acesso ao último registro, use o método **[MoveLast](recordset2-movelast-method-dao.md)** no objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-114">To force the last record to be accessed, use the **[MoveLast](recordset2-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="3d0c1-115">Além disso, é possível usar a função **Count** SQL para determinar o número de registros aproximado que a consulta retornará.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>

> [!NOTE]
> <span data-ttu-id="3d0c1-p103">[!OBSERVAçãO] O uso do método **MoveLast** para preencher um **Recordset** aberto recentemente causará impacto negativo no desempenho. A não ser que seja necessário ter um **RecordCount** preciso assim que você abrir um **Recordset**, é melhor aguardar até que o **Recordset** seja preenchido com outras partes do código antes de verificar a propriedade **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-p103">Using the **MoveLast** method to populate a newly opened **Recordset** negatively impacts performance. Unless it is necessary to have an accurate **RecordCount** as soon as you open a **Recordset**, it's better to wait until you populate the **Recordset** with other portions of code before checking the **RecordCount** property.</span></span>

<span data-ttu-id="3d0c1-p104">À medida que o aplicativo excluir os registros de um objeto **Recordset** do tipo dynaset, diminuirá o valor da propriedade **RecordCount**. No entanto, os registros excluídos por outros usuários não serão refletidos pela propriedade **RecordCount** até que o registro atual seja posicionado em um registro excluído. Se você executar uma transação que afeta a definição da propriedade **RecordCount** e reduzir posteriormente o preço da transação, a propriedade **RecordCount** não refletirá o número real de registros restantes.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-p104">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="3d0c1-121">A propriedade **RecordCount** de um objeto **Recordset** do tipo instantâneo ou somente encaminhamento não é afetado por alterações nas tabelas subjacentes.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="3d0c1-122">Um objeto **Recordset** ou **TableDef** sem registros tem a propriedade **RecordCount** configurada como 0.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="3d0c1-123">O uso do método **[Requery](recordset2-requery-method-dao.md)** em um objeto **Recordset** redefine a propriedade **RecordCount** exatamente como se a consulta tivesse sido reexecutada.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-123">Using the **[Requery](recordset2-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="3d0c1-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3d0c1-124">Example</span></span>

<span data-ttu-id="3d0c1-125">Este exemplo demonstra a propriedade **RecordCount** com tipos diferentes de **Recordsets** antes e depois de preenchidos.</span><span class="sxs-lookup"><span data-stu-id="3d0c1-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```
