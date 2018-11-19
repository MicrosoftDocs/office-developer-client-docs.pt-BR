---
title: Funções escalares ODBC
TOCTitle: ODBC scalar functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4e841da9d401558311682f0abcbefde9161b71b3
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025991"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="8d916-102">Funções escalares ODBC</span><span class="sxs-lookup"><span data-stu-id="8d916-102">ODBC scalar functions</span></span>

<span data-ttu-id="8d916-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d916-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d916-104">O Microsoft Access SQL suporta o uso da sintaxe ODBC definidas para funções escalares.</span><span class="sxs-lookup"><span data-stu-id="8d916-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="8d916-105">Por exemplo, a consulta `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` retornaria todas as linhas em que o valor absoluto da alteração no preço de uma ação foi maior que cinco.</span><span class="sxs-lookup"><span data-stu-id="8d916-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="8d916-p101">Um subconjunto de funções escalares definidas por ODBC é aceito. A tabela a seguir lista as funções aceitas.</span><span class="sxs-lookup"><span data-stu-id="8d916-p101">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="8d916-108">Para obter uma descrição dos argumentos e uma explicação completa da sintaxe de eliminação para a inclusão de funções em uma instrução SQL, consulte a documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d916-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="8d916-109">Funções de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="8d916-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d916-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="8d916-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="8d916-111">LENGTH</span><span class="sxs-lookup"><span data-stu-id="8d916-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="8d916-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="8d916-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d916-113">CHAR</span><span class="sxs-lookup"><span data-stu-id="8d916-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="8d916-114">LOCATE</span><span class="sxs-lookup"><span data-stu-id="8d916-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="8d916-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="8d916-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d916-116">CONCAT</span><span class="sxs-lookup"><span data-stu-id="8d916-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="8d916-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="8d916-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="8d916-118">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="8d916-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d916-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="8d916-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="8d916-120">RIGHT</span><span class="sxs-lookup"><span data-stu-id="8d916-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="8d916-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="8d916-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d916-122">LEFT</span><span class="sxs-lookup"><span data-stu-id="8d916-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="8d916-123">Funções numéricas</span><span class="sxs-lookup"><span data-stu-id="8d916-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d916-124">ABS</span><span class="sxs-lookup"><span data-stu-id="8d916-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="8d916-125">FLOOR</span><span class="sxs-lookup"><span data-stu-id="8d916-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="8d916-126">SIN</span><span class="sxs-lookup"><span data-stu-id="8d916-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d916-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="8d916-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="8d916-128">LOG</span><span class="sxs-lookup"><span data-stu-id="8d916-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="8d916-129">SQRT</span><span class="sxs-lookup"><span data-stu-id="8d916-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d916-130">CEILING</span><span class="sxs-lookup"><span data-stu-id="8d916-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="8d916-131">POWER</span><span class="sxs-lookup"><span data-stu-id="8d916-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="8d916-132">TAN</span><span class="sxs-lookup"><span data-stu-id="8d916-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d916-133">COS</span><span class="sxs-lookup"><span data-stu-id="8d916-133">COS</span></span></p></td>
<td><p><span data-ttu-id="8d916-134">RAND</span><span class="sxs-lookup"><span data-stu-id="8d916-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="8d916-135">MOD</span><span class="sxs-lookup"><span data-stu-id="8d916-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d916-136">EXP</span><span class="sxs-lookup"><span data-stu-id="8d916-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="8d916-137">SIGN</span><span class="sxs-lookup"><span data-stu-id="8d916-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="8d916-138">Funções de data e hora</span><span class="sxs-lookup"><span data-stu-id="8d916-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d916-139">CURDATE</span><span class="sxs-lookup"><span data-stu-id="8d916-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="8d916-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="8d916-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="8d916-141">MONTH</span><span class="sxs-lookup"><span data-stu-id="8d916-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d916-142">CURTIME</span><span class="sxs-lookup"><span data-stu-id="8d916-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="8d916-143">YEAR</span><span class="sxs-lookup"><span data-stu-id="8d916-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="8d916-144">WEEK</span><span class="sxs-lookup"><span data-stu-id="8d916-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d916-145">NOW</span><span class="sxs-lookup"><span data-stu-id="8d916-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="8d916-146">HOUR</span><span class="sxs-lookup"><span data-stu-id="8d916-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="8d916-147">QUARTER</span><span class="sxs-lookup"><span data-stu-id="8d916-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d916-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="8d916-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="8d916-149">MINUTE</span><span class="sxs-lookup"><span data-stu-id="8d916-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="8d916-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="8d916-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d916-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="8d916-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="8d916-152">SECOND</span><span class="sxs-lookup"><span data-stu-id="8d916-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="8d916-153">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="8d916-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="8d916-154">Conversão de tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8d916-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d916-155">CONVERT</span><span class="sxs-lookup"><span data-stu-id="8d916-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="8d916-156">Os literais de sequência podem ser convertidos para os seguintes tipos de dados: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR e SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="8d916-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

