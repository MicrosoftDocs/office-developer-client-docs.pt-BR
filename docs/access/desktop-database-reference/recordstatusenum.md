---
title: RecordStatusEnum (referência do banco de dados da área de trabalho do Access)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a83de7730224c5ecd5080c795d38cf2e9a3305a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309377"
---
# <a name="recordstatusenum"></a>RecordStatusEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica o status de um registro com relação a atualizações de batch e outras operações em massa.

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
<td><p><strong>adRecCanceled</strong></p></td>
<td><p>0x100</p></td>
<td><p>Indica que o registro não foi salvo porque a operação foi cancelada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecCantRelease</strong></p></td>
<td><p>0x400</p></td>
<td><p>Indica que o novo registro não foi salvo porque o registro existente foi bloqueado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecConcurrencyViolation</strong></p></td>
<td><p>0x800</p></td>
<td><p>Indica que o registro não foi salvo porque a concorrência otimista estava em uso.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecDBDeleted</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Indica que o registro já foi excluído da origem de dados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecDeleted</strong></p></td>
<td><p>0x4</p></td>
<td><p>Indica que o registro foi excluído.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecIntegrityViolation</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Indica que o registro não foi salvo porque o usuário violou as restrições de integridade.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecInvalid</strong></p></td>
<td><p>0x10</p></td>
<td><p>Indica que o registro não foi salvo porque seu indicador é inválido.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecMaxChangesExceeded</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Indica que o registro não foi salvo porque havia muitas alterações pendentes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecModified</strong></p></td>
<td><p>0x2</p></td>
<td><p>Indica que o registro foi modificado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecMultipleChanges</strong></p></td>
<td><p>0x40</p></td>
<td><p>Indica que o registro não foi salvo porque teria afetado vários registros.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecNew</strong></p></td>
<td><p>0x1</p></td>
<td><p>Indica que o registro é novo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecObjectOpen</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Indica que o registro não foi salvo devido a um conflito com um objeto de repositório aberto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecOK</strong></p></td>
<td><p>0</p></td>
<td><p>Indica que o registro foi atualizado com êxito.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecOutOfMemory</strong></p></td>
<td><p>0x8000</p></td>
<td><p>Indica que o registro não foi salvo porque o computador ficou sem memória.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecPendingChanges</strong></p></td>
<td><p>0x80</p></td>
<td><p>Indica que o registro não foi salvo porque se refere a uma inserção pendente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecPermissionDenied</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Indica que o registro não foi salvo porque o usuário possui permissões insuficientes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecSchemaViolation</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Indica que o registro não foi salvo porque viola a estrutura do banco de dados de base.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecUnmodified</strong></p></td>
<td><p>0x8</p></td>
<td><p>Indica que o registro não foi modificado.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente do ADO/WFC

AdoEnums.RecordStatus.

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.CANCELED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.CANTRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.CONCURRENCYVIOLATION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.DBDELETED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.DELETED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.INTEGRITYVIOLATION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.INVALID</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.MODIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.MULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.NEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.OBJECTOPEN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.OK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.OUTOFMEMORY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.PENDINGCHANGES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.PERMISSIONDENIED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.SCHEMAVIOLATION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.UNMODIFIED</p></td>
</tr>
</tbody>
</table>

