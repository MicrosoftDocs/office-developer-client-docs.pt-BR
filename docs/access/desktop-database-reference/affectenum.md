---
title: AffectEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ffb2ab2abbd24a19ddc433b5fd315dd535fd2a0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463197"
---
# <a name="affectenum"></a>AffectEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica quais registros foram afetados por uma operação.

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
<td><p><strong>adAffectAll</strong></p></td>
<td><p>3</p></td>
<td><p>Se não houver um <a href="filter-property-ado.md">Filter</a> aplicado ao <strong>Recordset</strong>, afeta todos os registros.
 Se a propriedade <strong>Filter</strong> estiver definida como um critério de sequência (como &quot;Author = 'Smith'&quot;), a operação afetará os registros visíveis no capítulo atual. Se a propriedade <strong>Filter</strong> estiver definida como um membro do <a href="filtergroupenum.md">FilterGroupEnum</a> ou uma matriz de Indicadores, a operação afetará todas as linhas do <strong>Recordset</strong>.</p>

> [!NOTE]
> <P>adAffectAll está oculto no Visual Basic Object Browser.</P>


</td>
</tr>
<tr class="even">
<td><p><strong>adAffectAllChapters</strong></p></td>
<td><p>4</p></td>
<td><p>Afeta todos os registros em todos os capítulos irmãos do <strong>Recordset</strong>, incluindo os que não são visíveis através de qualquer <strong>Filter</strong> que esteja aplicado no momento.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAffectCurrent</strong></p></td>
<td><p>1</p></td>
<td><p>Afeta apenas o registro atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>2</p></td>
<td><p>Afeta apenas os registros que satisfazem a definição da propriedade <a href="filter-property-ado.md">Filter</a> atual. Você deve definir a propriedade <strong>Filter</strong> para um valor <strong>FilterGroupEnum</strong> ou uma matriz de <strong>Indicadores</strong> para utilizar essa opção.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC Equivalente**

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
<td><p>AdoEnums.Affect.ALL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.ALLCHAPTERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Affect.CURRENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.GROUP</p></td>
</tr>
</tbody>
</table>

