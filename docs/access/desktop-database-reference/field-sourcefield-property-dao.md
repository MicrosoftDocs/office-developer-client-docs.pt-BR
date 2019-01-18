---
title: Propriedade Field.SourceField (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dabfa13bac6973cea4bd69e0867292c4a6967
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718207"
---
# <a name="fieldsourcefield-property-dao"></a>Propriedade Field.SourceField (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna um valor que indica o nome do campo que é a fonte de dados original de um objeto **Field**. **String** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . SourceField

*expressão* Uma variável que representa um objeto **Field** .

## <a name="remarks"></a>Comentários

Para um objeto **Field**, o uso das propriedades **SourceField** e **SourceTable** depende do objeto que contém a coleção **Fields** à qual o objeto **Field** foi acrescentado, como mostra a tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto acrescentado a</p></th>
<th><p>Uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Índice</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p><strong>Relação</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
</tbody>
</table>


Essas propriedades indicam o campo original e os nomes das tabelas associados ao objeto **Field**. Por exemplo, você pode usar essas propriedades para determinar a fonte de dados original de um campo de consulta cujo nome não está relacionado ao nome do campo na tabela base.

