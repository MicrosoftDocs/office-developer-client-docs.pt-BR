---
title: ExecuteOptionEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: febeb3b52eb579647c995b01d6723a5c1f1b0c1f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718305"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum

**Aplica-se a**: Access 2013, o Office 2013

Especifica como um provedor deve executar um comando.

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
<td><p>Indica que um encadeamento principal nunca é bloqueado durante a recuperação. Se a linha solicitada não tiver sido recuperada, a linha atual se moverá automaticamente para o final do arquivo.
</p><p>Se você abrir um <a href="recordset-object-ado.md">Recordset</a> a partir de um <a href="stream-object-ado.md">Stream</a> que contenha um <strong>Recordset</strong> persistentemente armazenado, <strong>adAsyncFetchNonBlocking</strong> não terá um efeito; a operação será síncrona e de bloqueio. O <strong>adAsynchFetchNonBlocking</strong> não terá efeito quando a opção <a href="commandtypeenum.md">adCmdTableDirect</a> for usada para abrir o <strong>Recordset</strong>.</p></td>
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

