---
title: Método CreateRecordset (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3dda0840617c32e9dceea3bd1baa362c5652a373
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703017"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="9b1ff-102">Método CreateRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="9b1ff-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="9b1ff-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b1ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b1ff-104">Cria um [Recordset](recordset-object-ado.md) vazio e desconectado.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9b1ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b1ff-105">Syntax</span></span>

<span data-ttu-id="9b1ff-106">*objeto*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="9b1ff-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="9b1ff-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b1ff-107">Parameters</span></span>

|<span data-ttu-id="9b1ff-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b1ff-108">Parameter</span></span>|<span data-ttu-id="9b1ff-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b1ff-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9b1ff-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="9b1ff-110">*Object*</span></span> |<span data-ttu-id="9b1ff-111">Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) ou [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="9b1ff-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="9b1ff-112">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="9b1ff-112">*ColumnsInfos*</span></span> |<span data-ttu-id="9b1ff-113">Uma matriz de atributos **Variant** que define cada coluna no **Recordset** criado.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="9b1ff-114">Cada definição de coluna contém uma matriz de quatro atributos obrigatórios e um atributo opcional.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="9b1ff-115">Em seguida, o conjunto de matrizes de coluna é agrupado em uma matriz, que define o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="9b1ff-116">Para obter uma lista de atributos, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="9b1ff-117">Atributos de matriz Variant</span><span class="sxs-lookup"><span data-stu-id="9b1ff-117">Variant array attributes</span></span>

|<span data-ttu-id="9b1ff-118">Atributo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-118">Attribute</span></span>|<span data-ttu-id="9b1ff-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b1ff-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9b1ff-120">Name</span><span class="sxs-lookup"><span data-stu-id="9b1ff-120">Name</span></span> |<span data-ttu-id="9b1ff-121">Nome do cabeçalho da coluna.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-121">Name of the column header.</span></span>|
|<span data-ttu-id="9b1ff-122">Type</span><span class="sxs-lookup"><span data-stu-id="9b1ff-122">Type</span></span> |<span data-ttu-id="9b1ff-123">Inteiro do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-123">Integer of the data type.</span></span>|
|<span data-ttu-id="9b1ff-124">Size</span><span class="sxs-lookup"><span data-stu-id="9b1ff-124">Size</span></span> |<span data-ttu-id="9b1ff-125">Inteiro da largura em caracteres, independentemente do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="9b1ff-126">Nullability</span><span class="sxs-lookup"><span data-stu-id="9b1ff-126">Nullability</span></span> |<span data-ttu-id="9b1ff-127">Valor booliano.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-127">Boolean value.</span></span>|
|<span data-ttu-id="9b1ff-128">Scale (opcional)</span><span class="sxs-lookup"><span data-stu-id="9b1ff-128">Scale (optional)</span></span> |<span data-ttu-id="9b1ff-p102">Este atributo opcional define a escala para campos numéricos. Se esse valor não for especificado, os valores numéricos serão truncados para uma escala de três. A precisão não é afetada, mas o número de dígitos que seguem a vírgula decimal será truncado para três.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9b1ff-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b1ff-132">Remarks</span></span>

<span data-ttu-id="9b1ff-133">O objeto corporativo no servidor pode preencher o **Recordset** resultante com dados de um provedor de dados de banco de dados não-OLE, tal como um arquivo do sistema operacional que contenha cotações de ações.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="9b1ff-p103">A tabela a seguir lista os valores de [DataTypeEnum](datatypeenum.md) suportados pelo método **CreateRecordset**. O número listado é o número de referência utilizado para definir campos.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="9b1ff-p104">Cada um dos tipos de dados tem comprimento fixo ou comprimento variável. Os tipos de comprimento fixo devem ser definidos com um tamanho igual a –1, porque o tamanho é predeterminado e uma definição de tamanho ainda é necessária. Os tipos de dados de comprimento variável permitem um tamanho de 1 até 32767.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="9b1ff-p105">Para alguns dos tipos de dados variáveis, o tipo pode ser forçado para o tipo anotado na coluna Substituição. Você não verá as substituições até que o **Recordset** seja criado e preenchido. Em seguida, será possível verificar o tipo de dados real, se necessário.</span><span class="sxs-lookup"><span data-stu-id="9b1ff-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b1ff-142">Comprimento</span><span class="sxs-lookup"><span data-stu-id="9b1ff-142">Length</span></span></p></th>
<th><p><span data-ttu-id="9b1ff-143">Constante</span><span class="sxs-lookup"><span data-stu-id="9b1ff-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="9b1ff-144">Número</span><span class="sxs-lookup"><span data-stu-id="9b1ff-144">Number</span></span></p></th>
<th><p><span data-ttu-id="9b1ff-145">Substituição</span><span class="sxs-lookup"><span data-stu-id="9b1ff-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-146">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-147"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-148">16</span><span class="sxs-lookup"><span data-stu-id="9b1ff-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-149">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-150"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-151">2</span><span class="sxs-lookup"><span data-stu-id="9b1ff-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-152">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-153"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-154">3</span><span class="sxs-lookup"><span data-stu-id="9b1ff-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-155">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-156"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-157">20</span><span class="sxs-lookup"><span data-stu-id="9b1ff-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-158">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-159"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-160">17</span><span class="sxs-lookup"><span data-stu-id="9b1ff-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-161">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-162"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-163">18</span><span class="sxs-lookup"><span data-stu-id="9b1ff-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-164">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-165"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-166">19</span><span class="sxs-lookup"><span data-stu-id="9b1ff-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-167">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-168"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-169">21</span><span class="sxs-lookup"><span data-stu-id="9b1ff-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-170">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-171"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-172">4</span><span class="sxs-lookup"><span data-stu-id="9b1ff-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-173">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-174"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-175">5</span><span class="sxs-lookup"><span data-stu-id="9b1ff-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-176">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-177"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-178">6</span><span class="sxs-lookup"><span data-stu-id="9b1ff-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-179">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-181">14</span><span class="sxs-lookup"><span data-stu-id="9b1ff-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-182">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-184">131</span><span class="sxs-lookup"><span data-stu-id="9b1ff-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-185">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-186"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-187">11</span><span class="sxs-lookup"><span data-stu-id="9b1ff-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-188">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-189"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-190">10</span><span class="sxs-lookup"><span data-stu-id="9b1ff-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-191">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-192"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-193">72</span><span class="sxs-lookup"><span data-stu-id="9b1ff-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-194">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-195"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-196">7</span><span class="sxs-lookup"><span data-stu-id="9b1ff-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-197">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-198"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-199">133</span><span class="sxs-lookup"><span data-stu-id="9b1ff-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-200">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-201"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-202">134</span><span class="sxs-lookup"><span data-stu-id="9b1ff-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-203">Fixo</span><span class="sxs-lookup"><span data-stu-id="9b1ff-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-204"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-205">135</span><span class="sxs-lookup"><span data-stu-id="9b1ff-205">135</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-206">7</span><span class="sxs-lookup"><span data-stu-id="9b1ff-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-207">Variável</span><span class="sxs-lookup"><span data-stu-id="9b1ff-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-208"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-209">8</span><span class="sxs-lookup"><span data-stu-id="9b1ff-209">8</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-210">130</span><span class="sxs-lookup"><span data-stu-id="9b1ff-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-211">Variável</span><span class="sxs-lookup"><span data-stu-id="9b1ff-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-212"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-213">129</span><span class="sxs-lookup"><span data-stu-id="9b1ff-213">129</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-214">200</span><span class="sxs-lookup"><span data-stu-id="9b1ff-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-215">Variável</span><span class="sxs-lookup"><span data-stu-id="9b1ff-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-216"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-217">200</span><span class="sxs-lookup"><span data-stu-id="9b1ff-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-218">Variável</span><span class="sxs-lookup"><span data-stu-id="9b1ff-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-219"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-220">201</span><span class="sxs-lookup"><span data-stu-id="9b1ff-220">201</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-221">200</span><span class="sxs-lookup"><span data-stu-id="9b1ff-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-222">Variável</span><span class="sxs-lookup"><span data-stu-id="9b1ff-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-223"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-224">130</span><span class="sxs-lookup"><span data-stu-id="9b1ff-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-225">Variável</span><span class="sxs-lookup"><span data-stu-id="9b1ff-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-227">202</span><span class="sxs-lookup"><span data-stu-id="9b1ff-227">202</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-228">130</span><span class="sxs-lookup"><span data-stu-id="9b1ff-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-229">Variável</span><span class="sxs-lookup"><span data-stu-id="9b1ff-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-230"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-231">203</span><span class="sxs-lookup"><span data-stu-id="9b1ff-231">203</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-232">130</span><span class="sxs-lookup"><span data-stu-id="9b1ff-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-233">Variável</span><span class="sxs-lookup"><span data-stu-id="9b1ff-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-234"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-235">128</span><span class="sxs-lookup"><span data-stu-id="9b1ff-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b1ff-236">Variável</span><span class="sxs-lookup"><span data-stu-id="9b1ff-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-237"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-238">204</span><span class="sxs-lookup"><span data-stu-id="9b1ff-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b1ff-239">Variável</span><span class="sxs-lookup"><span data-stu-id="9b1ff-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-240"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9b1ff-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9b1ff-241">205</span><span class="sxs-lookup"><span data-stu-id="9b1ff-241">205</span></span></p></td>
<td><p><span data-ttu-id="9b1ff-242">204</span><span class="sxs-lookup"><span data-stu-id="9b1ff-242">204</span></span></p></td>
</tr>
</tbody>
</table>

