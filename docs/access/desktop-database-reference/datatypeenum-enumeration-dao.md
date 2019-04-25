---
title: Enumeração DataTypeEnum (DAO)
TOCTitle: DataTypeEnum Enumeration
ms:assetid: 59ead483-52fc-53cd-02e6-084814f961ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194420(v=office.15)
ms:contentKeyID: 48545028
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 499513d706b254e72433d37d4eb5452ccbbaa257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294446"
---
# <a name="datatypeenum-enumeration-dao"></a>Enumeração DataTypeEnum (DAO)


**Aplica-se ao**: Access 2013, Office 2013

Especifica o tipo de dados operacionais de um objeto.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbAttachment</p></td>
<td><p>101</p></td>
<td><p>Dados Anexo</p></td>
</tr>
<tr class="even">
<td><p>dbBigInt</p></td>
<td><p>16</p></td>
<td><p>Dados Número Inteiro Grande</p></td>
</tr>
<tr class="odd">
<td><p>dbBinary</p></td>
<td><p>9</p></td>
<td><p>Dados Binários</p></td>
</tr>
<tr class="even">
<td><p>dbBoolean</p></td>
<td><p>1</p></td>
<td><p>Dados Booleanos (Verdadeiro/Falso)</p></td>
</tr>
<tr class="odd">
<td><p>dbByte</p></td>
<td><p>2</p></td>
<td><p>Dados Byte (8 bits)</p></td>
</tr>
<tr class="even">
<td><p>dbChar</p></td>
<td><p>18</p></td>
<td><p>Dados Texto (largura fixa)</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexByte</p></td>
<td><p>102</p></td>
<td><p>Dados de byte de valores múltiplos</p></td>
</tr>
<tr class="even">
<td><p>dbComplexDecimal</p></td>
<td><p>108</p></td>
<td><p>Dados decimais de valores múltiplos</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexDouble</p></td>
<td><p>106</p></td>
<td><p>Dados de ponto flutuante de dupla precisão de valores múltiplos</p></td>
</tr>
<tr class="even">
<td><p>dbComplexGUID</p></td>
<td><p>107</p></td>
<td><p>Dados de GUID de valores múltiplos</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexInteger</p></td>
<td><p>103</p></td>
<td><p>Dados inteiros de valores múltiplos</p></td>
</tr>
<tr class="even">
<td><p>dbComplexLong</p></td>
<td><p>104</p></td>
<td><p>Dados de inteiro longo de valores múltiplos</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexSingle</p></td>
<td><p>105</p></td>
<td><p>Dados de ponto flutuante de precisão simples de valores múltiplos</p></td>
</tr>
<tr class="even">
<td><p>dbComplexText</p></td>
<td><p>109</p></td>
<td><p>Dados Texto de valores múltiplos (largura variável)</p></td>
</tr>
<tr class="odd">
<td><p>dbCurrency</p></td>
<td><p>5</p></td>
<td><p>Dados de moeda</p></td>
</tr>
<tr class="even">
<td><p>dbDate</p></td>
<td><p>8</p></td>
<td><p>Dados de valor de data</p></td>
</tr>
<tr class="odd">
<td><p>dbDecimal</p></td>
<td><p>20</p></td>
<td><p>Dados decimais (somente ODBCDirect)</p><p><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use o ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</p>
</td>
</tr>
<tr class="even">
<td><p>dbDouble</p></td>
<td><p>7</p></td>
<td><p>Dados de ponto flutuante de precisão dupla</p></td>
</tr>
<tr class="odd">
<td><p>dbFloat</p></td>
<td><p>21</p></td>
<td><p>Dados de ponto flutuante (somente ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbGUID</p></td>
<td><p>15</p></td>
<td><p>Dados de GUID</p></td>
</tr>
<tr class="odd">
<td><p>dbInteger</p></td>
<td><p>3</p></td>
<td><p>Dados Integer</p></td>
</tr>
<tr class="even">
<td><p>dbLong</p></td>
<td><p>4</p></td>
<td><p>Dados Inteiros Longos</p></td>
</tr>
<tr class="odd">
<td><p>dbLongBinary</p></td>
<td><p>11</p></td>
<td><p>Dados binários (bitmap)</p></td>
</tr>
<tr class="even">
<td><p>dbMemo</p></td>
<td><p>12</p></td>
<td><p>Dados de memorando (texto estendido)</p></td>
</tr>
<tr class="odd">
<td><p>dbNumeric</p></td>
<td><p>19</p></td>
<td><p>Dados numéricos (somente ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbSingle</p></td>
<td><p>6</p></td>
<td><p>Dados de ponto flutuante de precisão simples</p></td>
</tr>
<tr class="odd">
<td><p>dbText</p></td>
<td><p>10</p></td>
<td><p>Dados de texto (largura variável)</p></td>
</tr>
<tr class="even">
<td><p>dbTime</p></td>
<td><p>22</p></td>
<td><p>Dados no formato de hora (somente ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="odd">
<td><p>dbTimeStamp</p></td>
<td><p>23</p></td>
<td><p>Dados no formato de hora e data (somente ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbVarBinary</p></td>
<td><p>17</p></td>
<td><p>Dados Binários Variáveis (somente ODBCDirect)</p>

<br/>


</td>
</tr>
</tbody>
</table>

