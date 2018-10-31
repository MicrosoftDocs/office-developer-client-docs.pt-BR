---
title: ObjectTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c5fb9dbf86823ab4d84327d97eceb037eb77dec0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863708"
---
# <a name="objecttypeenum"></a>ObjectTypeEnum

**Aplica-se a**: Access 2013 | Office 2013

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
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adPermObjColumn</strong></p></td>
<td><p>2</p></td>
<td><p>O objeto é uma coluna.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjDatabase</strong></p></td>
<td><p>3</p></td>
<td><p>O objeto é um banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPermObjProcedure</strong></p></td>
<td><p>4</p></td>
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
<td><p>5</p></td>
<td><p>O objeto é um modo de exibição.</p></td>
</tr>
</tbody>
</table>

