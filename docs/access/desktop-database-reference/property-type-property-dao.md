---
title: Propriedade Property. Type (DAO)
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
# <a name="propertytype-property-dao"></a><span data-ttu-id="77303-102">Propriedade Property. Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="77303-102">Property.Type property (DAO)</span></span>


<span data-ttu-id="77303-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77303-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77303-104">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto.</span><span class="sxs-lookup"><span data-stu-id="77303-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="77303-105">**Integer** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="77303-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="77303-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77303-106">Syntax</span></span>

<span data-ttu-id="77303-107">*expressão* . Escreva</span><span class="sxs-lookup"><span data-stu-id="77303-107">*expression* .Type</span></span>

<span data-ttu-id="77303-108">*expressão* Uma variável que representa um objeto **Property** .</span><span class="sxs-lookup"><span data-stu-id="77303-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="77303-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="77303-109">Remarks</span></span>

<span data-ttu-id="77303-p102">A configuração ou o valor de retorno é uma constante que indica um tipo operacional ou de dados. Para um objeto **[Property](property-object-dao.md)**, essa propriedade será leitura/gravação até que o objeto seja acrescentando a uma coleção ou a outro objeto. Depois disso, se tornará somente leitura.</span><span class="sxs-lookup"><span data-stu-id="77303-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="77303-112">Para um objeto **Property**, as configurações e os valores de retorno possíveis são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="77303-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77303-113">Constante</span><span class="sxs-lookup"><span data-stu-id="77303-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="77303-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="77303-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77303-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="77303-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-116">Número inteiro grande</span><span class="sxs-lookup"><span data-stu-id="77303-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77303-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="77303-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-118">Binary</span><span class="sxs-lookup"><span data-stu-id="77303-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77303-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="77303-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-120">Booliano</span><span class="sxs-lookup"><span data-stu-id="77303-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77303-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="77303-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-122">Byte</span><span class="sxs-lookup"><span data-stu-id="77303-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77303-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="77303-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-124">Char</span><span class="sxs-lookup"><span data-stu-id="77303-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77303-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="77303-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-126">Moeda</span><span class="sxs-lookup"><span data-stu-id="77303-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77303-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="77303-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-128">Data/Hora</span><span class="sxs-lookup"><span data-stu-id="77303-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77303-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="77303-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="77303-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77303-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="77303-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-132">Duplo</span><span class="sxs-lookup"><span data-stu-id="77303-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77303-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="77303-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-134">Ponto</span><span class="sxs-lookup"><span data-stu-id="77303-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77303-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="77303-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-136">GUID</span><span class="sxs-lookup"><span data-stu-id="77303-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77303-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="77303-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-138">Inteiro</span><span class="sxs-lookup"><span data-stu-id="77303-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77303-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="77303-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-140">Long</span><span class="sxs-lookup"><span data-stu-id="77303-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77303-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="77303-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-142">Long Binary (Objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="77303-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77303-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="77303-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-144">Memorando</span><span class="sxs-lookup"><span data-stu-id="77303-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77303-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="77303-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-146">Numeric</span><span class="sxs-lookup"><span data-stu-id="77303-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77303-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="77303-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-148">Único</span><span class="sxs-lookup"><span data-stu-id="77303-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77303-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="77303-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-150">Texto</span><span class="sxs-lookup"><span data-stu-id="77303-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77303-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="77303-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-152">Hora</span><span class="sxs-lookup"><span data-stu-id="77303-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77303-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="77303-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-154">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="77303-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77303-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="77303-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="77303-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="77303-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77303-157">Quando você acrescentar um novo objeto **Field**, **Parameter** ou **Property** à coleção de um objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, ocorrerá um erro, caso o banco de dados base não ofereça suporte ao tipo de dados especificado para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="77303-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

