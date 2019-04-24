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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314746"
---
# <a name="streamopenoptionsenum"></a>StreamOpenOptionsEnum


**Aplica-se ao:** Access 2013, Office 2013

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
<td><p><strong>Openoptions</strong></p></td>
<td><p>quatro</p></td>
<td><p>Identifica o conteúdo do parâmetro <em>Source</em> para ser um objeto <a href="record-object-ado.md">Record</a> já aberto. O comportamento padrão é tratar <em>Source</em> com um URL que aponta diretamente para um nó em uma estrutura em árvore. O fluxo padrão associado àquele nó é aberto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenStreamUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Padrão. Especifica a abertura do objeto <strong>Stream</strong> com as opções padrão.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente do ADO/WFC

Essas constantes não têm ADO/WFC equivalentes.

