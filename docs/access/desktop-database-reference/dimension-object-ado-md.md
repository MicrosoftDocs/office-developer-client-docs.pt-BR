---
title: Objeto Dimension (ADO MD)
TOCTitle: Dimension object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: afea442aa535660b5bb618297640db8fbd546dec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293893"
---
# <a name="dimension-object-ado-md"></a>Objeto Dimension (ADO MD)


**Aplica-se ao:** Access 2013, Office 2013

Representa uma das dimensões de um cubo multidimensional, contendo uma ou maishierarquias de membros.

## <a name="remarks"></a>Comentários

Com as coleções e propriedades de um objeto **Dimension**, você pode fazer o que segue:

  - Identificar a **Dimension** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).

  - Retornar uma cadeia de caracteres consistente que descreva a **Dimension** com a propriedade [Description](description-property-ado-md.md).

  - Retornar os objetos [Hierarchy](hierarchy-object-ado-md.md) que compõem a **Dimension** com a coleção [Hierarchies](hierarchies-collection-ado-md.md).

  - Usar a coleção [Properties](properties-collection-ado.md) do ADO padrão para obter informações adicionais sobre o objeto **Dimension**.

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
<td><p>DefaultHierarchy</p></td>
<td><p>O nome exclusivo da hierarquia padrão.</p></td>
</tr>
<tr class="even">
<td><p>Descrição</p></td>
<td><p>Uma descrição consistente do cubo.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionCaption</p></td>
<td><p>Um rótulo ou uma legenda associada à dimensão.</p></td>
</tr>
<tr class="even">
<td><p>Dimension DimensionNality</p></td>
<td><p>O número de membros na dimensão.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionGUID</p></td>
<td><p>O GUID da dimensão.</p></td>
</tr>
<tr class="even">
<td><p>DimensionName</p></td>
<td><p>O nome da dimensão.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionOrdinal</p></td>
<td><p>O número ordinal da dimensão no grupo de dimensões que formam o cubo.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>O tipo da dimensão.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>O nome inequívoco da dimensão.</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>O nome do esquema ao qual este cubo pertence.</p></td>
</tr>
</tbody>
</table>

