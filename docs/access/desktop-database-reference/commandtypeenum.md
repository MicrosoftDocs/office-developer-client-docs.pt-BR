---
title: CommandTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a570aaed8f0b2da415c3866ec88e7023085a1319
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887940"
---
# <a name="commandtypeenum"></a>CommandTypeEnum

**Aplica-se a**: Access 2013, o Office 2013

Especifica como um argumento de comando deve ser interpretado.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adCmdUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Não especifica o argumento de tipo de comando.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdText</strong></p></td>
<td><p>1</p></td>
<td><p>Avalia o <a href="commandtext-property-ado.md">CommandText</a> como uma definição textual de um comando ou chamada de procedimento armazenado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTable</strong></p></td>
<td><p>2</p></td>
<td><p>Avalia o <strong>CommandText</strong> como um nome de tabela cujas colunas são todas retornadas por uma consulta SQL gerada internamente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdStoredProc</strong></p></td>
<td><p>4</p></td>
<td><p>Avalia o <strong>CommandText</strong> como um nome de procedimento armazenado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdUnknown</strong></p></td>
<td><p>8</p></td>
<td><p>Padrão. Indica que o tipo de comando na propriedade <strong>CommandText</strong> não é conhecido.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdFile</strong></p></td>
<td><p>256</p></td>
<td><p>Avalia o <strong>CommandText</strong> como o nome do arquivo de um <a href="recordset-object-ado.md">Recordset</a> armazenado de forma persistente. Utilizado com <strong>Recordset.</strong>Apenas <a href="open-method-ado-recordset.md">Open</a> ou <a href="requery-method-ado.md">Requery</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTableDirect</strong></p></td>
<td><p>512</p></td>
<td><p>Avalia o <strong>CommandText</strong> como um nome de tabela cujas colunas são todas retornadas. Usado somente com <strong>Recordset</strong> ou <strong>Requery</strong> . Para usar o método <a href="seek-method-ado.md">Seek</a> , o <strong>Recordset</strong> deve ser aberto com <strong>adCmdTableDirect</strong>. Esse valor não pode ser combinado com o valor  <strong>adAsyncExecute </strong><a href="executeoptionenum.md">ExecuteOptionEnum</a>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.CommandType.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.TEXT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.STOREDPROC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.UNKNOWN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.FILE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLEDIRECT</p></td>
</tr>
</tbody>
</table>

