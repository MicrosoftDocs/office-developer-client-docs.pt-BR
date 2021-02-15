---
title: Propriedade Property.Type (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4280b89102e06b2ecc09a783840e671b0af9ff73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302895"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="65401-102">Propriedade Property.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="65401-102">Property.Type property (DAO)</span></span>


<span data-ttu-id="65401-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65401-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65401-104">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto.</span><span class="sxs-lookup"><span data-stu-id="65401-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="65401-105">**número inteiro** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="65401-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="65401-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65401-106">Syntax</span></span>

<span data-ttu-id="65401-107">*expressão* .Type</span><span class="sxs-lookup"><span data-stu-id="65401-107">*expression* .Type</span></span>

<span data-ttu-id="65401-108">*expressão* Uma variável que representa um **objeto Property** .</span><span class="sxs-lookup"><span data-stu-id="65401-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="65401-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="65401-109">Remarks</span></span>

<span data-ttu-id="65401-p102">A configuração ou o valor de retorno é uma constante que indica um tipo operacional ou de dados. Para um objeto **[Property](property-object-dao.md)**, essa propriedade será leitura/gravação até que o objeto seja acrescentando a uma coleção ou a outro objeto. Depois disso, se tornará somente leitura.</span><span class="sxs-lookup"><span data-stu-id="65401-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="65401-112">Para um objeto **Property**, as configurações e os valores de retorno possíveis são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="65401-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65401-113">Constante</span><span class="sxs-lookup"><span data-stu-id="65401-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="65401-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="65401-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65401-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="65401-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-116">Número inteiro grande</span><span class="sxs-lookup"><span data-stu-id="65401-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65401-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="65401-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-118">Binário</span><span class="sxs-lookup"><span data-stu-id="65401-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65401-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="65401-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-120">Booliano</span><span class="sxs-lookup"><span data-stu-id="65401-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65401-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="65401-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-122">Byte</span><span class="sxs-lookup"><span data-stu-id="65401-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65401-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="65401-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-124">Char</span><span class="sxs-lookup"><span data-stu-id="65401-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65401-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="65401-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-126">Moeda</span><span class="sxs-lookup"><span data-stu-id="65401-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65401-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="65401-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-128">Data/Hora</span><span class="sxs-lookup"><span data-stu-id="65401-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65401-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="65401-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="65401-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65401-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="65401-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-132">Duplo</span><span class="sxs-lookup"><span data-stu-id="65401-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65401-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="65401-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-134">Flutuação</span><span class="sxs-lookup"><span data-stu-id="65401-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65401-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="65401-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-136">GUID</span><span class="sxs-lookup"><span data-stu-id="65401-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65401-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="65401-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-138">Inteiro</span><span class="sxs-lookup"><span data-stu-id="65401-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65401-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="65401-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-140">Longo</span><span class="sxs-lookup"><span data-stu-id="65401-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65401-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="65401-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-142">Long Binary (Objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="65401-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65401-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="65401-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-144">Memorando</span><span class="sxs-lookup"><span data-stu-id="65401-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65401-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="65401-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-146">Numérico</span><span class="sxs-lookup"><span data-stu-id="65401-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65401-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="65401-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-148">Único</span><span class="sxs-lookup"><span data-stu-id="65401-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65401-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="65401-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-150">Texto</span><span class="sxs-lookup"><span data-stu-id="65401-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65401-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="65401-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-152">Hora</span><span class="sxs-lookup"><span data-stu-id="65401-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65401-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="65401-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-154">Carimbo de Data/Hora</span><span class="sxs-lookup"><span data-stu-id="65401-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65401-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="65401-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="65401-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="65401-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65401-157">Quando você acrescentar um novo objeto **Field**, **Parameter** ou **Property** à coleção de um objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, ocorrerá um erro, caso o banco de dados base não ofereça suporte ao tipo de dados especificado para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="65401-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

