---
title: Tipo de dados equivalentes ao ANSI SQL
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293508"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="8d819-102">Tipo de dados equivalentes ao ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="8d819-102">Equivalent ANSI SQL data types</span></span>


<span data-ttu-id="8d819-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d819-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d819-104">A tabela a seguir lista os tipos de dados ANSI SQL, seus tipos de dados equivalentes do mecanismo SQL do banco de dados do Microsoft Access e seus sinônimos válidos.</span><span class="sxs-lookup"><span data-stu-id="8d819-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="8d819-105">Ele também lista os tipos de dados equivalentes do Microsoft SQL Server™.</span><span class="sxs-lookup"><span data-stu-id="8d819-105">It also lists the equivalent Microsoft® SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d819-106">Tipo de dados ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="8d819-106">ANSI SQL
data type</span></span></p></th>
<th><p><span data-ttu-id="8d819-107">Tipos de dados do Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="8d819-107">Microsoft Access
SQL data type</span></span></p></th>
<th><p><span data-ttu-id="8d819-108">Sinônimos</span><span class="sxs-lookup"><span data-stu-id="8d819-108">Synonym lookup</span></span></p></th>
<th><p><span data-ttu-id="8d819-109">Tipo de dados do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="8d819-109">Microsoft SQL
Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d819-110">BIT, BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="8d819-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="8d819-111">BINARY (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="8d819-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="8d819-112">VARBINARY, BINARY VARYING BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="8d819-112">VARBINARY,
BINARY VARYING
BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="8d819-113">BINARY, VARBINARY</span><span class="sxs-lookup"><span data-stu-id="8d819-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d819-114">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="8d819-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="8d819-115">BIT (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="8d819-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="8d819-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span><span class="sxs-lookup"><span data-stu-id="8d819-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="8d819-117">BIT</span><span class="sxs-lookup"><span data-stu-id="8d819-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d819-118">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="8d819-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="8d819-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="8d819-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="8d819-120">INTEGER1, BYTE</span><span class="sxs-lookup"><span data-stu-id="8d819-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="8d819-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="8d819-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d819-122">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="8d819-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="8d819-123">COUNTER (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="8d819-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="8d819-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="8d819-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="8d819-125">(Consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="8d819-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d819-126">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="8d819-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="8d819-127">DINHEIRO</span><span class="sxs-lookup"><span data-stu-id="8d819-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="8d819-128">MOEDA</span><span class="sxs-lookup"><span data-stu-id="8d819-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="8d819-129">DINHEIRO</span><span class="sxs-lookup"><span data-stu-id="8d819-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d819-130">DATE, TIME, TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="8d819-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="8d819-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="8d819-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="8d819-132">DATA, HORA (Consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="8d819-132">DATE, TIME  (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="8d819-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="8d819-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d819-134">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="8d819-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="8d819-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="8d819-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="8d819-136">GUID</span><span class="sxs-lookup"><span data-stu-id="8d819-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="8d819-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="8d819-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d819-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="8d819-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="8d819-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="8d819-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="8d819-140">NUMERIC, DEC</span><span class="sxs-lookup"><span data-stu-id="8d819-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="8d819-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="8d819-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d819-142">REAL</span><span class="sxs-lookup"><span data-stu-id="8d819-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="8d819-143">REAL</span><span class="sxs-lookup"><span data-stu-id="8d819-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="8d819-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="8d819-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="8d819-145">REAL</span><span class="sxs-lookup"><span data-stu-id="8d819-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d819-146">DOUBLE PRECISION, FLOAT</span><span class="sxs-lookup"><span data-stu-id="8d819-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="8d819-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="8d819-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="8d819-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="8d819-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="8d819-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="8d819-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d819-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="8d819-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="8d819-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="8d819-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="8d819-152">SHORT, INTEGER2</span><span class="sxs-lookup"><span data-stu-id="8d819-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="8d819-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="8d819-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d819-154">INTEIRO</span><span class="sxs-lookup"><span data-stu-id="8d819-154">Integer</span></span></p></td>
<td><p><span data-ttu-id="8d819-155">INTEIRO</span><span class="sxs-lookup"><span data-stu-id="8d819-155">Integer</span></span></p></td>
<td><p><span data-ttu-id="8d819-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="8d819-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="8d819-157">INTEIRO</span><span class="sxs-lookup"><span data-stu-id="8d819-157">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d819-158">INTERVALO</span><span class="sxs-lookup"><span data-stu-id="8d819-158">Interval</span></span></p></td>
<td><p><span data-ttu-id="8d819-159">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="8d819-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8d819-160">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="8d819-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d819-161">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="8d819-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="8d819-162">IMAGEM</span><span class="sxs-lookup"><span data-stu-id="8d819-162">Image</span></span></p></td>
<td><p><span data-ttu-id="8d819-163">LONGBINARY, GENERAL, OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="8d819-163">LONGBINARY,  GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="8d819-164">IMAGEM</span><span class="sxs-lookup"><span data-stu-id="8d819-164">Image</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d819-165">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="8d819-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="8d819-166">TEXTO (Consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="8d819-166">TEXT  (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="8d819-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="8d819-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="8d819-168">TEXTO</span><span class="sxs-lookup"><span data-stu-id="8d819-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d819-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="8d819-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="8d819-170">CHAR (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="8d819-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="8d819-171">TEXTO(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (consulte Observações)</span><span class="sxs-lookup"><span data-stu-id="8d819-171">TEXT(n), ALPHANUMERIC,  CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="8d819-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="8d819-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="8d819-p102">O tipo de dados ANSI SQL BIT não corresponde ao tipo de dados do Microsoft Access SQL BIT. Ele corresponde ao tipo de dados BINARY. Não há nenhum ANSI SQL equivalente para o tipo de dados do Microsoft Access SQL BIT.</span><span class="sxs-lookup"><span data-stu-id="8d819-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="8d819-176">TIMESTAMP não é mais aceito como um sinônimo de DATETIME.</span><span class="sxs-lookup"><span data-stu-id="8d819-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="8d819-p103">NUMERIC não é mais aceito como um sinônimo de FLOAT ou DOUBLE. NUMERIC é agora utilizado como um sinônimo de DECIMAL.</span><span class="sxs-lookup"><span data-stu-id="8d819-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="8d819-179">Um campo LONGTEXT é sempre armazenado no formato de representação Unicode.</span><span class="sxs-lookup"><span data-stu-id="8d819-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="8d819-p104">Se o nome do tempo de dados TEXT for usado sem especificar o tamanho original, por exemplo, TEXT(25), um campo LONGTEXT será criado. Isso permite que as [instruções CREATE TABLE](create-table-statement-microsoft-access-sql.md) sejam gravadas para que os tipos de dados sejam processados de forma consistente com o Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8d819-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="8d819-182">Um campo CHAR sempre será armazenado no formato de representação Unicode, o que equivale ao tipo de dados ANSI SQL NATIONAL CHAR.</span><span class="sxs-lookup"><span data-stu-id="8d819-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="8d819-p105">Se o nome do tipo de dados TEXT for usado e o tamanho opcional for especificado, por exemplo TEXT(25), o tipo de dados do campo será equivalente ao tipo de dados CHAR. Isso preserva a compatibilidade com versões anteriores para a maioria dos aplicativos Microsoft Jet, permitindo, ao mesmo tempo, que o tipo de dados TEXT (sem uma especificação de tamanho) seja alinhado ao Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8d819-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


