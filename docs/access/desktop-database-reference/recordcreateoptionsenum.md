---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bc0d378428c00882c49f7783892ca2bf4d4638c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300690"
---
# <a name="recordcreateoptionsenum"></a>RecordCreateOptionsEnum


**Aplica-se ao:** Access 2013, Office 2013

Especifica se um **Record** existente deve ser aberto ou um novo **Record** criado para o método [Open](record-object-ado.md) do objeto [Record](open-method-ado-record.md). Os valores podem ser combinados com um operador AND.

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
<td><p><strong>adCreateCollection</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Cria um novo <strong>Record</strong> no nó especificado pelo parâmetro <em>Source</em>, em vez abrir um <strong>Record</strong> existente. Se a origem apontar para um nó existente, ocorrerá um erro de tempo de execução, a menos que <strong>adCreateCollection</strong> seja combinado com <strong>adOpenIfExists</strong> ou <strong>adCreateOverwrite</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateNonCollection</strong></p></td>
<td><p>,0</p></td>
<td><p>Cria um novo <strong>Record</strong> do tipo <a href="recordtypeenum.md">adSimpleRecord</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCreateOverwrite</strong></p></td>
<td><p>0x4000000</p></td>
<td><p>Modifica os sinalizadores de criação <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> e <strong>adCreateStructDoc</strong>. Quando OR for usado com esse valor e um dos valores do sinalizador de criação, se a URL de origem apontar para o nó existente ou <strong>Record</strong>, o <strong>Record</strong> existente será sobregravado e um novo será criado em seu local. Esse valor não pode ser usado juntamente com <strong>adOpenIfExists</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateStructDoc</strong></p></td>
<td><p>0x80000000</p></td>
<td><p>Cria um novo <strong>Record</strong> de tipo <a href="recordtypeenum.md">adStructDoc</a>, em vez abrir um <strong>Record</strong> existente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFailIfNotExists</strong></p></td>
<td><p>-1</p></td>
<td><p>Padrão. Resulta em um erro de tempo de execução se <em>Source</em> apontar para um nó não existente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenIfExists</strong></p></td>
<td><p>0x2000000</p></td>
<td><p>Modifica os sinalizadores <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> e <strong>adCreateStructDoc</strong>. Quando OR for usado com esse valor e um dos valores do sinalizador de criação, se a URL de origem apontar para um nó existente ou objeto <strong>Record</strong>, o provedor deve abrir o <strong>Record</strong> existente em vez de criar um novo. Esse valor não pode ser usado com <strong>adCreateOverwrite</strong>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente do ADO/WFC

Essas constantes não têm ADO/WFC equivalentes.

