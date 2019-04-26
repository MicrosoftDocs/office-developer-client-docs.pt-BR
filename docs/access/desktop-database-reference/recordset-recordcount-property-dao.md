---
title: Propriedade Recordset.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9bdc243aae48bd928468362cb86ca077f4abe52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307634"
---
# <a name="recordsetrecordcount-property-dao"></a><span data-ttu-id="4596c-102">Propriedade Recordset.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="4596c-102">Recordset.RecordCount Property (DAO)</span></span>

<span data-ttu-id="4596c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4596c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4596c-p101">Retorna o número de registros acessados em um objeto **[Recordset](recordset-object-dao.md)** ou o número total de registros em um objeto **Recordset** do tipo tabela ou do objeto **[TableDef](tabledef-object-dao.md)**. **Long** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4596c-p101">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4596c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4596c-107">Syntax</span></span>

<span data-ttu-id="4596c-108">*expressão* .RecordCount</span><span class="sxs-lookup"><span data-stu-id="4596c-108">expression  . RecordCount</span></span>

<span data-ttu-id="4596c-109">*expressão* Uma variável que representa um objeto **Conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="4596c-109">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4596c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4596c-110">Remarks</span></span>

<span data-ttu-id="4596c-111">Use a propriedade **RecordCount** para descobrir quantos registros de um objeto **Recordset** ou **TableDef** foram acessados.</span><span class="sxs-lookup"><span data-stu-id="4596c-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="4596c-112">A propriedade **RecordCount** não indica quantos registros foram contidos em um objeto **Recordset** do tipo dynaset, instantâneo ou somente encaminhamento até que todos os registros tenham sido acessados.</span><span class="sxs-lookup"><span data-stu-id="4596c-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="4596c-113">Assim que o último registro tiver sido acessado, a propriedade **RecordCount** indicará o número total de registros não excluídos no objeto **Recordset** ou **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="4596c-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="4596c-114">Para forçar o acesso ao último registro, use o método **[MoveLast](recordset-movelast-method-dao.md)** no objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="4596c-114">To force the last record to be accessed, use the **[MoveLast](recordset-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="4596c-115">Além disso, é possível usar a função **Count** SQL para determinar o número de registros aproximado que a consulta retornará.</span><span class="sxs-lookup"><span data-stu-id="4596c-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>

> [!NOTE]
> <span data-ttu-id="4596c-p103">O uso do método **MoveLast** para preencher um **Recordset** aberto recentemente causará impacto negativo no desempenho. A não ser que seja necessário ter um **RecordCount** preciso assim que você abrir um **Recordset**, é melhor aguardar até que o **Recordset** seja preenchido com outras partes do código antes de verificar a propriedade **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="4596c-p103">Using the **MoveLast** method to populate a newly opened **Recordset** negatively impacts performance. Unless it is necessary to have an accurate **RecordCount** as soon as you open a **Recordset**, it's better to wait until you populate the **Recordset** with other portions of code before checking the **RecordCount** property.</span></span>

<span data-ttu-id="4596c-p104">À medida que o aplicativo excluir os registros de um objeto **Recordset** do tipo dynaset, diminuirá o valor da propriedade **RecordCount**. No entanto, os registros excluídos por outros usuários não serão refletidos pela propriedade **RecordCount** até que o registro atual seja posicionado em um registro excluído. Se você executar uma transação que afeta a definição da propriedade **RecordCount** e reduzir posteriormente o preço da transação, a propriedade **RecordCount** não refletirá o número real de registros restantes.</span><span class="sxs-lookup"><span data-stu-id="4596c-p104">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="4596c-121">A propriedade **RecordCount** de um objeto **Recordset** do tipo instantâneo ou somente encaminhamento não é afetado por alterações nas tabelas subjacentes.</span><span class="sxs-lookup"><span data-stu-id="4596c-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="4596c-122">Um objeto **Recordset** ou **TableDef** sem registros tem a propriedade **RecordCount** configurada como 0.</span><span class="sxs-lookup"><span data-stu-id="4596c-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="4596c-123">O uso do método **[Requery](recordset-requery-method-dao.md)** em um objeto **Recordset** redefine a propriedade **RecordCount** exatamente como se a consulta tivesse sido reexecutada.</span><span class="sxs-lookup"><span data-stu-id="4596c-123">Using the **[Requery](recordset-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="4596c-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4596c-124">Example</span></span>

<span data-ttu-id="4596c-125">Este exemplo demonstra a propriedade **RecordCount** com tipos diferentes de **Recordsets** antes e depois de preenchidos.</span><span class="sxs-lookup"><span data-stu-id="4596c-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
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
