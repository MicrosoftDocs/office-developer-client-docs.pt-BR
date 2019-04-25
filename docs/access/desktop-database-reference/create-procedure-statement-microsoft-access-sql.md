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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295398"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a><span data-ttu-id="4a74c-102">Instrução CREATE PROCEDURE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="4a74c-102">CREATE PROCEDURE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="4a74c-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a74c-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="4a74c-104">Cria um procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="4a74c-104">Creates a stored procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="4a74c-105">O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de CREATE PROCEDURE nem de nenhuma instrução DDL, com os bancos de dados cujos mecanismos sejam diferentes do Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="4a74c-105">The Microsoft Access database engine does not support the use of CREATE PROCEDURE, or any of the DDL statements, with non-Microsoft Jet database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a74c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a74c-106">Syntax</span></span>

<span data-ttu-id="4a74c-107">CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement</span><span class="sxs-lookup"><span data-stu-id="4a74c-107">CREATE PROCEDURE procedure
    [param1 datatype[, param2 datatype[, …]] AS sqlstatement</span></span>

<span data-ttu-id="4a74c-108">A instrução CREATE PROCEDURE tem as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="4a74c-108">The CREATE PROCEDURE statement has these parts:</span></span>

|<span data-ttu-id="4a74c-109">Sair</span><span class="sxs-lookup"><span data-stu-id="4a74c-109">Part</span></span>|<span data-ttu-id="4a74c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a74c-110">Description</span></span>|
|:---|:----------|
|<span data-ttu-id="4a74c-111">*procedure*</span><span class="sxs-lookup"><span data-stu-id="4a74c-111">*procedure*</span></span>|<span data-ttu-id="4a74c-112">Um nome para o procedimento.</span><span class="sxs-lookup"><span data-stu-id="4a74c-112">A name for the procedure.</span></span> <span data-ttu-id="4a74c-113">Ele deve seguir as convenções de nomenclatura padrão.</span><span class="sxs-lookup"><span data-stu-id="4a74c-113">It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="4a74c-114">*param1*, *param2*</span><span class="sxs-lookup"><span data-stu-id="4a74c-114">*param1*, *param2*</span></span>|<span data-ttu-id="4a74c-115">De um a 255 nomes ou parâmetros de campo.</span><span class="sxs-lookup"><span data-stu-id="4a74c-115">From one to 255 field names or parameters.</span></span> <span data-ttu-id="4a74c-116">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="4a74c-116">For example:</span></span><br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="4a74c-117">Para obter mais informações sobre parâmetros, consulte [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="4a74c-117">For more information on parameters, see [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="4a74c-118">*datatype*</span><span class="sxs-lookup"><span data-stu-id="4a74c-118">*DataType*</span></span>|<span data-ttu-id="4a74c-119">Um dos principais [tipos de dados do Microsoft Access SQL](sql-data-types.md) ou seus sinônimos.</span><span class="sxs-lookup"><span data-stu-id="4a74c-119">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span>|
|<span data-ttu-id="4a74c-120">*sqlstatement*</span><span class="sxs-lookup"><span data-stu-id="4a74c-120">*SQLStatement*</span></span>|<span data-ttu-id="4a74c-121">Uma instrução SQL, como SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4a74c-121">An SQL statement such as SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, and so on.</span></span>|


## <a name="remarks"></a><span data-ttu-id="4a74c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a74c-122">Remarks</span></span>

<span data-ttu-id="4a74c-123">Um procedimento SQL consiste em uma instrução PROCEDURE que especifica o nome do procedimento, uma lista opcional de definições de parâmetros e uma única instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="4a74c-123">An SQL procedure consists of a PROCEDURE clause that specifies the name of the procedure, an optional list of parameter definitions, and a single SQL statement.</span></span>

<span data-ttu-id="4a74c-124">O nome de um procedimento não pode ser igual ao nome de uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="4a74c-124">A procedure name cannot be the same as the name of an existing table.</span></span>

## <a name="example"></a><span data-ttu-id="4a74c-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4a74c-125">Example</span></span>

<span data-ttu-id="4a74c-126">Este exemplo chama a consulta CategoryList e o procedimento EnumFields, o que pode ser localizado no exemplo da instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="4a74c-126">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
