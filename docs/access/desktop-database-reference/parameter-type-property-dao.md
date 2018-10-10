---
title: Propriedade Parameter.Type (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a1efe394193b9f8e74c02ecb71758d94fac9259a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462558"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="d55c2-102">Propriedade Parameter.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="d55c2-102">Parameter.Type Property (DAO)</span></span>


<span data-ttu-id="d55c2-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d55c2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d55c2-p101">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d55c2-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d55c2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d55c2-106">Syntax</span></span>

<span data-ttu-id="d55c2-107">*expressão* . Tipo</span><span class="sxs-lookup"><span data-stu-id="d55c2-107">*expression* .Type</span></span>

<span data-ttu-id="d55c2-108">*expressão* Uma variável que representa um objeto **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="d55c2-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d55c2-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d55c2-109">Remarks</span></span>

<span data-ttu-id="d55c2-p102">A configuração ou o valor de retorno é uma constante que indica um tipo operacional ou de dados. Para um objeto **[Parameter](parameter-object-dao.md)** em um espaço de trabalho do Microsoft Access, a propriedade será somente leitura; enquanto em um espaço de trabalho ODBCDirect, a propriedade será sempre de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d55c2-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="d55c2-112">Para um objeto **Parameter**, as configurações e os valores de retorno possíveis são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d55c2-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d55c2-113">Constant</span><span class="sxs-lookup"><span data-stu-id="d55c2-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="d55c2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d55c2-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d55c2-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-116">Número inteiro grande</span><span class="sxs-lookup"><span data-stu-id="d55c2-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d55c2-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-118">Binário</span><span class="sxs-lookup"><span data-stu-id="d55c2-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d55c2-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="d55c2-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d55c2-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-122">Byte</span><span class="sxs-lookup"><span data-stu-id="d55c2-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d55c2-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-124">Caractere</span><span class="sxs-lookup"><span data-stu-id="d55c2-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d55c2-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-126">Moeda</span><span class="sxs-lookup"><span data-stu-id="d55c2-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d55c2-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-128">Data/Hora</span><span class="sxs-lookup"><span data-stu-id="d55c2-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d55c2-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="d55c2-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d55c2-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-132">Duplo</span><span class="sxs-lookup"><span data-stu-id="d55c2-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d55c2-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-134">Flutuante</span><span class="sxs-lookup"><span data-stu-id="d55c2-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d55c2-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-136">GUID</span><span class="sxs-lookup"><span data-stu-id="d55c2-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d55c2-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-138">Inteiro</span><span class="sxs-lookup"><span data-stu-id="d55c2-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d55c2-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-140">Long</span><span class="sxs-lookup"><span data-stu-id="d55c2-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d55c2-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-142">Long Binary (Objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="d55c2-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d55c2-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-144">Memorando</span><span class="sxs-lookup"><span data-stu-id="d55c2-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d55c2-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-146">Numeric</span><span class="sxs-lookup"><span data-stu-id="d55c2-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d55c2-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-148">Single</span><span class="sxs-lookup"><span data-stu-id="d55c2-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d55c2-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-150">Texto</span><span class="sxs-lookup"><span data-stu-id="d55c2-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d55c2-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-152">Time</span><span class="sxs-lookup"><span data-stu-id="d55c2-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d55c2-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-154">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="d55c2-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d55c2-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d55c2-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d55c2-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="d55c2-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d55c2-157">Quando você acrescentar um novo objeto **Field**, **Parameter** ou **Property** à coleção de um objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, ocorrerá um erro, caso o banco de dados base não ofereça suporte ao tipo de dados especificado para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="d55c2-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

