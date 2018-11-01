---
title: Propriedade Property.Type (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15a1ac18a504a723948b8f1539c1bf002cf9833a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888143"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="5bd1d-102">Propriedade Property.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="5bd1d-102">Property.Type Property (DAO)</span></span>


<span data-ttu-id="5bd1d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5bd1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5bd1d-p101">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd1d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bd1d-106">Syntax</span></span>

<span data-ttu-id="5bd1d-107">*expressão* . Tipo</span><span class="sxs-lookup"><span data-stu-id="5bd1d-107">*expression* .Type</span></span>

<span data-ttu-id="5bd1d-108">*expressão* Uma variável que representa um objeto **Property** .</span><span class="sxs-lookup"><span data-stu-id="5bd1d-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd1d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bd1d-109">Remarks</span></span>

<span data-ttu-id="5bd1d-p102">A configuração ou o valor de retorno é uma constante que indica um tipo operacional ou de dados. Para um objeto **[Property](property-object-dao.md)**, essa propriedade será leitura/gravação até que o objeto seja acrescentando a uma coleção ou a outro objeto. Depois disso, se tornará somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="5bd1d-112">Para um objeto **Property**, as configurações e os valores de retorno possíveis são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5bd1d-113">Constant</span><span class="sxs-lookup"><span data-stu-id="5bd1d-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="5bd1d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bd1d-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5bd1d-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-116">Número inteiro grande</span><span class="sxs-lookup"><span data-stu-id="5bd1d-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd1d-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-118">Binário</span><span class="sxs-lookup"><span data-stu-id="5bd1d-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd1d-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="5bd1d-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd1d-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-122">Byte</span><span class="sxs-lookup"><span data-stu-id="5bd1d-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd1d-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-124">Caractere</span><span class="sxs-lookup"><span data-stu-id="5bd1d-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd1d-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-126">Moeda</span><span class="sxs-lookup"><span data-stu-id="5bd1d-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd1d-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-128">Data/Hora</span><span class="sxs-lookup"><span data-stu-id="5bd1d-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd1d-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="5bd1d-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd1d-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-132">Duplo</span><span class="sxs-lookup"><span data-stu-id="5bd1d-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd1d-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-134">Flutuante</span><span class="sxs-lookup"><span data-stu-id="5bd1d-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd1d-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-136">GUID</span><span class="sxs-lookup"><span data-stu-id="5bd1d-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd1d-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-138">Inteiro</span><span class="sxs-lookup"><span data-stu-id="5bd1d-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd1d-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-140">Long</span><span class="sxs-lookup"><span data-stu-id="5bd1d-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd1d-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-142">Long Binary (Objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="5bd1d-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd1d-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-144">Memorando</span><span class="sxs-lookup"><span data-stu-id="5bd1d-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd1d-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-146">Numeric</span><span class="sxs-lookup"><span data-stu-id="5bd1d-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd1d-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-148">Single</span><span class="sxs-lookup"><span data-stu-id="5bd1d-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd1d-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-150">Texto</span><span class="sxs-lookup"><span data-stu-id="5bd1d-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd1d-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-152">Time</span><span class="sxs-lookup"><span data-stu-id="5bd1d-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bd1d-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-154">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="5bd1d-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bd1d-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="5bd1d-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5bd1d-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="5bd1d-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5bd1d-157">Quando você acrescentar um novo objeto **Field**, **Parameter** ou **Property** à coleção de um objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, ocorrerá um erro, caso o banco de dados base não ofereça suporte ao tipo de dados especificado para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

