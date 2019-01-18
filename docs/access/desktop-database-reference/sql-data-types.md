---
title: Tipos de dados do SQL (referência de banco de dados da área de trabalho do Access)
TOCTitle: SQL data types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: fb72a0090550692e7cf5028a6a58a078fc5d9d32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722197"
---
# <a name="sql-data-types"></a>Tipos de dados SQL

**Aplica-se a**: Access 2013, o Office 2013

Os tipos de dados SQL do mecanismo de banco de dados do Microsoft Access consistem em 13 tipos de dados principais definidos pelo mecanismo de banco de dados do Microsoft Jet e vários sinônimos válidos, reconhecidos para esses tipos de dados.

A tabela a seguir lista os principais tipos de dados. Os sinônimos são identificados em [Palavras reservadas SQL do mecanismo de banco de dados Microsoft Access](sql-reserved-words.md).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de dado</p></th>
<th><p>Espaço de repositório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BINARY</p></td>
<td><p>1 byte por caractere</p></td>
<td><p>Qualquer tipo de dados pode ser armazenado em um campo desse tipo. Nenhuma conversão de dados (por exemplo, para texto) é feita. A forma como os dados são inseridos em um campo binário indica o modo como serão exibidos na saída.</p></td>
</tr>
<tr class="even">
<td><p>BIT</p></td>
<td><p>1 byte</p></td>
<td><p>Os valores Sim e Não e os campos que contêm apenas um desses dois valores.</p></td>
</tr>
<tr class="odd">
<td><p>TINYINT</p></td>
<td><p>1 byte</p></td>
<td><p>Um valor inteiro entre 0 e 255.</p></td>
</tr>
<tr class="even">
<td><p>MONEY</p></td>
<td><p>8 bytes</p></td>
<td><p>Um inteiro em escala entre – 922,337,203,685,477.5808 e 922,337,203,685,477.5807.</p></td>
</tr>
<tr class="odd">
<td><p>DATETIME (consulte DOUBLE)</p></td>
<td><p>8 bytes</p></td>
<td><p>Um valor de data ou hora entre os anos 100 e 9999.</p></td>
</tr>
<tr class="even">
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>128 bits</p></td>
<td><p>Um número de identificação exclusiva utilizado com as chamadas de procedimento remoto.</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>4 bytes</p></td>
<td><p>Um valor de ponto de flutuação de precisão única com um intervalo de – 3.402823E38 a – 1.401298E-45 para valores negativos, 1.401298E-45 a 3.402823E38 para valores positivos e 0.</p></td>
</tr>
<tr class="even">
<td><p>FLOAT</p></td>
<td><p>8 bytes</p></td>
<td><p>Um valor de ponto de flutuação de precisão dupla com um intervalo de – 1.79769313486232E308 a – 4.94065645841247E-324 para valores negativos, 4.94065645841247E-324 a 1.79769313486232E308 para valores positivos e 0.</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>2 bytes</p></td>
<td><p>Um inteiro curto entre –  32,768 e 32,767 (consulte Observações)</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>4 bytes</p></td>
<td><p>Um inteiro longo entre –  2,147,483,648 e 2,147,483,647 (consulte Observações)</p></td>
</tr>
<tr class="odd">
<td><p>DECIMAL</p></td>
<td><p>17 bytes</p></td>
<td><p>Um tipo de dados numérico exato que mantém valores de 1028 - 1 a - 1028 - 1. Você pode definir a precisão (1 - 28) e a escala (0 - precisão definida). A precisão e a escala padrão são 18 e 0, respectivamente.</p></td>
</tr>
<tr class="even">
<td><p>TEXT</p></td>
<td><p>2 bytes por caractere (Consulte Observações)</p></td>
<td><p>Zero para um máximo de 2,14 gigabytes.</p></td>
</tr>
<tr class="odd">
<td><p>IMAGE</p></td>
<td><p>Conforme necessário</p></td>
<td><p>Zero para um máximo de 2,14 gigabytes. Usado para objetos OLE.</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER</p></td>
<td><p>2 bytes por caractere (Consulte Observações)</p></td>
<td><p>Zero para 255 caracteres.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> - A propagação e o incremento podem ser modificados utilizando uma [instrução ALTER TABLE](alter-table-statement-microsoft-access-sql.md). Novas linhas inseridas na tabela terão valores baseados nos novos valores de propagação e incremento, que são automaticamente gerados para a coluna. Se a nova propagação e o novo incremento puderem processar valores que correspondem a valores gerados com base na propagação e no incremento anteriores, duplicações serão geradas. Se a coluna for uma chave primária, a inserção de novas linhas poderá resultar em erros quando valores duplicados forem gerados.
> - Para localizar o último valor que foi utilizado para uma coluna de incremento automático, você pode usar a seguinte instrução: SELECT @@IDENTITY. Você não pode especificar um nome de tabela. O valor retornado é da última tabela atualizada que contém uma coluna de incremento automático.
