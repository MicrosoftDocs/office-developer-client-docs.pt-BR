---
title: Objeto Level (ADO MD)
TOCTitle: Level object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70fb359aa4faa0bcfc99f0b1700b0eb51f665bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290111"
---
# <a name="level-object-ado-md"></a>Objeto Level (ADO MD)


**Aplica-se ao:** Access 2013, Office 2013

Contém um conjunto de membros, sendo que cada um tem a mesma ordem em uma hierarquia.

## <a name="remarks"></a>Comentários

Com as coleções e propriedades de um objeto **Level**, você pode fazer o que segue:

  - Identificar o **Level** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).

  - Retornar uma cadeia de caracteres para ser usada ao exibir o **Level** com a propriedade [Caption](caption-property-ado-md.md).

  - Retornar uma cadeia de caracteres consistente que descreva o **Level** com a propriedade [Description](description-property-ado-md.md).

  - Retornar os objetos [Member](member-object-ado-md.md) que compõem o **Level** com a coleção [Members](members-collection-ado-md.md).

  - Retornar o número de níveis a partir da raiz do **Level** com a propriedade [Depth](depth-property-ado-md.md).

  - Usar a coleção [Properties](properties-collection-ado.md) do ADO padrão para obter informações adicionais sobre o objeto **Level**.

A coleção **Properties** contém propriedades fornecidas pelo provedor. A tabela a seguir lista propriedades que talvez estejam disponíveis. A lista de propriedades verdadeira pode diferir, de acordo com a implementação do provedor. Consulte a documentação do seu provedor para obter uma lista mais completa de propriedades disponíveis.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CatalogName</p></td>
<td><p>O nome do catálogo ao qual o cubo pertence.</p></td>
</tr>
<tr class="even">
<td><p>CubeName</p></td>
<td><p>O nome do cubo.</p></td>
</tr>
<tr class="odd">
<td><p>Descrição</p></td>
<td><p>Uma descrição consistente do nível.</p></td>
</tr>
<tr class="even">
<td><p>DimensionUniqueName</p></td>
<td><p>O nome inequívoco da <a href="dimension-object-ado-md.md">dimensão</a>.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyUniqueName</p></td>
<td><p>O nome inequívoco da hierarquia.</p></td>
</tr>
<tr class="even">
<td><p>LevelCaption</p></td>
<td><p>Um rótulo ou uma legenda associada ao nível.</p></td>
</tr>
<tr class="odd">
<td><p>LevelItudenality</p></td>
<td><p>O número de membros no nível.</p></td>
</tr>
<tr class="even">
<td><p>LevelGUID</p></td>
<td><p>O GUID do nível.</p></td>
</tr>
<tr class="odd">
<td><p>LevelName</p></td>
<td><p>Nome do nível.</p></td>
</tr>
<tr class="even">
<td><p>LevelNumber</p></td>
<td><p>A distância entre o nível e a raiz da hierarquia.</p></td>
</tr>
<tr class="odd">
<td><p>LevelType</p></td>
<td><p>O tipo do nível.</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>O nome inequívoco do nível.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>O nome do esquema ao qual este cubo pertence.</p></td>
</tr>
</tbody>
</table>

