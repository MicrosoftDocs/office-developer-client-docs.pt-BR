---
title: Objeto CubeDef (ADO MD)
TOCTitle: CubeDef Object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7dc244483c3111e6e354496f1ffbbd12f463800
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878288"
---
# <a name="cubedef-object-ado-md"></a>Objeto CubeDef (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Representa um cubo em um esquema multidimensional, contendo um conjunto de dimensões relacionadas.

## <a name="remarks"></a>Comentários

Com as coleções e propriedades de um objeto **CubeDef**, você pode fazer o que segue:

  - Identificar um **CubeDef** com a propriedade [Name](name-property-ado-md.md).

  - Retornar uma cadeia de caracteres que descreva o cubo com a propriedade [Description](description-property-ado-md.md).

  - Retornar as dimensões do cubo com a coleção [Dimensions](dimensions-collection-ado-md.md).

  - Obter informações adicionais sobre **CubeDef** com a coleção [Properties](properties-collection-ado.md) do ADO padrão.

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
<td><p>Nome_do_catálogo</p></td>
<td><p>O nome do catálogo ao qual este cubo pertence.</p></td>
</tr>
<tr class="even">
<td><p>CreatedOn</p></td>
<td><p>Data e hora de criação do cubo.</p></td>
</tr>
<tr class="odd">
<td><p>CubeGUID</p></td>
<td><p>GUID do cubo.</p></td>
</tr>
<tr class="even">
<td><p>Nome do cubo</p></td>
<td><p>O nome do cubo.</p></td>
</tr>
<tr class="odd">
<td><p>CubeType</p></td>
<td><p>O tipo do cubo.</p></td>
</tr>
<tr class="even">
<td><p>DataUpdatedBy</p></td>
<td><p>Identificação de usuário da pessoa que realizou a última atualização de dados.</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>Uma descrição consistente do cubo.</p></td>
</tr>
<tr class="even">
<td><p>LastSchemaUpdate</p></td>
<td><p>Data e hora da última atualização do esquema.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>O nome do esquema ao qual este cubo pertence.</p></td>
</tr>
<tr class="even">
<td><p>SchemaUpdatedBy</p></td>
<td><p>Identificação de usuário da pessoa que realizou a última atualização de esquema.</p></td>
</tr>
</tbody>
</table>

