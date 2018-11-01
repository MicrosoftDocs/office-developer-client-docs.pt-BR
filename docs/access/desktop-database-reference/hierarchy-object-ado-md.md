---
title: Objeto Hierarchy (ADO MD)
TOCTitle: Hierarchy Object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad6eb40873d0cd88b441adaa5568ad57dced83c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869782"
---
# <a name="hierarchy-object-ado-md"></a>Objeto Hierarchy (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Representa uma maneira como os membros de uma [dimensão](dimension-object-ado-md.md) podem ser agregados. É possível agregar uma dimensão juntamente com uma ou mais hierarquias.

## <a name="remarks"></a>Comentários

Com as coleções e as propriedades de um objeto **Hierarchy**, você pode fazer o que segue:

  - Identificar **Hierarchy** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).

  - Retornar uma cadeia de caracteres consistente que descreva **Hierarchy** com a propriedade [Description](description-property-ado-md.md).

  - Retornar os objetos [Level](level-object-ado-md.md) que compõem a **Hierarchy** com a coleção [Levels](levels-collection-ado-md.md).

  - Usar a coleção [Properties](properties-collection-ado.md) do ADO padrão para obter informações adicionais sobre o objeto **Hierarchy**.

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
<td><p>AllMember</p></td>
<td><p>O membro de nível mais alto de acúmulo na hierarquia.</p></td>
</tr>
<tr class="even">
<td><p>Nome_do_catálogo</p></td>
<td><p>O nome do catálogo ao qual o cubo pertence.</p></td>
</tr>
<tr class="odd">
<td><p>Nome do cubo</p></td>
<td><p>O nome do cubo.</p></td>
</tr>
<tr class="even">
<td><p>DefaultMember</p></td>
<td><p>O nome exclusivo do membro padrão desta hierarquia.</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>Uma descrição consistente da hierarquia.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>O tipo da dimensão ao qual esta hierarquia pertence.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>O nome inequívoco da dimensão.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyCaption</p></td>
<td><p>Um rótulo ou uma legenda associada à hierarquia.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyCardinality</p></td>
<td><p>O número de membros na hierarquia.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyGUID</p></td>
<td><p>O GUID da hierarquia.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyName</p></td>
<td><p>O nome da hierarquia.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>O nome inequívoco da hierarquia.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>O nome do esquema ao qual este cubo pertence.</p></td>
</tr>
</tbody>
</table>

