---
title: ExecuteOptionEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aeb1083c693e0848e30a0b9217ae709994daddb5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463503"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica como um provedor deve executar um comando.

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
<td><p><strong>adAsyncExecute</strong></p></td>
<td><p>0x10</p></td>
<td><p>Indica que o comando deve ser executado de forma assíncrona .
 Este valor não pode ser combinado ao valor <a href="commandtypeenum.md">CommandTypeEnum </a><strong>adCmdTableDirect</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAsyncFetch</strong></p></td>
<td><p>0x20</p></td>
<td><p>Indica que as linhas restantes após a quantidade inicial especificada na propriedade <a href="cachesize-property-ado.md">CacheSize</a> devem ser recuperadas de forma assíncrona.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAsyncFetchNonBlocking</strong></p></td>
<td><p>0x40</p></td>
<td><p>Indica que o thread principal nunca bloqueia ao recuperar. Se a linha solicitada não foi recuperada, a linha atual se move automaticamente até o final do arquivo. Se você abrir um <a href="recordset-object-ado.md">Recordset</a> a partir de um <a href="stream-object-ado.md">Stream</a> que contenha um <strong>Recordset</strong> persistentemente armazenado, <strong>adAsyncFetchNonBlocking</strong> não terá um efeito; a operação será síncrona e de bloqueio. O <strong>adAsynchFetchNonBlocking</strong> não terá efeito quando a opção <a href="commandtypeenum.md">adCmdTableDirect</a> for usada para abrir o <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteNoRecords</strong></p></td>
<td><p>0x80</p></td>
<td><p>Indica que o texto do comando é um comando ou procedimento armazenado que não retorne linhas (por exemplo, um comando que apenas insere dados). Se qualquer linha será recuperada, elas são descartadas e não retornadas. <strong>adExecuteNoRecords</strong> pode ser transmitido como um parâmetro opcional para o <strong>comando</strong> ou o método <strong>Execute</strong> de <strong>Conexão</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adExecuteStream</strong></p></td>
<td><p>0x400</p></td>
<td><p>Indica que os resultados de uma execução de comando devem ser retornados como um fluxo.
 <strong>adExecuteStream</strong> pode ser transmitido como um parâmetro opcional para o método de <strong>execução</strong> do <strong>comando</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteRecord</strong></p></td>
<td><p><br />
</p></td>
<td><p>Indica que o <strong>CommandText</strong> é um comando ou procedimento armazenado que retorna uma única linha que deve ser retornada como um objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Feita</strong></p></td>
<td><p>-1</p></td>
<td><p>Indica que o comando não está especificado.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC Equivalente**

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
<td><p>AdoEnums.ExecuteOption.ASYNCEXECUTE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCH</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.NORECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>
