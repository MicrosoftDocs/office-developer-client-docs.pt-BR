---
title: Propriedade Property.Type (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c52f03d0e2fc541cb15397d0c924859cd31ccb17
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465464"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="b06e0-102">Propriedade Property.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="b06e0-102">Property.Type Property (DAO)</span></span>


<span data-ttu-id="b06e0-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b06e0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b06e0-p101">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b06e0-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b06e0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b06e0-106">Syntax</span></span>

<span data-ttu-id="b06e0-107">*expressão* . Tipo</span><span class="sxs-lookup"><span data-stu-id="b06e0-107">*expression* .Type</span></span>

<span data-ttu-id="b06e0-108">*expressão* Uma variável que representa um objeto **Property** .</span><span class="sxs-lookup"><span data-stu-id="b06e0-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b06e0-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b06e0-109">Remarks</span></span>

<span data-ttu-id="b06e0-p102">A configuração ou o valor de retorno é uma constante que indica um tipo operacional ou de dados. Para um objeto **[Property](property-object-dao.md)**, essa propriedade será leitura/gravação até que o objeto seja acrescentando a uma coleção ou a outro objeto. Depois disso, se tornará somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b06e0-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="b06e0-112">Para um objeto **Property**, as configurações e os valores de retorno possíveis são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b06e0-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b06e0-113">Constant</span><span class="sxs-lookup"><span data-stu-id="b06e0-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="b06e0-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b06e0-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b06e0-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-116">Número inteiro grande</span><span class="sxs-lookup"><span data-stu-id="b06e0-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b06e0-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-118">Binário</span><span class="sxs-lookup"><span data-stu-id="b06e0-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b06e0-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="b06e0-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b06e0-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-122">Byte</span><span class="sxs-lookup"><span data-stu-id="b06e0-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b06e0-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-124">Caractere</span><span class="sxs-lookup"><span data-stu-id="b06e0-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b06e0-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-126">Moeda</span><span class="sxs-lookup"><span data-stu-id="b06e0-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b06e0-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-128">Data/Hora</span><span class="sxs-lookup"><span data-stu-id="b06e0-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b06e0-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="b06e0-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b06e0-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-132">Duplo</span><span class="sxs-lookup"><span data-stu-id="b06e0-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b06e0-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-134">Flutuante</span><span class="sxs-lookup"><span data-stu-id="b06e0-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b06e0-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-136">GUID</span><span class="sxs-lookup"><span data-stu-id="b06e0-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b06e0-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-138">Inteiro</span><span class="sxs-lookup"><span data-stu-id="b06e0-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b06e0-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-140">Long</span><span class="sxs-lookup"><span data-stu-id="b06e0-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b06e0-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-142">Long Binary (Objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="b06e0-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b06e0-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-144">Memorando</span><span class="sxs-lookup"><span data-stu-id="b06e0-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b06e0-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-146">Numeric</span><span class="sxs-lookup"><span data-stu-id="b06e0-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b06e0-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-148">Single</span><span class="sxs-lookup"><span data-stu-id="b06e0-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b06e0-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-150">Texto</span><span class="sxs-lookup"><span data-stu-id="b06e0-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b06e0-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-152">Time</span><span class="sxs-lookup"><span data-stu-id="b06e0-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b06e0-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-154">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="b06e0-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b06e0-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="b06e0-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="b06e0-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="b06e0-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b06e0-157">Quando você acrescentar um novo objeto **Field**, **Parameter** ou **Property** à coleção de um objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, ocorrerá um erro, caso o banco de dados base não ofereça suporte ao tipo de dados especificado para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="b06e0-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

