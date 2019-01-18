---
title: Propriedade RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9bdc243aae48bd928468362cb86ca077f4abe52
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707609"
---
# <a name="recordsetrecordcount-property-dao"></a><span data-ttu-id="38d9c-102">Propriedade RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="38d9c-102">Recordset.RecordCount property (DAO)</span></span>

<span data-ttu-id="38d9c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="38d9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38d9c-p101">Retorna o número de registros acessados em um objeto **[Recordset](recordset-object-dao.md)** ou o número total de registros em um objeto **Recordset** do tipo tabela ou em um objeto **[TableDef](tabledef-object-dao.md)**. **Long** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="38d9c-p101">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d9c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38d9c-107">Syntax</span></span>

<span data-ttu-id="38d9c-108">*expressão* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="38d9c-108">*expression* .RecordCount</span></span>

<span data-ttu-id="38d9c-109">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="38d9c-109">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="38d9c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="38d9c-110">Remarks</span></span>

<span data-ttu-id="38d9c-111">Use a propriedade **RecordCount** para descobrir quantos registros de um objeto **Recordset** ou **TableDef** foram acessados.</span><span class="sxs-lookup"><span data-stu-id="38d9c-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="38d9c-112">A propriedade **RecordCount** não indica quantos registros estão contido em um dynaset, instantâneo ou objeto **Recordset** do tipo somente encaminhamento, até que todos os registros foram acessados.</span><span class="sxs-lookup"><span data-stu-id="38d9c-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="38d9c-113">Assim que o último registro tiver sido acessado, a propriedade **RecordCount** indicará o número total de registros não excluídos no objeto **Recordset** ou **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="38d9c-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="38d9c-114">Para impor que o último registro seja acessado, use o método **[MoveLast](recordset-movelast-method-dao.md)** no objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="38d9c-114">To force the last record to be accessed, use the **[MoveLast](recordset-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="38d9c-115">Você também pode usar uma função **Count** SQL para determinar o número aproximado de registros que a sua consulta retornará.</span><span class="sxs-lookup"><span data-stu-id="38d9c-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>

> [!NOTE]
> <span data-ttu-id="38d9c-p103">[!OBSERVAçãO] Usar o método **MoveLast** para preencher um **Recordset** recém-aberto afeta negativamente o desempenho. A menos que seja necessário ter uma **RecordCount** precisa assim que você abrir um **Recordset**, será melhor aguardar até o preenchimento do **Recordset** com outras partes de código antes da verificação da propriedade **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="38d9c-p103">Using the **MoveLast** method to populate a newly opened **Recordset** negatively impacts performance. Unless it is necessary to have an accurate **RecordCount** as soon as you open a **Recordset**, it's better to wait until you populate the **Recordset** with other portions of code before checking the **RecordCount** property.</span></span>

<span data-ttu-id="38d9c-p104">À medida que seu aplicativo exclui registros em um objeto **Recordset** do tipo dynaset, o valor da propriedade **RecordCount** será reduzido. Entretanto, os registros excluídos por outros usuários não serão refletidos pela propriedade **RecordCount** até o registro atual ser posicionado em um registro excluído. Se você executar uma transação que afete a configuração da propriedade **RecordCount** e se depois a transação for revertida, a propriedade **RecordCount** não afetará o número real de registros restantes.</span><span class="sxs-lookup"><span data-stu-id="38d9c-p104">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="38d9c-121">A propriedade **RecordCount** de um objeto **Recordset** de instantâneo – ou – tipo forward only não é afetada pelas alterações nas tabelas base.</span><span class="sxs-lookup"><span data-stu-id="38d9c-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="38d9c-122">Um objeto **Recordset** ou **TableDef** sem registros tem a propriedade **RecordCount** configurada como 0.</span><span class="sxs-lookup"><span data-stu-id="38d9c-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="38d9c-123">O uso do método **[Requery](recordset-requery-method-dao.md)** em um objeto **Recordset** redefine a propriedade **RecordCount** como se a consulta tivesse sido executada novamente.</span><span class="sxs-lookup"><span data-stu-id="38d9c-123">Using the **[Requery](recordset-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="38d9c-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="38d9c-124">Example</span></span>

<span data-ttu-id="38d9c-125">Este exemplo demonstra a propriedade **RecordCount** com tipos diferentes de **Recordsets** antes e depois de preenchidos.</span><span class="sxs-lookup"><span data-stu-id="38d9c-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

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
