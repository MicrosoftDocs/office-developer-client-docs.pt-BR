---
title: Objeto Member (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 380fdf6c15f6774e27221e8500100870d22350c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289419"
---
# <a name="member-object-ado-md"></a>Objeto Member (ADO MD)


**Aplica-se ao:** Access 2013, Office 2013

Representa um membro de um nível em um cubo, os filhos de um membro de um nível ou um membro de uma posição em um eixo de um conjunto de células.

## <a name="remarks"></a>Comentários

As propriedades de um **Member** diferem de acordo com o contexto em que ele é usado. Um **Member** de um [Level](level-object-ado-md.md) em um [CubeDef](cubedef-object-ado-md.md) tem uma propriedade [Children](children-property-ado-md.md) que retorna os **members** do nível mais baixo a seguir na hierarquia a partir do **member** atual. Para um **member** de uma [posição](position-object-ado-md.md), a coleção **Children** está sempre vazia. Além disso, a propriedade [Type](type-property-ado-md.md) aplica-se apenas a **members** de um **Level**.

Um **Member** de uma **Position** tem duas propriedades  [DrilledDown](drilleddown-property-ado-md.md) e [ParentSameAsPrev](parentsameasprev-property-ado-md.md)  que são úteis ao exibir o [Cellset](cellset-object-ado-md.md). Um erro ocorrerá se essas propriedades forem acessadas em um **Member** de um **Level**.

Com as coleções e propriedades de um objeto **Member** de um **Level**, você pode fazer o que segue:

  - Identificar o **Member** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).

  - Retornar uma cadeia de caracteres para ser usada ao exibir o **Member** com a propriedade [Caption](caption-property-ado-md.md).

  - Retornar uma cadeia de caracteres consistente que descreva um **Member** de medida ou fórmula com a propriedade [Description](description-property-ado-md.md).

  - Determinar a natureza do **Member** com a propriedade [Type](type-property-ado-md.md).

  - Obter informações sobre o **Level** do **Member** com as propriedades [LevelDepth](leveldepth-property-ado-md.md) e [LevelName](levelname-property-ado-md.md).

  - Obter **Members** relacionados em uma [Hierarchy](hierarchy-object-ado-md.md) com as propriedades [Parent](parent-property-ado-md.md) e [Children](children-property-ado-md.md).

  - Contar os filhos de um **Member** com a propriedade [ChildCount](childcount-property-ado-md.md).

  - Usar a coleção [Properties](properties-collection-ado.md) do ADO padrão para obter informações adicionais sobre o objeto **Level**.

Com as coleções e propriedades de um **Member** de uma **Position** ao longo de um [Axis](axis-object-ado-md.md), você pode fazer o que segue:

  - Identificar o **Member** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).

  - Retornar uma cadeia de caracteres para ser usada ao exibir o **Member** com a propriedade [Caption](caption-property-ado-md.md).

  - Retornar uma cadeia de caracteres consistente que descreva um **Member** de medida ou fórmula com a propriedade [Description](description-property-ado-md.md).

  - Obter informações sobre o **Level** do **Member** com as propriedades [LevelDepth](leveldepth-property-ado-md.md) e [LevelName](levelname-property-ado-md.md).

  - Contar os filhos de um **Member** com a propriedade [ChildCount](childcount-property-ado-md.md).

  - Usar a propriedade [DrilledDown](drilleddown-property-ado-md.md) para determinar se há pelo menos um filho no **Axis** imediatamente depois deste **Member**.

  - Usar a propriedade [ParentSameAsPrev](parentsameasprev-property-ado-md.md) para determinar se o pai deste **Member** é o mesmo pai do **Member** imediatamente anterior.

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
<td><p>ChildrenItudenality</p></td>
<td><p>O número de filhos que o membro tem.</p></td>
</tr>
<tr class="odd">
<td><p>CubeName</p></td>
<td><p>O nome do cubo.</p></td>
</tr>
<tr class="even">
<td><p>Descrição</p></td>
<td><p>Uma descrição consistente do membro.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>O nome inequívoco da <a href="dimension-object-ado-md.md">dimensão</a>.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>O nome inequívoco da hierarquia.</p></td>
</tr>
<tr class="odd">
<td><p>LevelNumber</p></td>
<td><p>A distância entre o nível e a raiz da hierarquia.</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>O nome inequívoco do nível.</p></td>
</tr>
<tr class="odd">
<td><p>MemberCaption</p></td>
<td><p>Um rótulo ou uma legenda associada ao membro.</p></td>
</tr>
<tr class="even">
<td><p>MemberGUID</p></td>
<td><p>O GUID do membro.</p></td>
</tr>
<tr class="odd">
<td><p>MemberName</p></td>
<td><p>O nome do membro.</p></td>
</tr>
<tr class="even">
<td><p>MemberOrdinal</p></td>
<td><p>O número ordinal do membro.</p></td>
</tr>
<tr class="odd">
<td><p>MemberType</p></td>
<td><p>O tipo do membro.</p></td>
</tr>
<tr class="even">
<td><p>MemberUniqueName</p></td>
<td><p>O nome inequívoco do membro.</p></td>
</tr>
<tr class="odd">
<td><p>ParentCount</p></td>
<td><p>A contagem do número de pais que este membro tem.</p></td>
</tr>
<tr class="even">
<td><p>ParentLevel</p></td>
<td><p>O número do nível do pai do membro.</p></td>
</tr>
<tr class="odd">
<td><p>ParentUniqueName</p></td>
<td><p>O nome inequívoco do pai do membro.</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>O nome do esquema ao qual este cubo pertence.</p></td>
</tr>
</tbody>
</table>

