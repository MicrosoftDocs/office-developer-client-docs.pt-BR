---
title: Enumeração RecordsetOptionEnum (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9e2a69f6952feb892de736e7ff3c3ca94e9da64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307179"
---
# <a name="recordsetoptionenum-enumeration-dao"></a>Enumeração RecordsetOptionEnum (DAO)


**Aplica-se ao**: Access 2013, Office 2013

Usado com o método **OpenRecordset** para especificar as características de um novo objeto **Recordset**.

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
<td><p>dbAppendOnly</p></td>
<td><p>8</p></td>
<td><p>Permite ao usuário adicionar novos registros ao dynaset, mas impede que ele leia registros existentes.</p></td>
</tr>
<tr class="even">
<td><p>dbConsistent</p></td>
<td><p>32</p></td>
<td><p>Aplica atualizações somente aos campos que não irão afetar outros registros do dynaset (somente tipos dynaset e instantâneo).</p></td>
</tr>
<tr class="odd">
<td><p>dbDenyRead</p></td>
<td><p>2</p></td>
<td><p>Impede que outros usuários leiam registros do Conjunto de Registros (somente tipo tabela).</p></td>
</tr>
<tr class="even">
<td><p>dbDenyWrite</p></td>
<td><p>1</p></td>
<td><p>Impede que outros usuários alterem registros do Conjunto de Registros.</p></td>
</tr>
<tr class="odd">
<td><p>dbExecDirect</p></td>
<td><p>2048</p></td>
<td><p>Executa a consulta sem primeiro chamar a função SQLPrepare do ODBC.</p></td>
</tr>
<tr class="even">
<td><p>dbFailOnError</p></td>
<td><p>128</p></td>
<td><p>Reverte as atualizações quando ocorre um erro.</p></td>
</tr>
<tr class="odd">
<td><p>dbForwardOnly</p></td>
<td><p>256</p></td>
<td><p>Cria um Conjunto de Registros de rolagem, do tipo instantâneo, somente de encaminhamento (somente tipo instantâneo).</p></td>
</tr>
<tr class="even">
<td><p>dbInconsistent</p></td>
<td><p>16</p></td>
<td><p>Aplica atualizações a todos os campos dynaset, mesmo que outros registros sejam afetados (somente tipos dynaset e instantâneo).</p></td>
</tr>
<tr class="odd">
<td><p>dbReadOnly</p></td>
<td><p>4</p></td>
<td><p>Abre o Conjunto de Registros como somente leitura.</p></td>
</tr>
<tr class="even">
<td><p>dbRunAsync</p></td>
<td><p>1024</p></td>
<td><p>Executa a consulta de forma assíncrona.</p></td>
</tr>
<tr class="odd">
<td><p>dbSeeChanges</p></td>
<td><p>512</p></td>
<td><p>Gera um erro em tempo de execução se outro usuário estiver alterando dados que você estiver editando (somente tipo dynaset).</p></td>
</tr>
<tr class="even">
<td><p>dbSQLPassThrough</p></td>
<td><p>64</p></td>
<td><p>Envia uma instrução SQL a um banco de dados ODBC (somente tipo instantâneo).</p></td>
</tr>
</tbody>
</table>

