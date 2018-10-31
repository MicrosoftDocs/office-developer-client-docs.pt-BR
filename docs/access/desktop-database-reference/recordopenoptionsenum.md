---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 54499cc9c8b45e411b4121963d1a571100b7e0e5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860943"
---
# <a name="recordopenoptionsenum"></a>RecordOpenOptionsEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica as opções para abrir um objeto [Record](record-object-ado.md). Esses valores podem ser combinadas usando o OR.

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
<td><p><strong>adDelayFetchFields</strong></p></td>
<td><p>0x8000</p></td>
<td><p>Indica para o provedor que os campos associados ao <strong>Record</strong> não precisam ser recuperados inicialmente, mas podem ser recuperados na primeira tentativa para acessar o campo. O comportamento padrão, indicado pela ausência deste indicador, é para recuperar todos os campos de objetos <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelayFetchStream</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Indica ao provedor que o fluxo padrão associado ao <strong>Record</strong> não precisa ser recuperado inicialmente. O comportamento padrão, indicado pela ausência deste indicador, é para recuperar o fluxo padrão associado ao objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenAsync</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Indica que o objeto <strong>Record</strong> é aberto no modo assíncrono.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenExecuteCommand</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Indica que a sequência Source contém o texto do comento que deveria ser executado. Este valor é equivalente à opção <strong>adCmdText</strong> em <strong>Recordset.Open</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenRecordUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Padrão. Indica que nenhuma opção foi especificada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenOutput</strong></p></td>
<td><p>0x800000</p></td>
<td><p>Indica que se a fonte apontar para um nó que contenha um script executável (como uma página .ASP), então o <strong>Record</strong> aberto conterá os resultados do script executado. Este valor só é válido com registros que não pertencem à coleções.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Essas constantes não têm ADO/WFC equivalentes.

