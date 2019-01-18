---
title: Propriedade Field.Type (DAO)
TOCTitle: Type Property
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c8f212c5e1f10f4270987c9453802575d88cebfa
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709478"
---
# <a name="fieldtype-property-dao"></a><span data-ttu-id="d196c-102">Propriedade Field.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="d196c-102">Field.Type property (DAO)</span></span>


<span data-ttu-id="d196c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d196c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d196c-p101">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d196c-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d196c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d196c-106">Syntax</span></span>

<span data-ttu-id="d196c-107">*expressão* . Tipo</span><span class="sxs-lookup"><span data-stu-id="d196c-107">*expression* .Type</span></span>

<span data-ttu-id="d196c-108">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="d196c-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d196c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d196c-109">Remarks</span></span>

<span data-ttu-id="d196c-p102">A configuração ou o valor de retorno é uma constante que indica um tipo operacional ou de dados. Para um objeto **Field**, essa propriedade será leitura/gravação até que o objeto seja acrescentado a uma coleção ou a outro objeto. Depois disso o objeto se tornará somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d196c-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="d196c-112">Para um objeto **Field**, as configurações e os valores de retorno possíveis são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d196c-112">For a **Field** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d196c-113">Constant</span><span class="sxs-lookup"><span data-stu-id="d196c-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="d196c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d196c-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d196c-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-116">Número inteiro grande</span><span class="sxs-lookup"><span data-stu-id="d196c-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d196c-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-118">Binária</span><span class="sxs-lookup"><span data-stu-id="d196c-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d196c-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-120">Booliano</span><span class="sxs-lookup"><span data-stu-id="d196c-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d196c-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-122">Byte</span><span class="sxs-lookup"><span data-stu-id="d196c-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d196c-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-124">Caractere</span><span class="sxs-lookup"><span data-stu-id="d196c-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d196c-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-126">Moeda</span><span class="sxs-lookup"><span data-stu-id="d196c-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d196c-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-128">Data/Hora</span><span class="sxs-lookup"><span data-stu-id="d196c-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d196c-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="d196c-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d196c-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-132">Duplo</span><span class="sxs-lookup"><span data-stu-id="d196c-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d196c-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-134">Flutuante</span><span class="sxs-lookup"><span data-stu-id="d196c-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d196c-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-136">GUID</span><span class="sxs-lookup"><span data-stu-id="d196c-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d196c-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-138">Inteiro</span><span class="sxs-lookup"><span data-stu-id="d196c-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d196c-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-140">Long</span><span class="sxs-lookup"><span data-stu-id="d196c-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d196c-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-142">Long Binary (Objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="d196c-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d196c-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-144">Memorando</span><span class="sxs-lookup"><span data-stu-id="d196c-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d196c-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-146">Numeric</span><span class="sxs-lookup"><span data-stu-id="d196c-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d196c-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-148">Single</span><span class="sxs-lookup"><span data-stu-id="d196c-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d196c-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-150">Texto</span><span class="sxs-lookup"><span data-stu-id="d196c-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d196c-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-152">Time</span><span class="sxs-lookup"><span data-stu-id="d196c-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d196c-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-154">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="d196c-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d196c-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d196c-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d196c-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="d196c-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d196c-157">Quando você acrescentar um novo objeto **Field**, **Parameter** ou **Property** à coleção de um objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, ocorrerá um erro, caso o banco de dados base não ofereça suporte ao tipo de dados especificado para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="d196c-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

