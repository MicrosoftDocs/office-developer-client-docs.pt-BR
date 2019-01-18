---
title: CursorTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bcaaa1298f12d72c5e836dcfe1e74cdcda68d19
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710787"
---
# <a name="cursortypeenum"></a>CursorTypeEnum

**Aplica-se a**: Access 2013, o Office 2013

Especifica o tipo de cursor usado em um objeto [Recordset](recordset-object-ado.md).

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
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p>2</p></td>
<td><p>Usa um cursor dinâmico. As adições, alterações e exclusões feitas por outros usuários estão visíveis e são permitidos todos os tipos de movimento pelo <strong>Recordset</strong>, exceto para os marcadores, se o provedor não oferecer suporte a eles.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>0</p></td>
<td><p>Padrão. Usa um cursor somente de encaminhamento. Idêntico a um cursor estático, exceto que você pode rolar para frente somente pelos registros. Isso melhora o desempenho quando você precisa fazer apenas uma passagem por um <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p>1</p></td>
<td><p>Usa um cursor de conjunto de chaves. Como um cursor dinâmico, exceto que você não pode ver os registros que outros usuários adicionam, embora os registros que outros usuários excluem estejam inacessíveis a partir do seu <strong>Recordset</strong>. As alterações de dados feitas por outros usuários ainda estão visíveis.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p>3</p></td>
<td><p>Usa um cursor estático. Uma cópia estática de um conjunto de registros que você pode usar para localizar dados ou gerar relatórios. As adições, alterações ou exclusões feitas por outros usuários não estão visíveis.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Não especifica o tipo de cursor.</p></td>
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
<td><p>AdoEnums.CursorType.DYNAMIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.FORWARDONLY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.KEYSET</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.STATIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

