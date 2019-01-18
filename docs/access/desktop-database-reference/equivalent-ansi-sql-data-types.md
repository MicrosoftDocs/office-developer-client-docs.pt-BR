---
title: Tipo de dados ANSI SQL equivalentes
TOCTitle: Equivalent ANSI SQL data types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 3ea0641c7325bfcb4339572bc8b50724115af8d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699377"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="ac6df-102">Tipo de dados ANSI SQL equivalentes</span><span class="sxs-lookup"><span data-stu-id="ac6df-102">Equivalent ANSI SQL data types</span></span>


<span data-ttu-id="ac6df-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac6df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ac6df-104">A tabela a seguir lista os tipos de dados ANSI SQL, seus tipos de dados SQL do mecanismo de banco de dados do Microsoft Access e seus sinônimos válidos.</span><span class="sxs-lookup"><span data-stu-id="ac6df-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="ac6df-105">Ela também lista os tipos de dados Microsoft SQL Server™ equivalentes.</span><span class="sxs-lookup"><span data-stu-id="ac6df-105">It also lists the equivalent Microsoft SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac6df-106">Tipo de dados ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="ac6df-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="ac6df-107">Tipo de dados do Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="ac6df-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="ac6df-108">
Sinônimo</span><span class="sxs-lookup"><span data-stu-id="ac6df-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="ac6df-109">Tipo de dados do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ac6df-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac6df-110">BIT, BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="ac6df-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="ac6df-111">BINARY (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="ac6df-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ac6df-112">VARBINARY, BINÁRIO VARIANTE BIT VARIADOS</span><span class="sxs-lookup"><span data-stu-id="ac6df-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="ac6df-113">BINARY, VARBINARY</span><span class="sxs-lookup"><span data-stu-id="ac6df-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac6df-114">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ac6df-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ac6df-115">BIT (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="ac6df-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ac6df-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span><span class="sxs-lookup"><span data-stu-id="ac6df-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="ac6df-117">BIT</span><span class="sxs-lookup"><span data-stu-id="ac6df-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac6df-118">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ac6df-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ac6df-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="ac6df-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="ac6df-120">INTEGER1, BYTE</span><span class="sxs-lookup"><span data-stu-id="ac6df-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="ac6df-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="ac6df-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac6df-122">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ac6df-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ac6df-123">COUNTER (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="ac6df-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ac6df-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="ac6df-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="ac6df-125">(Consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="ac6df-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac6df-126">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ac6df-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ac6df-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="ac6df-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="ac6df-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="ac6df-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="ac6df-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="ac6df-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac6df-130">DATE, TIME, TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="ac6df-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="ac6df-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="ac6df-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="ac6df-132">DATE, TIME (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="ac6df-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ac6df-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="ac6df-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac6df-134">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ac6df-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ac6df-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="ac6df-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="ac6df-136">GUID</span><span class="sxs-lookup"><span data-stu-id="ac6df-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="ac6df-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="ac6df-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac6df-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="ac6df-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="ac6df-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="ac6df-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="ac6df-140">NUMERIC, DEC</span><span class="sxs-lookup"><span data-stu-id="ac6df-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="ac6df-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="ac6df-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac6df-142">REAL</span><span class="sxs-lookup"><span data-stu-id="ac6df-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="ac6df-143">REAL</span><span class="sxs-lookup"><span data-stu-id="ac6df-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="ac6df-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="ac6df-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="ac6df-145">REAL</span><span class="sxs-lookup"><span data-stu-id="ac6df-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac6df-146">DOUBLE PRECISION, FLOAT</span><span class="sxs-lookup"><span data-stu-id="ac6df-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="ac6df-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ac6df-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="ac6df-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="ac6df-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ac6df-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ac6df-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac6df-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="ac6df-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="ac6df-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="ac6df-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="ac6df-152">SHORT, INTEGER2</span><span class="sxs-lookup"><span data-stu-id="ac6df-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="ac6df-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="ac6df-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac6df-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="ac6df-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="ac6df-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="ac6df-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="ac6df-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="ac6df-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="ac6df-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="ac6df-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac6df-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="ac6df-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="ac6df-159">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ac6df-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ac6df-160">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ac6df-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac6df-161">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ac6df-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ac6df-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="ac6df-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="ac6df-163">LONGBINARY, GENERAL, OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="ac6df-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="ac6df-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="ac6df-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac6df-165">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ac6df-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ac6df-166">TEXTO (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="ac6df-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ac6df-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="ac6df-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ac6df-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="ac6df-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac6df-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="ac6df-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="ac6df-170">CHAR (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="ac6df-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ac6df-171">Text (n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="ac6df-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ac6df-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="ac6df-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="ac6df-p102">O tipo de dados ANSI SQL BIT não corresponde ao tipo de dados do Microsoft Access SQL BIT. Ele corresponde ao tipo de dados BINARY. Não há nenhum ANSI SQL equivalente para o tipo de dados do Microsoft Access SQL BIT.</span><span class="sxs-lookup"><span data-stu-id="ac6df-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="ac6df-176">TIMESTAMP não é mais aceito como um sinônimo de DATETIME.</span><span class="sxs-lookup"><span data-stu-id="ac6df-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="ac6df-p103">NUMERIC não é mais aceito como um sinônimo de FLOAT ou DOUBLE. NUMERIC é agora utilizado como um sinônimo de DECIMAL.</span><span class="sxs-lookup"><span data-stu-id="ac6df-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="ac6df-179">Um campo LONGTEXT é sempre armazenado no formato de representação Unicode.</span><span class="sxs-lookup"><span data-stu-id="ac6df-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="ac6df-p104">Se o nome do tempo de dados TEXT for usado sem especificar o tamanho original, por exemplo, TEXT(25), um campo LONGTEXT será criado. Isso permite que as [instruções CREATE TABLE](create-table-statement-microsoft-access-sql.md) sejam gravadas para que os tipos de dados sejam processados de forma consistente com o Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ac6df-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="ac6df-182">Um campo CHAR sempre será armazenado no formato de representação Unicode, o que equivale ao tipo de dados ANSI SQL NATIONAL CHAR.</span><span class="sxs-lookup"><span data-stu-id="ac6df-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="ac6df-p105">Se o nome do tipo de dados TEXT for usado e o tamanho opcional for especificado, por exemplo TEXT(25), o tipo de dados do campo será equivalente ao tipo de dados CHAR. Isso preserva a compatibilidade com versões anteriores para a maioria dos aplicativos Microsoft Jet, permitindo, ao mesmo tempo, que o tipo de dados TEXT (sem uma especificação de tamanho) seja alinhado ao Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ac6df-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


