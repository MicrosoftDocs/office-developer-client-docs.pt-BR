---
title: Propriedade Field2.Type (DAO)
TOCTitle: Type Property
ms:assetid: 057d6ec9-b72c-cee6-005a-6d916e3dda29
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844921(v=office.15)
ms:contentKeyID: 48543032
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e1ebb10e2a9248ec38d49a874cf319c3120cd009
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876999"
---
# <a name="field2type-property-dao"></a><span data-ttu-id="a78c1-102">Propriedade Field2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="a78c1-102">Field2.Type Property (DAO)</span></span>


<span data-ttu-id="a78c1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a78c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a78c1-p101">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a78c1-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a78c1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a78c1-106">Syntax</span></span>

<span data-ttu-id="a78c1-107">*expressão* . Tipo</span><span class="sxs-lookup"><span data-stu-id="a78c1-107">*expression* .Type</span></span>

<span data-ttu-id="a78c1-108">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="a78c1-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a78c1-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a78c1-109">Remarks</span></span>

<span data-ttu-id="a78c1-p102">O valor de configuração ou de retorno é uma constante que indica um tipo operacional ou de dados. Para um objeto **Field2**, essa propriedade é de leitura/gravação até que o objeto seja acrescentado a uma coleção ou a outro objeto, depois ele se torna somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a78c1-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="a78c1-112">Para um objeto **Field2**, as configurações e valores de retorno possíveis são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a78c1-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a78c1-113">Constant</span><span class="sxs-lookup"><span data-stu-id="a78c1-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="a78c1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a78c1-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a78c1-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-116">Número inteiro grande</span><span class="sxs-lookup"><span data-stu-id="a78c1-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78c1-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-118">Binário</span><span class="sxs-lookup"><span data-stu-id="a78c1-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78c1-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="a78c1-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78c1-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-122">Byte</span><span class="sxs-lookup"><span data-stu-id="a78c1-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78c1-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-124">Caractere</span><span class="sxs-lookup"><span data-stu-id="a78c1-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78c1-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-126">Moeda</span><span class="sxs-lookup"><span data-stu-id="a78c1-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78c1-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-128">Data/Hora</span><span class="sxs-lookup"><span data-stu-id="a78c1-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78c1-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="a78c1-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78c1-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-132">Duplo</span><span class="sxs-lookup"><span data-stu-id="a78c1-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78c1-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-134">Flutuante</span><span class="sxs-lookup"><span data-stu-id="a78c1-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78c1-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-136">GUID</span><span class="sxs-lookup"><span data-stu-id="a78c1-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78c1-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-138">Inteiro</span><span class="sxs-lookup"><span data-stu-id="a78c1-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78c1-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-140">Long</span><span class="sxs-lookup"><span data-stu-id="a78c1-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78c1-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-142">Long Binary (Objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="a78c1-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78c1-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-144">Memorando</span><span class="sxs-lookup"><span data-stu-id="a78c1-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78c1-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-146">Numeric</span><span class="sxs-lookup"><span data-stu-id="a78c1-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78c1-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-148">Single</span><span class="sxs-lookup"><span data-stu-id="a78c1-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78c1-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-150">Texto</span><span class="sxs-lookup"><span data-stu-id="a78c1-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78c1-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-152">Time</span><span class="sxs-lookup"><span data-stu-id="a78c1-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78c1-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-154">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="a78c1-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78c1-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a78c1-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a78c1-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="a78c1-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a78c1-157">Quando você acrescenta um novo objeto **Field2**, **Parameter** ou **Property** a uma coleção de um objeto **Index**, **QueryDef**, **Recordset** ou **TableDef**, ocorre um erro se o banco de dados base não aceitar o tipo de dados especificado para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="a78c1-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

