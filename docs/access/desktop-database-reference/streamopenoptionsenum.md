---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f335f8572fbade23b949abacce8dd3690d205e32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721217"
---
# <a name="streamopenoptionsenum"></a>StreamOpenOptionsEnum


**Aplica-se a**: Access 2013, o Office 2013

Especifica as opções para abrir um objeto [Stream](stream-object-ado.md). Os valores podem ser combinados com um operador OR.

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
<td><p><strong>adOpenStreamAsync</strong></p></td>
<td><p>1</p></td>
<td><p>Abre o objeto <strong>Stream</strong> no modo assíncrono.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStreamFromRecord</strong></p></td>
<td><p>4</p></td>
<td><p>Identifica o conteúdo do parâmetro <em>Source</em> para ser um objeto <a href="record-object-ado.md">Record</a> já aberto. O comportamento padrão é tratar <em>Source</em> com um URL que aponta diretamente para um nó em uma estrutura em árvore. O fluxo padrão associado àquele nó é aberto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenStreamUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Padrão. Especifica a abertura do objeto <strong>Stream</strong> com as opções padrão.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Essas constantes não têm ADO/WFC equivalentes.

