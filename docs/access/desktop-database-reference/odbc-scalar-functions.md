---
title: Funções escalares ODBC
TOCTitle: ODBC Scalar Functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 21e6000e8620011f5f6f0c2481bb9c03fd71bab5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887954"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="14a8b-102">Funções escalares ODBC</span><span class="sxs-lookup"><span data-stu-id="14a8b-102">ODBC Scalar Functions</span></span>


<span data-ttu-id="14a8b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="14a8b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14a8b-p101">O Microsoft® Access SQL fornece suporte ao uso da sintaxe definida ODBC para funções escalares. Por exemplo, a consulta:</span><span class="sxs-lookup"><span data-stu-id="14a8b-p101">Microsoft® Access SQL supports the use of the ODBC defined syntax for scalar functions. For example, the query:</span></span>

<span data-ttu-id="14a8b-106">SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} \> 5</span><span class="sxs-lookup"><span data-stu-id="14a8b-106">SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} \> 5</span></span>

<span data-ttu-id="14a8b-107">retorna todas as linhas em que o valor absoluto da alteração no preço de uma ação foi maior que cinco.</span><span class="sxs-lookup"><span data-stu-id="14a8b-107">Would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="14a8b-p102">Um subconjunto de funções escalares definidas por ODBC é aceito. A tabela a seguir lista as funções aceitas.</span><span class="sxs-lookup"><span data-stu-id="14a8b-p102">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="14a8b-110">Para obter uma descrição dos argumentos e uma explicação completa da sintaxe de eliminação para a inclusão de funções em uma instrução SQL, consulte a documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="14a8b-110">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="14a8b-111">Funções de sequência</span><span class="sxs-lookup"><span data-stu-id="14a8b-111">String Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14a8b-112">ASCII</span><span class="sxs-lookup"><span data-stu-id="14a8b-112">ASCII</span></span></p></td>
<td><p><span data-ttu-id="14a8b-113">LENGTH</span><span class="sxs-lookup"><span data-stu-id="14a8b-113">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="14a8b-114">RTRIM</span><span class="sxs-lookup"><span data-stu-id="14a8b-114">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a8b-115">CHAR</span><span class="sxs-lookup"><span data-stu-id="14a8b-115">CHAR</span></span></p></td>
<td><p><span data-ttu-id="14a8b-116">LOCATE</span><span class="sxs-lookup"><span data-stu-id="14a8b-116">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="14a8b-117">SPACE</span><span class="sxs-lookup"><span data-stu-id="14a8b-117">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a8b-118">CONCAT</span><span class="sxs-lookup"><span data-stu-id="14a8b-118">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="14a8b-119">LTRIM</span><span class="sxs-lookup"><span data-stu-id="14a8b-119">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="14a8b-120">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="14a8b-120">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a8b-121">LCASE</span><span class="sxs-lookup"><span data-stu-id="14a8b-121">LCASE</span></span></p></td>
<td><p><span data-ttu-id="14a8b-122">RIGHT</span><span class="sxs-lookup"><span data-stu-id="14a8b-122">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="14a8b-123">UCASE</span><span class="sxs-lookup"><span data-stu-id="14a8b-123">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a8b-124">LEFT</span><span class="sxs-lookup"><span data-stu-id="14a8b-124">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="14a8b-125">Funções numéricas</span><span class="sxs-lookup"><span data-stu-id="14a8b-125">Numeric Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14a8b-126">ABS</span><span class="sxs-lookup"><span data-stu-id="14a8b-126">ABS</span></span></p></td>
<td><p><span data-ttu-id="14a8b-127">FLOOR</span><span class="sxs-lookup"><span data-stu-id="14a8b-127">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="14a8b-128">SIN</span><span class="sxs-lookup"><span data-stu-id="14a8b-128">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a8b-129">ATAN</span><span class="sxs-lookup"><span data-stu-id="14a8b-129">ATAN</span></span></p></td>
<td><p><span data-ttu-id="14a8b-130">LOG</span><span class="sxs-lookup"><span data-stu-id="14a8b-130">LOG</span></span></p></td>
<td><p><span data-ttu-id="14a8b-131">SQRT</span><span class="sxs-lookup"><span data-stu-id="14a8b-131">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a8b-132">CEILING</span><span class="sxs-lookup"><span data-stu-id="14a8b-132">CEILING</span></span></p></td>
<td><p><span data-ttu-id="14a8b-133">POWER</span><span class="sxs-lookup"><span data-stu-id="14a8b-133">POWER</span></span></p></td>
<td><p><span data-ttu-id="14a8b-134">TAN</span><span class="sxs-lookup"><span data-stu-id="14a8b-134">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a8b-135">COS</span><span class="sxs-lookup"><span data-stu-id="14a8b-135">COS</span></span></p></td>
<td><p><span data-ttu-id="14a8b-136">RAND</span><span class="sxs-lookup"><span data-stu-id="14a8b-136">RAND</span></span></p></td>
<td><p><span data-ttu-id="14a8b-137">MOD</span><span class="sxs-lookup"><span data-stu-id="14a8b-137">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a8b-138">EXP</span><span class="sxs-lookup"><span data-stu-id="14a8b-138">EXP</span></span></p></td>
<td><p><span data-ttu-id="14a8b-139">SIGN</span><span class="sxs-lookup"><span data-stu-id="14a8b-139">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="14a8b-140">Funções de hora e data</span><span class="sxs-lookup"><span data-stu-id="14a8b-140">Time & Date Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14a8b-141">CURDATE</span><span class="sxs-lookup"><span data-stu-id="14a8b-141">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="14a8b-142">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="14a8b-142">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="14a8b-143">MONTH</span><span class="sxs-lookup"><span data-stu-id="14a8b-143">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a8b-144">CURTIME</span><span class="sxs-lookup"><span data-stu-id="14a8b-144">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="14a8b-145">YEAR</span><span class="sxs-lookup"><span data-stu-id="14a8b-145">YEAR</span></span></p></td>
<td><p><span data-ttu-id="14a8b-146">WEEK</span><span class="sxs-lookup"><span data-stu-id="14a8b-146">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a8b-147">NOW</span><span class="sxs-lookup"><span data-stu-id="14a8b-147">NOW</span></span></p></td>
<td><p><span data-ttu-id="14a8b-148">HOUR</span><span class="sxs-lookup"><span data-stu-id="14a8b-148">HOUR</span></span></p></td>
<td><p><span data-ttu-id="14a8b-149">QUARTER</span><span class="sxs-lookup"><span data-stu-id="14a8b-149">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a8b-150">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="14a8b-150">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="14a8b-151">MINUTE</span><span class="sxs-lookup"><span data-stu-id="14a8b-151">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="14a8b-152">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="14a8b-152">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a8b-153">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="14a8b-153">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="14a8b-154">SECOND</span><span class="sxs-lookup"><span data-stu-id="14a8b-154">SECOND</span></span></p></td>
<td><p><span data-ttu-id="14a8b-155">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="14a8b-155">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="14a8b-156">Conversão de tipo de dados</span><span class="sxs-lookup"><span data-stu-id="14a8b-156">Data Type Conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14a8b-157">CONVERT</span><span class="sxs-lookup"><span data-stu-id="14a8b-157">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="14a8b-158">Os literais de sequência podem ser convertidos para os seguintes tipos de dados: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR e SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="14a8b-158">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

