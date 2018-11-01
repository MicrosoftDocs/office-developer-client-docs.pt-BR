---
title: Objetos do ADO MD (referência de banco de dados da área de trabalho do Access)
TOCTitle: ADO MD Objects
ms:assetid: 13501e44-70b6-1036-a8b7-c276f187e4f4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248907(v=office.15)
ms:contentKeyID: 48543366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e09676b222e7199b7f2f9f7520ebf3d5436f9a3c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875130"
---
# <a name="ado-md-objects"></a>Objetos do ADO MD


**Aplica-se a**: Access 2013, o Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="axis-object-ado-md.md">Eixo</a></p></td>
<td><p>Representa um eixo de posição ou de filtro de um conjunto de células, contendo membros selecionados de uma ou mais dimensões.</p></td>
</tr>
<tr class="even">
<td><p><a href="catalog-object-ado-md.md">Catálogo</a></p></td>
<td><p>Contém informações de esquema multidimensionais (isto é, cubos e dimensões subjacentes, hierarquias, níveis e membros) específicos de um MDP (provedor de dados multidimensionais).</p></td>
</tr>
<tr class="odd">
<td><p><a href="cell-object-ado-md.md">Cell</a></p></td>
<td><p>Representa os dados na interseção de coordenadas de eixo, contidos em um conjunto de células.</p></td>
</tr>
<tr class="even">
<td><p><a href="cellset-object-ado-md.md">Conjunto de células</a></p></td>
<td><p>Representa os resultados de uma consulta multidimensional. É uma coleção das células selecionadas em cubos ou outros conjuntos de células.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cubedef-object-ado-md.md">CubeDef</a></p></td>
<td><p>Representa um cubo em um esquema multidimensional, contendo um conjunto de dimensões relacionadas.</p></td>
</tr>
<tr class="even">
<td><p><a href="dimension-object-ado-md.md">Dimensão</a></p></td>
<td><p>Representa uma das dimensões de um cubo multidimensional, contendo uma ou maishierarquias de membros.</p></td>
</tr>
<tr class="odd">
<td><p><a href="hierarchy-object-ado-md.md">Hierarquia</a></p></td>
<td><p>Representa uma forma em que os membros de uma dimensão possam ser agregados ou &quot;acumulados. &quot; Uma dimensão possa ser agregada ao longo de uma ou mais hierarquias.</p></td>
</tr>
<tr class="even">
<td><p><a href="level-object-ado-md.md">Nível</a></p></td>
<td><p>Contém um conjunto de membros, sendo que cada um tem a mesma ordem em uma hierarquia.</p></td>
</tr>
<tr class="odd">
<td><p><a href="member-object-ado-md.md">Membro</a></p></td>
<td><p>Representa um membro de um nível em um cubo, os filhos de um membro de um nível ou um membro de uma posição em um eixo de um conjunto de células.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-object-ado-md.md">Position</a></p></td>
<td><p>Representa um conjunto de um ou mais membros de diferentes dimensões que define um ponto em um eixo.</p></td>
</tr>
</tbody>
</table>


Além disso, o objeto **Catalog** está conectado a um objeto **Connection** do ADO, que está incluído na biblioteca padrão do ADO:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="connection-object-ado.md">Connection</a></p></td>
<td><p>Representa uma conexão aberta com uma fonte de dados.</p></td>
</tr>
</tbody>
</table>


Muitos objetos do ADO MD pode estar contidos em uma coleção correspondente. Por exemplo, um objeto [CubeDef](cubedef-object-ado-md.md) pode estar contido em uma coleção [CubeDefs](cubedefs-collection-ado-md.md) de um **Catalog**. Para obter mais informações, consulte [Coleções do ADO MD](ado-md-collections.md).

