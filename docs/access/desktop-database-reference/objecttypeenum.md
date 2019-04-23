---
title: ObjectTypeEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e3b470c8c0d0c3f04b59bd382b66117bd79c188
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288529"
---
# <a name="objecttypeenum"></a>ObjectTypeEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica o tipo de objeto de banco de dados para o qual devem ser definidas permissões ou cuja propriedade deve ser estabelecida.

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
<td><p><strong>adPermObjColumn</strong></p></td>
<td><p>duas</p></td>
<td><p>O objeto é uma coluna.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjDatabase</strong></p></td>
<td><p>3D</p></td>
<td><p>O objeto é um banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPermObjProcedure</strong></p></td>
<td><p>quatro</p></td>
<td><p>O objeto é um procedimento.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjProviderSpecific</strong></p></td>
<td><p>-1</p></td>
<td><p>O objeto é de um tipo definido pelo provedor. Ocorrerá um erro se o parâmetro <em>ObjectType</em> for <strong>adPermObjProviderSpecific</strong> e um <em>ObjectTypeId</em> não for fornecido.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPermObjTable</strong></p></td>
<td><p>1</p></td>
<td><p>O objeto é uma tabela.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjView</strong></p></td>
<td><p>0,5</p></td>
<td><p>O objeto é um modo de exibição.</p></td>
</tr>
</tbody>
</table>

