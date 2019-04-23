---
title: Funções escalares ODBC
TOCTitle: ODBC scalar functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 33443fda474b3785d34d457719e49f5e358bb254
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288508"
---
# <a name="odbc-scalar-functions"></a>Funções escalares ODBC

**Aplica-se ao:** Access 2013, Office 2013

O Microsoft Access SQL suporta o uso da sintaxe definida por ODBC para funções escalares. 

Por exemplo, a consulta `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` retorna todas as linhas em que o valor absoluto da alteração no preço de um estoque era maior que cinco.

Um subconjunto de funções escalares definidas por ODBC é aceito. A tabela a seguir lista as funções aceitas.

Para obter uma descrição dos argumentos e uma explicação completa da sintaxe de eliminação para a inclusão de funções em uma instrução SQL, consulte a documentação do ODBC.

## <a name="string-functions"></a>Funções de cadeia de caracteres

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ASCII</p></td>
<td><p>COMPRIMENTO</p></td>
<td><p>RTRIM</p></td>
</tr>
<tr class="even">
<td><p>CHAR</p></td>
<td><p>LOCALIZADO</p></td>
<td><p>ESPAÇO</p></td>
</tr>
<tr class="odd">
<td><p>CONCATENA</p></td>
<td><p>LTRIM</p></td>
<td><p>SUBCADEIA</p></td>
</tr>
<tr class="even">
<td><p>LCASE</p></td>
<td><p>Certo</p></td>
<td><p>UCASE</p></td>
</tr>
<tr class="odd">
<td><p>DEIXOU</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a>Funções numéricas

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ABS</p></td>
<td><p>FLOOR</p></td>
<td><p>SIN</p></td>
</tr>
<tr class="even">
<td><p>ATAN</p></td>
<td><p>REGISTRA</p></td>
<td><p>SQRT</p></td>
</tr>
<tr class="odd">
<td><p>RENDIMENTO</p></td>
<td><p>FORÇA</p></td>
<td><p>Claro</p></td>
</tr>
<tr class="even">
<td><p>EXIBI</p></td>
<td><p>RAND</p></td>
<td><p>MOD</p></td>
</tr>
<tr class="odd">
<td><p>ESP</p></td>
<td><p>CIFRÃO</p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a>Funções de data de tempo &

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>CURDATE</p></td>
<td><p>DAYOFYEAR</p></td>
<td><p>MENSAL</p></td>
</tr>
<tr class="even">
<td><p>CURTIME</p></td>
<td><p>ANUAIS</p></td>
<td><p>ÚTIL</p></td>
</tr>
<tr class="odd">
<td><p>DISPONIBILIZA</p></td>
<td><p>HORA</p></td>
<td><p>TRIMESTRE</p></td>
</tr>
<tr class="even">
<td><p>DAYOFMONTH</p></td>
<td><p>INCLUSÕES</p></td>
<td><p>MONTHNAME</p></td>
</tr>
<tr class="odd">
<td><p>DAYOFWEEK</p></td>
<td><p>SECUNDÁRIA</p></td>
<td><p>DAYNAME</p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a>Conversão de tipo de dados

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>CONVERSÃO</p></td>
<td><p>Os literais de sequência podem ser convertidos para os seguintes tipos de dados: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR e SQL_DATETIME.</p></td>
</tr>
</tbody>
</table>

