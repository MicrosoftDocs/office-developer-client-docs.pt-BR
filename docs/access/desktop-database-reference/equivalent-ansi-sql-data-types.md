---
title: Tipo de dados equivalentes ao ANSI SQL
TOCTitle: Equivalent ANSI SQL data types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 3ea0641c7325bfcb4339572bc8b50724115af8d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293508"
---
# <a name="equivalent-ansi-sql-data-types"></a>Tipo de dados equivalentes ao ANSI SQL


**Aplica-se ao**: Access 2013, Office 2013

A tabela a seguir lista os tipos de dados ANSI SQL, seus tipos de dados equivalentes do mecanismo SQL do banco de dados do Microsoft Access e seus sinônimos válidos. Ele também lista os tipos de dados equivalentes do Microsoft SQL Server™.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de dados ANSI SQL</p></th>
<th><p>Tipos de dados do Microsoft Access SQL</p></th>
<th><p>Sinônimos</p></th>
<th><p>Tipo de dados do Microsoft SQL Server</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BIT, BIT VARYING</p></td>
<td><p>BINARY (consulte Observações)</p></td>
<td><p>VARBINARY, BINARY VARYING BIT VARYING</p></td>
<td><p>BINARY, VARBINARY</p></td>
</tr>
<tr class="even">
<td><p>Sem suporte</p></td>
<td><p>BIT (consulte Observações)</p></td>
<td><p>BOOLEAN, LOGICAL, LOGICAL1, YESNO</p></td>
<td><p>BIT</p></td>
</tr>
<tr class="odd">
<td><p>Sem suporte</p></td>
<td><p>TINYINT</p></td>
<td><p>INTEGER1, BYTE</p></td>
<td><p>TINYINT</p></td>
</tr>
<tr class="even">
<td><p>Sem suporte</p></td>
<td><p>COUNTER (consulte Observações)</p></td>
<td><p>AUTOINCREMENT</p></td>
<td><p>(Consulte Observações)</p></td>
</tr>
<tr class="odd">
<td><p>Sem suporte</p></td>
<td><p>DINHEIRO</p></td>
<td><p>MOEDA</p></td>
<td><p>DINHEIRO</p></td>
</tr>
<tr class="even">
<td><p>DATE, TIME, TIMESTAMP</p></td>
<td><p>DATETIME</p></td>
<td><p>DATA, HORA (Consulte Observações)</p></td>
<td><p>DATETIME</p></td>
</tr>
<tr class="odd">
<td><p>Sem suporte</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>GUID</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
</tr>
<tr class="even">
<td><p>DECIMAL</p></td>
<td><p>DECIMAL</p></td>
<td><p>NUMERIC, DEC</p></td>
<td><p>DECIMAL</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>REAL</p></td>
<td><p>SINGLE, FLOAT4, IEEESINGLE</p></td>
<td><p>REAL</p></td>
</tr>
<tr class="even">
<td><p>DOUBLE PRECISION, FLOAT</p></td>
<td><p>FLOAT</p></td>
<td><p>DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (consulte Observações)</p></td>
<td><p>FLOAT</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>SMALLINT</p></td>
<td><p>SHORT, INTEGER2</p></td>
<td><p>SMALLINT</p></td>
</tr>
<tr class="even">
<td><p>INTEIRO</p></td>
<td><p>INTEIRO</p></td>
<td><p>LONG, INT, INTEGER4</p></td>
<td><p>INTEIRO</p></td>
</tr>
<tr class="odd">
<td><p>INTERVALO</p></td>
<td><p>Sem suporte</p></td>
<td><p></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td><p>Sem suporte</p></td>
<td><p>IMAGEM</p></td>
<td><p>LONGBINARY, GENERAL, OLEOBJECT</p></td>
<td><p>IMAGEM</p></td>
</tr>
<tr class="odd">
<td><p>Sem suporte</p></td>
<td><p>TEXTO (Consulte Observações)</p></td>
<td><p>LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (consulte Observações)</p></td>
<td><p>TEXTO</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</p></td>
<td><p>CHAR (consulte Observações)</p></td>
<td><p>TEXTO(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (consulte Observações)</p></td>
<td><p>CHAR, VARCHAR, NCHAR, NVARCHAR</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - O tipo de dados ANSI SQL BIT não corresponde ao tipo de dados do Microsoft Access SQL BIT. Ele corresponde ao tipo de dados BINARY. Não há nenhum ANSI SQL equivalente para o tipo de dados do Microsoft Access SQL BIT.
> - TIMESTAMP não é mais aceito como um sinônimo de DATETIME.
> - NUMERIC não é mais aceito como um sinônimo de FLOAT ou DOUBLE. NUMERIC é agora utilizado como um sinônimo de DECIMAL.
> - Um campo LONGTEXT é sempre armazenado no formato de representação Unicode.
> - Se o nome do tempo de dados TEXT for usado sem especificar o tamanho original, por exemplo, TEXT(25), um campo LONGTEXT será criado. Isso permite que as [instruções CREATE TABLE](create-table-statement-microsoft-access-sql.md) sejam gravadas para que os tipos de dados sejam processados de forma consistente com o Microsoft SQL Server.
> - Um campo CHAR sempre será armazenado no formato de representação Unicode, o que equivale ao tipo de dados ANSI SQL NATIONAL CHAR.
> - Se o nome do tipo de dados TEXT for usado e o tamanho opcional for especificado, por exemplo TEXT(25), o tipo de dados do campo será equivalente ao tipo de dados CHAR. Isso preserva a compatibilidade com versões anteriores para a maioria dos aplicativos Microsoft Jet, permitindo, ao mesmo tempo, que o tipo de dados TEXT (sem uma especificação de tamanho) seja alinhado ao Microsoft SQL Server.


