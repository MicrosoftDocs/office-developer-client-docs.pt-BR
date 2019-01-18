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
# <a name="fieldtype-property-dao"></a>Propriedade Field.Type (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Tipo

*expressão* Uma variável que representa um objeto **Field** .

## <a name="remarks"></a>Comentários

A configuração ou o valor de retorno é uma constante que indica um tipo operacional ou de dados. Para um objeto **Field**, essa propriedade será leitura/gravação até que o objeto seja acrescentado a uma coleção ou a outro objeto. Depois disso o objeto se tornará somente leitura.

Para um objeto **Field**, as configurações e os valores de retorno possíveis são descritos na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbBigInt</strong></p></td>
<td><p>Número inteiro grande</p></td>
</tr>
<tr class="even">
<td><p><strong>dbBinary</strong></p></td>
<td><p>Binária</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbBoolean</strong></p></td>
<td><p>Booliano</p></td>
</tr>
<tr class="even">
<td><p><strong>dbByte</strong></p></td>
<td><p>Byte</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbChar</strong></p></td>
<td><p>Caractere</p></td>
</tr>
<tr class="even">
<td><p><strong>dbCurrency</strong></p></td>
<td><p>Moeda</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDate</strong></p></td>
<td><p>Data/Hora</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecimal</strong></p></td>
<td><p>Decimal</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDouble</strong></p></td>
<td><p>Duplo</p></td>
</tr>
<tr class="even">
<td><p><strong>dbFloat</strong></p></td>
<td><p>Flutuante</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbGUID</strong></p></td>
<td><p>GUID</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInteger</strong></p></td>
<td><p>Inteiro</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLong</strong></p></td>
<td><p>Long</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLongBinary</strong></p></td>
<td><p>Long Binary (Objeto OLE)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbMemo</strong></p></td>
<td><p>Memorando</p></td>
</tr>
<tr class="even">
<td><p><strong>dbNumeric</strong></p></td>
<td><p>Numeric</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSingle</strong></p></td>
<td><p>Single</p></td>
</tr>
<tr class="even">
<td><p><strong>dbText</strong></p></td>
<td><p>Texto</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbTime</strong></p></td>
<td><p>Time</p></td>
</tr>
<tr class="even">
<td><p><strong>dbTimeStamp</strong></p></td>
<td><p>Carimbo de data/hora</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVarBinary</strong></p></td>
<td><p>VarBinary</p></td>
</tr>
</tbody>
</table>


Quando você acrescentar um novo objeto **Field**, **Parameter** ou **Property** à coleção de um objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, ocorrerá um erro, caso o banco de dados base não ofereça suporte ao tipo de dados especificado para o novo objeto.

