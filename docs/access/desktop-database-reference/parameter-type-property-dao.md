---
title: Propriedade Parameter.Type (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 294d61ba964958d7933a68919df940cb7501ec0d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927029"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="a63a5-102">Propriedade Parameter.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="a63a5-102">Parameter.Type property (DAO)</span></span>


<span data-ttu-id="a63a5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a63a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a63a5-p101">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a63a5-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a63a5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a63a5-106">Syntax</span></span>

<span data-ttu-id="a63a5-107">*expressão* . Tipo</span><span class="sxs-lookup"><span data-stu-id="a63a5-107">*expression* .Type</span></span>

<span data-ttu-id="a63a5-108">*expressão* Uma variável que representa um objeto **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="a63a5-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a63a5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a63a5-109">Remarks</span></span>

<span data-ttu-id="a63a5-p102">A configuração ou o valor de retorno é uma constante que indica um tipo operacional ou de dados. Para um objeto **[Parameter](parameter-object-dao.md)** em um espaço de trabalho do Microsoft Access, a propriedade será somente leitura; enquanto em um espaço de trabalho ODBCDirect, a propriedade será sempre de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a63a5-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="a63a5-112">Para um objeto **Parameter**, as configurações e os valores de retorno possíveis são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a63a5-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a63a5-113">Constant</span><span class="sxs-lookup"><span data-stu-id="a63a5-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="a63a5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a63a5-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a63a5-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-116">Número inteiro grande</span><span class="sxs-lookup"><span data-stu-id="a63a5-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a63a5-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-118">Binário</span><span class="sxs-lookup"><span data-stu-id="a63a5-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a63a5-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="a63a5-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a63a5-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-122">Byte</span><span class="sxs-lookup"><span data-stu-id="a63a5-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a63a5-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-124">Caractere</span><span class="sxs-lookup"><span data-stu-id="a63a5-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a63a5-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-126">Moeda</span><span class="sxs-lookup"><span data-stu-id="a63a5-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a63a5-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-128">Data/Hora</span><span class="sxs-lookup"><span data-stu-id="a63a5-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a63a5-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="a63a5-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a63a5-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-132">Duplo</span><span class="sxs-lookup"><span data-stu-id="a63a5-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a63a5-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-134">Flutuante</span><span class="sxs-lookup"><span data-stu-id="a63a5-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a63a5-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-136">GUID</span><span class="sxs-lookup"><span data-stu-id="a63a5-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a63a5-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-138">Inteiro</span><span class="sxs-lookup"><span data-stu-id="a63a5-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a63a5-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-140">Long</span><span class="sxs-lookup"><span data-stu-id="a63a5-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a63a5-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-142">Long Binary (Objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="a63a5-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a63a5-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-144">Memorando</span><span class="sxs-lookup"><span data-stu-id="a63a5-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a63a5-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-146">Numeric</span><span class="sxs-lookup"><span data-stu-id="a63a5-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a63a5-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-148">Single</span><span class="sxs-lookup"><span data-stu-id="a63a5-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a63a5-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-150">Texto</span><span class="sxs-lookup"><span data-stu-id="a63a5-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a63a5-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-152">Time</span><span class="sxs-lookup"><span data-stu-id="a63a5-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a63a5-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-154">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="a63a5-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a63a5-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a63a5-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a63a5-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="a63a5-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a63a5-157">Quando você acrescentar um novo objeto **Field**, **Parameter** ou **Property** à coleção de um objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, ocorrerá um erro, caso o banco de dados base não ofereça suporte ao tipo de dados especificado para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="a63a5-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

