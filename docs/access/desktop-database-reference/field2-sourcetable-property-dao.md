---
title: Propriedade Field2.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a3ecf8b6655bb9f1dd2b25d264708112834e8a90
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717941"
---
# <a name="field2sourcetable-property-dao"></a>Propriedade Field2.SourceTable (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna um valor que indique o nome da tabela que é a origem dos dados para um objeto **Field2**. **String** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . SourceTable

*expressão* Uma variável que representa um objeto **Field2** .

## <a name="remarks"></a>Comentários

Para um objeto **Field2**, a utilização das propriedades **SourceField** e **SourceTable** depende do objeto que contém a coleta **Fields** à qual o objeto **Field2** foi acrescentado, como mostrado na tabela a seguir.

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


Estas propriedades indicam os nomes originais de campos e tabelas associados ao objeto **Field2**. Por exemplo, você pode utilizar essas propriedades para determinar a fonte original dos dados em um campo de consulta cujo nome não está relacionado ao nome do campo na tabela de base.


> [!NOTE]
> [!OBSERVAçãO] A propriedade **SourceTable** não retornará um nome de tabela significativo se utilizada em um objeto **Field2** na coleção **Fields** de um objeto **Recordset** de tipo tabela.


