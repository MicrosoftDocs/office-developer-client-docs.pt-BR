---
title: Método CreateRecordset (RDS)
TOCTitle: CreateRecordset Method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 696daaeb060387d5f3ca454ef665517a8ff7be74
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462214"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="43ebd-102">Método CreateRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="43ebd-102">CreateRecordset Method (RDS)</span></span>


<span data-ttu-id="43ebd-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="43ebd-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="43ebd-104">Cria um [Recordset](recordset-object-ado.md) vazio e desconectado.</span><span class="sxs-lookup"><span data-stu-id="43ebd-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="43ebd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43ebd-105">Syntax</span></span>

<span data-ttu-id="43ebd-106">*objeto*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="43ebd-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="43ebd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43ebd-107">Parameters</span></span>

  - <span data-ttu-id="43ebd-108">*Object*</span><span class="sxs-lookup"><span data-stu-id="43ebd-108">*Object*</span></span>

  - <span data-ttu-id="43ebd-109">Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) ou [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="43ebd-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="43ebd-110">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="43ebd-110">*ColumnsInfos*</span></span>

  - <span data-ttu-id="43ebd-p101">Uma matriz de atributos **Variant** que define cada coluna no **Recordset** criado. Cada definição de coluna contém uma matriz de quatro atributos obrigatórios e um atributo opcional. Em seguida, o conjunto de matrizes de coluna é agrupado em uma matriz, que define o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="43ebd-p101">A **Variant** array of attributes that defines each column in the **Recordset** created. Each column definition contains an array of four required attributes and one optional attribute. The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="43ebd-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="43ebd-114">Attribute</span></span></p></th>
    <th><p><span data-ttu-id="43ebd-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="43ebd-115">Description</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="43ebd-116">Name</span><span class="sxs-lookup"><span data-stu-id="43ebd-116">Name</span></span></p></td>
    <td><p><span data-ttu-id="43ebd-117">Nome do cabeçalho da coluna.</span><span class="sxs-lookup"><span data-stu-id="43ebd-117">Name of the column header.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="43ebd-118">Type</span><span class="sxs-lookup"><span data-stu-id="43ebd-118">Type</span></span></p></td>
    <td><p><span data-ttu-id="43ebd-119">Inteiro do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="43ebd-119">Integer of the data type.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="43ebd-120">Size</span><span class="sxs-lookup"><span data-stu-id="43ebd-120">Size</span></span></p></td>
    <td><p><span data-ttu-id="43ebd-121">Inteiro da largura em caracteres, independentemente do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="43ebd-121">Integer of the width in characters, regardless of data type.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="43ebd-122">Nullability</span><span class="sxs-lookup"><span data-stu-id="43ebd-122">Nullability</span></span></p></td>
    <td><p><span data-ttu-id="43ebd-123">Valor booliano.</span><span class="sxs-lookup"><span data-stu-id="43ebd-123">Boolean value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="43ebd-124">Scale</span><span class="sxs-lookup"><span data-stu-id="43ebd-124">Scale</span></span><br />
<span data-ttu-id="43ebd-125">(Opcional)</span><span class="sxs-lookup"><span data-stu-id="43ebd-125">(Optional)</span></span></p></td>
    <td><p><span data-ttu-id="43ebd-p102">Este atributo opcional define a escala para campos numéricos. Se esse valor não for especificado, os valores numéricos serão truncados para uma escala de três. A precisão não é afetada, mas o número de dígitos que seguem a vírgula decimal será truncado para três.</span><span class="sxs-lookup"><span data-stu-id="43ebd-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="43ebd-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="43ebd-129">Remarks</span></span>

<span data-ttu-id="43ebd-130">O objeto corporativo no servidor pode preencher o **Recordset** resultante com dados de um provedor de dados de banco de dados não-OLE, tal como um arquivo do sistema operacional que contenha cotações de ações.</span><span class="sxs-lookup"><span data-stu-id="43ebd-130">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="43ebd-p103">A tabela a seguir lista os valores de [DataTypeEnum](datatypeenum.md) suportados pelo método **CreateRecordset**. O número listado é o número de referência utilizado para definir campos.</span><span class="sxs-lookup"><span data-stu-id="43ebd-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="43ebd-p104">Cada um dos tipos de dados tem comprimento fixo ou comprimento variável. Os tipos de comprimento fixo devem ser definidos com um tamanho igual a –1, porque o tamanho é predeterminado e uma definição de tamanho ainda é necessária. Os tipos de dados de comprimento variável permitem um tamanho de 1 até 32767.</span><span class="sxs-lookup"><span data-stu-id="43ebd-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="43ebd-p105">Para alguns dos tipos de dados variáveis, o tipo pode ser forçado para o tipo anotado na coluna Substituição. Você não verá as substituições até que o **Recordset** seja criado e preenchido. Em seguida, será possível verificar o tipo de dados real, se necessário.</span><span class="sxs-lookup"><span data-stu-id="43ebd-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43ebd-139">Comprimento</span><span class="sxs-lookup"><span data-stu-id="43ebd-139">Length</span></span></p></th>
<th><p><span data-ttu-id="43ebd-140">Constante</span><span class="sxs-lookup"><span data-stu-id="43ebd-140">Constant</span></span></p></th>
<th><p><span data-ttu-id="43ebd-141">Número</span><span class="sxs-lookup"><span data-stu-id="43ebd-141">Number</span></span></p></th>
<th><p><span data-ttu-id="43ebd-142">Substituição</span><span class="sxs-lookup"><span data-stu-id="43ebd-142">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-143">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-143">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-144"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-144"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-145">16</span><span class="sxs-lookup"><span data-stu-id="43ebd-145">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-146">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-147"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-147"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-148">2</span><span class="sxs-lookup"><span data-stu-id="43ebd-148">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-149">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-150"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-150"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-151">3</span><span class="sxs-lookup"><span data-stu-id="43ebd-151">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-152">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-153"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-153"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-154">20</span><span class="sxs-lookup"><span data-stu-id="43ebd-154">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-155">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-156"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-156"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-157">17</span><span class="sxs-lookup"><span data-stu-id="43ebd-157">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-158">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-159"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-159"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-160">18</span><span class="sxs-lookup"><span data-stu-id="43ebd-160">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-161">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-162"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-162"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-163">19</span><span class="sxs-lookup"><span data-stu-id="43ebd-163">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-164">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-165"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-165"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-166">21</span><span class="sxs-lookup"><span data-stu-id="43ebd-166">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-167">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-168"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-168"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-169">4</span><span class="sxs-lookup"><span data-stu-id="43ebd-169">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-170">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-171"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-171"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-172">5</span><span class="sxs-lookup"><span data-stu-id="43ebd-172">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-173">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-174"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-174"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-175">6</span><span class="sxs-lookup"><span data-stu-id="43ebd-175">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-176">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-177"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-177"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-178">14</span><span class="sxs-lookup"><span data-stu-id="43ebd-178">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-179">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-180"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-180"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-181">131</span><span class="sxs-lookup"><span data-stu-id="43ebd-181">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-182">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-183"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-183"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-184">11</span><span class="sxs-lookup"><span data-stu-id="43ebd-184">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-185">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-186"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-186"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-187">10</span><span class="sxs-lookup"><span data-stu-id="43ebd-187">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-188">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-189"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-189"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-190">72</span><span class="sxs-lookup"><span data-stu-id="43ebd-190">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-191">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-192"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-192"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-193">7</span><span class="sxs-lookup"><span data-stu-id="43ebd-193">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-194">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-195"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-195"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-196">133</span><span class="sxs-lookup"><span data-stu-id="43ebd-196">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-197">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-198"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-198"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-199">134</span><span class="sxs-lookup"><span data-stu-id="43ebd-199">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-200">Fixo</span><span class="sxs-lookup"><span data-stu-id="43ebd-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="43ebd-201"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-201"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-202">135</span><span class="sxs-lookup"><span data-stu-id="43ebd-202">135</span></span></p></td>
<td><p><span data-ttu-id="43ebd-203">7</span><span class="sxs-lookup"><span data-stu-id="43ebd-203">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-204">Variável</span><span class="sxs-lookup"><span data-stu-id="43ebd-204">Variable</span></span></p></td>
<td><p><span data-ttu-id="43ebd-205"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-205"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-206">8</span><span class="sxs-lookup"><span data-stu-id="43ebd-206">8</span></span></p></td>
<td><p><span data-ttu-id="43ebd-207">130</span><span class="sxs-lookup"><span data-stu-id="43ebd-207">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-208">Variável</span><span class="sxs-lookup"><span data-stu-id="43ebd-208">Variable</span></span></p></td>
<td><p><span data-ttu-id="43ebd-209"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-209"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-210">129</span><span class="sxs-lookup"><span data-stu-id="43ebd-210">129</span></span></p></td>
<td><p><span data-ttu-id="43ebd-211">200</span><span class="sxs-lookup"><span data-stu-id="43ebd-211">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-212">Variável</span><span class="sxs-lookup"><span data-stu-id="43ebd-212">Variable</span></span></p></td>
<td><p><span data-ttu-id="43ebd-213"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-213"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-214">200</span><span class="sxs-lookup"><span data-stu-id="43ebd-214">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-215">Variável</span><span class="sxs-lookup"><span data-stu-id="43ebd-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="43ebd-216"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-216"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-217">201</span><span class="sxs-lookup"><span data-stu-id="43ebd-217">201</span></span></p></td>
<td><p><span data-ttu-id="43ebd-218">200</span><span class="sxs-lookup"><span data-stu-id="43ebd-218">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-219">Variável</span><span class="sxs-lookup"><span data-stu-id="43ebd-219">Variable</span></span></p></td>
<td><p><span data-ttu-id="43ebd-220"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-220"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-221">130</span><span class="sxs-lookup"><span data-stu-id="43ebd-221">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-222">Variável</span><span class="sxs-lookup"><span data-stu-id="43ebd-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="43ebd-223"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-223"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-224">202</span><span class="sxs-lookup"><span data-stu-id="43ebd-224">202</span></span></p></td>
<td><p><span data-ttu-id="43ebd-225">130</span><span class="sxs-lookup"><span data-stu-id="43ebd-225">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-226">Variável</span><span class="sxs-lookup"><span data-stu-id="43ebd-226">Variable</span></span></p></td>
<td><p><span data-ttu-id="43ebd-227"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-227"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-228">203</span><span class="sxs-lookup"><span data-stu-id="43ebd-228">203</span></span></p></td>
<td><p><span data-ttu-id="43ebd-229">130</span><span class="sxs-lookup"><span data-stu-id="43ebd-229">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-230">Variável</span><span class="sxs-lookup"><span data-stu-id="43ebd-230">Variable</span></span></p></td>
<td><p><span data-ttu-id="43ebd-231"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-231"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-232">128</span><span class="sxs-lookup"><span data-stu-id="43ebd-232">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43ebd-233">Variável</span><span class="sxs-lookup"><span data-stu-id="43ebd-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="43ebd-234"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-234"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-235">204</span><span class="sxs-lookup"><span data-stu-id="43ebd-235">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43ebd-236">Variável</span><span class="sxs-lookup"><span data-stu-id="43ebd-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="43ebd-237"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="43ebd-237"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="43ebd-238">205</span><span class="sxs-lookup"><span data-stu-id="43ebd-238">205</span></span></p></td>
<td><p><span data-ttu-id="43ebd-239">204</span><span class="sxs-lookup"><span data-stu-id="43ebd-239">204</span></span></p></td>
</tr>
</tbody>
</table>

