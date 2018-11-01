---
title: Propriedade Field.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c582795dc104171bd4c8435521e0da31718b1a38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868886"
---
# <a name="fieldvalidationtext-property-dao"></a>Propriedade Field.ValidationText (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que especifica o texto da mensagem exibido pelo aplicativo, caso o valor de um objeto **Field** não satisfaça a regra de validação especificada pela definição da propriedade **ValidationRule** (somente nos espaços de trabalho do Microsoft Access). **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . ValidationText

*expressão* Uma variável que representa um objeto **Field** .

## <a name="remarks"></a>Comentários

O valor de definição ou de retorno é um **String** que especificará o texto exibido se um usuário tentar inserir um valor inválido em um campo. Para um objeto ainda não acrescentado a uma coleção, essa propriedade será leitura/gravação.

Para um objeto **Field**, o uso da propriedade **ValidationText** depende do objeto que contém a coleção **[Fields](fields-collection-dao.md)** na qual o objeto **Field** foi acrescentado, como mostra a tabela a seguir.

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
<td><p>Leitura/gravação</p></td>
</tr>
</tbody>
</table>

