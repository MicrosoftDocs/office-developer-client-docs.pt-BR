---
title: DataTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f5c192589f2c90b2ce7b6c7b376b80c92b341e2d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860655"
---
# <a name="datatypeenum"></a><span data-ttu-id="dc76b-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="dc76b-102">DataTypeEnum</span></span>

<span data-ttu-id="dc76b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc76b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dc76b-p101">Especifica o tipo de dados de [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) ou [Property](property-object-ado.md). O indicador de tipo OLE DB correspondente é mostrado entre parênteses na coluna descrição da tabela a seguir. Para obter mais informações sobre os tipos de dados OLE DB, consulte o Capítulo 13 e o Apêndice A do manual *OLE DB Programmer's Reference (Referências para o programador de OLE DB)*.</span><span class="sxs-lookup"><span data-stu-id="dc76b-p101">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md). The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc76b-107">Constant</span><span class="sxs-lookup"><span data-stu-id="dc76b-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="dc76b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="dc76b-108">Value</span></span></p></th>
<th><p><span data-ttu-id="dc76b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc76b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="dc76b-110"><strong>AdArray</span></span><br /><span data-ttu-id="dc76b-111">
</strong>(Não se aplica ao ADOX.)</span><span class="sxs-lookup"><span data-stu-id="dc76b-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="dc76b-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="dc76b-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="dc76b-113">Um valor de sinalizador sempre combinado a outra constante de tipo de dados, indicando uma matriz desse outro tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dc76b-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-115">20</span><span class="sxs-lookup"><span data-stu-id="dc76b-115">20</span></span></p></td>
<td><p><span data-ttu-id="dc76b-116">Indica um inteiro assinado de oito bytes (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="dc76b-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-118">128</span><span class="sxs-lookup"><span data-stu-id="dc76b-118">128</span></span></p></td>
<td><p><span data-ttu-id="dc76b-119">Indica um valor binário (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="dc76b-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-121">11</span><span class="sxs-lookup"><span data-stu-id="dc76b-121">11</span></span></p></td>
<td><p><span data-ttu-id="dc76b-122">Indica um valor booliano (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="dc76b-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-124">8</span><span class="sxs-lookup"><span data-stu-id="dc76b-124">8</span></span></p></td>
<td><p><span data-ttu-id="dc76b-125">Indica uma cadeia de caracteres terminada em nulo (Unicode) (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="dc76b-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-127">136</span><span class="sxs-lookup"><span data-stu-id="dc76b-127">136</span></span></p></td>
<td><p><span data-ttu-id="dc76b-128">Indica um valor de capítulo de quatro bytes que identifica linhas em um conjunto de linhas filho (DBTYPE_HCHAPTER).</span><span class="sxs-lookup"><span data-stu-id="dc76b-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-129"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-130">129</span><span class="sxs-lookup"><span data-stu-id="dc76b-130">129</span></span></p></td>
<td><p><span data-ttu-id="dc76b-131">Indica um valor da cadeia de caracteres (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="dc76b-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-133">6</span><span class="sxs-lookup"><span data-stu-id="dc76b-133">6</span></span></p></td>
<td><p><span data-ttu-id="dc76b-p102">Indica um valor de moeda (DBTYPE_CY). A moeda é um número de ponto fixo com quatro dígitos à direita do ponto decimal. Ele é armazenado em um inteiro assinado de oito bytes expansível até 10.000.</span><span class="sxs-lookup"><span data-stu-id="dc76b-p102">Indicates a currency value (DBTYPE_CY). Currency is a fixed-point number with four digits to the right of the decimal point. It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-138">7</span><span class="sxs-lookup"><span data-stu-id="dc76b-138">7</span></span></p></td>
<td><p><span data-ttu-id="dc76b-p103">Indica um valor de data (DBTYPE_DATE). Uma data é armazenada como uma dupla, a parte inteira é o número de dias desde 30 de dezembro de 1899, e a parte fracionada é a fração de um dia.</span><span class="sxs-lookup"><span data-stu-id="dc76b-p103">Indicates a date value (DBTYPE_DATE). A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-142">133</span><span class="sxs-lookup"><span data-stu-id="dc76b-142">133</span></span></p></td>
<td><p><span data-ttu-id="dc76b-143">Indica um valor de data (aaaammdd) (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="dc76b-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-145">134</span><span class="sxs-lookup"><span data-stu-id="dc76b-145">134</span></span></p></td>
<td><p><span data-ttu-id="dc76b-146">Indica um valor de hora (hhmmss) (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="dc76b-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-148">135</span><span class="sxs-lookup"><span data-stu-id="dc76b-148">135</span></span></p></td>
<td><p><span data-ttu-id="dc76b-149">Indica uma marcação de data/hora (aaaammddhhmmss mais uma fração em bilionésimo) (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="dc76b-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-151">14</span><span class="sxs-lookup"><span data-stu-id="dc76b-151">14</span></span></p></td>
<td><p><span data-ttu-id="dc76b-152">Indica um valor numérico exato com precisão e escala fixas (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="dc76b-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-154">5</span><span class="sxs-lookup"><span data-stu-id="dc76b-154">5</span></span></p></td>
<td><p><span data-ttu-id="dc76b-155">Indica um valor de ponto flutuante de precisão dupla (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="dc76b-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-157">0</span><span class="sxs-lookup"><span data-stu-id="dc76b-157">0</span></span></p></td>
<td><p><span data-ttu-id="dc76b-158">Não especifica nenhum valor (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="dc76b-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-160">10</span><span class="sxs-lookup"><span data-stu-id="dc76b-160">10</span></span></p></td>
<td><p><span data-ttu-id="dc76b-161">Indica um código de erro de 32 bits (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="dc76b-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-163">64</span><span class="sxs-lookup"><span data-stu-id="dc76b-163">64</span></span></p></td>
<td><p><span data-ttu-id="dc76b-164">Indica um valor de 64 bits representando o número de intervalos de 100 nanossegundos, desde 1º de janeiro de 1601 (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="dc76b-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-166">72</span><span class="sxs-lookup"><span data-stu-id="dc76b-166">72</span></span></p></td>
<td><p><span data-ttu-id="dc76b-167">Indica o GUID (identificador global exclusivo) (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="dc76b-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-169">9</span><span class="sxs-lookup"><span data-stu-id="dc76b-169">9</span></span></p></td>
<td><p><span data-ttu-id="dc76b-170">Indica um ponteiro para uma interface <strong>IDispatch</strong> em um objeto COM (DBTYPE_IDISPATCH).
</span><span class="sxs-lookup"><span data-stu-id="dc76b-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="dc76b-171"><strong>Observação</strong>: esse tipo de dados atualmente não é suportado pelo ADO.</span><span class="sxs-lookup"><span data-stu-id="dc76b-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="dc76b-172">Uso pode causar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="dc76b-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-173"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-174">3</span><span class="sxs-lookup"><span data-stu-id="dc76b-174">3</span></span></p></td>
<td><p><span data-ttu-id="dc76b-175">Indica um inteiro assinado de quatro bytes (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="dc76b-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-177">13</span><span class="sxs-lookup"><span data-stu-id="dc76b-177">13</span></span></p></td>
<td><p><span data-ttu-id="dc76b-178">Indica um ponteiro para uma interface <strong>IUnknown</strong> em um objeto COM (DBTYPE_IUNKNOWN).
</span><span class="sxs-lookup"><span data-stu-id="dc76b-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="dc76b-179"><strong>Observação</strong>: esse tipo de dados atualmente não é suportado pelo ADO.</span><span class="sxs-lookup"><span data-stu-id="dc76b-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="dc76b-180">Uso pode causar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="dc76b-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-182">205</span><span class="sxs-lookup"><span data-stu-id="dc76b-182">205</span></span></p></td>
<td><p><span data-ttu-id="dc76b-183">Indica um valor binário longo.</span><span class="sxs-lookup"><span data-stu-id="dc76b-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-185">201</span><span class="sxs-lookup"><span data-stu-id="dc76b-185">201</span></span></p></td>
<td><p><span data-ttu-id="dc76b-186">Indica um valor longo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="dc76b-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-188">203</span><span class="sxs-lookup"><span data-stu-id="dc76b-188">203</span></span></p></td>
<td><p><span data-ttu-id="dc76b-189">Indica um valor longo de cadeia de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="dc76b-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-191">131</span><span class="sxs-lookup"><span data-stu-id="dc76b-191">131</span></span></p></td>
<td><p><span data-ttu-id="dc76b-192">Indica um valor numérico exato com precisão e escala fixas (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="dc76b-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-194">138</span><span class="sxs-lookup"><span data-stu-id="dc76b-194">138</span></span></p></td>
<td><p><span data-ttu-id="dc76b-195">Indica uma PROPVARIANT de automação (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="dc76b-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-197">4</span><span class="sxs-lookup"><span data-stu-id="dc76b-197">4</span></span></p></td>
<td><p><span data-ttu-id="dc76b-198">Indica um valor de ponto de flutuação de precisão única (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="dc76b-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-200">2</span><span class="sxs-lookup"><span data-stu-id="dc76b-200">2</span></span></p></td>
<td><p><span data-ttu-id="dc76b-201">Indica um inteiro assinado de dois bytes (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="dc76b-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-203">16</span><span class="sxs-lookup"><span data-stu-id="dc76b-203">16</span></span></p></td>
<td><p><span data-ttu-id="dc76b-204">Indica um inteiro assinado de um byte (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="dc76b-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-206">21</span><span class="sxs-lookup"><span data-stu-id="dc76b-206">21</span></span></p></td>
<td><p><span data-ttu-id="dc76b-207">Indica um inteiro não assinado de oito bytes (DBTYPE_U8).</span><span class="sxs-lookup"><span data-stu-id="dc76b-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-209">19</span><span class="sxs-lookup"><span data-stu-id="dc76b-209">19</span></span></p></td>
<td><p><span data-ttu-id="dc76b-210">Indica um inteiro não assinado de quatro bytes (DBTYPE_U4).</span><span class="sxs-lookup"><span data-stu-id="dc76b-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-212">18</span><span class="sxs-lookup"><span data-stu-id="dc76b-212">18</span></span></p></td>
<td><p><span data-ttu-id="dc76b-213">Indica um inteiro não assinado de dois bytes (DBTYPE_U2).</span><span class="sxs-lookup"><span data-stu-id="dc76b-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-215">17</span><span class="sxs-lookup"><span data-stu-id="dc76b-215">17</span></span></p></td>
<td><p><span data-ttu-id="dc76b-216">Indica um inteiro não assinado de um byte (DBTYPE_U1).</span><span class="sxs-lookup"><span data-stu-id="dc76b-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-218">132</span><span class="sxs-lookup"><span data-stu-id="dc76b-218">132</span></span></p></td>
<td><p><span data-ttu-id="dc76b-219">Indica uma variável definida pelo usuário (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="dc76b-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-220"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-221">204</span><span class="sxs-lookup"><span data-stu-id="dc76b-221">204</span></span></p></td>
<td><p><span data-ttu-id="dc76b-222">Indica um valor binário (apenas objeto <strong>Parameter</strong>).</span><span class="sxs-lookup"><span data-stu-id="dc76b-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-223"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-224">200</span><span class="sxs-lookup"><span data-stu-id="dc76b-224">200</span></span></p></td>
<td><p><span data-ttu-id="dc76b-225">Indica um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="dc76b-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-227">12</span><span class="sxs-lookup"><span data-stu-id="dc76b-227">12</span></span></p></td>
<td><p><span data-ttu-id="dc76b-228">Indica uma <strong>Variant</strong> de automação (DBTYPE_VARIANT).
</span><span class="sxs-lookup"><span data-stu-id="dc76b-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="dc76b-229"><strong>Observação</strong>: esse tipo de dados atualmente não é suportado pelo ADO.</span><span class="sxs-lookup"><span data-stu-id="dc76b-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="dc76b-230">Uso pode causar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="dc76b-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-232">139</span><span class="sxs-lookup"><span data-stu-id="dc76b-232">139</span></span></p></td>
<td><p><span data-ttu-id="dc76b-233">Indica um valor numérico (apenas objeto <strong>Parameter</strong>).</span><span class="sxs-lookup"><span data-stu-id="dc76b-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-235">202</span><span class="sxs-lookup"><span data-stu-id="dc76b-235">202</span></span></p></td>
<td><p><span data-ttu-id="dc76b-236">Indica uma cadeia de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="dc76b-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="dc76b-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dc76b-238">130</span><span class="sxs-lookup"><span data-stu-id="dc76b-238">130</span></span></p></td>
<td><p><span data-ttu-id="dc76b-239">Indica uma cadeia de caracteres Unicode terminada em nulo (DBTYPE_WSTR).</span><span class="sxs-lookup"><span data-stu-id="dc76b-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="dc76b-240">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="dc76b-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="dc76b-241">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="dc76b-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc76b-242">Constante</span><span class="sxs-lookup"><span data-stu-id="dc76b-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="dc76b-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="dc76b-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="dc76b-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="dc76b-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="dc76b-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="dc76b-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="dc76b-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="dc76b-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="dc76b-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="dc76b-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="dc76b-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="dc76b-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="dc76b-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="dc76b-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="dc76b-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="dc76b-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="dc76b-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="dc76b-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="dc76b-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="dc76b-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="dc76b-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="dc76b-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="dc76b-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="dc76b-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="dc76b-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="dc76b-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="dc76b-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="dc76b-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="dc76b-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="dc76b-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="dc76b-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="dc76b-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="dc76b-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="dc76b-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="dc76b-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="dc76b-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="dc76b-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="dc76b-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc76b-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="dc76b-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc76b-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="dc76b-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

