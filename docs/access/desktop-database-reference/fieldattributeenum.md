---
title: FieldAttributeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 4a99bf18207b6bd1744fb0ee2b1a2dc10254c604
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874381"
---
# <a name="fieldattributeenum"></a><span data-ttu-id="6fb7c-102">FieldAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="6fb7c-102">FieldAttributeEnum</span></span>

<span data-ttu-id="6fb7c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fb7c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6fb7c-104">Especifica um ou mais atributos de um objeto [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6fb7c-104">Specifies one or more attributes of a [Field](field-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6fb7c-105">Constant</span><span class="sxs-lookup"><span data-stu-id="6fb7c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6fb7c-106">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb7c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6fb7c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fb7c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-108"><strong>adFldCacheDeferred</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-108"><strong>adFldCacheDeferred</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="6fb7c-109">0x1000</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-110">Indica que o provedor armazena os valores do campo e que as leituras subsequentes são feitas do cache.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-110">Indicates that the provider caches field values and that subsequent reads are done from the cache.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-111"><strong>adFldFixed</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-111"><strong>adFldFixed</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-112">0x10</span><span class="sxs-lookup"><span data-stu-id="6fb7c-112">0x10</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-113">Indica que o campo contém dados com tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-113">Indicates that the field contains fixed-length data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-114"><strong>adFldIsChapter</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-114"><strong>adFldIsChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="6fb7c-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-p101">Indica que o campo contém um valor de capítulo que especifica um recordset filho para esse campo pai. Normalmente os campos de capítulo são usados com data shaping ou filtros.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-p101">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field. Typically chapter fields are used with data shaping or filters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-118"><strong>adFldIsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-118"><strong>adFldIsCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-119">0x40000</span><span class="sxs-lookup"><span data-stu-id="6fb7c-119">0x40000</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-120">Indica que o campo especifica que o recurso representado pelo registro é uma coleção de outros recursos, como pasta, em vez de um recurso simples, como arquivo de texto.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-120">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-121"><strong>adFldIsDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-121"><strong>adFldIsDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-122">0x20000</span><span class="sxs-lookup"><span data-stu-id="6fb7c-122">0x20000</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-123">Indica que o campo contém um fluxo padrão para o recurso representado pelo record.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-123">Indicates that the field contains the default stream for the resource represented by the record.</span></span> <span data-ttu-id="6fb7c-124">Por exemplo, um fluxo padrão pode ser o conteúdo HTML de uma pasta raiz de um site que sejam atendida automaticamente quando a URL raiz é especificada.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-124">For example, the default stream can be the HTML content of a root folder on a website, which is automatically served when the root URL is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-125"><strong>adFldIsNullable</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-125"><strong>adFldIsNullable</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-126">0x20</span><span class="sxs-lookup"><span data-stu-id="6fb7c-126">0x20</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-127">Indica que o campo aceita os valores nulos.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-127">Indicates that the field accepts null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-128"><strong>adFldIsRowURL</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-128"><strong>adFldIsRowURL</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-129">0x10000</span><span class="sxs-lookup"><span data-stu-id="6fb7c-129">0x10000</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-130">Indica que o campo contém a URL que nomeia o recurso do repositório de dados representado pelo registro.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-130">Indicates that the field contains the URL that names the resource from the data store represented by the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-131"><strong>adFldLong</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-131"><strong>adFldLong</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-132">0x80</span><span class="sxs-lookup"><span data-stu-id="6fb7c-132">0x80</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-p103">Indica que o campo é campo binário longo. Além disso, indica que você pode utilizar os métodos <a href="appendchunk-method-ado.md">AppendChunk</a> e <a href="getchunk-method-ado.md">GetChunk</a>.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-p103">Indicates that the field is a long binary field. Also indicates that you can use the <a href="appendchunk-method-ado.md">AppendChunk</a> and <a href="getchunk-method-ado.md">GetChunk</a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-135"><strong>adFldMayBeNull</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-135"><strong>adFldMayBeNull</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-136">0x40</span><span class="sxs-lookup"><span data-stu-id="6fb7c-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-137">Indica que você pode ler valores nulos do campo.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-137">Indicates that you can read null values from the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-138"><strong>adFldMayDefer</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-138"><strong>adFldMayDefer</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-139">0x2</span><span class="sxs-lookup"><span data-stu-id="6fb7c-139">0x2</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-140">Indica que o campo é adiado — isto é, os valores do campo não são recuperados da fonte de dados com todo o registro, mas somente quando você os acessa explicitamente.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-140">Indicates that the field is deferred — that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-141"><strong>adFldNegativeScale</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-141"><strong>adFldNegativeScale</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="6fb7c-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-p104">Indica que o campo representa um valor numérico de uma coluna que permite valores de escala negativos. A escala é especificada pela propriedade <a href="numericscale-property-ado.md">NumericScale</a>.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-p104">Indicates that the field represents a numeric value from a column that supports negative scale values. The scale is specified by the <a href="numericscale-property-ado.md">NumericScale</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-145"><strong>adFldRowID</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-145"><strong>adFldRowID</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-146">0x100</span><span class="sxs-lookup"><span data-stu-id="6fb7c-146">0x100</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-147">Indica que o campo contém um identificador de linha persistente que não pode ser escrito e não tem nenhum valor significativo exceto o de identificar a linha (como um número de registro, identificador exclusivo e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="6fb7c-147">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-148"><strong>adFldRowVersion</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-148"><strong>adFldRowVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-149">0x200</span><span class="sxs-lookup"><span data-stu-id="6fb7c-149">0x200</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-150">Indica que o campo contém algum tipo de marcação de data e hora utilizada para controlar as atualizações.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-150">Indicates that the field contains some kind of time or date stamp used to track updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-151"><strong>adFldUnknownUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-151"><strong>adFldUnknownUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-152">0x8</span><span class="sxs-lookup"><span data-stu-id="6fb7c-152">0x8</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-153">Indica que o provedor não pode determinar se você pode escrever no campo.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-153">Indicates that the provider cannot determine if you can write to the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-154"><strong>adFldUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-154"><strong>adFldUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-155">-1</span><span class="sxs-lookup"><span data-stu-id="6fb7c-155">-1</span></span><br />
<span data-ttu-id="6fb7c-156">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="6fb7c-156">0xFFFFFFFF</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-157">Indica que o provedor não especifica atributos de campo.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-157">Indicates that the provider does not specify the field attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-158"><strong>adFldUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="6fb7c-158"><strong>adFldUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="6fb7c-159">0x4</span><span class="sxs-lookup"><span data-stu-id="6fb7c-159">0x4</span></span></p></td>
<td><p><span data-ttu-id="6fb7c-160">Indica que você pode escrever no campo.</span><span class="sxs-lookup"><span data-stu-id="6fb7c-160">Indicates that you can write to the field.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="6fb7c-161">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="6fb7c-161">ADO/WFC equivalent</span></span>

<span data-ttu-id="6fb7c-162">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6fb7c-162">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6fb7c-163">Constante</span><span class="sxs-lookup"><span data-stu-id="6fb7c-163">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="6fb7c-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-165">AdoEnums.FieldAttribute.FIXED</span><span class="sxs-lookup"><span data-stu-id="6fb7c-165">AdoEnums.FieldAttribute.FIXED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-166">AdoEnums.FieldAttribute.ISNULLABLE</span><span class="sxs-lookup"><span data-stu-id="6fb7c-166">AdoEnums.FieldAttribute.ISNULLABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-167">AdoEnums.FieldAttribute.LONG</span><span class="sxs-lookup"><span data-stu-id="6fb7c-167">AdoEnums.FieldAttribute.LONG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-168">AdoEnums.FieldAttribute.MAYBENULL</span><span class="sxs-lookup"><span data-stu-id="6fb7c-168">AdoEnums.FieldAttribute.MAYBENULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-169">AdoEnums.FieldAttribute.MAYDEFER</span><span class="sxs-lookup"><span data-stu-id="6fb7c-169">AdoEnums.FieldAttribute.MAYDEFER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span><span class="sxs-lookup"><span data-stu-id="6fb7c-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-171">AdoEnums.FieldAttribute.ROWID</span><span class="sxs-lookup"><span data-stu-id="6fb7c-171">AdoEnums.FieldAttribute.ROWID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-172">AdoEnums.FieldAttribute.ROWVERSION</span><span class="sxs-lookup"><span data-stu-id="6fb7c-172">AdoEnums.FieldAttribute.ROWVERSION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span><span class="sxs-lookup"><span data-stu-id="6fb7c-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fb7c-174">AdoEnums.FieldAttribute.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="6fb7c-174">AdoEnums.FieldAttribute.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fb7c-175">AdoEnums.FieldAttribute.UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="6fb7c-175">AdoEnums.FieldAttribute.UPDATABLE</span></span></p></td>
</tr>
</tbody>
</table>

