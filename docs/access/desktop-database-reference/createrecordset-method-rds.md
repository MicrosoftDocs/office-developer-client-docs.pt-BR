---
title: Método CreateRecordset (RDS)
TOCTitle: CreateRecordset Method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d975faf45cf6a16bdae9f800084ebbbbaec3127d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868529"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="f44dd-102">Método CreateRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="f44dd-102">CreateRecordset Method (RDS)</span></span>


<span data-ttu-id="f44dd-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f44dd-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f44dd-104">Cria um [Recordset](recordset-object-ado.md) vazio e desconectado.</span><span class="sxs-lookup"><span data-stu-id="f44dd-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f44dd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f44dd-105">Syntax</span></span>

<span data-ttu-id="f44dd-106">*objeto*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="f44dd-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="f44dd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f44dd-107">Parameters</span></span>

  - <span data-ttu-id="f44dd-108">*Object*</span><span class="sxs-lookup"><span data-stu-id="f44dd-108">*Object*</span></span>

  - <span data-ttu-id="f44dd-109">Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) ou [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="f44dd-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="f44dd-110">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="f44dd-110">*ColumnsInfos*</span></span>

  - <span data-ttu-id="f44dd-p101">Uma matriz de atributos **Variant** que define cada coluna no **Recordset** criado. Cada definição de coluna contém uma matriz de quatro atributos obrigatórios e um atributo opcional. Em seguida, o conjunto de matrizes de coluna é agrupado em uma matriz, que define o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f44dd-p101">A **Variant** array of attributes that defines each column in the **Recordset** created. Each column definition contains an array of four required attributes and one optional attribute. The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="f44dd-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="f44dd-114">Attribute</span></span></p></th>
    <th><p><span data-ttu-id="f44dd-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f44dd-115">Description</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="f44dd-116">Name</span><span class="sxs-lookup"><span data-stu-id="f44dd-116">Name</span></span></p></td>
    <td><p><span data-ttu-id="f44dd-117">Nome do cabeçalho da coluna.</span><span class="sxs-lookup"><span data-stu-id="f44dd-117">Name of the column header.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="f44dd-118">Type</span><span class="sxs-lookup"><span data-stu-id="f44dd-118">Type</span></span></p></td>
    <td><p><span data-ttu-id="f44dd-119">Inteiro do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f44dd-119">Integer of the data type.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="f44dd-120">Size</span><span class="sxs-lookup"><span data-stu-id="f44dd-120">Size</span></span></p></td>
    <td><p><span data-ttu-id="f44dd-121">Inteiro da largura em caracteres, independentemente do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f44dd-121">Integer of the width in characters, regardless of data type.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="f44dd-122">Nullability</span><span class="sxs-lookup"><span data-stu-id="f44dd-122">Nullability</span></span></p></td>
    <td><p><span data-ttu-id="f44dd-123">Valor booliano.</span><span class="sxs-lookup"><span data-stu-id="f44dd-123">Boolean value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="f44dd-124">Scale</span><span class="sxs-lookup"><span data-stu-id="f44dd-124">Scale</span></span><br />
<span data-ttu-id="f44dd-125">(Opcional)</span><span class="sxs-lookup"><span data-stu-id="f44dd-125">(Optional)</span></span></p></td>
    <td><p><span data-ttu-id="f44dd-p102">Este atributo opcional define a escala para campos numéricos. Se esse valor não for especificado, os valores numéricos serão truncados para uma escala de três. A precisão não é afetada, mas o número de dígitos que seguem a vírgula decimal será truncado para três.</span><span class="sxs-lookup"><span data-stu-id="f44dd-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="f44dd-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="f44dd-129">Remarks</span></span>

<span data-ttu-id="f44dd-130">O objeto corporativo no servidor pode preencher o **Recordset** resultante com dados de um provedor de dados de banco de dados não-OLE, tal como um arquivo do sistema operacional que contenha cotações de ações.</span><span class="sxs-lookup"><span data-stu-id="f44dd-130">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="f44dd-p103">A tabela a seguir lista os valores de [DataTypeEnum](datatypeenum.md) suportados pelo método **CreateRecordset**. O número listado é o número de referência utilizado para definir campos.</span><span class="sxs-lookup"><span data-stu-id="f44dd-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="f44dd-p104">Cada um dos tipos de dados tem comprimento fixo ou comprimento variável. Os tipos de comprimento fixo devem ser definidos com um tamanho igual a –1, porque o tamanho é predeterminado e uma definição de tamanho ainda é necessária. Os tipos de dados de comprimento variável permitem um tamanho de 1 até 32767.</span><span class="sxs-lookup"><span data-stu-id="f44dd-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="f44dd-p105">Para alguns dos tipos de dados variáveis, o tipo pode ser forçado para o tipo anotado na coluna Substituição. Você não verá as substituições até que o **Recordset** seja criado e preenchido. Em seguida, será possível verificar o tipo de dados real, se necessário.</span><span class="sxs-lookup"><span data-stu-id="f44dd-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f44dd-139">Comprimento</span><span class="sxs-lookup"><span data-stu-id="f44dd-139">Length</span></span></p></th>
<th><p><span data-ttu-id="f44dd-140">Constante</span><span class="sxs-lookup"><span data-stu-id="f44dd-140">Constant</span></span></p></th>
<th><p><span data-ttu-id="f44dd-141">Número</span><span class="sxs-lookup"><span data-stu-id="f44dd-141">Number</span></span></p></th>
<th><p><span data-ttu-id="f44dd-142">Substituição</span><span class="sxs-lookup"><span data-stu-id="f44dd-142">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-143">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-143">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-144"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-144"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-145">16</span><span class="sxs-lookup"><span data-stu-id="f44dd-145">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-146">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-147"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-147"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-148">2</span><span class="sxs-lookup"><span data-stu-id="f44dd-148">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-149">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-150"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-150"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-151">3</span><span class="sxs-lookup"><span data-stu-id="f44dd-151">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-152">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-153"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-153"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-154">20</span><span class="sxs-lookup"><span data-stu-id="f44dd-154">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-155">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-156"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-156"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-157">17</span><span class="sxs-lookup"><span data-stu-id="f44dd-157">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-158">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-159"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-159"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-160">18</span><span class="sxs-lookup"><span data-stu-id="f44dd-160">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-161">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-162"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-162"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-163">19</span><span class="sxs-lookup"><span data-stu-id="f44dd-163">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-164">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-165"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-165"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-166">21</span><span class="sxs-lookup"><span data-stu-id="f44dd-166">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-167">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-168"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-168"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-169">4</span><span class="sxs-lookup"><span data-stu-id="f44dd-169">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-170">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-171"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-171"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-172">5</span><span class="sxs-lookup"><span data-stu-id="f44dd-172">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-173">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-174"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-174"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-175">6</span><span class="sxs-lookup"><span data-stu-id="f44dd-175">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-176">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-177"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-177"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-178">14</span><span class="sxs-lookup"><span data-stu-id="f44dd-178">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-179">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-180"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-180"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-181">131</span><span class="sxs-lookup"><span data-stu-id="f44dd-181">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-182">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-183"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-183"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-184">11</span><span class="sxs-lookup"><span data-stu-id="f44dd-184">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-185">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-186"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-186"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-187">10</span><span class="sxs-lookup"><span data-stu-id="f44dd-187">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-188">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-189"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-189"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-190">72</span><span class="sxs-lookup"><span data-stu-id="f44dd-190">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-191">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-192"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-192"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-193">7</span><span class="sxs-lookup"><span data-stu-id="f44dd-193">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-194">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-195"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-195"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-196">133</span><span class="sxs-lookup"><span data-stu-id="f44dd-196">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-197">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-198"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-198"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-199">134</span><span class="sxs-lookup"><span data-stu-id="f44dd-199">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-200">Fixo</span><span class="sxs-lookup"><span data-stu-id="f44dd-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f44dd-201"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-201"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-202">135</span><span class="sxs-lookup"><span data-stu-id="f44dd-202">135</span></span></p></td>
<td><p><span data-ttu-id="f44dd-203">7</span><span class="sxs-lookup"><span data-stu-id="f44dd-203">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-204">Variável</span><span class="sxs-lookup"><span data-stu-id="f44dd-204">Variable</span></span></p></td>
<td><p><span data-ttu-id="f44dd-205"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-205"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-206">8</span><span class="sxs-lookup"><span data-stu-id="f44dd-206">8</span></span></p></td>
<td><p><span data-ttu-id="f44dd-207">130</span><span class="sxs-lookup"><span data-stu-id="f44dd-207">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-208">Variável</span><span class="sxs-lookup"><span data-stu-id="f44dd-208">Variable</span></span></p></td>
<td><p><span data-ttu-id="f44dd-209"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-209"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-210">129</span><span class="sxs-lookup"><span data-stu-id="f44dd-210">129</span></span></p></td>
<td><p><span data-ttu-id="f44dd-211">200</span><span class="sxs-lookup"><span data-stu-id="f44dd-211">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-212">Variável</span><span class="sxs-lookup"><span data-stu-id="f44dd-212">Variable</span></span></p></td>
<td><p><span data-ttu-id="f44dd-213"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-213"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-214">200</span><span class="sxs-lookup"><span data-stu-id="f44dd-214">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-215">Variável</span><span class="sxs-lookup"><span data-stu-id="f44dd-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="f44dd-216"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-216"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-217">201</span><span class="sxs-lookup"><span data-stu-id="f44dd-217">201</span></span></p></td>
<td><p><span data-ttu-id="f44dd-218">200</span><span class="sxs-lookup"><span data-stu-id="f44dd-218">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-219">Variável</span><span class="sxs-lookup"><span data-stu-id="f44dd-219">Variable</span></span></p></td>
<td><p><span data-ttu-id="f44dd-220"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-220"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-221">130</span><span class="sxs-lookup"><span data-stu-id="f44dd-221">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-222">Variável</span><span class="sxs-lookup"><span data-stu-id="f44dd-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="f44dd-223"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-223"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-224">202</span><span class="sxs-lookup"><span data-stu-id="f44dd-224">202</span></span></p></td>
<td><p><span data-ttu-id="f44dd-225">130</span><span class="sxs-lookup"><span data-stu-id="f44dd-225">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-226">Variável</span><span class="sxs-lookup"><span data-stu-id="f44dd-226">Variable</span></span></p></td>
<td><p><span data-ttu-id="f44dd-227"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-227"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-228">203</span><span class="sxs-lookup"><span data-stu-id="f44dd-228">203</span></span></p></td>
<td><p><span data-ttu-id="f44dd-229">130</span><span class="sxs-lookup"><span data-stu-id="f44dd-229">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-230">Variável</span><span class="sxs-lookup"><span data-stu-id="f44dd-230">Variable</span></span></p></td>
<td><p><span data-ttu-id="f44dd-231"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-231"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-232">128</span><span class="sxs-lookup"><span data-stu-id="f44dd-232">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f44dd-233">Variável</span><span class="sxs-lookup"><span data-stu-id="f44dd-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="f44dd-234"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-234"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-235">204</span><span class="sxs-lookup"><span data-stu-id="f44dd-235">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f44dd-236">Variável</span><span class="sxs-lookup"><span data-stu-id="f44dd-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="f44dd-237"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f44dd-237"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f44dd-238">205</span><span class="sxs-lookup"><span data-stu-id="f44dd-238">205</span></span></p></td>
<td><p><span data-ttu-id="f44dd-239">204</span><span class="sxs-lookup"><span data-stu-id="f44dd-239">204</span></span></p></td>
</tr>
</tbody>
</table>

