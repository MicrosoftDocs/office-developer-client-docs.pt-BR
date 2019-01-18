---
title: Instrução CREATE PROCEDURE (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: f223e164bd36a6a1a76140a28dd57cd2005e4a20
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700763"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a><span data-ttu-id="668d1-102">Instrução CREATE PROCEDURE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="668d1-102">CREATE PROCEDURE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="668d1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="668d1-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="668d1-104">Cria um procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="668d1-104">Creates a stored procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="668d1-105">[!OBSERVAçãO] O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de CREATE PROCEDURE nem de nenhuma instrução DDL, com os bancos de dados cujos mecanismos sejam diferentes do Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="668d1-105">The Microsoft Access database engine does not support the use of CREATE PROCEDURE, or any of the DDL statements, with non-Microsoft Jet database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="668d1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="668d1-106">Syntax</span></span>

<span data-ttu-id="668d1-107">CREATE PROCEDURE *procedimento* \[ *param1 datatype*\[, *param2 datatype*\[,... \] \] Como sqlstatement</span><span class="sxs-lookup"><span data-stu-id="668d1-107">CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement</span></span>

<span data-ttu-id="668d1-108">A instrução PROCEDURE INDEX contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="668d1-108">The CREATE PROCEDURE statement has these parts:</span></span>

|<span data-ttu-id="668d1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="668d1-109">Part</span></span>|<span data-ttu-id="668d1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="668d1-110">Description</span></span>|
|:---|:----------|
|<span data-ttu-id="668d1-111">*procedimento*</span><span class="sxs-lookup"><span data-stu-id="668d1-111">*procedure*</span></span>|<span data-ttu-id="668d1-p101">Um nome para o procedimento. Ele deve seguir as convenções de nomenclatura padrão.</span><span class="sxs-lookup"><span data-stu-id="668d1-p101">A name for the procedure. It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="668d1-114">*param1*, *param2*</span><span class="sxs-lookup"><span data-stu-id="668d1-114">*param1*, *param2*</span></span>|<span data-ttu-id="668d1-p102">De 1 a 255 nomes de campo ou parâmetros. Por exemplo:
</span><span class="sxs-lookup"><span data-stu-id="668d1-p102">From one to 255 field names or parameters. For example:</span></span><br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="668d1-117">Para obter mais informações sobre parâmetros, consulte [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="668d1-117">For more information about parameters, see [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="668d1-118">*tipo de dados*</span><span class="sxs-lookup"><span data-stu-id="668d1-118">*datatype*</span></span>|<span data-ttu-id="668d1-119">Um dos principais [tipos de dados do Microsoft Access SQL](sql-data-types.md) ou seus sinônimos.</span><span class="sxs-lookup"><span data-stu-id="668d1-119">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span>|
|<span data-ttu-id="668d1-120">*sqlstatement*</span><span class="sxs-lookup"><span data-stu-id="668d1-120">*sqlstatement*</span></span>|<span data-ttu-id="668d1-121">Uma instrução SQL como SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="668d1-121">An SQL statement such as SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, and so on.</span></span>|


## <a name="remarks"></a><span data-ttu-id="668d1-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="668d1-122">Remarks</span></span>

<span data-ttu-id="668d1-123">Um procedimento SQL consiste em uma cláusula PROCEDURE que especifica o nome do procedimento, uma lista opcional de definições de parâmetros e uma instrução SQL única.</span><span class="sxs-lookup"><span data-stu-id="668d1-123">An SQL procedure consists of a PROCEDURE clause that specifies the name of the procedure, an optional list of parameter definitions, and a single SQL statement.</span></span>

<span data-ttu-id="668d1-124">Um nome de procedimento não pode ser o mesmo de uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="668d1-124">A procedure name cannot be the same as the name of an existing table.</span></span>

## <a name="example"></a><span data-ttu-id="668d1-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="668d1-125">Example</span></span>

<span data-ttu-id="668d1-126">Este exemplo chama a consulta CategoryList e chama o procedimento EnumFields, que pode ser encontrado no exemplo da instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="668d1-126">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
