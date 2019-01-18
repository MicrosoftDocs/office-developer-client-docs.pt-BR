---
title: Propriedade Field.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a557a4941f5b4aa511489c5d057871df5fa72c08
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726061"
---
# <a name="fieldsourcetable-property-dao"></a>Propriedade Field.SourceTable (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna um valor que indica o nome da tabela que é a fonte de dados original de um objeto **Field**. **String** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . SourceTable

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


> [!NOTE]
> [!OBSERVAçãO] A propriedade **SourceTable** não retornará um nome de tabela significativo se for usado em um objeto **Field** na coleção **Fields** de um objeto **Recordset** do tipo tabela.


