---
title: Objeto Cell (ADO MD)
TOCTitle: Cell Object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f38de1adc48e7d63a3b67e45f242a8cc884633ac
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464457"
---
# <a name="cell-object-ado-md"></a>Objeto Cell (ADO MD)


**Aplica-se a**: Access 2013 | Office 2013

Representa os dados na interseção de coordenadas de eixo contidos em um conjunto de células.

## <a name="remarks"></a>Comentários

Um objeto **Cell** é retornado pela propriedade [Item](item-property-ado-md-cellset.md) de um objeto [Cellset](cellset-object-ado-md.md).

Com as coleções e as propriedades de um objeto **Cell**, você pode fazer o que segue:

  - Retornar os dados da **Célula** com a propriedade [Value](value-property-ado-md.md).

  - Retornar a cadeia de caracteres que representa a exibição formatada da propriedade **Value** com a propriedade [FormattedValue](formattedvalue-property-ado-md.md).

  - Retornar o valor ordinal da **Célula** dentro do **Conjunto de células** com a propriedade [Ordinal](ordinal-property-ado-md-cell.md).

  - Determinar a posição da **Célula** dentro de [CubeDef](cubedef-object-ado-md.md) com a coleção [Positions](positions-collection-ado-md.md).

  - Recuperar outras informações sobre a **Célula** com a coleção [Properties](properties-collection-ado.md) do ADO padrão.

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
<td><p>BackColor</p></td>
<td><p>Cor de plano de fundo usada ao exibir a célula.</p></td>
</tr>
<tr class="even">
<td><p>FontFlags</p></td>
<td><p>Bitmask que detalha efeitos da fonte.</p></td>
</tr>
<tr class="odd">
<td><p>FontName</p></td>
<td><p>Fonte usada para exibir o valor da célula.</p></td>
</tr>
<tr class="even">
<td><p>FontSize</p></td>
<td><p>Tamanho da fonte usada para exibir o valor da célula.</p></td>
</tr>
<tr class="odd">
<td><p>ForeColor</p></td>
<td><p>Cor de primeiro plano usada ao exibir a célula.</p></td>
</tr>
<tr class="even">
<td><p>FormatString</p></td>
<td><p>Valor em uma cadeia de caracteres formatada.</p></td>
</tr>
</tbody>
</table>
