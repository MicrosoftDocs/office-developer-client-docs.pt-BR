---
title: CursorOptionEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 211ab4fc9bf4cab6302c8f2bd5f236aecdd0b078
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863634"
---
# <a name="cursoroptionenum"></a>CursorOptionEnum

**Aplica-se a**: Access 2013 | Office 2013

Especifica a funcionalidade para a qual o método [Supports](supports-method-ado.md) deve ser testado.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adAddNew</strong></p></td>
<td><p>0x1000400</p></td>
<td><p>Fornece suporte ao método <a href="addnew-method-ado.md">AddNew</a> para adicionar novos registros.</p></td>
</tr>
<tr class="even">
<td><p><strong>adApproxPosition</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Fornece suporte às propriedades <a href="absoluteposition-property-ado.md">AbsolutePosition</a> e <a href="absolutepage-property-ado.md">AbsolutePage</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adBookmark</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Fornece suporte à propriedade <a href="bookmark-property-ado.md">Bookmark</a> para obter acesso a registros específicos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelete</strong></p></td>
<td><p>0x1000800</p></td>
<td><p>Fornece suporte ao método <a href="delete-method-ado-recordset.md">Delete</a> para excluir registros.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFind</strong></p></td>
<td><p>0x80000</p></td>
<td><p>Fornece suporte ao método <a href="find-method-ado.md">Find</a> para localizar uma linha em um <a href="recordset-object-ado.md">Recordset</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adHoldRecords</strong></p></td>
<td><p>0x100</p></td>
<td><p>Recupera mais registros ou alterar a posição seguinte sem confirmar todas as alterações pendentes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIndex</strong></p></td>
<td><p>0x100000</p></td>
<td><p>Fornece suporte à propriedade <a href="index-property-ado.md">Index</a> para nomear um índice.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMovePrevious</strong></p></td>
<td><p>0x200</p></td>
<td><p>Fornece suporte aos métodos <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> e <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> e aos métodos <a href="move-method-ado.md">Move</a> ou <a href="getrows-method-ado.md">GetRows</a> para mover a posição de registro atual para trás sem exigir indicadores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adNotify</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Indica que o provedor de dados subjacente fornece suporte às notificações (o que determina se os eventos <strong>Recordset</strong> são permitidos).</p></td>
</tr>
<tr class="even">
<td><p><strong>adResync</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Fornece suporte ao método <a href="resync-method-ado.md">Resync</a> para atualizar o cursor com os dados visíveis no banco de dados subjacente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSeek</strong></p></td>
<td><p>0x200000</p></td>
<td><p>Fornece suporte ao método <a href="seek-method-ado.md">Seek</a> para localizar uma linha em um <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUpdate</strong></p></td>
<td><p>0x1008000</p></td>
<td><p>Fornece suporte ao método <a href="update-method-ado.md">Update</a> para modificar dados existentes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUpdateBatch</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Fornece suporte à atualização em lote (métodos <a href="updatebatch-method-ado.md">UpdateBatch</a> e <a href="cancelbatch-method-ado.md">CancelBatch</a>) para transmitir grupos de alterações ao provedor.</p></td>
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
<td><p>AdoEnums.CursorOption.ADDNEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.APPROXPOSITION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.BOOKMARK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.DELETE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.FIND</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.HOLDRECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.INDEX</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.MOVEPREVIOUS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.NOTIFY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.RESYNC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.SEEK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.UPDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.UPDATEBATCH</p></td>
</tr>
</tbody>
</table>

