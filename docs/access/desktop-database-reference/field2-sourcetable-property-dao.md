---
title: Propriedade Field2.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb0c7b57b8ad5c0a1c202197e14fdaefd9a1103f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881017"
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
> <P>[!OBSERVAçãO] A propriedade <STRONG>SourceTable</STRONG> não retornará um nome de tabela significativo se utilizada em um objeto <STRONG>Field2</STRONG> na coleção <STRONG>Fields</STRONG> de um objeto <STRONG>Recordset</STRONG> de tipo tabela.</P>


