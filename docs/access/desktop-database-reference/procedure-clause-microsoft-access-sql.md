---
title: Cláusula PROCEDURE (Microsoft Access SQL)
TOCTitle: PROCEDURE Clause (Microsoft Access SQL)
ms:assetid: a718802c-9260-88d5-ec29-d5e5594927b0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821342(v=office.15)
ms:contentKeyID: 48546872
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277578
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 63b38a469c5de60588783381c24c61296b177bdd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877986"
---
# <a name="procedure-clause-microsoft-access-sql"></a><span data-ttu-id="5e5e4-102">Cláusula PROCEDURE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="5e5e4-102">PROCEDURE Clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="5e5e4-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e5e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5e5e4-104">Define um nome e os parâmetros opcionais para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="5e5e4-104">Defines a name and optional parameters for a query.</span></span>

> [!NOTE]
> <span data-ttu-id="5e5e4-p101">[!OBSERVAçãO] A cláusula PROCEDURE foi substituída pela instrução PROCEDURE. Embora a cláusula PROCEDURE ainda seja aceita, a instrução PROCEDURE fornece um superconjunto de recursos da cláusula PROCEDURE e é a sintaxe recomendada.</span><span class="sxs-lookup"><span data-stu-id="5e5e4-p101">The PROCEDURE clause has been superseded by the PROCEDURE statement. Although the PROCEDURE clause is still supported, the PROCEDURE statement provides a superset of the capability of the PROCEDURE clause and is the recommended syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5e4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e5e4-107">Syntax</span></span>

<span data-ttu-id="5e5e4-108">O *nome* do procedimento \[ *param1 datatype*\[, *param2 datatype*\[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="5e5e4-108">PROCEDURE *name* \[*param1 datatype*\[, *param2 datatype*\[, …\]\]</span></span>

<span data-ttu-id="5e5e4-109">A cláusula PROCEDURE contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="5e5e4-109">The PROCEDURE clause has these parts:</span></span>

|<span data-ttu-id="5e5e4-110">Parte</span><span class="sxs-lookup"><span data-stu-id="5e5e4-110">Part</span></span> |<span data-ttu-id="5e5e4-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e5e4-111">Description</span></span> |
|:----|:-----------|
|<span data-ttu-id="5e5e4-112">*name*</span><span class="sxs-lookup"><span data-stu-id="5e5e4-112">*name*</span></span> |<span data-ttu-id="5e5e4-p102">Um nome para o procedimento. Ele deve seguir as convenções de nomenclatura padrão.</span><span class="sxs-lookup"><span data-stu-id="5e5e4-p102">A name for the procedure. It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="5e5e4-115">*param1*, *param2*</span><span class="sxs-lookup"><span data-stu-id="5e5e4-115">*param1*, *param2*</span></span> |<span data-ttu-id="5e5e4-p103">Um ou mais campos ou parâmetros de campo. Por exemplo:
</span><span class="sxs-lookup"><span data-stu-id="5e5e4-p103">One or more field names or parameters. For example:</span></span><br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="5e5e4-118">Para obter mais informações sobre parâmetros, consulte [parameters](parameters-declaration-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="5e5e4-118">For more information about parameters, see [parameters](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="5e5e4-119">*tipo de dados*</span><span class="sxs-lookup"><span data-stu-id="5e5e4-119">*datatype*</span></span> | <span data-ttu-id="5e5e4-120">Um dos principais [tipos de dados do Microsoft Access SQL](sql-data-types.md) ou seus sinônimos.</span><span class="sxs-lookup"><span data-stu-id="5e5e4-120">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span> |


## <a name="remarks"></a><span data-ttu-id="5e5e4-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e5e4-121">Remarks</span></span>

<span data-ttu-id="5e5e4-122">Um procedimento SQL consiste em uma cláusula PROCEDURE (que especifica o nome do procedimento), uma lista opcional das definições de parâmetro e uma única instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="5e5e4-122">An SQL procedure consists of a PROCEDURE clause (which specifies the name of the procedure), an optional list of parameter definitions, and a single SQL statement.</span></span> <span data-ttu-id="5e5e4-123">Por exemplo, o procedimento Get\_Part\_número pode executar uma consulta que recupera um número de peça especificado.</span><span class="sxs-lookup"><span data-stu-id="5e5e4-123">For example, the procedure Get\_Part\_Number might run a query that retrieves a specified part number.</span></span>

> [!NOTE]
> - <span data-ttu-id="5e5e4-124">Se a cláusula incluir mais de uma definição de campo (isto é, pares de *param-datatype* ), separe-os com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="5e5e4-124">If the clause includes more than one field definition (that is, *param-datatype* pairs), separate them with commas.</span></span>
> - <span data-ttu-id="5e5e4-125">A cláusula PROCEDURE deve ser seguida por uma instrução SQL (por exemplo, uma instrução [SELECT](select-statement-microsoft-access-sql.md) ou [UPDATE](update-statement-microsoft-access-sql.md)).</span><span class="sxs-lookup"><span data-stu-id="5e5e4-125">The PROCEDURE clause must be followed by an SQL statement (for example, a [SELECT](select-statement-microsoft-access-sql.md) or [UPDATE](update-statement-microsoft-access-sql.md) statement).</span></span>

## <a name="example"></a><span data-ttu-id="5e5e4-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5e5e4-126">Example</span></span>

<span data-ttu-id="5e5e4-127">Este exemplo chama a consulta CategoryList e chama o procedimento EnumFields, que pode ser encontrado no exemplo da instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="5e5e4-127">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
