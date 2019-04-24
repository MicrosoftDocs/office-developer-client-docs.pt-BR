---
title: Método createRecordset (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3dda0840617c32e9dceea3bd1baa362c5652a373
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295335"
---
# <a name="createrecordset-method-rds"></a>Método createRecordset (RDS)

**Aplica-se ao:** Access 2013, Office 2013

Cria um [Recordset](recordset-object-ado.md) vazio e desconectado.

## <a name="syntax"></a>Sintaxe

*objeto*. CreateRecordset (*ColumnInfos*)

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Object* |Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) ou [RDS.DataControl](datacontrol-object-rds.md).|
|*ColumnsInfos* |Uma matriz de atributos **Variant** que define cada coluna no **Recordset** criado. Cada definição de coluna contém uma matriz de quatro atributos obrigatórios e um atributo opcional. Em seguida, o conjunto de matrizes de coluna é agrupado em uma matriz, que define o **Recordset**. Para obter uma lista de atributos, consulte a tabela a seguir.|

### <a name="variant-array-attributes"></a>Atributos de matriz variante

|Atributo|Descrição|
|:--------|:----------|
|Nome |Nome do cabeçalho da coluna.|
|Tipo |Inteiro do tipo de dados.|
|Tamanho |Inteiro da largura em caracteres, independentemente do tipo de dados.|
|Nulidade |Valor booliano.|
|Escala (opcional) |Este atributo opcional define a escala para campos numéricos. Se esse valor não for especificado, os valores numéricos serão truncados para uma escala de três. A precisão não é afetada, mas o número de dígitos que seguem a vírgula decimal será truncado para três.|

## <a name="remarks"></a>Comentários

O objeto corporativo no servidor pode preencher o **Recordset** resultante com dados de um provedor de dados de banco de dados não-OLE, tal como um arquivo do sistema operacional que contenha cotações de ações.

A tabela a seguir lista os valores de [DataTypeEnum](datatypeenum.md) suportados pelo método **CreateRecordset**. O número listado é o número de referência utilizado para definir campos.

Cada um dos tipos de dados tem comprimento fixo ou comprimento variável. Os tipos de comprimento fixo devem ser definidos com um tamanho igual a –1, porque o tamanho é predeterminado e uma definição de tamanho ainda é necessária. Os tipos de dados de comprimento variável permitem um tamanho de 1 até 32767.

Para alguns dos tipos de dados variáveis, o tipo pode ser forçado para o tipo anotado na coluna Substituição. Você não verá as substituições até que o **Recordset** seja criado e preenchido. Em seguida, será possível verificar o tipo de dados real, se necessário.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Comprimento</p></th>
<th><p>Constant</p></th>
<th><p>Número</p></th>
<th><p>Substituição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adTinyInt</strong></p></td>
<td><p>dezesseis</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adSmallInt</strong></p></td>
<td><p>duas</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adInteger</strong></p></td>
<td><p>3D</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adBigInt</strong></p></td>
<td><p>508</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adUnsignedTinyInt</strong></p></td>
<td><p>17.07.06</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adUnsignedSmallInt</strong></p></td>
<td><p>anos</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adUnsignedInt</strong></p></td>
<td><p>19</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adUnsignedBigInt</strong></p></td>
<td><p>21</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adSingle</strong></p></td>
<td><p>quatro</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adDouble</strong></p></td>
<td><p>0,5</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adCurrency</strong></p></td>
<td><p>6</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adDecimal</strong></p></td>
<td><p>14</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adBoolean</strong></p></td>
<td><p>11</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adError</strong></p></td>
<td><p>254</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adGuid</strong></p></td>
<td><p>72</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adDate</strong></p></td>
<td><p>178</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adDBDate</strong></p></td>
<td><p>133</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adDBTime</strong></p></td>
<td><p>134</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adDBTimestamp</strong></p></td>
<td><p>135</p></td>
<td><p>178</p></td>
</tr>
<tr class="odd">
<td><p>Variável</p></td>
<td><p><strong>adBSTR</strong></p></td>
<td><p>8</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Variável</p></td>
<td><p><strong>adChar</strong></p></td>
<td><p>129</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Variável</p></td>
<td><p><strong>adVarChar</strong></p></td>
<td><p>200</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variável</p></td>
<td><p><strong>adLongVarChar</strong></p></td>
<td><p>201</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Variável</p></td>
<td><p><strong>adWChar</strong></p></td>
<td><p>130</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variável</p></td>
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>130</p></td>
</tr>
<tr class="odd">
<td><p>Variável</p></td>
<td><p><strong>adLongVarWChar</strong></p></td>
<td><p>203</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Variável</p></td>
<td><p><strong>adBinary</strong></p></td>
<td><p>128</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Variável</p></td>
<td><p><strong>adVarBinary</strong></p></td>
<td><p>204</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variável</p></td>
<td><p><strong>adLongVarBinary</strong></p></td>
<td><p>205</p></td>
<td><p>204</p></td>
</tr>
</tbody>
</table>

